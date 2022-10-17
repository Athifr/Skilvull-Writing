# Writing Task Week 4

## **Javascript Asynchronus Fetch**
Dalam JavaScript kita bisa mengirimkan network request dan juga bisa mengambil informasi data terbaru dari server jika dibutuhkan.
Proses melakukan fetch() adalah salah satu proses asynchronous di JavaScript sehingga kita perlu menggunakan salah satu diantara promise atau async/await.

**Fetch dengan promise**
```
fetch("https://jsonplaceholder.typicode.com/posts")
  .then(function (response) {
    return response.json();
  })
  .then(function (post) {
    console.log(post);
  });
```

**FetAsync/await baru ada ketika update ES8  JavaScript dan dibangun menggunakan promise. Jadi sebenarnya async/await dan promise itu sama saja, namun hanya berbeda dari syntax dan cara penggunaannya.

Ada 2 kata kunci yang memiliki pengertian sebagai berikut:

async, mengubah function synchronous menjadi asynchronous.
await, menunda eksekusi hingga proses asynchronous selesai.
Sebuah async function bisa tidak berisi await sama sekali atau lebih dari satu await. Keyword await hanya bisa digunakan didalam async function, jika digunakan di luar async function maka akan terjadi error.ch dengan async/await**
```
const tesFetchAsync = async () => {
  let response = await fetch("https://jsonplaceholder.typicode.com/posts");
  response = await response.json();
  console.log(response);
};
tesFetchAsync();
```

## **Javascript Asynchronus Await**
Async/await baru ada ketika update ES8  JavaScript dan dibangun menggunakan promise. Jadi sebenarnya async/await dan promise itu sama saja, namun hanya berbeda dari syntax dan cara penggunaannya.
Ada 2 kata kunci yang memiliki pengertian sebagai berikut:
- async, mengubah function synchronous menjadi asynchronous.
- await, menunda eksekusi hingga proses asynchronous selesai.
Sebuah async function bisa tidak berisi await sama sekali atau lebih dari satu await. Keyword await hanya bisa digunakan didalam async function, jika digunakan di luar async function maka akan terjadi error.

Contoh penggunaan Async
```
// async menggunakan keyword function 
async function tesAsyncAwait() {
  return "Fulfilled";
}

console.log(tesAsyncAwait());
// async menggunakan arrow function
const tesAsyncAwait = async () => {
  return "Fulfilled";
};

console.log(tesAsyncAwait());
```
Contoh Penggunaan Await:
```
async function tesAsyncAwait() {
   await 'Fulfilled';
}
```

## **Git & Github lanjutan**
