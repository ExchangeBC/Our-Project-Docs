<a rel="Inspiration" href="https://github.com/BCDevExchange/docs/blob/master/discussion/projectstates.md"><img alt="An idea being explored and shaped. Open for discussion, but may never go anywhere." style="border-width:0" src="http://bcdevexchange.org/badge/1.svg" title="An idea being explored and shaped. Open for discussion, but may never go anywhere." /></a>

---
[Back to Discussion Index](../discussion_index.md)


##LinkedIn for Profiles

**Release 1** The LinkedIn API is somewhat limited in how it can be used (both in breadth of records being queried and throttling). It’s being proposed that LinkedIn profiles registered with BCDevExchange be regularly queried and cached on BCDevExchange, which can then be queried by users in real time. This is intended to prevent permanently storing this data, as it will persist temporarily (albeit repeatedly), and will help alleviate some architectural and performance concerns anticipated by using the LinkedIn API. Token used to query LinkedIn profiles via the LinkedIn API are only valid for 60 days. Users will have to be made aware of this limitation, and that they will only be returned by queries for 60 days following their last log in to BCDevExchange.
