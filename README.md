# js-codeing-test

### Sorting array without sort method in javascript

```js
let arr = [4, 32, 2, 5, 8];

for (let i = 0; i < arr.length; i++) {
  for (let j = i + 1; j < arr.length; j++) {
    if (arr[i] > arr[j]) {
      temp = arr[i];
      arr[i] = arr[j];
      arr[j] = temp;
    }
  }
}
console.log("Sorted array=>", arr);

```

```js

function bubbleSort(array) {
  var done = false;
  while (!done) {
    done = true;
    for (var i = 1; i < array.length; i += 1) {
      if (array[i - 1] > array[i]) {
        done = false;
        var tmp = array[i - 1];
        array[i - 1] = array[i];
        array[i] = tmp;
      }
    }
  }

  return array;
}

var numbers = [12, 10, 15, 11, 14, 13, 16];
bubbleSort(numbers);
console.log(numbers);

```

### Remove Duplicate value from an array

```js

const a = [11,41,56,34,34,78];

const newArray = [];
a.forEach((itema)=>{
    const index = newArray.findIndex((itemb)=>itema===itemb);
    if(index === -1){
        newArray.push(itema);
    }
})
console.log('Item--', newArray)

```

### Get same value from two array

```js

const a = [11,41,56,34, 78];
const b = [10,55,56,34 ,90,65,41];

const newArray = [];
a.forEach((itema)=>{
    const index = b.findIndex((itemb)=>itema===itemb);
    if(index > -1){
        newArray.push(itema);
    }
})
console.log('Item--', newArray)

//Out put Item-- [ 41, 56, 34 ]

```

### Get unique value from two arrays

```js

const arr1 = [11,41,56,34, 78];
const arr2 = [10, 55, 56, 34, 90, 65, 41];

let unique1 = arr1.filter((o) => arr2.indexOf(o) === -1);
let unique2 = arr2.filter((o) => arr1.indexOf(o) === -1);
const unique = unique1.concat(unique2);
console.log(unique);

// [ 11, 78, 10, 55, 90, 65 ]

```

### MAKE AN ARRAY EMPTY

```js

const array2 = [11, 41, 56, 34, 78];

array2.splice(0, array2.length)

OR 

for(let i = array2.length; i >= 0; i--){
    
    //array2.pop(i)
    OR
    //array2.shift(i)
}

console.log(array2)

```

```js

const a = [11,12,13,14,15];



let tmp = [ ...a ];
//array.splice(0,a.length)
for(let i = 0; i <= a.length; i++) {
    
    
    tmp.shift(i);
    
   // a.pop(i);
    
}

console.log('=',tmp);

```



