<!-- Ajukan KRS -->
Elemen	                        Deskripsi
Tujuan	                    Menghasilkan pengajuan KRS yang tersimpan
Aktor utama	                Mahasiswa
Sumber kebutuhan	        SIA-R03 dan SIA-R04
Pemicu	                    Mahasiswa memilih fungsi pengajuan KRS
Prasyarat	                Mahasiswa telah terautentikasi; data mata kuliah, prasyarat, dan jadwal tersedia
Pascakondisi berhasil	    Pengajuan tersimpan dengan status Menunggu Persetujuan Dosen Wali
Pascakondisi gagal	        Tidak ada pengajuan baru yang berhasil tersimpan
Include	                    SIA-UC04 — Validasi KRS
Extension point	            Konfirmasi penyimpanan pengajuan, pada langkah 6
Extend	                    SIA-UC05 jika [mahasiswa memilih unduh]

Alur utama:
Langkah	Tindakan mahasiswa	                        Respons sistem
1	Membuka menu pengajuan KRS	                Menampilkan formulir pengajuan
2	Memilih mata kuliah	                        Menampung pilihan mata kuliah
3	Mengirim pengajuan	                        Memeriksa kelengkapan data
4	—	                                        Menjalankan SIA-UC04 untuk memvalidasi KRS
5	—	                                        Jika validasi berhasil, menyimpan pengajuan dan menetapkan status Menunggu      Persetujuan Dosen Wali
6	Melihat konfirmasi pengajuan	            Menampilkan nomor pengajuan dan status penyimpanan
7	Memilih unduh bukti atau mengakhiri proses	Menjalankan SIA-UC05 jika mahasiswa memilih unduh


<!-- Validasi KRS -->
Elemen	                            Deskripsi
Tujuan	                        Memeriksa kelayakan pengajuan KRS sebelum disimpan
Aktor utama	                    Tidak ada aktor langsung; dijalankan oleh sistem dalam SIA-UC03
Sumber kebutuhan	            SIA-R04
Pemicu	                        Mahasiswa mengirim pengajuan KRS
Prasyarat	                    Mahasiswa telah memilih mata kuliah
Pascakondisi berhasil	        Pengajuan dinyatakan valid dan dapat dilanjutkan ke penyimpanan
Pascakondisi gagal	            Pengajuan dinyatakan tidak valid dan belum berhasil disimpan
Include                         	—
Extension point	                    —
Extend	                            —

Alur utama:
Langkah	Tindakan mahasiswa	                Respons sistem
1	                                    Mengirim pengajuan KRS	Memeriksa kelengkapan data
2	—	                                Memeriksa prasyarat mata kuliah
3	—	                                Memeriksa benturan jadwal
4	—	                                Menyatakan validasi berhasil jika seluruh pemeriksaan terpenuhi


<!-- Unduh Bukti Pengajuan KRS -->
Elemen	                         Deskripsi
Tujuan	                    Menyediakan bukti pengajuan KRS untuk diunduh
Aktor utama	                Mahasiswa
Sumber kebutuhan	        SIA-R05
Pemicu	                    Mahasiswa memilih unduh bukti pada konfirmasi pengajuan
Prasyarat	                KRS berhasil disimpan dan konfirmasi penyimpanan telah ditampilkan
Pascakondisi berhasil	    Bukti pengajuan tersedia untuk diunduh
Pascakondisi gagal	        Bukti tidak berhasil disediakan untuk diunduh
Include                     	—
Extension point             	—
Extend	                    SIA-UC03 — Ajukan KRS, jika [mahasiswa memilih unduh]

Alur utama:
Langkah	Tindakan mahasiswa	                    Respons sistem
1	Melihat konfirmasi penyimpanan	        Menampilkan pilihan unduh bukti
2	Memilih unduh bukti	                    Memproses permintaan unduh
3	Mengunduh bukti	                        Menyediakan bukti pengajuan untuk diunduh


<!-- Keputusan KRS -->
Elemen	                Deskripsi
Tujuan	                    Menghasilkan keputusan atas pengajuan KRS
Aktor utama	                Dosen wali
Sumber kebutuhan	        SIA-R06
Pemicu	                    Dosen wali memilih pengajuan KRS untuk diproses
Prasyarat	                Terdapat pengajuan KRS berstatus Menunggu Persetujuan Dosen Wali
Pascakondisi berhasil	    Keputusan dan catatan dosen wali tersimpan
Pascakondisi gagal	        Keputusan belum berhasil disimpan
Include                     	—
Extension point	                —
Extend	                        —

Alur utama:
Langkah	Tindakan dosen wali	                Respons sistem
1	Membuka pengajuan KRS	            Menampilkan informasi pengajuan
2	Memeriksa pengajuan	                Menampilkan data KRS yang diajukan
3	Memilih setujui atau tolak	        Menampilkan bagian catatan keputusan
4	Mengisi catatan keputusan	        Memproses keputusan dan catatan
5	Mengonfirmasi keputusan	            Menyimpan keputusan dan memperbarui status KRS