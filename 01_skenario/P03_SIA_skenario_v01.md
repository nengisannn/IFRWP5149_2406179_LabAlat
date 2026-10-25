<!-- Deskripsi Skenario -->
Mahasiswa mengajukan KRS dengan memilih mata kuliah. Setiap pengajuan menjalankan validasi KRS yang memeriksa kelengkapan, prasyarat mata kuliah, dan benturan jadwal. Jika validasi berhasil, sistem menyimpan pengajuan berstatus menunggu persetujuan dosen wali. Pada konfirmasi penyimpanan, mahasiswa dapat memilih mengunduh bukti pengajuan. Dosen wali menyetujui atau menolak KRS dan memberikan catatan keputusan.

<!-- Table Kebutuhan -->
| ID Kebutuhan | Kebutuhan Tugas                                                            |
|--------------|----------------------------------------------------------------------------|
| SIA-R01      | Mahasiswa dapat melihat jadwal kuliah.                                     |
| SIA-R02      | Admin akademik dapat mengelola jadwal kuliah.                              |
| SIA-R03      | Mahasiswa dapat mengajukan KRS.                                            |
| SIA-R04      | Sistem memvalidasi KRS sebagai bagian dari pengajuan.                      |
| SIA-R05      | Mahasiswa dapat mengunduh bukti jika memilihnya pada konfirmasi pengajuan. |
| SIA-R06      | Dosen wali dapat memproses persetujuan atau penolakan KRS.                 |

<!-- Batas Sistem dan aturan -->
• Pengguna telah terautentikasi. 
• Data mata kuliah, prasyarat, dan jadwal tersedia. 
• Validasi gagal menyebabkan pengajuan belum berhasil tersimpan. 
• Unduh bukti tidak menjadi syarat keberhasilan pengajuan. 
• KRS tersimpan belum berarti disetujui. 
• Pembayaran, pengisian nilai, dan implementasi basis data berada di luar tugas.

<!-- Table Identifikasi aktor -->
| Aktor          | Tujuan terhadap Sistem                                                                |
|----------------|---------------------------------------------------------------------------------------|
| Mahasiswa      | Melihat jadwal kuliah, mengajukan KRS, dan mengunduh bukti pengajuan jika memilihnya. |
| Admin akademik | Mengelola jadwal kuliah.                                                              |
| Dosen wali     | Memproses persetujuan atau penolakan KRS dan memberikan catatan keputusan.            |

<!-- Tabel katalog use case -->
| ID Use Case | Nama Use Case             | Aktor Terkait  | Sumber Kebutuhan |
|-------------|---------------------------|----------------|------------------|
| SIA-UC01    | Lihat jadwal kuliah       | Mahasiswa      | SIA-R01          |
| SIA-UC02    | Kelola jadwal kuliah      | Admin akademik | SIA-R02          |
| SIA-UC03    | Ajukan KRS                | Mahasiswa      | SIA-R03          |
| SIA-UC04    | Validasi KRS              | Sistem         | SIA-R04          |
| SIA-UC05    | Unduh bukti pengajuan KRS | Mahasiswa      | SIA-R05          |
| SIA-UC06    | Proses keputusan KRS      | Dosen wali     | SIA-R06          |

<!-- Relasi include -->
Sumber: SIA-UC03 — Ajukan KRS.
Tujuan: SIA-UC04 — Validasi KRS.
Alasan: setiap pengajuan harus menjalani validasi sebelum berhasil disimpan.
Arah panah: dari SIA-UC03 menuju SIA-UC04.

<!-- Relasi extend -->
Use case tambahan: SIA-UC05 — Unduh bukti pengajuan KRS.
Use case dasar: SIA-UC03 — Ajukan KRS.
Kondisi: [mahasiswa memilih unduh bukti].
Extension point: Konfirmasi penyimpanan.
Alasan: pengajuan tetap berhasil meskipun mahasiswa tidak mengunduh bukti
Arah panah: dari SIA-UC05 menuju SIA-UC03.