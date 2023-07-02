    from rembg import remove
    from PIL import Image
    import matplotlib.pyplot as plt

    def remove_background(input_path, output_path):
    # Buka gambar asli
    input_image = Image.open(input_path)

    # Tampilkan gambar asli sebelum penghapusan latar belakang
    plt.subplot(1, 2, 1)
    plt.imshow(input_image)
    plt.title('Original Image')

    # Hapus latar belakang
    output_image = remove(input_image)

    # Tampilkan gambar setelah penghapusan latar belakang
    plt.subplot(1, 2, 2)
    plt.imshow(output_image)
    plt.title('Image with Removed Background')

    # Tampilkan plot
    plt.tight_layout()
    plt.show()

    # Contoh penggunaan fungsi remove_background
    input_path = 'rivo.jpg'
    output_path = 'rivofotobaru.png'
    remove_background(input_path, output_path)

Berikut adalah teori tentang menghapus latar belakang gambar menggunakan Python dan Jupyter Notebook:

### 1. Import Library

Pertama, kita perlu mengimpor library yang diperlukan untuk menghapus latar belakang gambar. Dalam contoh ini, kita menggunakan library `rembg`, `PIL`, dan `matplotlib.pyplot`. `rembg` adalah library yang memungkinkan kita untuk menghapus latar belakang gambar, `PIL` digunakan untuk membuka dan menyimpan gambar, dan `matplotlib.pyplot` digunakan untuk menampilkan gambar.

```python
from rembg import remove
from PIL import Image
import matplotlib.pyplot as plt
```

### 2. Definisikan Fungsi `remove_background`

Berikut adalah definisi fungsi `remove_background` yang akan digunakan untuk menghapus latar belakang gambar. Fungsi ini menerima dua argumen, `input_path` yang merupakan path atau jalur file gambar asli, dan `output_path` yang merupakan path untuk menyimpan gambar yang telah dihapus latar belakang.

```python
def remove_background(input_path, output_path):
    # Buka gambar asli
    input_image = Image.open(input_path)

    # Tampilkan gambar asli sebelum penghapusan latar belakang
    plt.subplot(1, 2, 1)
    plt.imshow(input_image)
    plt.title('Original Image')

    # Hapus latar belakang
    output_image = remove(input_image)

    # Tampilkan gambar setelah penghapusan latar belakang
    plt.subplot(1, 2, 2)
    plt.imshow(output_image)
    plt.title('Image with Removed Background')

    # Tampilkan plot
    plt.tight_layout()
    plt.show()
```

### 3. Contoh Penggunaan Fungsi `remove_background`

Setelah mendefinisikan fungsi `remove_background`, kita dapat menggunakan fungsi ini dengan memberikan argumen yang sesuai untuk menjalankan proses penghapusan latar belakang gambar. Dalam contoh ini, kita menggunakan file gambar 'rivo.jpg' sebagai gambar asli dan menyimpan gambar hasil penghapusan latar belakang dengan nama 'rivofotobaru.png'.

```python
input_path = 'rivo.jpg'
output_path = 'rivofotobaru.png'
remove_background(input_path, output_path)
```

### Kesimpulan

Menghapus latar belakang gambar merupakan tugas yang umum dalam pemrosesan gambar. Dengan menggunakan library `rembg` dan fungsi-fungsinya, kita dapat menghapus latar belakang gambar dengan mudah dan efisien. Jupyter Notebook memungkinkan kita untuk menjalankan dan menguji kode secara interaktif, serta menampilkan hasil penghapusan latar belakang gambar secara langsung.