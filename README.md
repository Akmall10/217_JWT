# Praktikum 11 PWS — REST API Komik dengan Autentikasi JWT

Proyek REST API menggunakan **Express.js**, **Sequelize**, **PostgreSQL**, **bcrypt**, dan **JSON Web Token (JWT)** untuk autentikasi pengguna serta operasi CRUD data Komik.

## Teknologi yang Digunakan
- Node.js & Express.js
- PostgreSQL & Sequelize ORM
- JSON Web Token (`jsonwebtoken`) & `bcrypt`
- `dotenv` & `nodemon`

## Cara Menjalankan
1. Install dependensi:
   ```bash
   npm install
   ```
2. Salin `.env.example` menjadi `.env` lalu sesuaikan konfigurasi database PostgreSQL dan `JWT_SECRET`.
3. Jalankan server:
   ```bash
   npm start
   ```
   Server berjalan di `http://localhost:3000`.

## Daftar Endpoint API

| Fitur | Method | Endpoint | Autentikasi |
| :--- | :--- | :--- | :--- |
| Register User | `POST` | `/api/register` | Tidak |
| Login User | `POST` | `/api/login` | Tidak |
| Tambah Komik | `POST` | `/api/komik` | Bearer Token (JWT) |
| Lihat Semua Komik | `GET` | `/api/komik` | Tidak |
| Lihat Komik by ID | `GET` | `/api/komik/:id` | Tidak |
| Update Komik | `PUT` | `/api/komik/:id` | Bearer Token (JWT) |
| Hapus Komik | `DELETE` | `/api/komik/:id` | Bearer Token (JWT) |

## Hasil Pengujian Postman

### 1. Register (`POST /api/register`)
![Register](screenshots/01-register.jpg)

### 2. Login & Mendapatkan Token JWT (`POST /api/login`)
![Login](screenshots/02-login.jpg)

### 3. Tambah Komik dengan Bearer Token (`POST /api/komik`)
![Create Komik](screenshots/03-create-komik.png)

### 4. Ambil Semua Komik (`GET /api/komik`)
![Get All Komik](screenshots/04-get-all-komik.jpg)

### 5. Ambil Komik Berdasarkan ID (`GET /api/komik/1`)
![Get Komik by ID](screenshots/05-get-komik-by-id.jpg)

### 6. Update Komik dengan Bearer Token (`PUT /api/komik/1`)
![Update Komik](screenshots/06-update-komik.png)

### 7. Hapus Komik dengan Bearer Token (`DELETE /api/komik/1`)
![Delete Komik](screenshots/07-delete-komik.png)
