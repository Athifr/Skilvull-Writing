# Week 3

## Day 1
### Array
- **Array** merupakan pengorganisasian data dan tempat penyimpanan data 
- Array adalah tipe data list order yang dapat menyimpan tipe data apapun dialamnya seperti string, number, boolean dan lainnya
- contoh Array 
``` 
    Let randomData = ['ini string', 20, true];
    console.log(randomData);
```
- Membuat Array : Array didefinisikan dengan square brackets []
- Mengakses Array : Array pada javascript dihitung mulai dari index ke- 0 
``` 
   Let randomData = ['ini string', 20, true];
   console.log(randomDaData[1]); //Output : 20
```
- Update Array 
```
    let arrayData =[1,2,3,4,5]

    console.log("sebelum diupdate:" arrayData[0]]);

    arrayData[0] = 15
    console.log("sesudah diupdate:" arrayData[0]]); 
```
- Const in Array
  - Apabila menggunakan let, array dapat diubah dengan nilai yang baru
  - Const tidak dapat melakukan update data. Namun dapat melakukan update konten nilai di dalam array
  - Tidak dapat mengubah array dengan array baru jika menggunakan const
 - contoh penggunaan const 
 ``` 
    const cars = ['tesla', 'honda', 'toyota'];
    cars[2] = ['nissan'];

    console.log(cars)// output : ['tesla','honda','nissan']
```
- **Array Properti**. Array memiliki 5 properti yang sering digunakan yaitu :
  - constructor
  - length
  - index 
  - input
  - prototype
- .length yaitu mengembalikan nilai dari jumlah panjang data suatu array
    ``` 
    let cars = ['tesla', 'honda', 'toyota'];
    console.log(cars.length) // output 3
    ```
- **Array Method**  atau biasa disebut dengan built in methods 
- Contoh array built in method :
    - .push adalah method untuk menambahkan item array pada urutan yang paling akhir  
    ```
     let cars = ['tesla', 'honda', 'toyota'];
     cars.push('hyundai')
     console.log(cars) // output:['tesla','honda','toyota','hyundai']
    ```
    - .pop adalah method yang menghapus item array index terakhir
    ``` 
     let cars = ['tesla', 'honda', 'toyota'];
     cars.pop()
     console.log(cars) // output: ['tesla','honda']
    ```
    - .shift adalah method untuk menghapus item array pada index pertama 
    ``` 
     let cars = ['tesla', 'honda', 'toyota'];
     cars.shift()
     console.log(cars) // output: ['honda','toyota']
    ```
    - .unshift adalah method untuk menambahkan array pada index pertama 
    ``` 
     let cars = ['tesla', 'honda', 'toyota'];
     cars.unshift('hyundai')
     console.log(cars) // output:['hyundai','tesla','honda','toyota',]
     ```
     - .sort adalah method untuk mengurutkan array secara ascending atau descending
     ``` 
     const numbers = [1,3,5,2,4];
     numbers.sort();
     console.log(numbers) // output : [1,2,3,4,5]
     ```
- **Looping pada Array**. Built in methods untuk melakukan looping pada array ada .map dan .forEach
    - .forEach adalah method untuk melakukan looping pada setiap elemen array 
    ```
    const cars = ['tesla', 'honda', 'toyota'];
    cars.forEach(element => {
    console.log(element);
    });
    ```
    - .map adalah method untuk melakukan perulangan dengan membuat array baru
    ```
    let arr = [1,2,3,4,5];
    
    let doubled = arr.map(num => {
        return num * 2;
    });
    console.log(doubled);
    ```

### Multidimensional Array
   > Multidimensional array bisa dianalogikan sebagai array of array
- Multidimensional array sama seperti matriks yaitu memiliki 2 dimensi (x,y)
    ```
    let inventory = [
        ['Kaos Polos' , 10],
        ['Jaket' , 5],
        ['Topi' , 12],
        ['Celana' , 4],
    ];
    console.log(inventory);
    ```
- Mengakses multidimensional array
     ```
    let inventory = [
        ['Kaos Polos' , 10],
        ['Jaket' , 5],
        ['Topi' , 12],
        ['Celana' , 4],
    ];
    console.log(inventory[1][0]);
    ```
- Penggunaan built in method pada multidimensional array
    ```
    let inventory = [
        ['Kaos Polos' , 10],
        ['Jaket' , 5],
        ['Topi' , 12],
        ['Celana' , 4],
    ];
    inventory.push(['Hoodie', 2]);
    console.log(inventory);
    ```
- Operation using map in multidimensional array
    ```
    let inventory = [
        ['Kaos Polos' , 10],
        ['Jaket' , 5],
        ['Topi' , 12],
        ['Celana' , 4],
    ];
    inventory.map(dataInventory => {
        let terjual = 100 - dataInventory[1];
        dataInventory[2] = terjual;
    });

    console.table(inventory);
    // index | 0 | 1 | 2
    // 0 | 'Kaos Polos' | 10 | 90
    // 1 | 'Jaket' | 5 | 95
    // 2 | 'Topi' | 12 | 88
    // 3 | 'Celana' | 4 | 96
    ```
- Looping pada Multidimensional array
    ```
    let inventory = [
        ['Kaos Polos' , 10],
        ['Jaket' , 5],
        ['Topi' , 12],
        ['Celana' , 4],
    ];
    inventory.forEach((baris) => {
        baris.forEach((column) => {
            console.table(column);
        });
    });

    // Kaos Polos
    // 10
    // Jaket
    // 5
    // Topi
    // 12
    // Celana
    // 4
    ```

## Day 2
### Object
- Object adalah benda mati maupun benda hidup adalah object.
Pada programming object adalah sebuah tipe data pada variabel yg menyimpan properti dan fungsi (method)
- Properti adalah data lengkap dari sebuah object
- Method adalah action dari sebuah object. 
- Contoh object 
    ```
    let person = {
        name : 'Chaca',
        age : 22,
        isVerified: true
    }
    ```
- Cara mengakses object  
    ```
    let person = {
        name : 'Chaca',
        age : 22,
        isVerified: true
    }
    console.log(person);
    ```
- Cara mengakses properti pada object
    ```
    let person = {
        name : 'Chaca',
        age : 22,
        isVerified: true
    }
    console.log(person.name)
    ```
- Saat pemanggilan properti object dapat menggunakan bracket notation
    ```
    let person = {
        name : 'Chaca',
        age : 22,
        'current address': 'Malang','JawaTimur'
    }
    console.log(person['name'])
    ```
- Update object 
  - Object dapat mengupdate value dari key yang sudah tersedia
  - Object dapat menambah key dan value baru
    ```
    let person = {
        name : 'Chaca',
        age : 22,
        isVerified: true
    }
    person.age = 23;
    console.log(person);
    ```
- Delete object properti
    ```
    let person = {
        name : 'Chaca',
        age : 22,
        isVerified: true
    }
    delete person.age;

    console.log(person);
    ```
- Method : jika value yang dimasukkan pada properti berupa function 
- console adalah global javascript object dan log adalah properti yang berupa function dari object console
- Nested Object
- Pass by reference : mengubah data pada object melalui function dan memasukkan object sebagai parameter function
- Looping pada object
- Array of object

### OOP
- **OOP** atau Object Oriented Programming adalah suatu paradigma dalam pemrograman 
- 4 Pilar dalam OOP :
  - Encapsulation adalah cara untuk membatasi akses langsung ke properti atau method dari sebuah objek
    ```
        function Gojek(jarak) {
        const pricePerKm = 4000;
        this.jarak = jarak;

        this.price = function () {
        return pricePerKm * this.jarak;
        };
        }

        let gojek1 = new Gojek(10);
        gojek1.pricePerKm = 10000;

        console.log(gojek1.price());
     ```
  - Inheritance adalah sebuah proses dimana sebuah kelas mewariskan properti dan method ke kelas lain atau childnya
     ```
        class Person {
        constructor(name, age) {
          this.name = name;
          this.age = age;
        }
        greeting() {
        return `Hello ${this.name} umur ${this.age}`;
        }
        }
        class PNS extends Person {
        constructor(name, age, nik, lokasiPenempatan) {super(name, age);
        this.nik = nik;
        this.lokasiPenempatan = lokasiPenempatan;
        }
        detail() {
        return `Hello ${this.name} umur ${this.age} dengan nik ${this.nik} penempatan ${this.lokasiPenempatan}`;
        }
        }
        let pns1 = new PNS("Chaca Caliza", 22, 081119999, "Surabaya");

        console.log(pns1.detail());
     ``` 
  - Polymorpishm adalah kemampuan dari suatu objek untuk memiliki banyak bentuk
     ```
        class Animal {
        sound() {
        console.log("Animal Make sound");
        }
       }

        class Cat extends Animal {
        sound() {
        console.log("Miaw");
        }
       }
       
       class Cow extends Animal {
        sound() {
         console.log("Mooo");
        }
        }
        let anggoraCat = new Cat();
        let sayCow = new Cow();

        angoraCat.sound();
        sayCow.sound();
     ```
  - Abstraction adalah teknik untuk menyembunyikan detail tertentu dari sebuah object atau method dan hanya menampilkan fitur penting dari objek tersebut

### Modules
- Modules memungkinkan untuk memecah kode menjadi file terpisah sehingga mempermudah untuk maintain code
- JavaScript Module bergantung pada pernyataan impor dan ekspor

## Day 3
### Recursive
- Recursive adalah fungsi yang memanggil dirinya sendiri sampai suatu kondisi tertentu terpenuhi
- A new paradigm :
  - Procedural
  - Conditional
  - Looping
  - Modular (function)
  - Recursive
- Ciri dari recursive:
  - Fungsi recursive memiliki kondisi yang menyatakan kapan fungsi tersebut berhenti. 
  - fungsi recursive selalu memaanggil dirinya sendiri sambil mengurangi atau memecahkan data masukan setiap panggilannya.
- Contoh mencari nilai pangkat 
    ```
    function pow(x,n) {
        if (n=1){
            return x;
        } else {
            return x * pow(x, n-1);
        }
    }
    console.log(pow(2,3)) // 8
    ```

### Regex
- **Regex** adalah susunan karakter/karakter spesial yang menggambarkan pattern/pola untuk pencarian text pada sebuah string atau document
   > REGEX = Text Matching
- Contoh penggunaan Regex :
  - Validasi input dari sebuah form
  - Mencari keyword tertentu pada email atau halaman web
  - Mencari IP adress dalam kisaran tertentu
- Membuat Pola Regex
  - Literals adalah konsep regex adalah konsep yang paling sederhana yaitu dengan membuat regex sesuai dengan text yang ingin dicari
- Built in Method Regex
  - test() yaitu built in method untuk regex yang mengembalikan nilai Boolean untuk kecocokan sebuah nilai yang dicari
    ``` 
    let regex1 = new RegExp('Cat');
    console.log(regex1.test('Cat'))// true
    ```
  - Karakter Set digunakan untuk mencari minimal 1 karakter yabg sesuai. Karakter set menggunakan bracket square []
    ``` 
    let regex1 = new RegExp('[a-z]');
    console.log(regex1.test('abc'))// true
     ```
  - match() yaitu method yang mengembalikan nilai array dari karakter yang match
    ``` 
    let myRegex = /c/;
    let myName = 'Chaca';
    console.log(myName.match(myRegex)); // output : [ 'c', index: 3, input: 'Chaca', groups: undefined ]
    ```
   - Flags pada javascript :
     - i : untuk menghandle case-sensitive. Tidak mempermasalhkan besar kecilnya karakter
     - g : untuk mencari kedalam seluruh string yang ingin dicari. Jika tidak menggunakan flags g maka sistem akan mengembalikan nilai array pertama yang ditemukan tanpa melanjutkan pencarian
      ```
      let myRegex = /c/ig;
      let myName = 'Chaca';
      console.log(myName.match(myRegex)); 
      // output : [ 'c', index: 3, input: 'Chaca', groups: undefined ] // output: [ 'C', 'c' ]
      ```
- Karakter Set Short Syntax  
  - \d : seluruh number/digit character
  - \w : alphanumeric character
  - \s : whitespace character (space,tab,newline)
    ``` 
    let myRegex = /\d\s\w\w\w\w\w\w\w/;
    let myName = '3 Kelinci';
    console.log(myRegex.test(myName));// true
    ```
  - Negasi dari set short syntax yaitu menggunakan tanda ^
    ``` 
    let notBinary = /[^01]/
    console.log(notBinary.test['1012']) // true
    ```
  - Quantifiers berfungsi untuk membuat format regex menjadi lebih rapi. 
  - Quantifiers ditandai dengan format {} 
  contoh saat mencari roa{3}r maka akan match dengan string 'roaaar'
  - Quantifiers besifat greedy akan mengambil nilai yang paling besar atau maksimal
  contoh saat mencari roa{3,5}r maka akan match dengan 'roaaar' dan 'roaaaaar' maka yang akan didapatkan adalah yang 'roaaaaar'
  - Anchor yaitu digunakan jika ingin mencari karakter yang sama persis. 
  - Anchor diawali dengan ^ dan diakhiri dengan $
  - Alternation yaitu digunakan untuk mencari karakter yang sama persis dengan lebih dari 1 kalimat
  - Alternation ditandai dengan format (|)
    ``` 
    let search = /^Belajar javascript san react js$ |^ React JS$/
    console.log(search.test{'React JS'}); output : true
    ```

## Day 4
### Asynchronous
## Asynchronous of JavaScript
- Javascript dijalankan pada satu proses atau single-thread
- **Single-thread** atau satu jalur dimana urutan eksekusi kode dilakukan secara berurutan atau synchronous
- **Synchronous** dimana setiap perintah di eksekusi satu persatu sesuai urutan kode yang dituliskan
  - Output dari synchronous akan sesuai urutan, karena setiap perintah harus menunggu perintah sebelumnya selesai. Proses antrian ini disebut *blocking*
- **Multi-thread** atau banyak jalur yang memungkinkan program dapat dipecah dan mengerjakan lebih dari satu tugas dalam satu waktu
- **Asynchronous** dimana proses eksekusi dilakukan secara tidak berurutan (bisa menjalankan perintah lain selagi menunggu suatu perintah diproses)
  - Output dari asynchronous tidak selalu sesuai urutan kode, tetapi berdasarkan waktu proses
  - Proses asynchronous disebut *non-blocking*
- Asynchronous pada javascript memiliki 3 kunci utama, yaitu:
  - Callback
  - Promise
  - Async Await

## Asynchronous - Callback
- Callback merupakan function, namun cara eksekusinya berbeda dengan function biasa
- Function biasa dieksekusi secara langsung (dari atas ke bawah), *callback* dieksekusi pada poin tertentu (parameter)
- Callback dapat digunakan dalam synchronous maupun asynchronous
- Contoh asynchronous
![image](https://user-images.githubusercontent.com/85722923/194787369-9f350c67-2ee3-4baa-ab5d-9dbc47c517eb.png)
- Penjelasan:
  - `setTimeout()`: metode panggilan fungsi setelah beberapa millisecond (delay)
  - `p2` akan kedelay selama 100 millisecond atau 0.1 second
- Contoh penggunaan callback pada asynchronous
![image](https://user-images.githubusercontent.com/85722923/194787841-97762f47-d098-4336-b921-15361dd7fc59.png)
- Penjelasan:
  - Penggunaan callback untuk memperbaiki urutan p1, p2, p3 asynchronous
  - Buat fungsi `p3` menjadi callback untuk `p2`


## Asynchronous - Promise
- Promise merupakan fitur terbaru dari ES6
- Promise merupakan object yang merepresentasikan 3 state:
  - Pending (dalam proses)
  - Fulfilled (berhasil)
  - Rejected (gagal)
- Promise biasanya digunakan sebagai alternatif *callback*, ketika terdapat callback di dalam callback di dalam callback lagi
- Promise hanya dapat berjalan di asynchronous
- Promise dapat membuat kode lebih readable
- Promise memiliki error handling. Jadi, ketika ada kesalahan maka dapat ditindak lanjuti
- Promise mengembalikan object dan hanya dapat digunakan pada satu event
- Untuk membuat promise cukup dengan memanggil constructornya. Contoh penggunaan 3 state:

1. Pending merupakan state awal sebelum menjadi fullfilled atau rejected. Penggunaan state pending ada pada state fulfilled dan rejected

2. Fulfilled


![image](https://user-images.githubusercontent.com/85722923/194790834-ccbf9b76-78a3-4627-96b2-52b9118ff8e0.png)
- Keterangan:
  - `.then()` untuk mengakses promise fulfilled
  - Setelah 2000 ms maka akan tampil `berhasil` di tab console

3. Rejected


![image](https://user-images.githubusercontent.com/85722923/194790893-fe17a394-068f-44de-8cd9-cc11d3fb2ed8.png)
- Keterangan:
  - `.catch()` untuk mengakses promise rejected
  - Setelah 300 ms maka akan tampil `batal` di tab console

## Asynchronous - Async/Await
- Fitur yang hadir sejak ES2017 (ES8)
- Terdapat 2 kata kunci, yaitu `async` dan `await`
```js
    async function f() {

      let janji = new Promise((resolve, reject) => {
        setTimeout(() => resolve("done!"), 300)
      });

      let result = await janji; //wait until the promise resolves
      console.log(result); //Output: done!
    }

    f();
```
- Penjelasan:
  - `async` untuk mengubah function menjadi asynchronous
  - `await` untuk menunda eksekusi hingga proses asynchronous selesai. Dimana `console.log(result)` tidak akan di eksekusi sebelum proses `janji` selesai

## Asynchronous - Fetch
- Fetch merupakan cara baru dalam melakukan network request
- Fetch merupakan API yang memanfaatkan sebuah *Promise* dan diperkenalkan sejak ES6
- Untuk mengaksesnya, gunakan `fetch()` kemudian tuliskan URL yang akan dituju
```js
    fetch('<URL-to-the-resource-that-is-being-requested>')
           .then(response => {
               return response.json()
           })
           .catch(error => {
               console.log(error)
           })
           .then(function(data) {
               //variabel {data} siap digunakan! 
           })
```
- Penjelasan:
  - Fetch mengembalikan sebuah promise
  - Jika request pada fetch berhasil dilakukan, maka `.then()` akan terpanggil dan mengembalikan nilai objek sesuai response yang didapat
  - Jika request pada fetch gagal dilakukan, maka `.catch()` akan terpanggil dan menampilkan error pada console
  - Parameter data pada fungsi `.then()` merupakan nilai yang dikembalikan dari `response.json()` dan menjadi `undefined` jika fungsi fetch gagal dilakukan

## Day 5
### Web Storage
- Web Storage adalah wadah untuk sebuah data yang digunakan untuk penyimpanan data yang terikat di browsernya
- Jenis Web Storage yang umum digunakan yaitu :
  - Local Storage
  - Session storage
  - IndexDB
  - Cookies
- Cara menyimpan data pada local storage 
    ```
        let token = "asdfghjkl" //key
        localStorage.setItem("token", token);
    ```
- Cara mengambil token
    ```
        localstorage.getItem("token", token);
        console.log(localStorage.getItem('token");
    ```
- Cara menghapus data 
    ```
        localStorage.removeItem("token")
    ```
