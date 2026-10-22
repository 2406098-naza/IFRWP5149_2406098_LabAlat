ID dan nama                                  SIA-UC08: Input Nilai Mata Kuliah
Sumber kebutuhan                            SIA-R08 dan SIA-R12
Tujuan                                      Menyimpan nilai mata kuliah yang diampu dosen secara benar.
Aktor utama                                 Dosen
Aktor pendukung                             Sistem Informasi Akademik
Pemicu                                      Dosen membuka fungsi input nilai setelah masa perkuliahan berakhir.
Prasyarat                                   Dosen telah login dan merupakan dosen pengampu mata kuliah yang dipilih periode                                    input nilai telah dibuka.

Generalization                              Tidak memiliki generalization pada use case ini.
Collaboration                               SIA-CO01: Input Nilai Mata Kuliah
Pascakondisi berhasil                       Nilai tersimpan pada mata kuliah dan mahasiswa yang sesuai, dengan status belum dipublikasikan sampai dinyatakan resmi.

Pascakondisi gagal                          Nilai tidak tersimpan atau tidak berubah; sistem menampilkan alasan kegagalan.

Alur utama :
Dosen memilih mata kuliah yang diampunya.
Sistem memeriksa hak akses dosen dan menampilkan daftar mahasiswa pada mata kuliah tersebut.
Dosen memasukkan nilai untuk mahasiswa.
Sistem memeriksa kelengkapan dan rentang nilai.
Dosen mengonfirmasi penyimpanan.
Sistem menyimpan nilai sebagai nilai yang belum dipublikasikan dan menampilkan konfirmasi.