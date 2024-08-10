# PerfectSquares

An 8 kyu JavaScript Kata created by EricDalrymple91.

## Instructions and Background

Given an integer, if the length of it's digits is a perfect square, return a square block of sqroot(length) * sqroot(length). If not, simply return "Not a perfect square!".

Examples:

1212 returns:

"12
12"
Note: 4 digits so 2 squared (2x2 perfect square). 2 digits on each line.

123123123 returns:

"123
123
123"
Note: 9 digits so 3 squared (3x3 perfect square). 3 digits on each line.

## Solution

```
function squareIt(int) {
  var sqRootOfInt = Math.sqrt(int.toString().length)
  if (Number.isInteger(sqRootOfInt) ){
    let somethingMeaningful = []
    for (i=0;i < sqRootOfInt; i++){
      somethingMeaningful.push(int.toString().substring(sqRootOfInt*i, sqRootOfInt*(i+1)));
    } 
    return somethingMeaningful.join('\n')
  } else {
    return 'Not a perfect square!';
  }  
}
```