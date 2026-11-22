# Program Glute & Fat Loss 5 Hari

Prioritas: turunkan lemak sambil mempertahankan (dan menambah sedikit) otot, glute paling diutamakan, dan bisa pull-up.

## Data program

Angka program ada di folder `data/`, bukan di file ini:

- [`data/cycles.json`](data/cycles.json): siklus (tanggal mulai, beban dan hasil lift utama per minggu, beban aksesori) dan tangga pull-up. Minggu sekarang dihitung dari tanggal mulai siklus.
- [`data/program.json`](data/program.json): template (hari, latihan, set × rep, intensitas, rest, beban awal).

File ini berisi aturan yang dipakai untuk menyusun angka-angka itu.

- **Jadwal:** Senin Lower A, Selasa Upper A, Kamis Lower B, Jumat Upper B, Sabtu Glutes & Conditioning. Rabu dan Minggu libur (jalan santai boleh).
- **Jam latihan:** 06.00–07.30, maksimal 90 menit termasuk pemanasan dan treadmill.
- **Siklus:** 6 minggu, minggu 1–5 membangun, minggu 6 deload.
- **Nutrisi:** lihat [body.md](body.md).

## Aturan progresi

- **Double progression untuk semua latihan.** Tiap latihan punya rentang rep (misalnya 3×10–12). Mulai di rep bawah. Kalau semua set sudah mencapai rep teratas dengan teknik rapi dan set terakhir *berat tapi aman*, naikkan beban sesi berikutnya dan kembali ke rep bawah.
- **Besar kenaikan:** hip thrust dan leg press +5 kg; RDL dan dumbbell lain +1–2 kg per tangan (dumbbell terdekat); mesin dan cable 1 pin. Kalau lompatan terlalu besar sampai rep jatuh di bawah rentang, tetap di beban lama dan tambah rep pelan-pelan.
- **Rep turun sedikit di set akhir itu normal** (misalnya 12, 11, 10). Yang dihitung naik adalah ketika semua set sudah di angka teratas.
- **Rep tidak bertambah 2 minggu berturut-turut** di lift utama: cek tidur dan makan dulu. Kalau keduanya cukup, turunkan beban 10% dan bangun lagi.
- **Kalori defisit:** beban mungkin naik lebih pelan dibanding saat makan cukup; selama tidak turun, itu tandanya otot terjaga. Beban turun di beberapa lift sekaligus → lihat aturan di [body.md](body.md).
- **Deload minggu 6:** semua latihan 2 set, beban sama tapi berhenti di *enteng*. Treadmill tetap. Minggu pertama siklus berikutnya lanjut dari beban minggu 5.
- **Squat:** bodyweight dengan turun 3 detik sampai 3×12 stabil (lutut searah ujung kaki, berat rata di kedua kaki), lalu goblet squat mulai dumbbell 6–8 kg di 3×8.

## Skala effort

| Kategori | Rasanya | ≈ RPE |
|---|---|---|
| **Enteng** | Rep terakhir masih cepat, yakin bisa tambah banyak | 6–7 |
| **Berat tapi aman** | Rep terakhir mulai melambat, yakin masih 1–2 rep lagi | 8–9 |
| **Mentok** | Rep terakhir sangat lambat, atau gagal | 10 |

**Target berlaku untuk set terakhir.** Set awal wajar terasa lebih ringan. Kalau set pertama sudah *berat tapi aman*, beban hari itu terlalu berat: turunkan satu langkah.

- **Lift utama** (hip thrust, RDL, leg press, lat pulldown): set terakhir *berat tapi aman*, tidak sampai gagal.
- **Aksesori mesin & isolasi** (abduction, kickback, leg curl, leg extension, lateral raise, pec deck, curl, pushdown): set terakhir boleh sampai *mentok*, asal teknik tetap rapi.
- **Squat, split squat, RDL:** tidak pernah sampai gagal; berhenti kalau bentuk mulai berubah (punggung membulat di RDL, lutut masuk ke dalam di squat).

## Tangga pull-up

Target: **1 pull-up penuh tanpa bantuan, lalu 3×3**. Tahap sekarang dan riwayat tes ada di `data/cycles.json` bagian `pullup`, ditampilkan di halaman Ringkas.

- Dikerjakan di awal Upper A (3 set) dan Upper B (2 set), selagi segar.
- Naik ke tahap berikutnya kalau syarat lulus tahap sekarang tercapai di dua sesi berturut-turut. Boleh loncat tahap kalau tes menunjukkan Nina sudah melewatinya.
- Tes resmi di Selasa minggu deload: catat dead hang (detik), negative (berapa rep dan berapa detik turun), atau bantuan assisted (kg).
- Yang paling mendorong pull-up selain latihan pull-up itu sendiri: lat pulldown yang terus naik, straight-arm pulldown, biceps curl, dan berat badan yang turun.

## Pemanasan

- **Makan sebelum latihan:** latihan jam 6, jadi 30–45 menit sebelumnya makan karbohidrat cepat (pisang, roti, kurma) plus sedikit protein. Jangan latihan dengan perut kosong total.
- 5 menit treadmill atau sepeda santai, lalu hip mobility dan glute bridge tanpa beban 1×15.
- Lift utama pertama: 2 set pemanasan, misalnya hip thrust 50% × 10 → 75% × 5 → set kerja.

## Core dan pelvic floor

- Core yang dipakai sengaja yang tekanan perutnya rendah: dead bug (Senin) dan Pallof press (Kamis). Napas keluar saat bagian terberat gerakan.
- Kalau muncul perut menonjol di garis tengah (doming/coning), rasa berat atau bocor di pelvic floor, atau nyeri punggung bawah: hentikan gerakan itu dan ganti dengan versi lebih ringan. Kalau berulang, periksa ke fisioterapis (sebaiknya yang menangani women's health).

## Di luar sesi gym

- **Langkah harian:** target 7.000–8.000 per hari, termasuk hari libur. Ini kontributor defisit terbesar setelah makan, lebih besar dari treadmill di gym.
- **Treadmill di gym:** zona 2 (napas lebih cepat tapi masih bisa ngobrol). Bukan HIIT, karena HIIT mengganggu pemulihan kaki untuk sesi lower berikutnya.
- **Rabu & Minggu:** libur dari gym. Jalan santai 30–45 menit kalau memungkinkan.
