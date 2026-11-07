# NOTICE — kaynak ve atıf

Bu depo, Mişkat uygulamasının **âyet sesi aynası**dır. Ses dosyaları burada
üretilmedi; [everyayah.com](https://everyayah.com) üzerinden, `data/<klasör>/`
altındaki kayıtlardan kopyalandı.

| Kâri kimliği | Ad | everyayah klasörü | Paket adı |
| --- | --- | --- | --- |
| `mahir` | Mahir el-Muaykıli | `MaherAlMuaiqly128kbps` | `mahir-p01.zip` … |
| `sudais` | Abdurrahman es-Sudeys | `Abdurrahmaan_As-Sudais_192kbps` | `sudais-p01.zip` … |
| `shuraym` | Suud eş-Şüreyim | `Saood_ash-Shuraym_128kbps` | `shuraym-p01.zip` … |
| `hudhaify` | Ali el-Huzeyfî | `Hudhaify_128kbps` | `hudhaify-p01.zip` … |
| `husary` | Mahmud Halil el-Husarî | `Husary_128kbps` | `husary-p01.zip` … |
| `abdulbasit` | Abdülbasit Abdüssamed | `Abdul_Basit_Murattal_192kbps` | `abdulbasit-p01.zip` … |
| `minshawi` | Muhammed Sıddık el-Minşâvî | `Minshawy_Murattal_128kbps` | `minshawi-p01.zip` … |
| `alafasy` | Mişari el-Afâsî | `Alafasy_128kbps` | `alafasy-p01.zip` … |
| `rifai` | Hânî er-Rifâî | `Hani_Rifai_192kbps` | `rifai-p01.zip` … |

## Biçim

- Ürün dosyaları **GitHub Releases** altındadır (`v1` etiketi): her kâri,
  250 âyetlik parçalara bölünmüş `<kari>-pNN.zip` paketleri hâlinde.
- Zip içinde dosyalar **kök seviyededir** ve adları `SSSAAA.mp3` biçimindedir
  (sûre üç hane + âyet üç hane). Uygulama adı çözer, zip'teki sıraya güvenmez.
- Paketler **sıkıştırmasızdır**: mp3 zaten sıkıştırılmıştır.
- `MANIFEST.sha256` yayınlanan paketlerin özetlerini taşır.

```bash
sha256sum -c MANIFEST.sha256   # indirilen dist/*.zip ile karşılaştırır
```

## Lisans

everyayah.com, ses dosyaları için dosya bazında bir lisans metni yayınlamıyor.
Bu ayna yalnızca **tek bir uygulamanın** çevrimdışı indirmesi için, kaynağı
belirtilerek kopyalanmıştır; ticari kullanım iddiası yoktur. Kayıtların hak
sahibi itiraz ederse ilgili kâri paketleri **yayından kaldırılır** ve uygulama o
kâri için kaynağa (everyayah) döner.

## Kaynaklar

- [everyayah.com](https://everyayah.com) — kâri klasörleri ve dosya adlandırması
  (`SSSAAA.mp3`) buradan gelir.
- Kayıtların okunuşu/icrası ilgili kârilere aittir; ayna yalnızca dağıtım
  kolaylığı sağlar.
