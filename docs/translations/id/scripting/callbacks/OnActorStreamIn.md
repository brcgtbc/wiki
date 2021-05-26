---
title: OnActorStreamIn
description: Callback ini akan terpanggil jika Aktor berada dalam jangkauan radius stream dari pemain lain
tags: []
---

:::warning

Fungsi ini telah ditambahkan kedalam SA-MP 0.3.7 dan tidak akan bekerja pada versi dibawahnya!

:::

## Deskripsi

Callback ini akan terpanggil jika Aktor berada dalam jangkauan radius stream dari pemain lain.

| Nama        | Deskripsi                                                            |
| ----------- | -------------------------------------------------------------------- |
| actorid     | ID dari aktor yang berada dalam stream radius jangkauan pemain lain. |
| forplayerid | ID dari pemain lain yang berada dalam radius jangkauan si aktor.     |

## Returns

Callback ini akan selalu dipanggi duluan dalam filterscripts.

## Contoh

```c
public OnActorStreamIn(actorid, forplayerid)
{
    new sring[40];
    format(string, sizeof(string), "Aktor %d ada dalam jangkauan anda.", actorid);
    SendClientMessage(forplayerid, 0xFFFFFFFF, string);
    return 1;
}
```

## Catatan

:::tip

Callback ini juga bisa terpanggil kepada NPC.

:::

## Fungsi Terkait
