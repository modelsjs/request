# Concepts on requesting models

Request is a model caller, which adds some benefits.

## Memoization

If third argument passed to request call, it is used as cache storage.

Request composes cache key for model depending on model `displayName` and `props`.

Then it searches this key in cache and returns it if found.

Otherwise it calls model and saves to cache [*unfailure](unfailure) promise.

[1]: If promise will fail it will be automatically uncached. 