# jawa_shortcut_command

*Karena gw males run javac + java, mending run jawa ;p*

## Instalasi

Untuk menggunakan script `jawa` sebagai perintah pintasan (shortcut command) di terminal mana pun, Anda harus menempatkannya di direktori yang terdaftar dalam variabel lingkungan PATH sistem operasi Anda.

### 💻 Windows

Di Windows, Anda dapat menempatkan script `jawa` di folder tempat symbolic links ke `java.exe` dan `javac.exe` berada, sehingga mudah diakses oleh sistem.

1. Pastikan Script Dapat Dieksekusi:

    - Pastikan Anda menggunakan lingkungan yang dapat menjalankan Bash, seperti **Git Bash** atau **Windows Subsystem for Linux (WSL)**, karena `jawa` adalah script bash.

2. Pindahkan Script:

    - Pindahkan file jawa (yang berisi script bash) ke lokasi yang sering digunakan oleh lingkungan Java:

        ```bash
        # Ganti dengan path folder javapath_target yang sesuai di sistem Anda
        mv jawa "C:\Program Files\Common Files\Oracle\Java\javapath_target_3405906"
        ```

    - Catatan: Jika direktori ini tidak ada dalam PATH Anda, cara yang lebih andal adalah menambahkan lokasi yang Anda pilih (misalnya `C:\Users\YourUser\Scripts`) ke variabel lingkungan PATH sistem Windows Anda.

### 🐧 MacOS dan 🐘 Linux

Di sistem berbasis Unix (Linux, macOS, BSD), Anda hanya perlu membuat script jawa dapat dieksekusi dan memindahkannya ke salah satu direktori binari standar sistem.

1. Jadikan Script Dapat Dieksekusi:

    - Berikan izin eksekusi pada script jawa menggunakan perintah chmod:

        ```bash
        chmod +x jawa
        ```

2. Pindahkan ke Direktori PATH:

    - Pindahkan file jawa ke direktori yang sudah ada di variabel lingkungan PATH Anda. Direktori yang direkomendasikan untuk binari pengguna lokal adalah `/usr/local/bin/` atau `~/.local/bin/`.

        ```bash
        # Menggunakan sudo untuk /usr/local/bin/ (direkomendasikan)
        sudo mv jawa /usr/local/bin/

        # ATAU, jika Anda tidak memiliki izin sudo dan ingin menginstalnya di direktori home
        mv jawa ~/.local/bin/
        ```


    - Jika Anda memindahkannya ke ~/.local/bin/, pastikan direktori tersebut ada di PATH Anda.

### ✅ Selesai

Setelah langkah-langkah di atas, Anda dapat membuka terminal baru dan menjalankan perintah:

```bash
$ jawa

╔════════════════════════════════════╗
║       ☕ JAWA, JAWA, JAWA! ☕     ║
╚════════════════════════════════════╝

"Karena gw males run javac + java, mending run jawa;p"

Compile and Run Java Program
Usage: jawa [-s] [-c|-r] <filename.java>
  -s : Silent mode (no banner or messages)
  -c : Compile only
  -r : Run only

```