---
title: Promise/Async & Await Caveat
date: "2019-03-19T16:39:44.619Z"
spoiler: "Some notes on Promise and Async/Await."
---

# Knowledge

1. `.then()` and `.catch()` return new Promise.

2. `Promise.resolve()` and `Promise.reject()` is shorthand for `new Promise((resolve, reject) => {})`, also return new Promise.

3. `async` function returns Promise.

4. `return await` is redundant *relative to* just `return`

```javascript
const promise = () => {
    return asyncFunction();
}

const redundantPromise = async() => {
    return await asyncFunction();
}

// Also returns a promise but won't resolve as expected!!! Because the wanted promise is not returned, instead returned a new promise as what async function returns
const differentPromise = async() => {
    await asyncFunction();
}

console.log((async() => {})()) // Promise { undefined }
console.log((async () => { await null; })()) // Promise { <pending> }
```

5. `Promise.all()` returns one Promise
