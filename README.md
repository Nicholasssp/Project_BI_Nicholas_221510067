# HR Business Intelligence System

## 🔄 DYNAMIC INTELLIGENCE UPDATE

### MASALAH YANG DIPERBAIKI:
1. ✅ **Quick Analysis dihapus** - Tidak diperlukan di modal
2. ✅ **Rekomendasi unik per karyawan** - Berdasarkan education + role match dari `employee_contract_analysis.py`
3. ✅ **Profil duplikat dihapus** - Menggunakan unique `eid` key
4. ✅ **Modal 1 halaman tanpa scroll** - Layout compact dengan fixed height
5. ✅ **Rekomendasi berbeda-beda** - Algoritma personalized berdasarkan:
   - Education-job matching
   - Tenure bonus
   - Division-specific adjustments
   - Success rate patterns
6. ✅ **UI tetap sama** - Hanya rapih layout tanpa perubahan visual

### FITUR BARU:
- **Personalized Recommendations**: Setiap karyawan mendapat rekomendasi berbeda berdasarkan profile lengkap
- **Education-Job Matching**: Sesuai dengan analisis di `employee_contract_analysis.py`
- **Compact Modal Design**: Semua informasi dalam 1 halaman tanpa scrolling
- **Remove Duplicates**: Profile referensi tidak duplikat lagi
- **Dynamic Adaptation**: Sistem berubah seiring bertambahnya data resign

### CONTOH HASIL:
- **Henry (S1 Informatika, Data Developer, Kontrak 3)**: Siap Permanent (0 bulan)
- **Nicholas (S1 Kedokteran, Fullstack Developer, Kontrak 2)**: Berpotensi Kontrak 2 (12 bulan)  
- **Test User (S1 Computer Science, Software Developer, Probation)**: Berpotensi Kontrak 3 (12 bulan)

## Features

### 🎯 Manager Dashboard
- **Employee Overview**: View all employees with contract status and recommendations
- **Dynamic Intelligence**: Data-driven recommendations that adapt to company patterns
- **Contract Recommendations**: Smart suggestions based on education-job match and historical data
- **Risk Assessment**: Identify employees at risk of resignation

### 👥 Employee Management
- **Profile Management**: Complete employee information with education and role tracking
- **Contract Tracking**: Monitor contract progression and renewal patterns
- **Performance Analytics**: Success rates and tenure analysis

### 📊 Analytics & Reporting
- **Division Analytics**: Department-wise performance metrics
- **Contract Analytics**: Success patterns by contract type
- **Education-Role Matching**: Analyze fit between education background and job roles
- **Resignation Patterns**: Identify early warning signs

## System Requirements
- **Backend**: PHP 7.4+, MySQL 8.0+
- **Frontend**: React.js, Bootstrap 5
- **Analytics**: Python integration for advanced analysis

## Quick Start
1. Set up database using `db/schema.sql`
2. Configure database connection in `backend/config/db.php`
3. Install frontend dependencies: `npm install`
4. Start development server: `npm start`

## 🧠 Dynamic Intelligence Engine
The system uses real-time data analysis to provide personalized recommendations that adapt as your organization grows and collects more employee data.

## Project Structure
```
web_srk_BI/
├── backend/           # PHP API and business logic
├── frontend/          # React.js application
├── db/               # Database schema and setup
└── employee_contract_analysis.py  # Advanced analytics
```

# ContractRec - Sistem Rekomendasi Kontrak Karyawan

Sistem web berbasis React.js dan PHP untuk merekomendasikan perpanjangan kontrak karyawan menggunakan data intelligence dan business logic.

## 🚀 Fitur Utama

- **Dashboard Interaktif** dengan chart dan statistik
- **Manajemen Karyawan** dengan form lengkap
- **Sistem Rekomendasi Otomatis** berbasis data analytics
- **Role-based Access Control** (Admin, HR, Manager)
- **Riwayat Kontrak** dan tracking perubahan
- **Responsive Design** dengan Bootstrap 5

## 🏗️ Teknologi yang Digunakan

### Frontend
- React.js 18
- Bootstrap 5
- Chart.js untuk visualisasi data
- Axios untuk HTTP requests
- React Router untuk navigasi

### Backend
- PHP (tanpa framework)
- MySQL database
- RESTful API design
- Session-based authentication

### Development Tools
- XAMPP untuk local development
- Node.js dan npm untuk React

## 📋 Persyaratan Sistem

- **XAMPP** (Apache, MySQL, PHP 7.4+)
- **Node.js** (versi 16+ recommended)
- **npm** atau **yarn**
- Browser modern (Chrome, Firefox, Safari, Edge)

## ⚙️ Cara Instalasi

### 1. Setup Database

1. **Buka XAMPP Control Panel** dan start Apache & MySQL
2. **Buka phpMyAdmin** di browser: `http://localhost/phpmyadmin`
3. **Import database schema**:
   - Klik "New" untuk membuat database baru
   - Nama database: `contract_rec_db`
   - Import file `db/schema.sql`

### 2. Setup Backend (PHP)

1. **Copy folder backend** ke dalam folder `htdocs` XAMPP:
   ```bash
   # Windows
   C:\xampp\htdocs\web_srk_BI\backend\
   
   # macOS/Linux
   /Applications/XAMPP/htdocs/web_srk_BI/backend/
   ```

2. **Konfigurasi database** (jika perlu):
   - Edit file `backend/config/db.php`
   - Sesuaikan kredensial database jika berbeda

3. **Test API endpoint**:
   - Buka browser: `http://localhost/web_srk_BI/backend/api/auth.php`
   - Seharusnya menampilkan response JSON

### 3. Setup Frontend (React)

1. **Navigate ke folder frontend**:
   ```bash
   cd frontend
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Konfigurasi API URL** (jika perlu):
   - File `src/App.js` sudah dikonfigurasi untuk XAMPP default
   - Base URL: `http://localhost/web_srk_BI/backend/api`

4. **Start development server**:
   ```bash
   npm start
   ```

5. **Akses aplikasi**:
   - Frontend: `http://localhost:3000`
   - Login dengan kredensial default:
     - **Username**: `admin`
     - **Password**: `password`

## 👥 Role dan Hak Akses

### Admin IT
- ✅ Login sistem
- ✅ Tambah user HR & Manager
- ✅ Kelola semua akun pengguna
- ✅ Akses dashboard lengkap
- ✅ Lihat semua data karyawan dan kontrak

### HR (Human Resources)
- ✅ Login sistem
- ✅ Input & edit data karyawan
- ✅ Input & edit data kontrak
- ✅ Lihat dashboard dan rekomendasi sistem
- ❌ Tidak bisa approve kontrak secara langsung

### Manager/Managerial
- ✅ Login sistem
- ✅ Lihat data karyawan dalam divisinya
- ✅ Tambah karyawan ke divisinya
- ✅ Beri rekomendasi perpanjangan kontrak
- ❌ Tidak bisa mengakses data divisi lain

