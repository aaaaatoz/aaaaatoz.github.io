#Cache In Browser

There are two types of caching in modern web browser:
- Strong caching: get the content directly from the browser caching
- negotiated caching: check between browser and web server, then get the content from browser caching

the basic steps:
- when the browser loads the page resource, it will check if it has the content in the cache and if the cache has expired, if not, then it will load the content from cache directly. it is called `strong cache`
- when the resource is still in cache but already expired, browser will check if the content can be got from cache via negotiated with the server, it is called `negotiated cache`
- if the resource is not cached, the browser will get the content from the server directly.

## Strong Cache
Strong Cache is achieved via HTTP `Expired` or `Cache Control` field
eg: Expires:Thu, 31 Dec 2037 23:55:55 GMT. The time is generated either via backend code or attached by the web server. It gives an absolute time to indicate when the resource will be expired.
Strong Cache can be cheated by the client time. In HTTP, it is improved via another field called Cache-Control, eg Cache-Control:max-age=3600 means the resource will be expired after 1 hour from

## Negotiated Cache
Negotiated Cache is achieved via HTTP request and response. Two pairs of field are used:
- Last-Modified/If-Modified-Since
	when the reponse is back from the server, the Last-Modified field will be appended to indicate the last modified time. then when the browser try to request the resource again, it will use that value as If-Modified-Since. If the server checks and finds the resource is not changed, it will reply with a 304.
- ETag/If-None-Match
	the server will attach a etag field (like checksum) to the resource, and the browser will use that field in the request. the server then will compare the two etags and see if they are identical.