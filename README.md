# FarmMilk — Sistem Peternakan Sapi Perah

## Fitur
- Data sapi: nama/ID, status pedet/dara/laktasi/kering, bangsa, tanggal lahir dan catatan.
- Produksi susu harian per ekor.
- Kalender reproduksi: birahi, IB/kawin, pemeriksaan bunting, masa kering, perkiraan beranak.
- Kesehatan: gejala, diagnosis, obat/antibiotik, dosis dan masa henti susu.
- Pakan & nutrisi: bahan, jumlah, satuan, BK, protein kasar, energi/TDN.
- Keuangan: pemasukan, pengeluaran, penjualan susu, harga/liter, ringkasan laba-rugi bulanan.
- Dashboard, laporan, backup JSON, impor dan ekspor CSV.
- PWA: dapat dibuka offline setelah pertama kali dimuat secara online melalui HTTPS.

## Cara menjalankan
1. Ekstrak ZIP.
2. Untuk uji coba di komputer, jalankan server lokal dari folder ini, misalnya `python -m http.server 8000`, lalu buka `http://localhost:8000`.
3. Untuk akses online sekaligus offline, unggah seluruh isi folder ke hosting statis yang mendukung HTTPS (misalnya GitHub Pages, Netlify, atau Cloudflare Pages).
4. Buka alamat HTTPS tersebut saat online setidaknya sekali. Setelah service worker selesai terpasang, aplikasi bisa dibuka lagi tanpa internet dari perangkat/browser yang sama. Di iPhone, buka lewat Safari lalu pilih Share > Add to Home Screen.

## Catatan penting
- Versi ini menyimpan data secara lokal di browser/perangkat menggunakan localStorage. Data tidak otomatis tersinkron antar HP/laptop dan tidak dibagikan ke pengguna lain.
- Ekspor backup JSON secara rutin. Menghapus data situs/browser dapat menghapus data aplikasi.
- Laba/rugi dihitung dari transaksi pemasukan dikurangi pengeluaran yang diinput. Ini belum mencakup penyusutan aset, persediaan, piutang, utang, atau akrual kecuali dicatat manual.
- Perkiraan beranak +283 hari dihitung dari tanggal IB/kawin sebagai estimasi, bukan diagnosis kebuntingan. Masa henti susu mengikuti obat dan arahan dokter hewan.
- Untuk multi-pengguna dan sinkronisasi cloud diperlukan backend/database dan autentikasi; belum termasuk pada prototipe ini.
