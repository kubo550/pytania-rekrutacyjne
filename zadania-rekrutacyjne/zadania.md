1. **Please write a function that reverses a string**

2. **Please write a function that filters out numbers from a list**

3. **Please write a function that shows the usage of closures**

4. **Please write a recursive function that flattens an list of items**
   _example input_ `[[2, [4, [44,5,6]]], [4,5,6], [[2,4], 4], 5]`
   _example output_ `[2, 4, 44, 5, 6, 4, 5, 6, 2, 4, 4, 5]`

5. **Please write a function that finds all common elements of two arrays(only primitive types as array elements, order doesn't matter)**
   _example inputs_ `['b', 3, 4, 76, 'c']`, `['a', 'b', 4, 76, 21, 'e']`
   _example output_ `['b', 4, 76]`

6. **Please write a function that finds all different elements of two arrays(only primitive types as array elements, order doesn't matter)**
   _example inputs_ `['b', 3, 4, 76, 'c']`, `['a', 'b', 4, 76, 21, 'e']`
   _example output ['a', 3, 21, 'c', 'e']_

7. **Please write a function that transforms an object to a list of [key, value] tuples.**
   _example input_ `{ color: 'Blue', id: '22', size: 'xl' }`
   _example output_ `[['color', 'blue'], ['id', '22'], ['size', 'xl']]`

8. **Please write a function that transforms a list of [key, value] tuples to object. reverse or task 7**
   _example input_ `[['color', 'blue'], ['id', '22'], ['size', 'xl']]`
   _example output_ `{ color: 'Blue', id: '22', size: 'xl' }`

9. **Please write a function that takes two arrays of items and returns an array of tuples made from two input arrays at the same indexes. Excessive items should be dropped.**
   _example input_ `[1,2,3], [4,5,6,7]`
   _example output_ `[[1,4], [2,5], [3,6]]`

10. **Please write a function which takes a path(path is an array of keys) and object, then returns value at this path. If value at path doesn't exists, return undefined.**
    _example inputs_ `['a', 'b', 'c', 'd']`, `{ a: { b: { c: { d: '23' } } } }`
    _example output_ `'23'`

11. **Please write compare function which compares 2 objects for equality.**
    _example input_ `{ a: 'b', c: 'd' }`, `{ c: 'd', a: 'b' }` => `true`
    _example input_ `{ a: 'c', c: 'a' }`, `{ c: 'd', a: 'b', q: 's' }` => `false`

12. **Please write a function which takes a list of keys and an object, then returns this object, just without keys from the list**
    _example input_ `['color', 'size']`, `{ color: 'Blue', id: '22', size: 'xl' }`
    _example output_ `{ id: '22' }`

13. **Write a function that receives two sequences: A and B of integers and returns one sequence C. Sequence C should contain all elements from sequence A (maintaining the order) except those, that are present in sequence B p times, where p is a prime number.**

_Example:_
`A=[2,3,9,2,5,1,3,7,10] `
`B=[2,1,3,4,3,10,6,6,1,7,10,10,10] `
`C=[2,9,2,5,7,10] `

**Notes:**

1. The time complexity is important – try to write an algorithm with good time complexity and specify it in your answer.

2. You can choose any reasonable type present in your chosen language to represent the sequence.

3. Make sure the function signature is correct.

4. Write your own code to test primality.

5. We won't run the code, so don't worry about making it compilable. For example, you can skip any header files.
