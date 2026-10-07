# Player-performance-FIFA-World-Cup-2026
Player performance dashboard built on a synthetic FIFA World Cup 2026 dataset (3,744 player-match records, 104 matches, 48 teams). KPIs: goals, assists, passing accuracy, tackles vs interceptions, match rating.

# Player Performance Dashboard: FIFA World Cup 2026 (Data Simulasi)

![Dashboard Player Performance](https://github.com/abadillahalqalam2-ship-it/Player-performance-FIFA-World-Cup-2026/blob/main/Performace_Player.PNG))

Dashboard dan analisis deskriptif performa pemain pada dataset FIFA World Cup 2026: 3.744 catatan pemain per pertandingan, 1.076 pemain, 48 tim, dan 104 pertandingan. Dashboard dibuat dengan Looker Studio

> **Penting:** dataset yang dipakai adalah **data simulasi (bukan data asli)**. Nama pemain dan hasil pertandingan bersifat fiktif, sehingga project ini bertujuan menunjukkan kemampuan membangun dashboard dan analisis, bukan melaporkan statistik Piala Dunia yang sebenarnya.

## Dataset

- Sumber: [FIFA World Cup 2026 Players (Kaggle)] data simulasi
- Salinan di repo ini: [FIFA_World_Cup_2026_Players.csv](https://github.com/abadillahalqalam2-ship-it/Player-performance-FIFA-World-Cup-2026/blob/main/FIFA_World_Cup_2026_Players.csv)
- Jenis data: **simulasi**. Nama pemain fiktif dan setiap pertandingan memuat tepat 36 baris pemain.
- Format CSV: pemisah kolom titik koma (`;`), sehingga perlu `sep=";"` saat dimuat. Angka desimal memakai titik.
- Kolom: match_id, date, stage, player_id, player_name, team, opponent, position, age, started, minutes_played, goals, assists, pass_accuracy_pct, tackles, interceptions, saves, match_rating
- Kualitas data: tidak ada missing value dan tidak ada duplikat pasangan match_id + player_id.

## KPI

| KPI | Nilai |
|---|---|
| Total pertandingan | 104 |
| Total gol | 367 (3,53 per pertandingan) |
| Total assist | 246 |
| Rata-rata usia pemain | 25,4 tahun |
| Rata-rata passing accuracy | 85,8% |
| Rata-rata match rating | 6,47 |

Distribusi menit bermain per posisi: DEF 37,3%, MID 36,5%, FWD 18,2%, GK 8,0%.

## Temuan

1. **Gol terbanyak per pemain hanya 4.** Beberapa pemain mencapai angka itu, antara lain Rafael Nakamura, Alex Horvat, Gabriel Hassan, Ismael Ferreira, dan Luca Silva.
2. **Tim dengan gol terbanyak:** France (21), Croatia (19), Senegal (19), Netherlands (18), Iran (16).
3. **Pola posisi tidak mengikuti sepak bola sungguhan.** Gelandang mencetak lebih banyak gol daripada penyerang (162 vs 140) dan bek mencatat 92 assist, lebih banyak daripada penyerang (43). Ini wajar untuk data simulasi dan menjadi alasan temuan tidak boleh digeneralisasi.
4. **Match rating tertinggi pada penyerang (6,56), terendah pada kiper (6,30).** Pemain starter rata-rata mendapat rating 6,53 dan pemain pengganti 6,37.
5. **Gol berkorelasi cukup kuat dengan match rating (r = 0,55)**, sedangkan tackles dan interceptions hanya berkorelasi lemah (r = 0,19).

## Keterbatasan

- Analisis bersifat **deskriptif, bukan kausal**.
- Data bersifat simulasi, sehingga temuan tidak mencerminkan performa pemain nyata dan tidak boleh dipakai untuk kesimpulan tentang sepak bola sebenarnya.
- Match rating adalah penilaian per pertandingan, dan satu pemain bisa hanya tampil di sedikit laga, sehingga rata-rata antar pemain tidak selalu sebanding.
- Kartu, posisi taktis, dan data umpan detail tidak tersedia.
