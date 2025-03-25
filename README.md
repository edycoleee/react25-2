# REACT VITE 2025

## 1. PERSIAPAN AWAL

PERSIAPAN AWAL

```
npm create vite@latest siswa-app1 --template react
cd siswa-app
npm install
npm install nanoid
npm install --save-dev @playwright/test

```

GITHUB

```
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/edycoleee/react25-2.git

```

## 2. SIMULASI DATABASE DENGAN JSON SERVER

Instalasi JSON Server

```js
npm install -g json-server
```
Buat File db.json

```js
{
  "tbSiswa": [
    {
      "id": 1,
      "siswaName": "Budi",
      "siswaAlamat": "Jakarta"
    },
    {
      "id": 2,
      "siswaName": "Andi",
      "siswaAlamat": "Bandung"
    },
    {
      "id": 3,
      "siswaName": "Cindy",
      "siswaAlamat": "Surabaya"
    }
  ]
}
```
Jalankan JSON Server
```js
json-server --watch db.json --port 5000

```

## 3. API SPEC UNTUK DATA SISWA

```
Metode	Endpoint	    Fungsi	                    Body (JSON)
GET	    /tbSiswa	    Mendapatkan semua siswa	    ❌
GET	    /tbSiswa/:id	Mendapatkan satu siswa	    ❌
POST	/tbSiswa	    Menambah siswa baru	        ✅ (Lihat di bawah)
PUT	    /tbSiswa/:id	Mengupdate siswa	        ✅ (Lihat di bawah)
PATCH	/tbSiswa/:id	Mengupdate sebagian data	✅ (Lihat di bawah)
DELETE	/tbSiswa/:id	Menghapus siswa	            ❌
```

### 1. GET /tbSiswa
🔹 Deskripsi: Mengambil semua data siswa.

Request:
```http
GET /tbSiswa
```
Response: 200 OK
```json
[
  {
    "id": 1,
    "siswaName": "Budi",
    "siswaAlamat": "Jakarta"
  },
  {
    "id": 2,
    "siswaName": "Andi",
    "siswaAlamat": "Bandung"
  },
  {
    "id": 3,
    "siswaName": "Cindy",
    "siswaAlamat": "Surabaya"
  }
]
```
### 2. GET /tbSiswa/:id
🔹 Deskripsi: Mengambil data siswa berdasarkan id.

Request:
```http
GET /tbSiswa/2
```
Response: 200 OK
```json
{
  "id": 2,
  "siswaName": "Andi",
  "siswaAlamat": "Bandung"
}
```
Response: 404 Not Found (Jika ID tidak ditemukan)
```json
{}
```
### 3. POST /tbSiswa
🔹 Deskripsi: Menambahkan data siswa baru.

Request:
```http
POST /tbSiswa
Content-Type: application/json
```
Body (JSON)
```json
{
  "id": 4,
  "siswaName": "Dewi",
  "siswaAlamat": "Yogyakarta"
}
```
Response: 201 Created
```json
{
  "id": 4,
  "siswaName": "Dewi",
  "siswaAlamat": "Yogyakarta"
}
```
Response: 400 Bad Request (Jika format salah)
```json
{
  "error": "Bad Request"
}
```
### 4. PUT /tbSiswa/:id
🔹 Deskripsi: Mengupdate data siswa berdasarkan id.
🔹 Note: Seluruh data harus dikirim ulang, bukan hanya bagian yang ingin diubah.

Request:
```http
PUT /tbSiswa/2
Content-Type: application/json
```
Body (JSON)
```json

{
  "id": 2,
  "siswaName": "Andi Pratama",
  "siswaAlamat": "Semarang"
}
```
Response: 200 OK
```json
{
  "id": 2,
  "siswaName": "Andi Pratama",
  "siswaAlamat": "Semarang"
}
```
Response: 404 Not Found (Jika ID tidak ditemukan)
```json
{}
```
### 5. PATCH /tbSiswa/:id
🔹 Deskripsi: Mengupdate sebagian data siswa berdasarkan id.

Request:
```http
PATCH /tbSiswa/2
Content-Type: application/json
```
Body (JSON)
```json
{
  "siswaAlamat": "Semarang"
}
```
Response: 200 OK
```json
{
  "id": 2,
  "siswaName": "Andi",
  "siswaAlamat": "Semarang"
}
```
Response: 404 Not Found (Jika ID tidak ditemukan)
```json
{}
```
### 6. DELETE /tbSiswa/:id
🔹 Deskripsi: Menghapus siswa berdasarkan id.
Request:
```http
DELETE /tbSiswa/3
```
Response: 200 OK
```json
{}
```
Response: 404 Not Found (Jika ID tidak ditemukan)
```json
{}
```

## 4. MEMBUAT PAGE SISWA
Install depedency
```
npm install react-router-dom
npx playwright install
```
```js
react-app/
│── public/
│── src/
│   ├── siswa/
│   │   ├── components/
│   │   │   ├── SiswaList.jsx
│   │   │   ├── SiswaForm.jsx
│   │   ├── pages/
│   │   │   ├── Home.jsx
│   │   │   ├── AddSiswa.jsx
│   │   │   ├── EditSiswa.jsx
│   ├── App.jsx
│   ├── main.jsx
│   ├── routes.jsx
│── tests/
│   ├── e2e.spec.js
│── index.html
│── package.json
│── vite.config.js
```

## 5. MEMBUAT

## 6. MEMBUAT

## 7. MEMBUAT
```js

```