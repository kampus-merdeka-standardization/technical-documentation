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

### API details

![lld example 2](https://walkingtree.tech/wp-content/uploads/2022/04/image1-3.png)

### Database design
![lld example 3](https://walkingtree.tech/wp-content/uploads/2022/04/image4-2.png)

### Technical specifications

![lld example 4](https://walkingtree.tech/wp-content/uploads/2022/04/image2-3.png)

## Diagram

### Usecase

### Sequence

```mermaid
sequenceDiagram
    participant A as Alice
    participant J as John
    A->>J: Hello John, how are you?
    J->>A: Great!
```

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

## Swagger Link

Masukkan swagger link disini

## How To Build 

Tambahkan build di dalam Makefile untuk build project.

```Makefile
    build:
```

## How To Run

Tambahkan run di dalam Makefile untuk menjalankan project.

```Makefile
    run:
```

## How To Test

Tambahkan test dan test-coverage di dalam Makefile untuk menjalankan unit test project.

```Makefile
    test:
    
    test-coverage:
```