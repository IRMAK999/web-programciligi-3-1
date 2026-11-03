# Hafta 1 - Git ve GitHub

## Araştırma

**Git nedir?** Yazdığımız kodun zaman içindeki değişikliklerini kaydeden bir sürüm kontrol sistemidir. Bilgisayarımızda çalışır. Bir şeyi bozarsak eski haline dönebiliriz, kimin ne zaman ne değiştirdiğini görebiliriz.

**GitHub nedir?** Git ile tutulan projelerin internette saklandığı bir platformdur. Kodu yedeklemek, başkalarıyla ortak çalışmak ve projeyi paylaşmak için kullanılır.

**Git ile GitHub arasındaki fark:** Git bir araçtır (program), GitHub ise bu aracı kullanan bir internet sitesidir. Git'i GitHub olmadan da kullanabiliriz ama GitHub'ı Git olmadan kullanamayız.

**Repository (repo):** Projenin klasörü ve geçmişinin tutulduğu yerdir. Bilgisayarımızda (local) ve GitHub'da (remote) bulunabilir.

**Commit:** Yaptığımız değişikliklerin bir mesajla birlikte kaydedilmesidir. Oyundaki kayıt noktası gibi düşünülebilir.

**Branch:** Ana koddan ayrılıp bağımsız bir kolda çalışmaktır. Yeni bir özelliği ana kodu bozmadan denemek için kullanılır.

**Merge:** Ayrı branch'te yapılan değişikliklerin başka bir branch ile (genelde main) birleştirilmesidir.

**Clone:** GitHub'daki bir reponun bilgisayarımıza tüm geçmişiyle kopyalanmasıdır (`git clone adres`).

**Pull:** GitHub'daki yeni değişiklikleri bilgisayarımıza çekmektir (`git pull`).

**Push:** Bilgisayarımızdaki commit'leri GitHub'a göndermektir (`git push`).

**.gitignore:** Git'in takip etmemesini istediğimiz dosya ve klasörleri yazdığımız dosyadır. Örneğin `node_modules/` ve şifre içeren `.env` dosyaları buraya yazılır, böylece GitHub'a yüklenmez.

**Hangi problemi çözüyor?** Dosya adları `proje_son`, `proje_son2` gibi karışmaz. Birden fazla kişi aynı projede çalışırken kodlar birbirinin üzerine yazılmaz. Hata olursa eski sürüme dönülebilir.

**Avantajları:** Ücretsizdir, geçmiş tutulur, ekip çalışmasına uygundur. **Dezavantajları:** Başlangıçta komutları öğrenmek zor gelebilir, birleştirirken çakışma (conflict) çıkabilir.

**Alternatifler:** GitLab ve Bitbucket (platform olarak), SVN ve Mercurial (sürüm kontrol sistemi olarak).

## Sektörde Kullanımı

Yazılım şirketlerinin neredeyse hepsi Git kullanır. Ekipler genelde main branch'ini korur, her yeni özellik için ayrı branch açar ve Pull Request ile kod incelemesinden sonra birleştirir. Ayrıca otomatik test ve yayına alma (CI/CD) işleri de GitHub üzerinden yürütülür.

## İncelediğim Projeler

Not: Commit ve katkıcı sayıları yaklaşık değerlerdir, GitHub'daki güncel sayı biraz farklı olabilir.

### 1. Express

- **GitHub adresi:** https://github.com/expressjs/express
- **Dil:** JavaScript (Node.js)
- **Framework:** Kendisi Node.js için bir web framework'üdür
- **Amacı:** Web sitesi ve API yazmak için hızlı ve sade bir altyapı sunmak
- **Yaklaşık commit:** ~5.500
- **Contributor:** ~350
- **Klasör yapısı:** `lib/` (asıl kodlar), `test/`, `examples/`, `benchmarks/`, `package.json`, `History.md`, `LICENSE`
- **README yapısı:** Kısa tanıtım, kurulum, küçük örnek kod, dokümantasyon linkleri, katkı yapma ve lisans
- **Dikkatimi çeken:** README kısa tutulmuş, detaylar ayrı dokümantasyon sitesine bırakılmış.

### 2. Bootstrap

- **GitHub adresi:** https://github.com/twbs/bootstrap
- **Dil:** JavaScript, SCSS, HTML
- **Framework:** Kendisi bir CSS/JS framework'üdür
- **Amacı:** Mobil uyumlu sayfaları hazır bileşenlerle hızlı yapmak
- **Yaklaşık commit:** ~18.500
- **Contributor:** ~1.600
- **Klasör yapısı:** `scss/` (stiller), `js/` (bileşenler), `site/` (dokümantasyon sitesi), `dist/` (derlenmiş dosyalar), `.github/`
- **README yapısı:** Hızlı başlangıç, pakette neler var, hata bildirimi, dokümantasyon, katkı yapma, topluluk, sürümleme ve lisans
- **Dikkatimi çeken:** Katkı kuralları ve davranış kuralları ayrı dosyalarda yazılmış, büyük proje düzenli yönetiliyor.

### 3. Vue.js (Vue 3)

- **GitHub adresi:** https://github.com/vuejs/core
- **Dil:** TypeScript
- **Framework:** Kendisi bir JavaScript framework'üdür
- **Amacı:** Kullanıcı arayüzlerini bileşenlerle geliştirmek
- **Yaklaşık commit:** ~6.400
- **Contributor:** ~550
- **Klasör yapısı:** `packages/` (reactivity, compiler gibi ayrı paketler), `scripts/`, `.github/`, `package.json`
- **README yapısı:** Kısa tanıtım, sponsorlar, hata bildirimi, katkı ve lisans
- **Dikkatimi çeken:** Proje tek parça değil, `packages/` içinde küçük paketlere bölünmüş.

## Yaptığım Uygulama

`ornek-proje` klasöründe HTML ve CSS ile iki sayfalık küçük bir kulüp sitesi hazırladım (ana sayfa, menü ve iletişim sayfası). Proje 7 anlamlı commit ile ilerledi.

## Karşılaştığım Problemler

- GitHub'da dosya oluştururken klasör yolunu doğru yazmak ilk başta zor geldi.
- Mevcut bir dosyayı düzenleyip commit etmeyi öğrenmem gerekti.

## Öğrendiklerim

Git'in sadece yedekleme aracı olmadığını, değişikliklerin adım adım ve anlamlı mesajlarla kaydedilmesi gerektiğini öğrendim. Büyük projelerin README ve klasör düzenine önem verdiğini gördüm. Git ile GitHub'ın aynı şey olmadığını da netleştirdim.

## Kaynaklar

- Git dokümantasyonu: https://git-scm.com/doc
- GitHub Docs: https://docs.github.com
- Express: https://github.com/expressjs/express
- Bootstrap: https://github.com/twbs/bootstrap
- Vue.js: https://github.com/vuejs/core
