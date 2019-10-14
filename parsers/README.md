# Parsers

### `route_finder`

When an application starts growing it's hard to keep tracking the existing routes. Therefore, I created this script to look forward for all routes and a list of them and respective middlewares - which was really helpful when documenting them.
This parser would find routes described as:

```js
router.post('POST /some-route', 'some-route', 'someMiddleware', 'otherMiddleware', async () => { ... });
```

**Output:**

```text
POST /some-route  someMiddleware  otherMiddleware
POST /some-other-route-with-no-middlewares
```

Also, it has the stopping case when the route is bad formed (like being commented) or has more than 5 middlewares (which would never happen in the application I was building).
