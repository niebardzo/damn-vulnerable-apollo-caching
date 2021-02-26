# damn-vulnerable-apollo-caching
The damn vulnerable apollo caching based on the apollo tutorial with little tweaks to make the caching broken.

Based on:
https://github.com/apollographql/fullstack-tutorial

Caching issues:
- Apollo-client stores passwords in in-memory cache, potentially leading to stealing the password through XSS.
- Apollo-client do not clear the in-memory cache upon user's logout, potentially exposing the user's data stored in in-memory cache to users of the same device.
- Apollo-client persist a in-memory cache in local storage, potentially expose user's private data to leakage.
- Apollo-server has wrongly used \@cacheControl, leading to user's private data potential leakage through caching on CDNs.


For full issues write-up, refer to the following blog post:
LINK

To run:
1) Open first terminal, then:
```
cd client && npm install && npm start
```
2) Open second terminal, then:
```
cd server && npm install && npm start
```
