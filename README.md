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


