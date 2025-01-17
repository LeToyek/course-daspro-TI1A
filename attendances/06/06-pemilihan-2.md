## JOBSHEET 6

## PEMILIHAN 2

### Tujuan

Mahasiswa memahami tentang operator logika; Mahasiswa mampu menyelesaikan permasalahan dengan menggunakan sintaks pemilihan bersarang; Mahasiswa mampu membuat sebuah program Java yang memanfaatkan sintaks pemilihan bersarang


### Alat dan Bahan
+ PC/laptop
+ Browser(chrome, firefox, safari)
+ Koneksi internet

### Praktikum

#### Percobaan 1

#### Waktu percobaan : 40 menit

1. Tambahkan library Scanner, deklarasi Scanner

2. Buatlah variabel nilai yang memiliki tipe data int untuk menampung data yang diinput melalui keyboard

    ![](images/03.png)


```Java
// Ketik kode di sini
import java.util.Scanner;
Scanner input = new Scanner(System.in);
int nilai;
System.out.print("Masukkan nilai ujian0-100: ");
nilai = input.nextInt();
```

    Masukkan nilai ujian0-100: 60


3. Buatlah struktur pengecekan kondisi bersarang. Pengecekan pertama digunakan untuk memastikan bahwa nilai yang dimasukkan berada pada rentang 0 – 100. Jika nilai berada pada rentang 0 – 100, maka akan dilakukan pengecekan status kelulusan mahasiswa, yaitu jika nilai di antara 90 – 100 maka nilainya A, jika nilai di antara 80 – 89 maka nilainya B, jika nilai di antara 60 – 79 maka nilainya C, jika nilai di antara 50 – 59 maka nilainya D, dan jika nilai di antara 0 – 49 maka nilainya E. Sedangkan jika nilai berada di luar rentang 0 – 100, maka ditampilkan informasi bahwa nilai yang dimasukkan tidak valid.

    ![](images/04.png)


```Java
// Ketik kode di sini
if (nilai >= 0 && nilai <=100){
    if(nilai >= 90 && nilai <= 100){
        System.out.println("Nilai A, EXCELLENT");
    } else if (nilai >= 80 && nilai <= 89){
         System.out.println("Nilai B, Pertahanakn nilai Anda! ");
    } else if (nilai >= 60 && nilai <= 79){
        System.out.println("Nilai C, Tingkatkan pretasi anda! ");
    } else if(nilai >= 50 && nilai <= 59){
        System.out.println("Nilai D,Tingkatkan belajar anda! ");
    } else{
        System.out.println("Nilai E, Anda tidak lulus!");
    }
} else {
    System.out.println("Nilai yang anda  masukkan tidak valid! ");
}
```

    Nilai C, Tingkatkan pretasi anda! 


> Penjelasan kode program percobaan 1

##### Pertanyaan

1. Modifikasi kode program pada Percobaan 1 sehingga jika nilai yang dimasukkan kurang dari 0 akan ditampilkan output “Nilai yang Anda masukkan kurang dari 0” dan jika nilai yang dimasukkan lebih dari 100 akan ditampilkan output “Nilai yang Anda masukkan lebih dari 100”!

2. Jelaskan fungsi sintaks if (nilai >= 0 && nilai <= 100)!

3. Ubah operator && menjadi || pada sintaks if (nilai >= 0 && nilai <= 100). Jalankan program dengan memasukkan nilai = 105. Amati apa yang terjadi! Mengapa hasilnya demikian?


```Java
// Jawaban pertanyaan
```

#### Percobaan 2

#### Waktu percobaan : 40 menit

1. Perhatikan flowchart dibawah ini!

![](images/02.png)

> Flowchart tersebut digunakan untuk menghitung gaji bersih seseorang setelah dipotong pajak sesuai dengan kategorinya (pekerja dan pebisnis) dan besarnya penghasilan. 

2. Tambahkan library Scanner dan deklarasi Scanner

3. Deklarasikan variabel kategori, penghasilan, gajiBersih, dan pajak

    ![](images/05.png)


```Java
// Ketik kode di sini
import java.util.Scanner;
Scanner input = new Scanner (System.in);
String kategori ;
int penghasilan, gajiBersih;
double pajak= 0;

System.out.print("Masukkan kategori : ");
kategori = input.nextLine();
System.out.print("Masukkan besarnya penghasilan: ");
penghasilan = input.nextInt();
```

    Masukkan kategori : 5
    Masukkan besarnya penghasilan: 500000


4. Buatlah struktur pengecekan kondisi bersarang. Pengecekan pertama digunakan untuk mengecek kategori (pekerja atau pebisnis). Selanjutnya dilakukan pengecekan kedua untuk menentukan besarnya pajak berdasarkan penghasilan yang telah dimasukkan.Kemudian tambahkan kode program untuk menghitung gaji bersih yang diterima setelah dipotong pajak!

    ![](images/06.png)


```Java
 if (kategori.equalsIgnoreCase("Pekerja")){
 if (penghasilan<=2000000){
     pajak = 0.1;
 }else if (penghasilan <=3000000){
     pajak = 0.15;
 }else {
     pajak = 0.2;
 }
 gajiBersih = (int) (penghasilan - (penghasilan*pajak));
 System.out.println("Gaji bersih yang anda terima adalah" + gajiBersih);
 
 }else if (kategori.equalsIgnoreCase ("Pebinis ")){
 if (penghasilan <= 2500000){
     pajak = 0.15;
 }else if (penghasilan <= 3500000){
     pajak = 0.2;
 } else{
 pajak = 0.25;
 }
 gajiBersih = (int) (penghasilan - (penghasilan * pajak));
 System.out.println("Gaji bersih yang anda terima " + gajiBersih);
 }else{
     System.out.println("Kategori yang anda masukkan salah! ");
 }
```

    Kategori yang anda masukkan salah! 


5. Jalankan program di atas. Amati apa yang terjadi!

> Penjelasan kode program percobaan 2

##### Pertanyaan

1. Jalankan program dengan memasukkan kategori = pekerja dan penghasilan = 2048485. Amati apa yang terjadi! Mengapa angka di belakang koma tidak ditampilkan?

2. Jelaskan fungsi dari (int) pada sintaks:
```
gajiBersih = (int) (penghasilan - (penghasilan * pajak));
```

3.	Jalankan program dengan memasukkan kategori = pebisnis dan penghasilan = 2000000. Amati apa yang terjadi! Apa kegunaan dari equalsIgnoreCase?

4.	Ubah equalsIgnoreCase menjadi equals, kemudian jalankan program dengan memasukkan kategori = pebisnis dan penghasilan = 2000000. Amati apa yang terjadi! Mengapa hasilnya demikian? Apa kegunaan dari equals?


```Java
// Jawaban pertanyaan
```

### Tugas

#### Waktu pengerjaan Tugas: 140 menit

1. Buatlah program kalkulator sederhana menggunakan bahasa pemrograman Java. User akan menginputkan dua buah bilangan riil dan satu buah operator aritmatika (+, -, *, atau /), kemudian program akan mengoperasikan dua bilangan tersebut dengan operator yang sesuai. Petunjuk: gunakan pernyataan switch-case.
Contoh tampilan program:

```
Masukkan bilangan pertama: 2.5
Masukkan operator (+, -, *, /): *
Masukkan bilangan kedua: 4
2.5 * 4.0 = 10.0

```


```Java
import java.util.Scanner;
public class Tugas1{
    public static void main (String[] args){
    Scanner input = new Scanner (System.in);
     System.out.println("Nilai");
    
    System.out.print("Masukkan bilangan pertama: ");
    double bilanganPertama = input.nextDouble();
    System.out.print("Masukkan operator");
    input.nextLine();
    String operator =  input.nextLine();
    System.out.print("Masukkan bilangan kedua: ");
    double bilanganKedua = input.nextDouble();

    switch(operator.charAt(0)){
        case'+':
        System.out.println(bilanganPertama+""+operator+""+bilanganKedua+"=" + (bilanganPertama + bilanganKedua));
        break;
        case '-':
        System.out.println(bilanganKedua+""+operator+""+bilanganKedua+"="+ (bilanganPertama - bilanganKedua));
        break;
        case '*':
        System.out.println(bilanganPertama+""+operator+""+bilanganKedua+"="+(bilanganPertama * bilanganKedua));
        break;
        case '/':
        System.out.println(bilanganPertama+""+operator+""+bilanganKedua+"="+(bilanganPertama / bilanganKedua));
        break;
        default:
        System.out.println("Operator yang anda masukkan salah");
    }
    }
}
```

2. Dengan menggunakan tiga nilai yang mewakili panjang tiga sisi sebuah segitiga, tentukan apakah segitiga tersebut sama sisi (ketiga sisinya bernilai sama), sama kaki (kedua sisinya bernilai sama), atau sembarang (tidak ada sisi yang bernilai sama)! 


```Java
import java.util.Scanner;
public class Tugas2{
    public static void main (String[] args){
         Scanner input = new Scanner (System.in);
    System.out.println("Panjang sisi segitiga");

    System.out.print("Masukkan sisi 1 ");
    double sisi1 = input.nextDouble();
    System.out.print("Masukkan sisi 2 ");
    double sisi2 = input.nextDouble();
    System.out.print("Masukkan sisi 3 ");
    double sisi3 = input.nextDouble();

    if (sisi1 == sisi2 && sisi1 == sisi3 && sisi2 == sisi3){
         System.out.println ("Sama sisi");   
    }if (sisi1 == sisi2 || sisi1 == sisi3 || sisi2 == sisi3){
        System.out.println ("Sama kaki");
    }else {
        System.out.println("sembarang");
    }
    }
}
```

3. Warung Padang Gembira meminta Anda membuat sebuah program untuk menerima pesanan dari internet. Program yang Anda buat meminta user untuk memasukkan nama makanan dan harga. Setelah itu, user ditawarkan untuk menggunakan pengiriman ekspres. Jika pengguna menolak, maka jenis pengiriman yang digunakan adalah pengiriman reguler. Biaya pengiriman reguler untuk harga makanan kurang dari Rp 100.000 adalah Rp 20.000, sedangkan untuk harga makanan sama dengan atau lebih dari Rp 100.000 biaya pengirimannya adalah Rp 30.000. Untuk jenis pengiriman ekspres, tambahkan biaya tambahan sebesar Rp 25.000 dari standar biaya pengiriman reguler. Tampilkan struk yang berisi nama makanan yang dibeli + harga, biaya pengiriman, dan total yang harus dibayar!
Contoh hasil output program:

```
Masukkan nama makanan: Tuna salad
Masukkan harga makanan: Rp 115000
Apakah Anda ingin pengiriman ekspres (0 = tidak, 1 = ya)? 0

STRUK PEMBELIAN
Tuna salad        Rp 115000
Biaya pengiriman  Rp 30000
TOTAL             Rp 145000

```

```
Masukkan nama makanan: Beef bulgogi
Masukkan harga makanan: Rp 78000
Apakah Anda ingin pengiriman ekspres (0 = tidak, 1 = ya)? 1

STRUK PEMBELIAN
Beef bulgogi      Rp 115000
Biaya pengiriman  Rp 45000
TOTAL             Rp 123000

```




```Java
import java.util.Scanner;
public class Tugas3{
    public static void main (String[] args){
        Scanner input = new Scanner(System.in);
        String namaMakanan,pengiriman;
        int hargaMakan,biayaKirim = 0, totalKirim = 0, totalBayar;

        System.out.print("Masukkan nama makanan : ");
        namaMakanan = input.nextLine();
        System.out.print("Masukkan harga makanan : ");
        hargaMakan = input.nextInt();
        input.nextLine();
        System.out.print("Apakah anda ingin pengiriman ekspres? (y/n) : ");
        pengiriman = input.nextLine();

        if (hargaMakan < 100000 && pengiriman.equalsIgnoreCase("y")){
            biayaKirim = 20000;
            totalKirim = biayaKirim + 25000;
        }else if (hargaMakan < 100000 && pengiriman.equalsIgnoreCase("n")){
            biayaKirim = 20000;
        }else if (hargaMakan >= 100000 && pengiriman.equalsIgnoreCase("y")){
            biayaKirim = 30000;
            totalKirim = biayaKirim + 25000;
        }else if(hargaMakan >= 100000 && pengiriman.equalsIgnoreCase("n")){
            biayaKirim = 30000;
        }else{
            System.out.print("Huruf yang anda masukkan salah ");
        }
        totalBayar = hargaMakan + totalKirim;
        System.out.println("Struk pembelian");
        System.out.println(namaMakanan +"Rp" + hargaMakan);
        System.out.println("Biaya pengiriman rp " + totalKirim);
        System.out.println("Total Rp " + totalBayar);
    }
}
```

4. Perhatikan flowchart berikut ini!

![](images/01.png)

> Buatlah program sesuai dengan flowchart diatas!


```Java
import java.util.Scanner;
public class Tugas4 {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        String status;
        int umur, gaji, tanggungan, biayaakhir;

        System.out.print("Umur \t  : ");
        umur = input.nextInt();
        input.nextLine();

    if(umur >=18){
        System.out.print("Sudah Bekerja? (y/n) ");
        status = input.nextLine();
    
    if (status.equalsIgnoreCase ("y")){
        System.out.print("Gaji Perbulan \t: Rp ");
        gaji = input.nextInt();
        System.out.print("Tanggungan Keluarga \t: ");
        tanggungan = input.nextInt();
        
        biayaakhir = gaji/tanggungan;
        System.out.print("\nBiaya Hidup Anda Rp "+biayaakhir);
        
    if (biayaakhir > 300000){
      System.out.println("\nAnda tidak termasuk penduduk miskin");
    } else {
      System.out.println("\nAnda termasuk penduduk miskin");
    }
        
} else {
    System.out.println("Anda termasuk penduduk miskin");
}
    
} else {
    System.out.print("Anda Masih Sekolah? (y/n) ");
    status = input.nextLine();
    
     if (status.equalsIgnoreCase ("y")){
        System.out.println("Anda tidak termasuk penduduk miskin");
    } else {
         System.out.println("Anda termasuk penduduk miskin");
    }
}
}
}
```


```Java

```
