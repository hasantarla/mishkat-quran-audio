# mishkat-quran-audio

Mişkat uygulaması için **âyet sesi aynası**. Ses dosyaları
[everyayah.com](https://everyayah.com) üzerinden alınır, 250 âyetlik
zip paketleri hâlinde **Releases**'te yayınlanır. Uygulama toplu indirmede önce
buradaki paketleri dener; paket yoksa everyayah'tan âyet âyet iner.

| | |
|---|---|
| Kâri sayısı | 9 |
| Paket boyu | 250 âyet (~47 MB) |
| Paket adı | `<kari>-pNN.zip` (`v1` etiketi) |
| Dosya adı (zip içinde) | `SSSAAA.mp3` |

## Paketleri yükleme

1. Aynayı üret (Mişkat deposunda):

   ```bash
   cd data/scripts
   node mirror-quran-audio.mjs --target <ayna-dizini>            # sesleri indir
   node mirror-quran-audio.mjs --target <ayna-dizini> --zip      # + dist/*.zip
   node mirror-quran-audio.mjs --target <ayna-dizini> --check    # doğrula
   ```

2. Yayınla (etiket **sabit**: içerik sonradan sessizce değişmesin):

   ```bash
   gh release create v1 dist/*.zip -R <kullanıcı>/mishkat-quran-audio \
     -t "v1 — ayet sesleri" -n "Kâri başına 250 âyetlik paketler."
   ```

3. `MANIFEST.sha256` ve `NOTICE.md` bu depoya commit edilir; `.audio/` ve
   `dist/` **commit edilmez** (10+ GB'lık ses verisi git geçmişine girmez).

Kaynak ve lisans notu: [NOTICE.md](NOTICE.md).
