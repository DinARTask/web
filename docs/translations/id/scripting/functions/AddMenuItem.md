---
title: AddMenuItem
description: Untuk menambah item di spesifik menu yang telah kita bikin sebelumnya.
tags: ["menu"]
---

## Deskripsi

Untuk menambah item di spesifik menu yang telah kita bikin sebelumnya.

| Nama    | Deskripsi                      |
| ------- | -------------------------------- |
| menuid  | ID menu yang telah kita bikin sebelumnya.   |
| column  | Kolom yang ingin kita masukkan itemnya.   |
| title[] | Judul untuk item yang kita bikin. |

## Returns

Index row dari item yang telah kita tambahkan.

## Contoh

```c
new Menu:gExampleMenu;

public OnGameModeInit()
{
    gExampleMenu = CreateMenu("Weapons", 2, 200.0, 100.0, 150.0, 150.0);
    AddMenuItem(gExampleMenu, 0, "AK-47");
    AddMenuItem(gExampleMenu, 0, "M4");
    return 1;
}
```

## Catatan

:::tip

Server akan crash ketika script mencatat/menemukan ada menu ID yang tidak valid. Kamu hanya dapat membuat 12 jumlah item setiap menu (item ke-13 akan membuatnya ke sebelah kiri dari header kolom nama (diwarnai), item ke-14 dan seterusnya tidak akan ditampilkan sama sekali). Kamu juga dapat menggunakan 2 kolom (0 dan 1). Kamu hanya dapat menambahkan 8 jenis kode warna untuk setiap satu item (cth: ~r~, ~g~, dll.). Maksimal panjang menu untuk 1 item adalah 31 karakter.

:::

## Main-main juga kesini

- [CreateMenu](CreateMenu): Untuk membuat sebuah menu.
- [SetMenuColumnHeader](SetMenuColumnHeader): Untuk menetapkan nama kolom header di menu.
- [DestroyMenu](DestroyMenu): Untuk menghapus/menghancurkan menu.
- [OnPlayerSelectedMenuRow](../callbacks/OnPlayerSelectedMenuRow): Untuk memanggil efek dari pemain ketika memilih item di menu.
- [OnPlayerExitedMenu](../callbacks/OnPlayerExitedMenu): Untuk memanggil efek saat pemain keluar dari menu yang ditampilkan.
