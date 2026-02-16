Sort vs toSorted in JS
user
explain me diff b/w sort and toSorted in js
ChatGPT
Good question 👍 Let’s break it down clearly:

### `Array.prototype.sort()`
- **Mutates (changes) the original array.**
- Sorts the array *in place*.
- Returns the **same array reference** after sorting.
- Example:

```js
let arr = [3, 1, 2];
let result = arr.sort(); 

console.log(arr);    // [1, 2, 3]  (original array changed)
console.log(result); // [1, 2, 3]  (same reference as arr)
console.log(arr === result); // true
```

---

### `Array.prototype.toSorted()`
- **Does not mutate** the original array.  
- Instead, it creates a **shallow copy** of the array, sorts it, and returns the new array.
- Introduced in **ES2023** as part of new immutable array methods.
- Example:

```js
let arr = [3, 1, 2];
let result = arr.toSorted();

console.log(arr);    // [3, 1, 2]  (original array unchanged)
console.log(result); // [1, 2, 3]  (new sorted array)
console.log(arr === result); // false
```

---

### Key Difference
- `sort()` → **mutable** (changes the original array).
- `toSorted()` → **immutable** (keeps the original intact, returns a new sorted copy).

---

👉 Think of it like this:  
- Use **`sort()`** if you’re okay with the array being changed in place.  
- Use **`toSorted()`** when you want a sorted version but need to keep the original array safe.  
