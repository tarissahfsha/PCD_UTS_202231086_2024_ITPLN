
# Analisis Project UTS Pengolahan Citra Digital

Di Soal Pertama dalam mendeteksi warna pada citra saya sudah menganalisis bahwasannya :
sebelum mendeteksi terlebih dahulu mengimpor cv2, matplotlib as plt, numpy as np. setelah dideteksi
terlihat bahwa gambar dari variabel citra_gabungan dibagi menjadi empat subplot menggunakan plt.subplot(2, 2, index). Setiap subplot menampilkan saluran warna tertentu dari citra asli, yaitu merah, hijau, dan biru, serta citra aaslinya.

dari gambar asli :
Subplot pertama menampilkan gambar asli tanpa perubahan.

Red Channel (Saluran Merah):
Subplot kedua menampilkan saluran warna merah dari citra. Saluran warna merah diambil dari citra_gabungan[:,:,0].
Menggunakan cmap="gray" untuk menampilkan saluran warna dalam skala abu-abu.

Green Channel (Saluran Hijau):
Subplot ketiga menampilkan saluran warna hijau dari citra. Saluran warna hijau diambil dari citra_gabungan[:,:,1].
Juga menggunakan cmap="gray" untuk menampilkan saluran warna dalam skala abu-abu.

Blue Channel (Saluran Biru):
Subplot keempat menampilkan saluran warna biru dari citra. Saluran warna biru diambil dari citra_gabungan[:,:,2].Menggunakan cmap="gray" untuk menampilkan saluran warna dalam skala abu-abu.

dengan representasi saluran warna ini, bisa melihat kontribusi masing-masing saluran warna terhadap gambar asli dan bagaimana perbedaan intensitas di setiap saluran warna dapat mempengaruhi citra secara keseluruhan.

lalu analisis histogramnya : 
dalam histogram,biru, dan hijau menunjukkan distribusi intensitas piksel untuk saluran warna masing masing dalam gambar.
Jika puncak histogram berada di sebelah kanan, ini menunjukkan bahwa masing-masing warna mendominasi gambar, sedangkan jika puncak histogram berada di sebelah kiri, masing-masing warna kurang dominan.

Kemudian di soal nomor dua dalam membuat batas ambang citra, saya menganalisis nilai batas ambang yg didapat bahwasannya :
- blue :
nilai yang didapatkan yaitu 500. alasannya bisa mendapatkan nilai 500 karena nilai ambang batas mungkin disesuaikan dengan resolusi dan kualitas gambar yang umumnya digunakan. Jika gambar memiliki resolusi yang tinggi, jumlah piksel yang diperlukan untuk membaca teks dengan jelas mungkin lebih rendah.

- red-blue :
nilai yang didapatkan yaitu 50. Alasannya bisa mendapatkan nilai ambang batas 50 karena teks yang terbaca dengan baik biasanya memiliki kontras yang cukup jelas dengan latar belakangnya. Dengan memiliki nilai ambang batas yang cukup rendah seperti 50 piksel, hal ini mungkin menunjukkan bahwa teks berwarna merah dan biru harus memiliki kontras yang cukup tinggi dengan latar belakangnya sehingga dapat dibaca dengan jelas oleh manusia, meskipun hanya dengan jumlah piksel yang terbatas.

- red-green-blue : 
nilai yang didapatkan yaitu 500. alasannya bisa mendapatkan nilai 500 karena nilai ambang batas yang cukup tinggi mungkin mencerminkan ukuran teks yang diperlukan agar tetap terlihat jelas, bahkan ketika terdapat pencampuran warna merah, biru, dan hijau dalam teks tersebut. Teks yang lebih besar atau lebih tebal akan membutuhkan jumlah piksel yang lebih besar untuk dapat dibaca dengan jelas.
