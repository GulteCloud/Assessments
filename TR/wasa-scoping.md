# Kapsam Belirleme
Kapsam Belirleme bileşeni, bir kapsam belirleme e-postası ve teslimattan en az iki hafta veya daha uzun bir süre önce müşteriyle planlanmış **30 dakika** bir çağrı içerir. Bu aşama, beklentilerin belirlenmesini, ön koşulların karşılanmasını, paydaşların belirlenmesini ve çıktıların net olmasını sağlamak için önemlidir.
Bu aşamadaki önemli bir unsur, müşteri paydaşlarının teslimatın Soru-Cevap kısmı için kullanılabilir olmasını sağlamaktır.  
Kapsam belirleme aşaması:
- Kapsam belirleme e-postası
- Kapsam belirleme çağrısı 
- Azure İzleyici çalışma kitabı önkoşul doğrulaması  
## E-postanın kapsamını belirleme
Kapsam belirleme e-postası, gönderilen teslim kaynağı tarafından birincil müşteri iletişim noktasına, Müşteri Başarısı Hesap Yöneticisi'ne (CSAM), Bulut Çözümü Mimarı'na (CSA) ve Microsoft hesabı ekibine uygun şekilde gönderilir.
Müşteri irtibat noktası, lojistiği, gereksinimleri ve paydaşları koordine etmekten sorumlu temsilci olmalıdır. Genellikle kapsam belirleme e-posta alıcıları, değerlendirmeye katılacak paydaşlardır. Well-Architected Assessment başına ayrı bir e-posta şablonu vardır ve bu şablon ilgili değerlendirmedeki kapsam belirleme klasöründen elde edilebilir [IPKit](https://aka.ms/waf/ipkits).
**Kapsam Belirleme E-posta şablonunu görüntüleyin [burada](https://microsoft.sharepoint.com/:u:/r/teams/ASDIPRelease/IP%20Release/Secure%20Infrastructure/Assessment%20Program/Well-Architected%20Security%20Assessment/3-Scopeping%20Call%20Artifacts/CUSTOMER%20NAME%20Well-Architected%20Security%20Assessment.oft?csf=1&web=1&e=rtfaYP)**
> [! NOT]
> E-posta, kapsam belirleme çağrısı müşteri, CSAM ve teslimat kaynağı ile zamanlanır planlanmaz gönderilmelidir.  İdeal olarak bu, müşteriye kaynak sağlayıcı kaydı için ön koşulları tamamlaması için zaman tanımak amacıyla kapsam belirleme çağrısından birkaç iş günü öncesidir.
Bu e-postanın amacı aşağıdaki gibidir:
- Planlanan kapsam belirleme çağrısının tarihini ve saatini iletir.
- Kapsam belirleme çağrısı için üst düzey bir gündem sağlar.
- Azure İzleyici çalışma kitabı için gereksinimleri karşılamak üzere adım adım dahil olmak üzere teknik gereksinimler sağlar.
## Kapsam Belirleme Çağrısı
Çağrı sırasında teslim kaynağı, teslimat akışını ve hangi konuların gözden geçirileceğini açıklar. Well-Architected Güvenlik Değerlendirmesi, iş yükü güvenliği için aşağıdaki kategorileri kapsar:  
- Uygulama Tasarımı
- Sağlık Modelleme
- Ağ ve Bağlantı
- Güvenlik ve Uyumluluk
- Operasyonel Prosedürler
- Dağıtım ve Test
- Operasyonel Model ve DevOps
- Kimlik ve Erişim Kontrolü
Kapsam belirleme çağrısı, aşağıdaki gibi sorular sormak için bir fırsat sağlar:
- Değerlendirmeden ne bekliyorsunuz?
- Hangi belirli Azure iş yükü değerlendirilecek?
- İlgilenilen belirli konular var mı?
- Yönetici brifingi hedef kitle ve zamanlama
İyi Tasarlanmış Değerlendirmeler, **belirli bir üretim Azure iş yüküne** odaklanır. 'İş yükü' veya 'uygulama', bir veya daha fazla istemciye (insanlar veya sistemler) uçtan uca işlevsellik sağlayan bir kaynak veya kaynak koleksiyonudur. Bunu düşünmenin başka bir yolu; **uçtan uca senaryo** (bir süreç) olarak iş yükü ve bunu destekleyen BT altyapısı. Tek bir uygulama olabilir, belirli bir işlevsellik sunmak için birlikte çalışan birden çok uygulama, API ve veritabanı olabilir**.
**Örnekler:**
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
3. Sonuçları Depolama'da saklar
4. Bir masaüstü uygulaması tarafından erişilir.
5. Yalnızca kuruluştaki kimliği doğrulanmış kullanıcılar için.
Buradaki kılavuz, müşterinin iş açısından kritik bir çalışma durumu iş yükü ve bunun destekleyici kaynaklarını/hizmetlerini (ön kapsam belirleme sırasında henüz tanımlanmamışsa) seçmesini sağlamaktır. Müşteriler güvenlik incelemesi için tek bir iş yükü seçmekte zorlandıklarında ("ancak Azure'da çok fazla uygulamamız var, hangisini seçmeliyiz?"), muhtemelen son ihlallerle birlikte en çok maruz kalan ve hassas olanı veya en temsili olanı seçmeleri önerilir - şirket %90 web uygulamaları çalıştırıyorsa, veri işleme iş yükünü analiz etmek mantıklı değilse,  bunun için belirli bir neden olmadıkça (ihlal).  
> [! ÖNEMLİ]
> Müşteri belirli bir iş yükünü tanımlayamazsa veya tanımlanan iş yükü Azure İzleyici çalışma kitabı tarafından kolayca ortaya çıkarılabilecek şekilde (abonelik, kaynak grubu, etiketler) yapılandırılmamışsa, mevcut iş yükünün kaynak etiketlerini içerecek şekilde değiştirilmesi gerekir. Etiketleme gerekiyorsa Azure Bulut Benimseme Çerçevesi'ndeki [Önerilen adlandırma ve etiketleme kuralları](https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/ready/azure-best-practices/adlandırma ve etiketleme) kılavuzunu izlemeniz önerilir.
> [! NOT]
> İş yükü mimarisi diyagramlarının teslimattan önce paylaşılmasını isteyin.  Diyagramlar, Soru-Cevap tartışmalarında müşteriye liderlik etmek için kullanılabilecek kapsamlı iş yükünün mimarisi hakkında değerli bilgiler içeren teslim kaynağı sağlar.
Kapsam belirleme ve kurulum aşamasının önemli bir bileşeni, müşterinin Azure İzleyici çalışma kitabı için önkoşulları yerine getirmesini sağlamaktır.  
Çağrıya dahil edilecek diğer konular:
- Etkileşim lojistiği  
- Azure İzleyici çalışma kitabı önkoşulları
- İlgilenilen belirli konular
- İş yükü daha önce değerlendirildi mi?
- Müşteri paydaş beklentileri
- Üzerinde anlaşmaya varılan bir iyileştirme uygulama planının temel çıktısı  
| Değerlendirme | Paydaşlar |
|-------|------------|
| İyi Tasarlanmış Güvenlik Değerlendirmesi | Bulut Mimarı, SecOps, IAM, Ağ mühendisliği, Çözüm sahibi, DevOps yöneticisi, Yönetim, risk, uyumluluk yöneticisi |  
>[! Önemli]
> Değerlendirmenin başlangıcında doğru paydaşların hazır bulunması, hem keşif aşamasına verilen yanıtların doğruluğu hem de ulaşılamayan paydaşlar nedeniyle zaman kaybının yaşanmaması açısından önemlidir.
> Kapsam belirleme aşamasında müşteri paydaş beklentilerinin oluşturulması, müşteriye değerlendirme sunumundan çok önce doğru kaynakları sıralama fırsatı sunar.  
> [! NOT]
> Yalnızca kapsam içi aboneliklerde etkinleştirilen Azure Defender aracılığıyla kullanılabilen değerli içgörüler vardır.  Örneğin, güvenlik uyarıları ve mevzuat uyumluluğu panosu raporları yalnızca Azure Defender ile kullanılabilir.  Müşterinin, deneme modunda olsa bile kapsam dahilindeki aboneliklerde Azure Defender'ı etkinleştirmesini teşvik edin.
>[! Önemli]
> Müşterinin, Azure İzleyici Çalışma Kitabı önkoşullarının teslimata girerken yerinde olduğundan emin olması önemlidir. Bu adımın tamamlandığından emin olmak için kapsam belirlemeden sonra ve teslimattan önce müşteri irtibatını e-posta yoluyla takip edin.  

