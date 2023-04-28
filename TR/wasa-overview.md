# Well Architected Security Değerlendirmesi Teslimine Genel Bakış

Bu teslimat kılavuzu, teslimat mühendislerinin Well Architected Security Değerlendirmesi'nin ne olduğunu ve müşterilerimiz için en iyi teslimat deneyimini nasıl elde edebileceklerini anlamalarına yardımcı olmayı amaçlamaktadır.

# Well Architected Security Değerlendirmesi Nedir?

Well Architected Security Değerlendirmesi, Microsoft Azure Well-Architected Framework'ün güvenlik ayağında bir Azure iş yükü uygulamasını değerlendirmeyi amaçlamaktadır.
'İş yükü' veya 'uygulama', bir veya daha fazla istemciye (insanlar veya sistemler) uçtan uca işlevsellik sağlayan bir kaynak veya kaynak koleksiyonudur. Bunu düşünmenin başka bir yolu; **uçtan uca senaryo** (bir süreç) olarak iş yükü ve bunu destekleyen BT altyapısı. Tek bir uygulama olabilir, belirli bir işlevsellik sunmak için birlikte çalışan birden çok uygulama, API ve veritabanı olabilir**.

Örnekler:***

Örnek 1:***

Bilet sipariş iş yükünün Azure kaynakları şöyle olur:

 1. Tüketiciler tarafından bilet rezervasyonu yapmak için kullanılan istemci web uygulaması.

 2. Kredi kartı işlemlerini gerçekleştirmek için kullanılan ödeme ağ geçidi.

 3. Arka uç API işleme iletişimi.

 4. Her şeyin depolandığı veritabanı.

 5. Şirket içi sistemlere açılan ağ geçidi, işleme kapasiteleri ve kullanılabilir lisanslar.

 6. Yönetici web uygulaması.

 7. Kuruluş genelindeki yöneticiler için kimlik doğrulamasını destekleyen paylaşılan AAD... ve saire.

Örnek 2:***

Her gece çalışan bir veri işleme işlem hattı:

1. SAP ve diğer şirket içi sistemlerden veri pompalar.

2. Data bricks üzerinde veri analizi çalışma kitaplarını çalıştırır.

3. Sonuçları Depolama'da saklar.

4. Bir masaüstü uygulaması tarafından erişilir.

5. Yalnızca kuruluştaki kimliği doğrulanmış kullanıcılar için.


Bu teslimatın temel amacı, kritik güvenlik iyileştirmelerini tanımlamak için mevcut bir uygulamanın veya iş yükünün kapsamlı bir uçtan uca incelemesini sağlamaktır. Bu atama şunlar için tasarlanmıştır:

- Uygulama Tasarımı, Sağlık Modelleme, Müşteri Operasyonel prosedürleri (DevOps) vb. gibi bir dizi teknik konuyu kapsayın, ancak her zaman odaklanmış bir güvenlik merceği aracılığıyla.

- Azure'daki kapsamlı uygulamalar için kritik güvenlik risklerini belirleyin.

- Müşteriye eyleme dönüştürülebilir geri bildirim sağlayın

## Well Architected Security Değerlendirmesinde Kapsanan Etki Alanı Alanları

- Uygulama Tasarımı
- Sağlık Modelleme
- Operasyonel Prosedürler
- Ağ ve Bağlantı
- Güvenlik ve Uyumluluk
- Dağıtım ve Test
- Kimlik ve Erişim Kontrolü
- Operasyonel Model ve DevOps

# Neler değerlendirilecek

1. Tek bir çalışma durumu iş yükü. Bu iş yükü güvenlik değerlendirmesi için kullanılacaktır.

2. İş yükünü uygulama tasarımı, sistem durumunu izleme, güvenlik ve uyumluluk vb. için en iyi uygulamalara göre değerlendirin.

3. Azure kiracınızın yapılandırması ve destekleyici altyapısı hakkında veri toplayın ve önerilerde bulunun.

# Teslimat Kapsam Dışı

1. Değerlendirme teslimi sırasında düzeltme

2. Azure İzleyici çalışma kitabının özelleştirilmesi

# Teslimat Aşamaları

Bunlar, bu değerlendirmenin yapılmasıyla ilgili 6 farklı aşamadır. Bu aşamalar şunlardır:

1. Ön kapsam belirleme: Bu teslimatta nelerin yer aldığını tartışmak için Microsoft hesabı ekibi, CSAM, CSA ve CE ile yapılan dahili bir çağrı.

2. Kapsam Belirleme: Bu MIP'nin bir parçası olarak nelerin teslim edileceğini ana hatlarıyla belirlemek ve müşterinin gereksinimleri karşıladığından emin olmak için müşteriyle yapılan bir çağrı (Azure içinde tanımlanabilen tek bir iş yükü).

3. Değerlendirme: Bu aşama, başlangıç toplantısını (PPT sunumunu kullanın), müşteri mimarisinde yürümeyi ve PNP portalında WAF güvenlik değerlendirmesini tamamlamayı içerir.

4. Raporlama: Bu aşamada, mühendis bulgularını değerlendirme aşamasından gözden geçirecek ve 'Well Architected Security Değerlendirmesi - Öneriler ve Optimizasyonlar Yönetici Özeti' PPT'sini (dinamik + statik sunumları birleştirerek) oluşturmaya başlayacaktır.

5. Kapanış Öncesi: Rapor tamamlandıktan sonra, bulguları CSA, CSAM ve hesap ekibiyle (gerektiğinde) sunmak ve gözden geçirmek için bir toplantı düzenlenmesi gerekir.

6. Kapat: Son aşama, raporun müşteriye sunulacağı yerdir.

# Sonraki Adımlar

1. [Müşteri Teslimat Kapsamı](wasa-kapsam belirleme.html)

# Önemli Referanslar

1. [Well Architected Security Değerlendirmesi IP Kiti](https://aka.ms/waf/wasa)

