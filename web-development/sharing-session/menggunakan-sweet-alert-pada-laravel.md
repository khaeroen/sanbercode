# Menggunakan Sweet Alert pada Laravel

**9 Februari 2017 by Andrika**

Kalian pasti pernah menggunakan aplikasi? khususnya \(_Website_\). Pernah tidak kepikiran untuk membuat feedback sebagai informasi yang akan didapatkan oleh user ketika user melakukan aktivitas di aplikasi \(_website_\)-nya ?

Jika tidak, ayo mulai memikirkannya, dan belajar membuatnya

## _Sweet Alert_

Yup, kalian pasti sudah tau kan apa itu _Sweet Alert_ ? Oke, Saya Jelaskan. \_Sweet Alert \_adalah sebuah alert \(Notifikasi\) yang ****sudah di design menarik dan mudah untuk digunakan. Referensi: [packagist.org](https://packagist.org/packages/uxweb/sweet-alert)

Langsung aja kali ya"

Langkah pertama siapakan Composer bisa di download pada link [ http://gitcomposer.org ](https://getcomposer.org)

```text
composer require uxweb/sweet-alert
```

```text
UxWeb\SweetAlert\SweetAlertServiceProvider::class,
```

```text
UxWeb\SweetAlert\SweetAlertServiceProvider::class,
```

```text
<link rel="stylesheet" href="{{ url('sweetalert/sweetalert.min.css') }}">
...
<script src="{{ url('sweetalert/sweetalert.min.js') }}"></script>
```

