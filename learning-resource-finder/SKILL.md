---
name: learning-resource-finder
description: Menggali dan menyusun daftar resource belajar (YouTube, PDF, artikel) untuk topik apapun — jenjang karir, bidang ilmu, atau buku tertentu — dalam bentuk learning path 4 tahap (Foundation, Core, Advanced, Mastery). Gunakan skill ini setiap kali user minta "cariin resource belajar", "learning path", "roadmap belajar", "mau belajar [topik/karir/buku/skill]", atau minta kumpulan link tutorial/referensi terstruktur untuk mempelajari sesuatu dari nol sampai mahir. Selalu pakai skill ini walaupun user tidak menyebut kata "skill" atau "learning path" secara eksplisit — cukup ada niat belajar terstruktur suatu topik.
---

# Learning Resource Finder

Skill untuk menyusun learning path terstruktur dari resource yang benar-benar ada di web (hasil pencarian nyata, bukan karangan), dengan urutan prioritas sumber yang ketat.

## Alur Kerja

1. **Klarifikasi topik singkat** (jika ambigu): pastikan tahu apakah user mau belajar karir/skill tertentu, bidang ilmu, atau buku spesifik. Jangan bertele-tele — kalau topik sudah jelas dari permintaan, langsung eksekusi.

2. **Susun struktur 4 tahap** untuk topik tersebut:
   - **Foundation** — konsep dasar, istilah, prasyarat mutlak sebelum lanjut
   - **Core** — kemampuan inti yang dipakai sehari-hari di bidang itu
   - **Advanced** — topik lanjutan, best practice, kasus lebih kompleks
   - **Mastery** — level ahli: arsitektur/strategi tingkat tinggi, tren terbaru, spesialisasi/niche

   Sesuaikan nama sub-topik di tiap tahap dengan bidang yang diminta (contoh: kalau topiknya "Data Analyst", Foundation bisa isinya Excel + statistik dasar; kalau topiknya buku tebal/bidang ilmu, Foundation bisa isinya bab pengantar / konsep kunci).

3. **Cari resource per tahap dengan urutan prioritas KETAT** (jangan dibalik urutannya):
   1. **YouTube** — prioritas pertama selalu. Cari video/playlist yang relevan dan kredibel untuk tahap tersebut.
   2. **PDF** — prioritas kedua. **WAJIB validasi**: hanya masukkan link yang URL-nya benar-benar berakhiran `.pdf`. Kalau saat pencarian dapat artikel/halaman yang *membahas* PDF tapi link aslinya bukan file `.pdf` langsung, JANGAN dimasukkan ke kategori PDF — buang saja, jangan dipaksakan jadi artikel juga kalau kualitasnya diragukan.
   3. **Artikel/link lain** — prioritas ketiga, dipakai untuk melengkapi kalau YouTube dan PDF belum cukup mengcover tahap itu, atau untuk referensi tambahan (dokumentasi resmi, blog teknis, dsb).

   Jumlah resource per tahap/sumber TIDAK dipatok — sesuaikan dengan kebutuhan nyata topik itu. Tahap Foundation biasanya butuh lebih banyak video dasar; tahap Mastery kadang cuma perlu 1-2 resource karena memang nichy. Jangan maksa-maksain jumlah kalau memang resource bagusnya sedikit — lebih baik sedikit tapi relevan daripada banyak tapi asal comot.

4. **Gunakan web_search dan image/video search sungguhan** untuk tiap tahap dan tiap kategori sumber — jangan pernah mengarang judul atau URL. Kalau hasil pencarian minim untuk suatu kombinasi tahap+sumber, itu wajar, tinggal laporkan apa adanya (tidak perlu dipaksakan mengisi kategori yang kosong).

## Format Output

Tampilkan sebagai list per tahap, tiap sumber dikelompokkan, format tiap item:

```
- [Judul singkat](URL)
```

Contoh struktur:

```markdown
## Foundation
### YouTube
- [Judul Video 1](url)
- [Judul Video 2](url)

### PDF
- [Judul Dokumen](url.pdf)

### Artikel
- [Judul Artikel](url)

## Core
...

## Advanced
...

## Mastery
...
```

Kalau salah satu kategori kosong untuk suatu tahap (misal tidak ketemu PDF valid), cukup tulis "PDF: tidak ditemukan sumber yang valid" — jangan diisi paksa.

## Hal yang harus dihindari

- Jangan pernah menyertakan link PDF yang URL-nya tidak diakhiri `.pdf`.
- Jangan membalik urutan prioritas (misal menaruh artikel duluan karena lebih gampang dicari).
- Jangan mengarang link atau judul — semua harus hasil pencarian nyata (web_search/web_fetch).
- Jangan beri deskripsi panjang per link — cukup judul singkat sesuai preferensi user, kecuali diminta lain.
