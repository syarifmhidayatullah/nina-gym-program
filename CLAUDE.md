# CLAUDE.md

Repo ini bukan aplikasi: isinya program gym Nina (fat loss, glute, pull-up). Angka ada di `data/*.json`, aturan dan alasan di `.md`, dan `index.html` + `app.js` merender keduanya sebagai situs statis. Peran, aturan pelatihan, dan gaya jawaban ada di [project-instructions.md](project-instructions.md) (bagian di bawah garis) — ikuti itu juga saat bekerja di sini, termasuk bagian "Memperbarui repo".

## Data

- `data/cycles.json` — `cycles[]`: `start` (Senin, `YYYY-MM-DD`), `version`, `weeks[]` (`type` build/deload/test, `loads` per id latihan `{kg, sets?, result?, note?}`, `note`, `acc`, `skip`), `loads` (beban aksesori tetap per siklus `{load, target, as?}`), `notes`. `pullup`: `goal`, `stage` (1-based), `stages[]` `{name, do, pass}`, `tests[]` `{date, result, note?}`.
- `data/program.json` — `lifts` (kategori lift utama: `{name, color}`), `versions[]` → `days[]` → `ex[]` dengan `id`. Latihan dengan `heavy: true` jadi kartu di Ringkas dan grafik progres.
- `data/body.json` — `nutrition`, `phase` (dengan `targets` berat/bf/waist), `next_scan`, `scans[]`.
- Nomor siklus, nomor minggu global, dan minggu sekarang **dihitung**, jangan ditulis manual.

## Konvensi

- `kg` di JSON berupa angka (`52.5`); teks bebas di `.md` dan field `load` pakai koma (`52,5 kg`). Dumbbell per tangan.
- Sebelum commit: `python3 tools/check_data.py` harus `OK`.
- Commit: pesan singkat bahasa Indonesia, langsung ke `main`.

## Cek tampilan lokal

`app.js` mengambil file lewat `fetch`, jadi harus lewat server (bukan `file://`):

```
python3 -m http.server 8000   # http://localhost:8000
                              # http://localhost:8000/?today=2026-12-01 untuk tanggal lain
```
