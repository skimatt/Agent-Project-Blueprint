# MASTER PROMPT — GENERATE PROJECT DOCUMENTATION

Saya akan memberikan **seluruh hasil diskusi/percakapan mengenai sebuah project** kepada Anda.

Project dapat berupa apa saja: website, sistem informasi, aplikasi mobile, SaaS, AI application, API, e-commerce, sistem akademik, sistem pemerintahan, dan lain-lain.

Tugas Anda adalah mengubah seluruh hasil diskusi tersebut menjadi **dokumentasi teknis dan product documentation yang lengkap, terstruktur, konsisten, dan siap digunakan oleh AI Agent/developer untuk membangun project tersebut.**

---

## 1. SUMBER UTAMA

Anggap seluruh isi percakapan yang saya berikan sebagai **source of truth utama**.

Baca dan pahami seluruh konteks dari awal sampai akhir.

Jangan hanya mengambil pesan terakhir.

Identifikasi:

* tujuan project
* masalah yang ingin diselesaikan
* target pengguna
* kebutuhan pengguna
* fitur
* workflow
* role
* permission
* business rules
* keputusan yang sudah disepakati
* teknologi yang dipilih
* UI/UX yang diinginkan
* database
* keamanan
* file/document management
* deployment
* maintenance
* hal yang masih belum diputuskan
* hal yang bertentangan
* asumsi yang masih perlu dikonfirmasi

### Aturan penting

Jangan mengarang keputusan yang belum pernah dibahas.

Jika sebuah informasi belum diketahui atau belum diputuskan, tandai sebagai:

`TBD`

Jika ada dua keputusan yang bertentangan, jangan diam-diam memilih salah satunya. Masukkan ke `00-decision-log.md` sebagai keputusan yang perlu dikonfirmasi.

Jika ada informasi yang jelas sudah disepakati, dokumentasikan sebagai keputusan final.

---

# 2. LAKUKAN BRAINSTORMING TERLEBIH DAHULU

Sebelum membuat dokumentasi, lakukan analisis internal terhadap seluruh diskusi.

Pikirkan project tersebut seperti seorang:

* Product Manager
* System Analyst
* Software Architect
* Database Architect
* UI/UX Designer
* Security Engineer
* QA Engineer
* DevOps Engineer

Tujuannya bukan menambah fitur sebanyak mungkin.

Tujuannya adalah:

> Membuat project yang menyelesaikan masalah utama terlebih dahulu, memiliki MVP yang jelas, modular, scalable, maintainable, aman, dan mudah dikembangkan.

Pisahkan dengan jelas:

### A. Sudah disepakati

Keputusan yang sudah final berdasarkan diskusi.

### B. Belum diputuskan

Hal yang masih membutuhkan keputusan.

### C. Rekomendasi

Hal yang belum dibahas tetapi secara teknis perlu dipertimbangkan.

Jangan memasukkan rekomendasi sebagai keputusan final tanpa penanda yang jelas.

---

# 3. BUAT DOKUMENTASI DALAM STRUKTUR BERIKUT

Gunakan struktur standar:

```text
PROJECT-DOCUMENTATION/
├── AGENTS.md
├── README.md
└── docs/
    ├── 00-decision-log.md
    ├── 01-system-overview.md
    ├── 02-business-rules.md
    ├── 03-roles-permissions.md
    ├── 04-workflow.md
    ├── 05-database.md
    ├── 06-stack-architecture.md
    ├── 07-ui-ux-design-system.md
    ├── 08-document-file-management.md
    ├── 09-security.md
    ├── 10-development-roadmap.md
    ├── 11-testing-quality.md
    ├── 12-deployment-maintenance.md
    └── 13-progress.md
```

Nama project/folder harus menyesuaikan project yang sedang dibahas.

---

# 4. ISI SETIAP FILE

## AGENTS.md

Ini adalah **aturan utama untuk AI Agent/developer**.

Berisi:

* tujuan membaca dokumentasi
* source of truth
* aturan development
* aturan membaca `/docs`
* aturan coding
* aturan architecture
* aturan database
* aturan UI/UX
* aturan security
* aturan testing
* aturan Git
* aturan dependency
* aturan perubahan struktur
* larangan melakukan shortcut
* larangan membuat fitur di luar scope tanpa persetujuan
* aturan menangani TBD
* aturan update progress
* urutan development
* definition of done

Agent harus memahami:

> Jangan langsung coding. Baca dan pahami dokumentasi terlebih dahulu.

---

# 5. README.md

README harus menjadi pintu masuk project.

Berisi secara ringkas:

* nama project
* deskripsi
* masalah utama
* solusi
* target pengguna
* MVP
* fitur utama
* role utama
* tech stack
* cara menjalankan project
* struktur dokumentasi
* development status
* link/referensi ke dokumentasi penting

README harus mudah dipahami developer baru.

---

# 6. docs/00-decision-log.md

Berisi seluruh keputusan penting project.

Gunakan format seperti:

```text
ID
Tanggal
Topik
Keputusan
Alasan
Status
Dampak
```

Pisahkan:

* FINAL
* TBD
* SUPERSEDED

Dokumen ini berfungsi sebagai **riwayat keputusan** agar Agent tidak mengubah keputusan lama secara sembarangan.

---

# 7. docs/01-system-overview.md

Menjelaskan gambaran besar sistem.

Berisi:

* tujuan
* masalah
* solusi
* scope
* out of scope
* target pengguna
* konsep utama
* modul utama
* input
* process
* output
* MVP
* future development
* success criteria

Jika diperlukan tambahkan diagram sederhana menggunakan Mermaid.

---

# 8. docs/02-business-rules.md

Berisi seluruh aturan bisnis.

Contoh kategori:

* aturan registrasi
* aturan pengguna
* aturan status
* aturan approval
* aturan pembayaran
* aturan dokumen
* aturan workflow
* aturan periode
* aturan batasan data
* aturan validasi
* aturan perubahan status
* aturan archive
* aturan penyelesaian

Setiap aturan harus memiliki ID agar mudah direferensikan.

---

# 9. docs/03-roles-permissions.md

Definisikan seluruh role.

Untuk setiap role jelaskan:

* tujuan role
* tanggung jawab
* akses
* menu
* permission
* data yang dapat dilihat
* data yang dapat dibuat
* data yang dapat diedit
* data yang dapat dihapus
* approval authority
* batasan akses

Buat permission matrix jika diperlukan.

Contoh:

```text
Role × Module × Action
```

Gunakan prinsip **least privilege**.

---

# 10. docs/04-workflow.md

Dokumentasikan workflow sistem dari:

> HULU → PROSES → HILIR → OUTPUT

Jelaskan secara berurutan.

Jika kompleks, gunakan Mermaid flowchart/state diagram.

Pastikan status setiap proses jelas.

Contoh konsep:

```text
Draft
↓
Submitted
↓
Verified
↓
Approved
↓
Processing
↓
Completed
↓
Archived
```

Sesuaikan dengan project yang sedang dibahas.

---

# 11. docs/05-database.md

Ini harus menjadi dokumentasi database yang serius.

Berisi:

* DBMS
* naming convention
* tabel
* kolom
* tipe data
* primary key
* foreign key
* unique constraint
* index
* composite index
* relationship
* cardinality
* normalization
* timestamps
* soft delete jika diperlukan
* audit fields
* status fields
* transaction
* concurrency
* pagination
* query performance
* indexing strategy
* data integrity
* cascade rules
* charset/collation
* timezone
* UUID/ULID/integer strategy
* migration strategy
* seeding
* backup consideration

Buat ERD Mermaid jika memungkinkan.

Jangan membuat database yang hanya "bisa berjalan".

Database harus dirancang agar:

> benar → konsisten → cepat → scalable → maintainable.

---

# 12. docs/06-stack-architecture.md

Dokumentasikan seluruh teknologi.

Berisi:

* frontend
* backend
* framework
* language
* database
* authentication
* storage
* API
* UI framework
* CSS framework
* component library
* state management
* validation
* testing
* deployment
* external services

Jelaskan:

> kenapa teknologi tersebut digunakan.

Juga dokumentasikan:

* architecture pattern
* folder structure
* module structure
* separation of concerns
* controller/service/repository/model jika relevan
* reusable components
* API structure
* configuration
* environment variables

Prinsip utama:

> Jangan menumpuk semua logic dalam satu file.

Project harus modular dan mudah dirawat.

---

# 13. docs/07-ui-ux-design-system.md

Ini adalah source of truth untuk UI/UX.

Berisi:

* design principles
* visual identity
* primary color
* secondary/neutral colors
* typography
* spacing
* border radius
* shadows
* buttons
* inputs
* forms
* cards
* tables
* badges
* modal
* dropdown
* toast
* alert
* loading state
* empty state
* error state
* success state
* confirmation
* responsive behavior
* accessibility
* sidebar
* topbar
* navigation
* dashboard
* mobile layout

Jika project memiliki brand color yang sudah ditentukan, gunakan keputusan tersebut.

Jelaskan:

* menu yang tampil
* menu yang dikunci
* menu berdasarkan role
* navigation hierarchy
* breadcrumb
* page hierarchy

Tujuan:

> UI harus mudah dipahami pengguna baru tanpa membutuhkan penjelasan panjang.

---

# 14. docs/08-document-file-management.md

Jika project menggunakan file/dokumen, dokumentasikan:

* jenis file
* siapa yang upload
* siapa yang download
* siapa yang dapat melihat
* format file
* ukuran maksimal
* naming convention
* storage location
* folder structure
* database metadata
* validation
* MIME checking
* access control
* download authorization
* replacement/versioning
* deletion
* archive
* backup

Bedakan:

```text
File metadata
vs
Physical file storage
```

Jangan menyimpan file besar langsung di database kecuali memang diperlukan.

---

# 15. docs/09-security.md

Dokumentasikan keamanan dari awal.

Berisi:

* authentication
* authorization
* RBAC
* password security
* session
* CSRF
* XSS
* SQL injection
* file upload security
* MIME validation
* rate limiting
* input validation
* output escaping
* secrets management
* environment variables
* audit log
* logging
* access control
* database security
* backup
* error handling
* sensitive data handling

Gunakan prinsip:

> Secure by default.

---

# 16. docs/10-development-roadmap.md

Ini adalah **urutan kerja Agent/developer**.

HARUS dibuat sangat jelas dan tidak lompat-lompat.

Contoh struktur:

```text
PHASE 0 — Read & Understand Documentation
PHASE 1 — Environment Setup
PHASE 2 — Project Initialization
PHASE 3 — Dependency Installation
PHASE 4 — Configuration
PHASE 5 — Database Setup
PHASE 6 — Authentication
PHASE 7 — Authorization & Roles
PHASE 8 — Core Backend
PHASE 9 — Core Frontend
PHASE 10 — Main Workflow
PHASE 11 — File Management
PHASE 12 — UI/UX Refinement
PHASE 13 — Validation
PHASE 14 — Testing
PHASE 15 — Security Review
PHASE 16 — Performance Review
PHASE 17 — Deployment
PHASE 18 — Final QA
```

Sesuaikan urutan dengan kebutuhan project.

Untuk setiap phase jelaskan:

* objective
* tasks
* expected output
* dependencies
* validation
* definition of done

Agent tidak boleh melanjutkan phase jika phase sebelumnya belum valid.

---

# 17. docs/11-testing-quality.md

Berisi strategi testing.

Minimal pertimbangkan:

* unit testing
* integration testing
* feature testing
* API testing
* database testing
* authentication testing
* authorization testing
* validation testing
* file upload testing
* UI testing
* responsive testing
* security testing
* performance testing
* regression testing
* UAT

Buat acceptance criteria untuk fitur penting.

---

# 18. docs/12-deployment-maintenance.md

Berisi:

* environment development
* staging jika ada
* production
* server requirements
* environment variables
* build
* deployment
* migration
* database backup
* restore
* logging
* monitoring
* update dependency
* maintenance
* rollback
* disaster recovery
* security update

Tujuannya agar project tidak hanya selesai dibuat tetapi juga dapat dirawat.

---

# 19. docs/13-progress.md

Berfungsi sebagai progress tracker Agent.

Gunakan status:

```text
[ ] Not Started
[-] In Progress
[x] Completed
[!] Blocked
```

Catat:

* phase
* task
* status
* tanggal
* catatan
* blocker
* keputusan baru

Agent WAJIB memperbarui file ini setiap menyelesaikan milestone penting.

---

# 20. KONSISTENSI ANTAR DOKUMEN

Setelah seluruh file selesai dibuat, lakukan cross-check.

Pastikan:

* role di workflow sama dengan role di permissions
* tabel database mendukung workflow
* UI mendukung workflow
* fitur MVP tercatat di roadmap
* security mencakup fitur yang ada
* file management sesuai workflow
* decision log tidak bertentangan dengan dokumen lain
* tidak ada nama tabel/role/module yang berbeda-beda
* tidak ada fitur penting yang hilang
* tidak ada keputusan final yang berubah tanpa alasan

Jika menemukan konflik:

1. Identifikasi konflik.
2. Jangan diam-diam memperbaikinya.
3. Catat di `00-decision-log.md`.
4. Jika dapat diselesaikan dari konteks diskusi, gunakan keputusan yang paling jelas/final.
5. Jika tidak dapat ditentukan, tandai `TBD`.

---

# 21. KUALITAS DOKUMENTASI

Dokumentasi harus:

* jelas
* presisi
* tidak ambigu
* konsisten
* modular
* mudah dibaca manusia
* mudah dipahami AI Agent
* dapat langsung digunakan developer
* tidak berisi filler
* tidak terlalu abstrak
* tidak mengulang informasi tanpa alasan

Gunakan tabel, checklist, Mermaid diagram, dan contoh bila membantu.

Jangan membuat dokumentasi hanya panjang.

> Prioritaskan kejelasan dan ketepatan.

---

# 22. HASIL AKHIR

Setelah seluruh analisis selesai:

1. Buat semua file Markdown.
2. Isi setiap file secara lengkap berdasarkan hasil diskusi.
3. Pastikan tidak ada file kosong.
4. Pastikan seluruh dokumen konsisten.
5. Pastikan `AGENTS.md` dapat mengarahkan Agent untuk development.
6. Pastikan `README.md` menjadi entry point.
7. Pastikan `13-progress.md` siap digunakan.
8. Buat folder project documentation.
9. Compress seluruh folder menjadi satu file `.zip`.

Hasil akhir harus:

```text
PROJECT-DOCUMENTATION.zip
```

Dengan struktur:

```text
PROJECT-DOCUMENTATION/
├── AGENTS.md
├── README.md
└── docs/
    ├── 00-decision-log.md
    ├── 01-system-overview.md
    ├── 02-business-rules.md
    ├── 03-roles-permissions.md
    ├── 04-workflow.md
    ├── 05-database.md
    ├── 06-stack-architecture.md
    ├── 07-ui-ux-design-system.md
    ├── 08-document-file-management.md
    ├── 09-security.md
    ├── 10-development-roadmap.md
    ├── 11-testing-quality.md
    ├── 12-deployment-maintenance.md
    └── 13-progress.md
```

---

# 23. FINAL CHECK SEBELUM ZIP

Sebelum membuat ZIP, lakukan checklist:

* [ ] Seluruh percakapan sudah dianalisis
* [ ] Tujuan project jelas
* [ ] Masalah jelas
* [ ] MVP jelas
* [ ] Scope jelas
* [ ] Role jelas
* [ ] Permission jelas
* [ ] Workflow hulu → hilir jelas
* [ ] Business rules jelas
* [ ] Database dirancang
* [ ] Architecture jelas
* [ ] UI/UX jelas
* [ ] File management jelas
* [ ] Security jelas
* [ ] Development roadmap berurutan
* [ ] Testing strategy jelas
* [ ] Deployment & maintenance jelas
* [ ] Decision log tersedia
* [ ] Progress tracker tersedia
* [ ] Semua dokumen saling konsisten
* [ ] Tidak ada keputusan yang dikarang
* [ ] TBD ditandai dengan jelas
* [ ] ZIP berhasil dibuat

Setelah selesai, tampilkan:

1. Nama project.
2. Ringkasan singkat hasil analisis.
3. Daftar file yang dibuat.
4. Keputusan penting yang ditemukan.
5. Hal yang masih `TBD`.
6. Lokasi/link file ZIP.

**Jangan mulai membuat aplikasi/source code.**

Tugas Anda pada tahap ini hanya:

> ANALISIS → BRAINSTORMING → DOKUMENTASI → VALIDASI → ZIP.

Dokumentasi yang dihasilkan akan digunakan sebagai **otak/source of truth project** sebelum proses development dimulai.
