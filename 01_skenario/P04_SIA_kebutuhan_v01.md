<!-- Kebutuhan -->
ID Kebutuhan                Deskripsi Kebutuhan
SIA-R01                   Mahasiswa dapat melihat jadwal kuliah 
SIA-R02                 Admin akademik dapat mengelola jadwal kuliah 
SIA-R03                 Mahasiswa dapat mengajukan KRS 
SIA-R04                 Sistem memvalidasi KRS sebagai bagian pengajuan 
SIA-R05                 Mahasiswa dapat mengunduh bukti jika memilihnya pada konfirmasi pengajuan 
SIA-R06                 Dosen wali dapat memproses persetujuan atau penolakan KRS 
<!-- lanjutan tugas pert4 -->
SIA-R07                 Mahasiswa dan Dosen sebagai Civitas Akademika dapat melihat kalender akademik.
SIA-R08                 Dosen dapat menginput nilai mata kuliah yang diampunya.
SIA-R09                 Mahasiswa dapat melihat KHS untuk semester yang nilainya sudah dipublikasikan.
SIA-R10                 Admin Akademik dapat mengelola data mahasiswa.
SIA-R11                 Pengelolaan data mahasiswa terdiri atas tambah, ubah, dan hapus data mahasiswa.
SIA-R12                 Model menunjukkan collaboration yang merealisasikan Input Nilai Mata Kuliah dan Lihat KHS.

<!-- identifikasi Aktor -->
Aktor                       Kedudukan                                 Tujuan terhadap sistem
Civitas Akademika           Aktor umum                                Melihat kalender akademik.
Mahasiswa                   Aktor khusus dari Civitas Akademika       Mewarisi fungsi melihat kalender akademik juga melihat 
                                                                      KHS dan menggunakan fungsi KRS.
Dosen                       Aktor khusus dari Civitas Akademika       Mewarisi fungsi melihat kalender akademik dapat menginput nilai mata kuliah yang diampunya.                

Admin Akademik              Aktor lama                              Mengelola jadwal/data mahasiswa sesuai fungsi yang ada pada diagram kumulatif.

Dosen Wali                  Aktor lama                                Terlibat pada proses keputusan KRS


<!-- katalog usecase -->
ID                  Nama Use Case           Aktor terkait               Sumber                  Status/keterangan
SIA-UC01            Lihat Jadwal Kuliah     Mahasiswa                   Pertemuan 2             Tetap      
SIA-UC02            Kelola Jadwal Kuliah    Admin Akademik              Pertemuan 2             Tetap
SIA-UC03            Ajukan KRS              Mahasiswa                   Pertemuan 3             Tetap; include SIA-UC04
SIA-UC04            Validasi KRS            Sistem                      Pertemuan 3             Tetap
SIA-UC05            Unduh Bukti Pengajuan KRS Mahasiswa                 Pertemuan 3             Tetap
SIA-UC06            Proses Keputusan KRS    Dosen Wali                  Pertemuan 3             Tetap
SIA-UC07            Lihat Kalender Akademik Civitas Akademika           SIA-R07                 Baru
SIA-UC08            Input Nilai Mata Kuliah Dosen                       SIA-R08                 Baru
SIA-UC09            Lihat KHS               Mahasiswa                   SIA-R09                 Baru
SIA-UC10            Kelola Data Mahasiswa   Admin Akademik              SIA-R10, SIA-R11        Baru; use case umum
SIA-UC11            Tambah Data Mahasiswa   Admin Akademik              SIA-R11                 Baru
SIA-UC12            Ubah Data Mahasiswa     Admin Akademik              SIA-R11                 Baru
SIA-UC13            Hapus Data Mahasiswa    Admin Akademik              SIA-R11                 Baru

<!-- Generalization USecase  -->
SIA-UC11 Tambah Data Mahasiswa: menghasilkan data mahasiswa baru yang tersimpan.
SIA-UC12 Ubah Data Mahasiswa: menghasilkan perubahan data mahasiswa yang sudah ada.
SIA-UC13 Hapus Data Mahasiswa: menghapus data mahasiswa hanya jika tidak memiliki data akademik aktif.

<!-- Collaboration -->
ID Collaboration            Nama collaboration          Use case yang direalisasikan
SIA-CO01                    Input Nilai Mata Kuliah     SIA-UC08 Input Nilai Mata Kuliah
SIA-CO02                    Lihat KHS                   SIA-UC09 Lihat KHS

