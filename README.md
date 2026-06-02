# namaz-content

Namaz iOS ilovasi uchun masofadan boshqariladigan ta'lim kontenti (jsDelivr CDN orqali).

## Tuzilma

```
config.json          # kill-switch va versiya boshqaruvi (har safar yangidan o'qiladi)
v1/
  duas_uz.json
  prayer_steps_uz.json
  rakat_chart_uz.json
  ramadan_content_uz.json
```

## config.json

| Maydon | Ma'no |
|---|---|
| `contentAvailable` | `false` bo'lsa ilova **hech qanday ma'lumot ko'rsatmaydi** (eng ustun flag) |
| `remoteContentEnabled` | `false` bo'lsa remote o'chadi, ilova ichidagi bundle kontent ishlatiladi |
| `contentVersion` | Qaysi papkadan kontent olinadi (`v1`, `v2`...) — CDN keshini chetlab o'tish uchun |
| `message` | Ixtiyoriy e'lon (hozircha ishlatilmaydi) |

## Kontentni yangilash

1. `v1/` ichidagi JSON faylni tahrirlang → commit & push.
2. jsDelivr `@main` keshini ~12 soat ushlaydi. Tezroq tarqalishi uchun yangi `v2/` papka yarating va `config.json`'da `contentVersion` ni `v2` qiling (`config.json` har safar yangidan o'qilgani uchun deyarli darhol qo'llanadi).

## URL formati (jsDelivr)

```
https://cdn.jsdelivr.net/gh/soyabon/namaz-content@main/config.json
https://cdn.jsdelivr.net/gh/soyabon/namaz-content@main/v1/duas_uz.json
```
