# damn-vulnerable-apollo-caching
The damn vulnerable apollo caching based on the apollo tutorial with little tweaks to make the caching broken.

Based on:
https://github.com/apollographql/fullstack-tutorial

Caching issues:
- Apollo-client stores passwords in in-memory cache, potentially leading to stealing the password through XSS.
- Apollo-client do not clear the in-memory cache upon user's logout, potentially exposing the user's data stored in in-memory cache to users of the same device.
- Apollo-client persist a in-memory cache in local storage, potentially expose user's private data to leakage.

Server issues:
- \@cacheControl directive wrongly used, leading to user's private data potential caching on CDNs.


For full issues write-up, refer to the following blog post:
LINK
