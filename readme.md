# Methods in JS
## What is a method in JS ?
>Method is block of code which helps writing code easyly, also method is known as function, there is string methods, array methods I know, I think there are A LOT of other methods
## What is Array in JS ?
>Array is an object variable which can contain many elements that can be with different values, and every element has its index

>You can change elements in array:
```js
let arr=[1,2,3,4,5,6]
arr[1]=6
//output " [1,6,3,4,5,6] " 
```
# Array Methods
>### pop(), shift(), push(), unshift(), concat(), slice(), <br> join(), includes(), indexOf(), splice(), toString(), toReversed()

>### forEach(), map(), find(), filter(), reduce(), toSorted()

## push() method
### push method adds elements to the end of array and returns length
```js
let arr=[1, true, 3, 4, 'hallo']
let add=arr.push(5, false, 'world')
console.log(add) // 8
console.log(arr) // [1, true, 3, 4, 'hallo', 5, false, 'world']
```
## pop() method
### pop method removes last element and takes it
```js
let arr=['a', 'b', 'c', 'd', 'e']
console.log(arr.pop()) // e
console.log(arr) // ['a', 'b', 'c', 'd']
```
## unshift() method
### unshift method adds elements to the start of array and returns length
```js
let arr=[3,4,5]
console.log(arr.unshift(1,2)) // 5
console.log(arr) // [1,2,3,4,5]
```
## shift() method
### shift method removes first element and takes it
```js
let arr=[1,2,3]
let fe=arr.shift()
console.log(fe) // 3
console.log(arr) // [2,3]
```
## toString() method
### toString method makes array elements string
```js
let arr=[1,2,3]
console.log(arr.toString()) // '1,2,3'
```
# JS array methods
## indexOf() method
### indexOf method finds index which element is given, if there is no element it will give "-1" because -1 index doesn't exist
```js
let arr=[1,'a',2,'b',3,'c']
let ind=arr.indexOf('b')
console.log(ind) // 3
console.log(arr.indexOf("JS")) // -1
```
## includes() method
### includes finds whether given element exists in array or not,and returns true or false
```js
let arr=[1,'hello world',2,3,4]
console.log(arr.includes('hello world')) // true
console.log(arr.includes('hello')) // false
```
## concat()
### concat method connects elements
```js
let arr1=[1,2,3,'hello']
let arr2=['world',4,5,6]
console.log(arr1.concat(arr2)) // [1,2,3,'hello','world',4,5,6]
```
## slice()
### slice method takes elements from given start to end
```js
let arr=[1,2,3,'horse',4,5,6]
console.log(arr.slice(2,5)) // [3,'horse']
```
## splice()
### splice method removes and adds new elements instead of removed element
```js
let arr=[1,2,3,true,4,4,false]
let arr2=arr.splice(2,1,'dog','cat')
console.log(arr2) // [3]-deleted item
console.log(arr) // [1,2,'dog','cat',true,4,4,false]
```
# JS array methods callbacks
## map()
### map method works like loop and works on every element in array
```js
const arr=[1,2,3,4]
// give function to map 
const map=arr.map((x)=>x*2)
console.log(map)
// Expected output: [2,4,6,8]  
```
## forEach()
### forEach method works on elements index
```js
let arr=['haLLo','HoW','are','YOU']
arr.forEach(function(el,ind,ar){
    arr[ind]=el[0].toUpperCase()+el.slice(1).toLowerCase()
})
console.log(arr) // ['Hallo','How','Are','You']
```
## find()
### find method finds first element which compares given testing function
```js
let arr=[1,2,3,4,5,6,7,8]
let f=arr.find((el)=>el>5)
console.log(f) // 6
```
## filter()
### filter method finds true elements and returns it
```js
let arr=['hallo','worlds','how','how you doin']
let fil=arr.filter((el)=>el.length>5)
console.log(fil) // ['worlds','how you doin']
```
## reduce()
### reduce method takes two //////// :
1. callback which takes two ////////
   1. accumulator 'starting with first index [0]'
   2. currentValue 'starting with second index [1]'
2. ///////////
```js
let arr=[1,2,3,4,5]
let sum=arr.reduce((acc,cur)=>acc+cur,0)
console.log(sum) // 15
```
## toSorted()
### toSorted method puts elements in ascending order
```js
let a=[3,5,2,1,4]
let reva=a.toSorted()
console.log(reva) // [1,2,3,4,5]
console.log(a) // [3,5,2,1,4]

let b=['d','a','e','c','b']
let revb=b.toSorted()
console.log(revb) // ['a','b','c','d','e']
console.log(b) // ['d','a','e','c','b']
```
# Mechanism
## Destructuring
### Destructuring mechanism can give values to variables from array or objects
```js
let a,b,rest
[a, b, ...rest]=[5,10,23,4,67,8]
console.log(a) // 5
console.log(b) // 10
console.log(rest) // [23,4.67.8]
```
## spread
### spread mechanism allows copy (japs) from other variables
```js
let a=[1,2,3,4,5]
let b=[...a]
console.log(b) // [1,2,3,4,5]
```
## rest 
### rest mechanism allows to enter infinit values into array
```js
function inf(a, ...b){
    console.log(a) // 1
    console.log(b) // [2,3,4,5]<=in array
}
console.log(inf(1,2,3,4,5))
```