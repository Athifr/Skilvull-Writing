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
### Perintah Git
- Membuat branch baru
Untuk menghindari conflict code yang dikembangkan. 
Kita tidak boleh berkolaborasi dalam project di satu branch yang sama!

```
    git branch nama_branch
```
- Melihat list branch
```
    git branch
```
- Pindah ke dalam branch tertentu
```
    git checkout namaBranch_tujuan
```
- Menghapus sebuah branch
```
    git branch -d nama_fitur
```

Setelah membuat branch baru, lalu lakukan commit.
Saatnya kita menyatukan pekerjaan ke master file/branch utama yaitu branch MASTER
Lakukan:
1. Kita harus checkout dahulu ke branch master
```
git checkout master
```
2. Lalu lakukan merge
```
git merge <nama>
```

## RESPONSIVE WEB DESIGN (RWD)
- RWD bertujuan untuk membuat desain web kita dapat diakses dalam device apapun (laptop/PC, smartphone, tablet)
- Tools yang digunakan untuk menerapkan responsive web design:
  - Mengatur viewport
  - Properti max-width
  - Relative CSS unit
  - Media query
  - Flexbox dan grid

### Viewport 
- Viewport merupakan bagian dari responsive website
- Viewport merupakan area website yang dapat diakses user (ukuran layar itu viewport)
- Viewport berada pada meta didalam head file .html
- 1vw = 1% lebar viewport
- Jika lebar viewport sebesar 100cm, maka 1vw adalah 1cm

### max-width
- Untuk menentukan lebar maksimal dari suatu element
- `max-width: 100%`: element akan memiliki lebar maksimum sebesar 100% dari parent element, namun jika ukuran maksimal aslinya tidak selebar parent elementnya, maka akan menampilkan ukuran maksimal aslinya

### Relative CSS Unit
- Salah satu satuan unit relative CSS unit, yaitu %, rem, vh, vw
- Ukuran relative `rem` dan `em` sama sama mengikuti ukuran huruf yang membedakan rem mengikuti ukuran huruf root elemen/HTML sedangkan em mengikuti parent elemen terdekat
- `rem` mengikuti font-size HTML. Ukuran huruf default HTML untuk device laptop itu 16px. Contoh: `font-size: 2rem;` (maka 2 kali 16px)

### Media Query
- Mengatur lebar suatu element atau memberikan style lain yang berbeda-beda sesuai dengan  ukuran dari browser

### Flexbox (*Flexible Box*)
- Memudahkan dalam mengatur layout, posisi, dan ukuran dari tiap element di dalamnya
- Mengatur arah dimensi hanya horizontal saja atau vertical saja
- Ada dua istilah penting saat belajar flexbox:
  - `container` adalah element yang membungkus dan mengatur tampilan dari element di dalamnya
  - `item` adalah element dalam container yang diatur tampilannya

### Grid
- Mengatur arah dimensi secara horizontal dan vertikal

## BOOTSTRAP 5
- Bootstrap adalah framework HTML, CSS, dan JavaScript
- Berfungsi untuk mendesain website menjadi responsive dengan cepat dan mudah
- Framework bootstrap tersusun dari kumpulan file CSS dan JavaScript yang berbentuk class dan tinggal pakai
- Bootstrap sering digunakan website pemerintah
- Framework bootstrap dan tailwind jangan dicollab
- Satu website hanya menggunakan satu framework saja menghindari bentrok class dan menghemat memory
- Cara menggunakan bootstrap:
  - Buka [Bootstrap 5](https://getbootstrap.com/)
  - Klik docs di navbar
  - Klik download di bagian side bar, scroll ke bagian CDN via jsDelivr
  - Copas code CDN ke file .html bagian header
- Grid system bootstrap dibangun dengan menggunakan flexbox
- Styling bootstrap bisa digabung sama css vanilla
