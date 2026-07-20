
## docs/SLO.md

In forming our SLOs, a main consideration that occurred was our much increased need for reliability over speed.

### Latency SLO

association-service: The association service is a user facing API, so it must respond quickly. Target latency thresholds are P99: 4-5s, P95: 1ms - 2s, P50: ~100ms. It is likely that, if response time exceeds P99, users will refresh the page or submit another request. 

liaison-service: The liaison-service is not user facing and therefore does not need to respond as quickly. The endpoint response thresholds are as follows: PP:4-5 min, PP95: 1 min, P50: 1-5s. Only the tenant board is waiting for a response, so the algorithm can prioritize finding the perfect match. However, if the algorithm somehow stretches for hours, it would cause frustration due to the need to find an assignee. 

### Reliability SLO

association-service: The association service is a user facing API with admin capabilities that is going to be used frequently to move the TOPA matching process forward. It should be available 99.95% with an error rate of <0.1% . Since the service will have the ability to both get and modify TAs, there will be a need for different delivery semantics for different requests. For example, initializing a TA. At-most-once might mean a tenant association isn’t initialized, which would mean the user would need to fill out the relevant forms again, this would be an annoyance that might discourage tenants from using the app. At-least-once might mean that duplicate associations are written to the database, which could create data consistency problems if TA data is written/fetched by name.

liaison-service: The liaison service must achieve a success rate of 99.9%. The algorithm that searches for an assignee should follow at-most-once semantics. If a query fails, it is better to retry that return out of date or a sub par assignee. The assignee communications feature should follow at-least-once semantics since redundant emails are better than the alternative of never actually informing the assignee of interest. 
