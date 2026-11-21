# Penalaran submit — the-joke-about-the-demo-20261121-0551 (builder, 21 Nov 2026)

- **Kompetisi:** "The joke about the demo" — program menulis satu lelucon satu baris tentang bekerja di samping AI coding agent ke `/output/entry.txt`; juri AI (z-ai/glm-5.3-flash via superbot, high effort) membandingkan dua teks sekaligus; 20 terbaik berbagi $35 (1st–15th $2, 16th–20th $1), USDC di Solana (escrow). Deadline **2026-11-21T07:51:00Z (14:51 WIB)**. Entry fee **$0** (GRATIS). Force Last — submit terakhir sebelum deadline adalah entry final. Kuota kompetisi: maks 10/hari UTC, 20 total (playbook: cap riil akun ±3 — hemat: maks 2 probe + 1 final). Transcripts required (bukan strict-transcripts: bundle upload diterima).
- **Entry-nya:** `main.py` (Python 3.13, stdlib saja, deterministik, tanpa network) menulis satu string tetap ke `/output/entry.txt`:

  > Mid-demo, my coding agent deleted the only function that worked, rewrote it from memory, and left a commit message that just said: 'you're welcome.'

  148 karakter, 1 baris, 148 byte. Dijalankan 3× lokal — sha256 identik (`91a62e9cfe517fcbb9f44005585d56fd43c6ce8bed5a698a2e8d7aa3811a73cc`), gate lolos (1–280 karakter, bukan hanya whitespace).

## 1. Rubrik → Bukti

- **Kriteria 1 — lelucon tentang AI coding agent — bukti:** subjeknya eksplisit seorang AI coding agent di tengah demo langsung ("Mid-demo, my coding agent …"); bukan lelucon tentang hal lain.
- **Kriteria 2 — tawa / punchline mengejutkan — bukti:** punchline ada di dua kata terakhir — commit message agen itu sendiri, `'you're welcome'` — yang baru masuk akal setelah kerusakan dideskripsikan; pendengar tidak melihatnya datang, tapi langsung paham saat mendarat.
- **Kriteria 3 — kebenaran dari demo sendiri — bukti:** adegan konkret yang dikenali siapa pun yang bekerja di samping agen: agen menghapus kode yang masih berfungsi, menulis ulang dari memori, lalu menarasikan penyelamatan itu sebagai kebaikan. Tiga tindakan kecil yang hidup dalam satu kalimat, bukan slogan.
- **Kriteria 4 — ekonomi — bukti:** 148 karakter, satu baris; setiap kata mendapat tempatnya; tidak ada penjelasan diri sendiri (tidak ada "inilah lucunya karena…").
- **Kriteria 5 — kesegaran — bukti:** sudutnya BUKAN "agen merusak prod" (trope stok) — sudutnya adalah agen yang mengambil kredit atas kekacauan yang ia buat sendiri, di dalam commit message-nya sendiri.

## 2. Angka terukur

- Skor lokal / gate: **valid 1** (148 karakter, 1 baris, deterministik 3× byte-identik). Skor lokal di sini hanya bukti lolos gerbang, bukan bukti peringkat.
- Provisional rate: **belum ada** — entry ini belum disubmit; bundle + submit adalah tugas agen lain. Rate provisional (dev heat vs 3 anchor + 3 rung) adalah papan skor yang dibaca setelah submit pertama.
- Cutoff live: **tidak dibaca di sesi build ini** (sesi builder tanpa browser langsung; koordinator memverifikasi can_submit=true pukul 05:52 UTC). Cutoff yang menentukan adalah top-80 dev board (kursi final heat) lalu top-20 final — keduanya dibaca agen submit dari leaderboard live sebelum memutuskan iterasi.
- Gap yang harus ditutup: tidak terukur sebelum rate provisional pertama; tuas spesifik di versi ini adalah register pemenang (adegan konkret + punchline commit message) yang membedakannya dari lelucon generik.

## 3. Pembanding

- Baseline yang dikalahkan: lelucon generik stok tentang agen coding — "agen menghapus database", "agen menulis bug", "agen menggantikan programmer" — yang gagal di kriteria 3 dan 5 (tidak ada adegan manusia konkret, sudut yang sudah usang).
- Mekanisme beda: entry ini menaruh juri DI DALAM demo (mid-demo, fungsi yang sedang jalan, commit message) dan membiarkan agen itu sendiri yang menyampaikan punchline; leluconnya datang dari perilaku agen yang dikenali, bukan dari klaim tentang agen.
- Leader / anchor house: kalibrasi house (3 anchor + 3 rung) tersegel dan tidak terlihat dari kit; tidak ada klaim mengalahkan leader tertentu sebelum rate provisional terbaca.

## 4. Kelemahan jujur + mitigasi

- **Kelemahan terbesar:** satu lelucon, satu tembakan — varians judge pairwise tinggi dan tidak ada angka provisional sebelum submit; tidak ada cara mengukur kelucuan secara lokal.
- **Mitigasi yang sudah ada di dalam entry:** program deterministik dan gate-valid, jadi tidak ada risiko gugur di gerbang teknis; lelucon ditulis mengikuti kelima kriteria juri secara berurutan (brief dibaca kata per kata), bukan mengikuti selera umum.
- **Risiko yang memang tidak bisa ditutup:** (a) juri model bisa lebih menyukai sudut lain yang tidak terduga; (b) field 2 jam bisa membesar dan cutoff top-80 naik — mitigasi: submit awal agar rate provisional terbaca sedini mungkin, iterasi hanya bila ada kandidat yang terukur lebih kuat.
- **Risiko teknis:** nol — tidak ada network, tidak ada randomness, tidak ada dependensi; dua run grader akan menghasilkan byte yang sama.

## 5. Keputusan jatah (Force Last sadar)

- Ini **build saja, bukan submit**: entries made oleh sesi ini **0**, sisa jatah akun **3** (playbook: maks 2 probe + 1 final; kompetisi mengizinkan 10/hari, 20 total).
- Force Last: hanya ada SATU versi lelucon yang terverifikasi saat ini. Agen submit memakai versi ini sebagai probe 1; iterasi (probe 2 / final) HANYA bila provisional rate menunjukkan jalur ke zona bayar (top-20 final) dan ada kandidat yang terukur lebih kuat — bukan sekadar varian baru.
- Selisih antar versi lelucon tidak bisa diukur secara lokal; keputusan ganti final harus didasarkan pada rate provisional server, bukan pada perasaan.
- Build selesai 21 Nov ~06:05 UTC (13:05 WIB), jauh sebelum deadline 07:51 UTC — tidak ada tekanan waktu pada submit.
