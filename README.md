# Antioch Rising · FRC 10947

Antioch Rising takımının (Hatay Fen Lisesi, FIRST Robotics Competition #10947) web sitesi. Türkçe ve İngilizce çalışır; tek bir HTML dosyasıdır, kurulum ya da derleme gerekmez.

## Dosyalar

```
index.html            Sitenin tamamı (tasarım, metinler, kod)
assets/logo/          Arma (logo) dosyaları
assets/robot/         Robot fotoğrafları (her biri 1600, 800 ve 240 px)
assets/sponsors/      Sponsor logoları (eklendikçe)
```

## Yazıları düzenlemek

`index.html` dosyasını açın (GitHub'da dosyaya tıklayıp kalem simgesiyle de düzenleyebilirsiniz). Metinler iki yerde durur:

- **`const CONTENT`**: Değişen bilgiler. E-posta ve Instagram, robotlar (fotoğraflar, teknik özellikler), ekipler ve üyeleri, sponsorlar, sezon geçmişi, sıradaki etkinlik tarihi.
- **`const I18N`**: Sitedeki diğer tüm yazılar (başlıklar, butonlar, paragraflar). `en` ve `tr` olarak iki liste vardır; bir yazıyı değiştirirken iki dildeki karşılığını da güncelleyin.

Her metin `{en:"...", tr:"..."}` şeklindedir. Tırnak işaretlerini ve virgülleri silmemeye dikkat edin.

### Örnekler

Ekibe üye eklemek (`CONTENT.team` içinde):

```js
{ cls:"soft", t:{en:"Software",tr:"Yazılım"}, p:{...},
  members:[ { name:"Ad Soyad", role:{en:"Team lead", tr:"Ekip lideri"} } ] }
```

Sponsor logosu eklemek: logoyu `assets/sponsors/` klasörüne yükleyin (şeffaf PNG ya da SVG), sonra `CONTENT.sponsors` içinde ilgili satıra yolunu yazın:

```js
{ name:"AYİDER", tier:"emblema", logo:"assets/sponsors/ayider.svg", url:"https://..." }
```

`tier`: `"emblema"` ana sponsor, `"grant"` hibe destekçisi, `"tessera"` destekçi.

Robot teknik özellikleri: `CONTENT.robots` içinde `specs` alanlarını doldurun. Boş bırakılan alan sitede "Doğrulanacak" olarak görünür.

## Yayınlamak (GitHub Pages)

1. Depoda **Settings → Pages** bölümüne gidin.
2. **Source** olarak "Deploy from a branch", dal olarak `main` ve klasör olarak `/ (root)` seçin, kaydedin.
3. Bir iki dakika sonra site `https://<kullanıcı-adı>.github.io/<depo-adı>/` adresinde yayında olur. Sonraki her değişiklik birkaç dakika içinde siteye yansır.

## Notlar

- Yalnızca doğrulanmış bilgi yayınlayın; ödül ve sonuçların kaynağı [FRC Events](https://frc-events.firstinspires.org/team/10947).
- Armayı yeniden renklendirmeyin ya da yeniden çizmeyin; her zaman `assets/logo/` içindeki dosyaları kullanın.
- FIRST® ve FIRST® Robotics Competition, FIRST®'ün tescilli markalarıdır.
