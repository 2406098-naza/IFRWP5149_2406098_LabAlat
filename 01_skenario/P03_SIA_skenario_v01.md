Mahasiswa mengajukan KRS dengan memilih mata kuliah. Setiap 
pengajuan menjalankan validasi KRS yang memeriksa kelengkapan, 
prasyarat mata kuliah, dan benturan jadwal. Jika validasi berhasil, 
sistem menyimpan pengajuan berstatus menunggu persetujuan dosen 
wali. Pada konfirmasi penyimpanan, mahasiswa dapat memilih 
mengunduh bukti pengajuan. Dosen wali menyetujui atau menolak KRS 
dan memberikan catatan keputusan.


<!--  -->
ID      Kebutuhan tugas 
SIA-R01 Mahasiswa dapat melihat jadwal kuliah 
SIA-R02 Admin akademik dapat mengelola jadwal kuliah 
SIA-R03 Mahasiswa dapat mengajukan KRS 
SIA-R04 Sistem memvalidasi KRS sebagai bagian pengajuan 
SIA-R05 Mahasiswa dapat mengunduh bukti jika memilihnya pada konfirmasi pengajuan 
SIA-R06 Dosen wali dapat memproses persetujuan atau penolakan KRS 


<!-- Batas dan asumsi:  -->
• Pengguna telah terautentikasi. 
• Data mata kuliah, prasyarat, dan jadwal tersedia. 
• Validasi gagal menyebabkan pengajuan belum berhasil tersimpan. 
• Unduh bukti tidak menjadi syarat keberhasilan pengajuan. 
• KRS tersimpan belum berarti disetujui. 
• Pembayaran, pengisian nilai, dan implementasi basis data berada di luar 
tugas. 


<!-- Katalog UseCAse -->
ID                  Nama use case                      Peran dalam model 
SIA-UC01        Lihat Jadwal Kuliah                    Fungsi utama mahasiswa 
SIA-UC02        Kelola Jadwal kuliah                   Fungsi utama Admin Akademik
SIA-UC03        Mengajukan KRS                         Fungsi utama mahasiswa 
SIA-UC04        Validasi KRS                           Perilaku yang disertakan UC03 
SIA-UC05        Unduh Bukti Pengajuan KRS              Tambahan bersyarat pada UC03
SIA-UC06        Menyetujui Keputusan KRS               Fungsi utama Dosen Wali

<!-- identifikasi Aktor -->
Aktor               Tujuan terhadap sistem 
Mahasiswa           Lihat Jadwal Kuliah, Ajukan KRS, dan Unduh Bukti Pengajuan KRS.
Dosen Wali          Menyetujui Keputusan KRS.
Admin Akademik      Mengelola Jadwal Kuliah


<!-- Relasi INclude -->
SIA-UC03 <<include>> SIA-UC04
Ajukan KRS selalu mencakup validasi kelengkapan data, prasyarat mata kuliah, dan benturan jadwal.


<!-- Relasi Extend -->
SIA-UC05 <<extend>> SIA-UC03
Unduh bukti merupakan proses tambahan yang dilakukan jika mahasiswa memilihnya setelah konfirmasi penyimpanan.