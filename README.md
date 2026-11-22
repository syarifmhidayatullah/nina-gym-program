# Program Gym Nina

Inti dari chat program latihan Nina: fat loss, glute, dan pull-up. Data harian (set, rep, beban) ada di aplikasi tracker, bukan di sini. Strukturnya sama dengan repo [`gym-program`](https://github.com/syarifmhidayatullah/gym-program) milik Syarif.

| File | Isi | Seberapa sering berubah |
|---|---|---|
| [data/cycles.json](data/cycles.json) | Siklus: tanggal mulai, beban & hasil lift utama per minggu, beban aksesori; tangga pull-up | Tiap review mingguan |
| [data/program.json](data/program.json) | Template: kategori lift utama, hari, latihan, set × rep, intensitas, rest, beban awal | Saat latihan diganti |
| [data/body.json](data/body.json) | Kalori sekarang, target fase, riwayat scan Evolt | Tiap scan / evaluasi kalori |
| [program.md](program.md) | Aturan progresi, skala effort, tangga pull-up, pemanasan, core & pelvic floor | Jarang |
| [decisions.md](decisions.md) | Keputusan yang sudah diambil beserta alasannya | Saat ada keputusan baru |
| [body.md](body.md) | Target fat loss, kalori & makro, aturan penyesuaian, cara mengukur | Saat aturan nutrisi berubah |
| [log-template.md](log-template.md) | Format log mingguan, nutrisi, dan scan untuk review | Jarang |
| [project-instructions.md](project-instructions.md) | Instruksi Claude Project "Nina Gym Progress" | Saat cara kerja project diubah |
| index.html + app.js | Halaman web, membaca `data/*.json` dan `.md` | Jarang |
| [tools/check_data.py](tools/check_data.py) | Cek `data/*.json` sebelum commit | Jarang |
| vendor/marked.min.js | Library marked v12.0.2 (Markdown → HTML), disimpan lokal | Hampir tidak pernah |

## Cara pakai di Claude Project

1. Di project **Nina Gym Progress**, tempel isi `project-instructions.md` (bagian di bawah garis) ke instruksi project.
2. Tidak perlu upload file. Tiap sesi meng-clone repo ini, membaca `data/*.json` dan file `.md`, lalu commit perubahannya langsung.
3. Review: kirim log sesuai `log-template.md` (lift utama + rasa set terakhir: *enteng*, *berat tapi aman*, *mentok*).

## Halaman web

`index.html` membaca `data/*.json` dan file `.md` langsung, jadi cukup edit lalu push. Deploy sebagai situs statis (misalnya Cloudflare Pages, tanpa build command, output directory `/`), sama seperti repo Syarif. Di lokal: `python3 -m http.server 8000` lalu buka http://localhost:8000.

Minggu sekarang dihitung dari tanggal `start` tiap siklus di `data/cycles.json`. Siklus baru = tambah satu entri di `cycles`; siklus lama otomatis pindah ke riwayat. Tambahkan `?today=YYYY-MM-DD` di URL untuk melihat tampilan di tanggal lain.

Bedanya dengan halaman Syarif: kategori lift utama dan warnanya diambil dari `lifts` di `data/program.json` (bukan Squat/Bench/Deadlift tetap), progres ditampilkan sebagai grafik beban lift utama (bukan e1RM), ada tangga pull-up, dan bagian tubuh menampilkan progres menuju target fat loss.

Sebelum commit, jalankan `python3 tools/check_data.py`.
