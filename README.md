# Title

Bagian ini tulislah satu kalimat saja yang menggambarkan keseluruhan project untuk membantu orang memahami apa tujuan dan sasaran utama project tersebut.

## Badge

Tambahkan badge di bawah title. Badge yang harus ditambahkan diantaranya adalah:
1. Build Status: Menunjukkan status dari sistem otomatisasi build
2. Code Coverage: Menunjukkan cakupan coverage unit test
3. Version: Menunjukkan versi terbaru dari project
4. Pull Requests: Menunjukkan banyaknya pull request yang terbuka

![Build Status](https://img.shields.io/badge/Build-Success-brightgreen) ![Code Coverage](https://img.shields.io/badge/Coverage-80%-brightgreen) ![Version](https://img.shields.io/badge/Version-v1.0.0-blue) ![Pull Requests](https://img.shields.io/badge/PR-1-informational)

## Description

Deskripsi adalah bagian yang memberikan gambaran umum tentang proyek yang sedang dikembangkan. Tujuannya adalah untuk menjelaskan apa tujuan proyek, apa masalah yang dipecahkan oleh proyek, dan mengapa proyek ini penting atau berguna.

Ini adalah bagian penting dari suatu proyek, dan banyak pengembang dan non-pengembang akan melihatnya. Sangat penting untuk memiliki informasi yang paling akurat dan benar. Deskripsi perlu ditulis dengan baik tanpa kesalahan tata bahasa dan dapat dibaca oleh pengguna dari berbagai latar belakang. Deskripsi tidak perlu panjang tetapi perlu merangkum keseluruhan proyek. Misalnya, apa yang dilakukan pada aplikasi ini? Teknologi apa saja yang gunakan? dan lain lain.

## Change Log

### [Versi Terbaru] - Tanggal Rilis Terbaru

### Tambah
- Fitur baru yang ditambahkan.
- Fitur baru kedua yang ditambahkan.

### Perbaikan
- Perbaikan bug yang memengaruhi penggunaan proyek.

### Menghapus
- Fitur A telah dihapus dan tidak lagi tersedia pada versi berikutnya.

### Pembaruan
- Pembaruan dokumen atau penjelasan yang ada.

## High Level Design

![hld example](https://media.geeksforgeeks.org/wp-content/cdn-uploads/20210128214233/Netflix-High-Level-System-Architecture.png)

## Low Level Design

### Architectural Diagrams

![lld example](https://walkingtree.tech/wp-content/uploads/2022/04/image3.jpg)

### Technical specifications

## Diagram

### Usecase

```plantuml
@startuml
left to right direction
actor Pustakawan as librarian
actor Anggota as member

rectangle "Sistem Perpustakaan" {
  usecase (UC1) as "Pinjam Buku" 
  usecase (UC2) as "Kembalikan Buku"
  usecase (UC3) as "Perpanjang Peminjaman"
  usecase (UC4) as "Cek Status Buku"
  
  librarian --> UC1
  librarian --> UC2
  member --> UC3
  member --> UC4
}
@enduml
```

hasilnya :

![contoh use case diagram](https://www.planttext.com/api/plantuml/svg/RP2xZW8n34NxVCNLL51GyAXNF4gQaH0VO0PlDaoIGOaZ2iI_huS1f5cjbEhw-DZEEWibAS4Rpzy2wP2S_H6SNU96N1SDDT8br4N1bcuKGHdUdH8bH-_g9bhR2VMbmE74oPY-dQBrZEhWid10pUawM2XMk1kWP6ueCoR7tNpQDrUrYnSAs9QsL1WJYu7Ogv-yQtMH9pM6bY-DZY8rHQjJmzEfCyVeQa1ttE8W92L_VFe-1s8s-uAkzq-sq6ouzXKi_mOhyp1hZcVztby0)

### Sequence

```mermaid
sequenceDiagram
    participant A as Alice
    participant J as John
    A->>J: Hello John, how are you?
    J->>A: Great!
```

atau 

![lld example 4](https://walkingtree.tech/wp-content/uploads/2022/04/image2-3.png)

### ERD

```mermaid
erDiagram
    CAR ||--o{ NAMED-DRIVER : allows
    CAR {
        string registrationNumber PK
        string make
        string model
        string[] parts
    }
    PERSON ||--o{ NAMED-DRIVER : is
    PERSON {
        string driversLicense PK "The license #"
        string(99) firstName "Only 99 characters are allowed"
        string lastName
        string phone UK
        int age
    }
    NAMED-DRIVER {
        string carRegistrationNumber PK, FK
        string driverLicence PK, FK
    }
    MANUFACTURER only one to zero or more CAR : makes
```

atau

![lld example 3](https://walkingtree.tech/wp-content/uploads/2022/04/image4-2.png)

## Swagger Link

Masukkan swagger link disini

## How To Build 

Proses build adalah konversi kode sumber menjadi program eksekusi atau perangkat lunak yang dapat dijalankan. Hasil dari proses build adalah eksekutabel atau pustaka yang siap untuk digunakan. Tambahkan build di dalam Makefile untuk build project.

```Makefile
    build:
```

## How To Run

Proses run adalah eksekusi program atau skrip yang telah dibangun. Ketika sebuah program dijalankan, sistem operasi mengalokasikan sumber daya seperti memori dan CPU, dan instruksi yang terkandung dalam program tersebut dieksekusi secara berurutan. Tambahkan run di dalam Makefile untuk menjalankan project.

```bash
make run
```

## How To Test

Tambahkan test dan test-coverage di dalam Makefile untuk menjalankan unit test project. seperti:

```bash
make test
```
```bash
make test-coverage
```