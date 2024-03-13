### Tutorial 5
Sebelum dilakukan optimasi:

![all_stud_before](https://github.com/Scarletra/exercise-profiling/assets/112821721/69ef37b8-a027-4257-a24a-ee4b2950bb91)
![image](https://github.com/Scarletra/exercise-profiling/assets/112821721/af88e0a6-146f-4394-bb82-3e82f1a563a5)
![highest_gpa_before](https://github.com/Scarletra/exercise-profiling/assets/112821721/6eafb49f-b016-4e01-af13-429aea9c9f26)
![image](https://github.com/Scarletra/exercise-profiling/assets/112821721/b83f8693-f46b-4c28-8281-3577d60beb4d)

Setelah dilakukan optimasi:
![all_stud_after](https://github.com/Scarletra/exercise-profiling/assets/112821721/3f6fbec7-800f-47c8-935c-80ad40ae1d33)
![image](https://github.com/Scarletra/exercise-profiling/assets/112821721/6248a500-ba91-407a-95eb-5c2319878637)
![highest_gpa_after](https://github.com/Scarletra/exercise-profiling/assets/112821721/2c6ece01-f72e-4eeb-8554-4c4c3468ad2c)
![image](https://github.com/Scarletra/exercise-profiling/assets/112821721/d9a22ecc-fb6a-4acf-82a7-a8770d5a4326)

Setelah melakukan optimsasi pada ketiga method yang ada, kita bisa lihat hasil dari test pada JMeter meningkat dengan cukup drastis. Bisa dilihat dari gambar di atas, waktu yang dibutuhkan pada all-student-name request dan highest-gpa request berkurang dengan cukup signifikan (all-student-name: 8000ms to 800ms, highest-gpa: 200ms to 30ms). Maka dari itu, dapat disimpulkan bahwa dengan melakukan profiling dan optimasi performa, kita bisa meningkatkan waktu respons pada aplikasi kita.

## Reflection
1. Kedua pendekatan performance testing tersebut (JMeter dan Inteliij Profiler) memiliki fungsi yang berbeda menurut saya. JMeter itu sendiri adalah alat yang dapat kita gunakan untuk melihat performa dari aplikasi yang sedang kembangkan. Kita bisa melihat banyak aspek performa lainnya selain dari waktu respons aplikasi kita. Selain itu, kita juga bisa menguji performa aplikasi kita dengan mensimulasikan sejumlah user tertentu yang dapat mengakses aplikasi kita dalam suatu waktu. Sedangkan, Inteliij Profiler adalah alat yang berguna untuk melakukan profiling. Melalui tools ini, kita sebagai pengembang dapat mengetahui secara rinci penggunaan memori dan juga waktu pada kode aplikasi kita. Dengan adanya tools ini, kita bisa mendeteksi dan melakukan optimasi performa aplikasi kita.

2. Dengan adanya profiling, saya bisa mendeteksi bagian mana yang menurunkan performa dari aplikasi saya. Hal ini dapat kita lihat berdasarkan penggunaan CPU< memori, dan juga jumlah pemanggilan method lain. Dari beberapa aspek tersebut, kita bisa tahu bagian mana yang berpengaruh besar dalam penurunan performa aplikasi kita. Sebagai contoh, pada tutorial ini, method getAllStudentWithCourses memiliki waktu eksekusi yang sangat lama, sehingga berpengaruh besar dalam performa aplikasi.

3. Ya, Inteliij Profiler sangatlah efektif dalam membantu saya dalam menemukan dan menganalisa bottleneck yang ada pada aplikasi saya. Itu disebabkan oleh fitur yang tersedia pada Inteliij Profile, yang menyajikan berbagai informasi yang berguna untuk mengoptimasikan performa aplikasi seperti, penggunaan memori, CPU, dan pemanggilan method. Tidak hanya itu, saya juga bisa melihat secara langsung persebaran waktu eksekusi serta hal lainnya dari kesuluruhan method yang digunakan pada aplikasi saya.

4. Tantangan yang saya dapatkan selama melakukan performance testing dan profiling adalah pemahaman saya akan tools yang disediakan. Saya rasa tanpa pemahaman yang baik terhadap tools yang ada, kita jadi kurang maksimal dalam melakukan optimasi performa aplikasi kita. Lalu, cara saya menghadapi tantangan tersebut tentunya adalah dengan melakukan eksplorasi sendiri seperti mencari di StackOverFlow ataupun menonton video yang ada di YouTube.

5. Keuntungan dari menggunakan Inteliij Profiler terletak pada fitur yang disajikan. Hal ini sudah dijelaskan pada poin yang ketiga.

6. Jika terjadi ketidakkonsistenan antara hasil testing yang ada pada JMeter dengan Inteliij Profiler, saya akan coba mencari tahu penyebabnya. Sebenarnya ada beberapa faktor yang dapat memengaruhi perbedaan hasil dari kedua tools tersebut. Saya juga akan melihat secara mendetil melalui bagian yang sedang saya uji, karena dari situ saya bisa menemukan informasi-informasi yang lebih jelas. Selain itu, karena cara penggunaan yang cukup berbeda antara kedua tools tersebut, menurut saya wajar saja jika terjadi perbedaan hasil testing.

7. Saya akan mencoba melakukan analisa secara mendetil pada bagian yang sedang saya uji. Setelah mengetahui penyebab peningkatan waktu eksekusi bagian tersebut, saya akan melakukan perubahan melalui pendekatan lainnya yang tentunya akan jauh lebih baik efektivitasnya dibandingkan kode yang sudah ada sebelumnya. Sebagai contoh, pada method untuk mendapatkan semua nama Student, saya menggunakan method mapping dan juga collection untuk langsung menyatukan isi dari array yang ada menjadi sebuah satu kesatuan string.
   
