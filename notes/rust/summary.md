# The Summary Of Rust Programming Language
![Rust programming language logo](../../assets/img/rust.svg =250x)

[Rust](https://www.rust-lang.org/) adalah bahasa pemrograman yang dikembangkan 
oleh Mozilla Research dan didukung komunitas open source yang besar. Dikembangkan
pertama kali oleh Graydon Hoare pada tahun 2006 😎.

Mozilla mulai mensponsori Rust pada tahun 2009 dan diperkenalkan secara resmi
pada tahun 2010. Versi 1.0.0 adalah first stable production Rust yang dirilis awal
tahun 2015 😮.

Rust merupakan bahasa pemrograman (compiled language) _general purpose_ dan
_multi-paradigma_; _imperative_, _structured_ dan _object-oriented_. Tipe
penulisannya adalah _static_ dan _strong_. **rustc** adalah nama dari Rust compiler.

**rustc** (compiler) merupakan _self-hosted compiler_ 🤔 yang artinya compiler tersebut
ditulis pada bahasa Rust itu sendiri yang menggunakan versi sebelumnya 😮. **rustc**
menggunakan framwork ⚙ [LLVM](https://en.wikipedia.org/wiki/LLVM) dan menghasilkan
_native executable code_ yang sama seperti _low-level code_  bahasa C++.

Rust didesain portable seperti C++ yang saat ini dapat berjalan pada perangkat
Linux, macOS X, Windows, FreeBSD, Android dan iOS 😮.

[> Lihat semua daftar perangkat yang didukung disini 😉](https://forge.rust-lang.org/platform-support.html)

**rustaceans** adalah sebutan bagi orang yang menggunakan bahasa pemrograman Rust 😍.

Beberapa perusahaan yang menggunakan Rust 😍:
- NPM
- Dropbox
- Tilde
- Yelp
- Firefox
- Cloudeflare
- Dll.

## 📦 Instalasi
**Linux 🐧, macOS 🍎 dan unix-like OS**
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

**Windows**
1. ⬇️ Download [rustup-init.exe](https://static.rust-lang.org/rustup/dist/i686-pc-windows-gnu/rustup-init.exe)
2. ⚡ Run `rustup-init.exe`

**OS lainnya**

[Metode instalasi Rust lainnya](https://forge.rust-lang.org/infra/other-installation-methods.html)

✔️ Cek instalasi
```bash
rustc --version
```
atau
```bash
rustc -V
```

## ❌ Uninstall
```bash
rustup self uninstall
```

## ⚙ rustc - The Rust Compiler
Instalasi Rust terletak pada folder berikut:
- Windows `C:\Users\username\.cargo\bin`
- Linux dan macOS `/home/username/.cargo/bin`

Format dasar menggunakan **rustc** 🤓:
```bash
rustc input [options]
```
- **options** adalah _flags_ (directives) yang digunakan untuk memberikan opsi
saat proses kompilasi.
- **input** adalah nama file dengan ekstensi `.rs` yang akan dikompilasi.

Contoh options: `-g`, `-W`, `--test`, `--version`, dll.

Contoh input: `main.rs`, `start_app.rs`, dll.

Contoh mengkompilasi program Rust:
```bash
rustc main.rs -o main
```

`rust -o` menghasilakan _native code_ yang sudah dioptimalkan untuk kecepatan
eksekusi (setara dengan menggunakan `rustc -C opt-level=2`). `rust -C opt-level=3`
adalah opsi kompilasi yang menghasilkan _native code_ dengan optimalisasi tertinggi 🤓.

## 📃 Anatomi Program Rust
```rust
// main.rs
fn main() {
  println!("Hello, Rust!");
}
```
Pada dasarnya anatomi program Rust sama seperti bahasa C/C++, Java atau C# dimana
eksekusi program dimulai dari _function_ yang bernama `main` 😃.

- `fn` merupakan singkatan dari _function_ yang digunakan untuk mendeklarasikan
sebuah _function_.
- `main` adalah nama _function_
- `()` merupakan tempat untuk menulis parameter.
- `{}` merupakan tempat untuk menulis code yang akan dijalankan.
- `println!()` disebut _macro_ (! menandakan itu adalah _macro_, bukan _function_).
- `;` digunakan untuk mengakhiri sebuah statement.
