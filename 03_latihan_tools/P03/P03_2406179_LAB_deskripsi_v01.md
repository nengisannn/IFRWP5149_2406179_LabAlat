| Elemen                | Deskripsi                                                                           |
|-----------------------|-------------------------------------------------------------------------------------|
| ID dan nama           | SIA-UC03 — Ajukan KRS                                                               |
| Sumber kebutuhan      | SIA-R03, SIA-R04, SIA-R05                                                           |
| Tujuan                | Menghasilkan pengajuan KRS yang tersimpan dan menunggu persetujuan dosen wali.      |
| Aktor utama           | Mahasiswa                                                                           |
| Aktor pendukung       | Sistem                                                                              |
| Pemicu                | Mahasiswa memilih fungsi pengajuan KRS.                                             |
| Prasyarat             | Mahasiswa telah terautentikasi; data mata kuliah, prasyarat, dan jadwal tersedia.   |
| Include               | SIA-UC04 — Validasi KRS                                                             |
| Extension point       | Konfirmasi penyimpanan                                                              |
| Extend                | SIA-UC05 — Unduh bukti pengajuan KRS, jika mahasiswa memilihnya.                    |
| Pascakondisi berhasil | Pengajuan KRS tersimpan dengan status menunggu persetujuan dosen wali.              |
| Pascakondisi gagal    | Pengajuan KRS belum berhasil tersimpan.                                             |
| Aturan bisnis         | Validasi harus berhasil sebelum pengajuan tersimpan. Unduh bukti bersifat opsional. |