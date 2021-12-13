# blockSortJS
A JS implementation of the blockSort algorithm 

## Usage
#### blockSort(Array arrayToSort, (<i>optional</i>)int sortby, (<i>optional</i>)boolean descend)
<b>arrayToSort</b>: array to be sorted

<b>sortby</b>: if arrayToSort is an array of arrays/objects, specify sortby which element of the subarrays/objects, default = 0

<b>descend</b>: sort in descend order if true

## Example
```
let sorted = blockSort([1.3,2.3,4.3,1.1,3.2,2,4.5]);
console.log(sorted);
// expect:[ 1.1, 1.3, 2, 2.3, 3.2, 4.3, 4.5 ]

sorted = blockSort([1.3,2.3,4.3,1.1,3.2,2,4.5], true);
console.log(sorted);
// expect:[ 4.5, 4.3, 3.2, 2.3, 2, 1.3, 1.1 ]

sorted = blockSort([["john", 4.5], ["k", 1.3], ["paul", 2.3], ["angle", 4.3], ["jack", 1.1], ["n", 3.2], ["abby", 2]]);
console.log(sorted);
// expect:[ [ "abby", 2 ], [ "angle", 4.3 ], [ "jack", 1.1 ], [ "john", 4.5 ], [ "k", 1.3 ], [ "n", 3.2 ], [ "paul", 2.3 ] ]

sorted = blockSort([["john", 4.5], ["k", 1.3], ["paul", 2.3], ["angle", 4.3], ["jack", 1.1], ["n", 3.2], ["abby", 2]], 1);
console.log(sorted);
// expect:[ [ "jack", 1.1 ], [ "k", 1.3 ], [ "abby", 2 ], [ "paul", 2.3 ], [ "n", 3.2 ], [ "angle", 4.3 ], [ "john", 4.5 ] ]

sorted = blockSort([["john", 4.5], ["k", 1.3], ["paul", 2.3], ["angle", 4.3], ["jack", 1.1], ["n", 3.2], ["abby", 2]], 1, true);
console.log(sorted);
// expect: [ [ "john", 4.5 ], [ "angle", 4.3 ], [ "n", 3.2 ], [ "paul", 2.3 ], [ "abby", 2 ], [ "k", 1.3 ], [ "jack", 1.1 ] ]

sorted = blockSort([{ name: "john", num: 4.5 }, { name: "k", num: 1.3 }, { name: "paul", num: 2.3 }, { name: "angle", num: 4.3 }, { name: "jack", num: 1.1 }, { name: "n", num: 3.2 }, { name: "abby", num: 2 }], "num")
console.log(sorted);
// expect: [ { name: "jack", num: 1.1 }, { name: "k", num: 1.3 }, { name: "abby", num: 2 }, { name: "paul", num: 2.3 }, { name: "n", num: 3.2 }, { name: "angle", num: 4.3 }, { name: "john", num: 4.5 } ]
```
