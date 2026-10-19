<-- deskripsi skenario -->

Skenario berikut merupakan bahan latihan yang ditetapkan untuk jobsheet, bukan hasil pengumpulan kebutuhan laboratorium nyata. Skenario ini melanjutkan potongan model Pertemuan 3. Selain mahasiswa, dosen juga meminjam peralatan laboratorium untuk kegiatan praktikum dan penelitian. Mahasiswa dan dosen sama-sama dapat melihat ketersediaan peralatan dan mengajukan peminjaman. Petugas laboratorium mengelola data peralatan: menambah peralatan baru, mengubah data peralatan, dan menghapus data peralatan yang tidak lagi dipakai. Setelah peminjaman disetujui dan alat diambil, petugas mencatat pengembalian peralatan. Pada saat mencatat pengembalian, petugas memeriksa dan mencatat kondisi peralatan. Dua use case utama pada potongan model ini, Ajukan Peminjaman dan Catat Pengembalian Peralatan, ditunjukkan realisasinya oleh collaboration yang bersesuaian. Seluruh fungsi Pertemuan 3 tetap berlaku dan tetap digambar: pemeriksaan ketersediaan di dalam pengajuan, pencetakan bukti pengajuan oleh mahasiswa, proses keputusan peminjaman oleh petugas, dan laporan peminjaman untuk kepala laboratorium. Diagram Pertemuan 4 adalah diagram Pertemuan 3 yang ditambah, bukan diagram baru yang menggantikannya.

<-- Aktor umum dan aktor khusus -->
Aktor                   : peminjam
kedudukan               : umum (general), baru pada pertemuan 4
tujuan terhadap sistem  : peran umum bagi peminjaman peralatan. mewariskan fungsinya kepada mahasiswa dan dosen

aktor                   : mahasiswa
kedudukan               : khusus dari peminjam, baru pada pertemuan 3
tujuan terhadap sistem  : melihat ketersediaan dan  mengajukan peminjaman (diwarisi dari peminjam), ditambah mencetak bukti pengajuan sebagai asosiasi khususnya sendiri.


aktor                   : dosen
kedudukan               : khusus dari peminjam, baru pada pertemuan 4
tujuan terhadap sistem  : melihat ketersediaan dan  mengajukan peminjaman (diwarisi dari peminjam).

aktor                   : petugas labolatorium
kedudukan               : tetap dari pertemuan 3
tujuan terhadap sistem  : mengelola data peralatan, memproses keputusan peminjaman, dan mencatat pengembalian peralatan.

aktor                   : kepala labolatorium
kedudukan               : tetap dari pertemuan 3
tujuan terhadap sistem  : melihat laporan peminjaman.


<-- katalog Use Case -->
| ID       | Nama Use Case                | Peran dalam Model                                                                                 | Sumber Kebutuhan |
| -------- | ---------------------------- | ------------------------------------------------------------------------------------------------- | ---------------- |
| LAB-UC01 | Lihat Ketersediaan Peralatan | Tetap dari Pertemuan 3; fungsi aktor umum Peminjam                                                | LAB-R01, LAB-R07 |
| LAB-UC02 | Kelola Data Peralatan        | Tetap dari Pertemuan 3; use case UMUM bagi LAB-UC08, LAB-UC09, LAB-UC10                           | LAB-R02, LAB-R08 |
| LAB-UC03 | Ajukan Peminjaman            | Tetap dari Pertemuan 3; fungsi aktor umum Peminjam; menyertakan LAB-UC04; direalisasikan LAB-CO01 | LAB-R03, LAB-R07 |
| LAB-UC04 | Periksa Ketersediaan         | Tetap dari Pertemuan 3; perilaku yang disertakan LAB-UC03                                         | LAB-R03          |
| LAB-UC05 | Cetak Bukti Pengajuan        | Tetap dari Pertemuan 3; tambahan bersyarat pada LAB-UC03 melalui `«extend»`                       | LAB-R04          |
| LAB-UC06 | Proses Keputusan Peminjaman  | Tetap dari Pertemuan 3; fungsi utama petugas                                                      | LAB-R05          |
| LAB-UC07 | Lihat Laporan Peminjaman     | Tetap dari Pertemuan 3; fungsi utama kepala laboratorium                                          | LAB-R06          |
| LAB-UC08 | Tambah Data Peralatan        | Baru pada Pertemuan 4; use case KHUSUS dari LAB-UC02                                              | LAB-R08          |
| LAB-UC09 | Ubah Data Peralatan          | Baru pada Pertemuan 4; use case KHUSUS dari LAB-UC02                                              | LAB-R08          |
| LAB-UC10 | Hapus Data Peralatan         | Baru pada Pertemuan 4                                                                             | LAB-R08          |