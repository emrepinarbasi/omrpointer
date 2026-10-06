# OMR PDF Etiketleyici — Android v1.6

OMR PDF Etiketleyici, Türk sanat müziği nota sayfalarında optik müzik tanıma eğitimi için kırmızı sınırlayıcı kutular çizmenizi ve sonuçları eğitim paketi olarak dışa aktarmanızı sağlayan dikey tablet uygulamasıdır.

## Veri kapsamı

- Tamamlanmış ve yeterli kabul edilen 19 sınıf görev listesinden çıkarılmıştır.
- Görsel olarak doğrulanabilen 31 eksik görev bulunmaktadır.
- Her görev için ilgili hedefi içeren 20 farklı TSM eseri seçilmiştir.
- Toplam 620 doğrulanmış görev/PDF eşleşmesi vardır.
- THM, Drive ve sınıflandırılmamış kaynak kullanılmaz.
- Güvenilir 20 eşleşmeye ulaşamayan görevler yanlış örnek göstermemek için listeye alınmaz.

## Kurulum

1. `OMR_Etiketleyici_Eksik_TSM_v1.6.apk` dosyasını Android tabletinize kopyalayın.
2. Android isterse dosya yöneticisi için “Bilinmeyen uygulamaları yükle” iznini açın.
3. APK’yı kurup **OMR Etiketleyici** uygulamasını başlatın.
4. Mevcut bir sürümün üzerine kuruyorsanız uygulamayı kaldırmayın; normal güncelleme ara kayıtları korur.

Android 8.0 veya daha yeni bir sürüm gerekir. Uygulama ve nota ekranları dikey yönde sabitlenmiştir.

## PDF’lerin hazırlanması

Yerel SARC klasörü tanıtılmaz. Bir görevi ilk açtığınızda o göreve ait 20 PDF güvenilir GitHub yayın arşivinden indirilir ve uygulamanın özel önbelleğine alınır. Sonraki açılışlarda indirilen dosyalar yeniden kullanılır.

Uygulama yalnız manifestte kayıtlı GitHub adreslerine bağlanır, gerekli PDF’nin arşivdeki byte aralığını indirir ve dosya özetini doğrular. Etiketler herhangi bir sunucuya yüklenmez.

## Etiketleme

- **KUTU ÇİZ:** Hedef sembolün çevresine kırmızı kutu çizin.
- **Kalem Koruması: AÇIK:** Tek parmak ve avuç içi yok sayılır; kalemle çizim ve iki parmakla yakınlaştırma çalışır.
- **İki parmak:** Sayfayı büyütün, küçültün ve kaydırın.
- **KUTU DÜZELT:** `Mod Değiştir` ile bu moda geçip kutuyu taşıyın veya kenarlarından yeniden boyutlandırın.
- **SAYFAYI TAŞI:** Tek parmakla büyütülmüş sayfayı sürükleyin.
- **Geri Al / Sil:** Son kutu işlemini geri alın.

Araç ve onay düğmeleri ekranın üstündedir. Böylece kalemle sayfanın alt bölümünde çalışırken elinizin düğmelere istemeden basma riski azalır. Her kutu ve düzeltme anında ara kaydedilir.

## PDF’ler arasında geri dönme

- **Önceki PDF** ve **Sonraki PDF** düğmeleriyle görevdeki 20 eser arasında gezebilirsiniz.
- Tamamlanan bir PDF tekrar açıldığında başlıkta `✓ onaylandı` görünür.
- Önceden çizilmiş kutular ara kayıttan yüklenir ve yeniden düzenlenebilir.
- `PDF’yi Tamamla` veya `Bu PDF’de Hedef Yok` ile durum tekrar değiştirilebilir.

## Görevi bitirme ve ZIP alma

1. PDF’deki bütün hedefleri kutuladıktan sonra **PDF’yi Tamamla ✓** düğmesine basın.
2. Hedef gerçekten yoksa **Bu PDF’de Hedef Yok** düğmesini kullanın.
3. Görev bitince **ZIP** düğmesiyle eğitim paketini kaydedin.

ZIP paketi temiz sayfa görüntülerini, hedef kırpımlarını, kutu koordinatlarını, COCO JSON ve CSV verilerini içerir. Kırmızı çerçeveler temiz eğitim görüntülerine yakılmaz.

## Android Studio’da açma

1. `OMR_Etiketleyici_Android_Studio_v1.6.zip` dosyasını açın.
2. Android Studio’da **Open** ile `omr_android_annotator` klasörünü seçin.
3. Gradle eşitlemesinin tamamlanmasını bekleyin.
4. Bağlı cihazda çalıştırın veya `./gradlew assembleDebug` komutuyla APK oluşturun.

## Teknik bilgiler

- Paket adı: `com.emrepinarbasi.omretiketleyici`
- Sürüm: `1.6` (`versionCode 8`)
- En düşük Android sürümü: API 26 / Android 8.0
- Hedef Android sürümü: API 37
- Ağ kaynağı: GitHub yayın varlıkları
- Veri: 31 görev × 20 farklı TSM eseri = 620 eşleşme
