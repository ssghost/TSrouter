---
id: useAwaitedHook
title: useAwaited hook
---

The `useAwaited` method is a hook that suspends until the provided promise is resolved or rejected.

### Options

#### `opts.promise`

- Type: `DeferredPromise<T>`
- Required
- The deferred promise to await

### Returns

- Throws an error if the promise is rejected
- Suspends (throws a promise) if the promise is pending
- Returns the resolved value of a deferred promise if the promise is resolved

### Examples

```tsx
import { useAwaited } from '@tanstack/react-router'

function Component() {
  const { deferredPromise } = route.useLoaderData()
  const data = useAwaited({ promise: myDeferredPromise })
}
```