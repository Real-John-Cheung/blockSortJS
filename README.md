# blockSortJS
A JS implementation of the blockSort algorithm 

## Usage
#### blockSort(Array arrayToSort, (<i>optional</i>)int sortby, (<i>optional</i>)boolean descend)
<b>arrayToSort</b>: 1-d or 2-d array to be sorted

<b>sortby</b>: if arrayToSort is 2-d, specify sortby which element of the subarray, default = 0

<b>descend</b>: sort in descend order if true

## Example
```
let sorted = blockSort([1.3,2.3,4.3,1.1,3.2,2,4.5]);
console.log(sort);
// expect:[ 1.1, 1.3, 2, 2.3, 3.2, 4.3, 4.5 ]

sorted = blockSort([1.3,2.3,4.3,1.1,3.2,2,4.5], true);
console.log(sort);
// expect:[ 4.5, 4.3, 3.2, 2.3, 2, 1.3, 1.1 ]

sorted = blockSort([["john", 4.5], ["k", 1.3], ["paul", 2.3], ["angle", 4.3], ["jack", 1.1], ["n", 3.2], ["abby", 2]]);
console.log(sort);
// expect:[ [ "abby", 2 ], [ "angle", 4.3 ], [ "jack", 1.1 ], [ "john", 4.5 ], [ "k", 1.3 ], [ "n", 3.2 ], [ "paul", 2.3 ] ]

sorted = blockSort([["john", 4.5], ["k", 1.3], ["paul", 2.3], ["angle", 4.3], ["jack", 1.1], ["n", 3.2], ["abby", 2]], 1);
console.log(sort);
// expect:[ [ "jack", 1.1 ], [ "k", 1.3 ], [ "abby", 2 ], [ "paul", 2.3 ], [ "n", 3.2 ], [ "angle", 4.3 ], [ "john", 4.5 ] ]

sorted = blockSort([["john", 4.5], ["k", 1.3], ["paul", 2.3], ["angle", 4.3], ["jack", 1.1], ["n", 3.2], ["abby", 2]], 1, true);
console.log(sort);
// expect: [ [ "john", 4.5 ], [ "angle", 4.3 ], [ "n", 3.2 ], [ "paul", 2.3 ], [ "abby", 2 ], [ "k", 1.3 ], [ "jack", 1.1 ] ]
```
