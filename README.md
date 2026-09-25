# Acil OtoExport

Fonet Canlı Vizit'in çalışan hasta toplama ve ayrıntı çekme altyapısını temel alan; servis ekranındaki açık hastaları tek seferde tarayıp vizit kağıdını Word veya Google Docs için hazırlayan bağımsız tarayıcı betiği.

## Güvenli kullanım

- Mevcut GitHub dosyasını ve çalışan `window.__FONET_SERVICE_PANEL__` durumunu değiştirmez.
- Kendi `window.__ACIL_OTOEXPORT__` ad alanını kullanır.
- Hasta verisini başka bir sunucuya göndermez; yalnızca açık Fonet oturumundaki istekleri kullanır.
- Gerçek hasta verisi içeren çıktıların yalnızca kurumun yetkili ortamında saklanması gerekir.

## Kullanım

1. `acil-otoexport.js` dosyasını size ait ayrı bir GitHub deposuna koyun.
2. `bookmarklet.txt` içindeki `BURAYA_RAW_GITHUB_URL_YAZILACAK` değerini yeni dosyanın raw GitHub adresiyle değiştirin.
3. Bookmarklet'i Fonet servis hasta listesi açıkken çalıştırın.
4. **Tüm Hastaları Tara** düğmesine basın.
5. **Word İndir** veya **Google Docs'a Hazırla** seçeneğini kullanın.

Google Docs seçeneği biçimli içeriği panoya alır ve yeni bir Google Dokümanı açar. Tarayıcı güvenlik kısıtlaması nedeniyle son yapıştırma işlemi `Ctrl+V` ile yapılır.

## Belge biçimi

- A4, Word/LibreOffice için zorunlu iki sütunlu tablo yerleşimi
- Tahoma
- Belge başlığı: 17 pt
- Hasta başlığı: 15 pt
- Görüntüleme/ana metin: 9 pt
- Order satırı: ilaç adı ve başlangıç tarihi
- Takip: tarihli klinik izlem kayıtları
- Gözlem: en güncel hemşire devir notu
- Tarihli görüntüleme ve konsültasyon bölümleri

## Not

Fonet kurulumları arasında endpoint ve alan adları değişebilir. Görüntüleme listesinin boş kalması halinde kurum sürümündeki RIS liste endpointi `fetchImaging` içindeki adaylara eklenmelidir.
