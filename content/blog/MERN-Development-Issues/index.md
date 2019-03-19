---
title: MERN Development Issues
date: "2019-02-25T011:34:44.933Z"
spoiler: "Some problems encountered to take notes."
---

# List of Issues

1. Async await array of promises
   > When using async operations inside a `map` function, `Promise.all` has to be added before `arr.map()`, because it returns an array of promises.

   ```javascript
   const result = await Promise.all(arr.map((ele) => {
       return Book.findById(ele._id)
   }));
   ```

2. Comparing Mongoose `_id`s
    > Since Mongoose `_id` is of type `ObjectId`, should use `.equals()` to compare instead of `===`

3. Omit keys from an object

    ```javascript
    const obj = { a: 1, b: 2, c: 3, d: 4 };
    const { a, ...wanted } = obj;
    ```