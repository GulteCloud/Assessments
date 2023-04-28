# Değerlendirme
Değerlendirme aşaması Discovery &; Insights olarak da adlandırılır. Bu aşama, bir dizi müşteri görüşmesine, iş yükü içgörülerine ve (uygun olduğunda) beyaz tahta oturumlarına liderlik ederek Microsoft teslim kaynaklarının çeşitli Azure kritik alanlarından içgörüler elde etmek için müşterilerle nasıl etkileşim kurduğunu standartlaştırmak üzere tasarlanmıştır. İyi Tasarlanmış Değerlendirmeler, belirli bir Azure iş yükünü hedefler ve çerçevenin belirli kiracısındaki belirli kritik alanlara (maliyet, güvenilirlik, işlemler, güvenlik) odaklanarak ortak bir teslim yaklaşımını paylaşır.
Görüşme oturumlarına ek olarak, Microsoft teslim kaynakları, kapsam dahilindeki iş yükü için müşteri güçlü yönleri ve iyileştirme alanları hakkında kritik içgörüler elde etmek üzere Azure İzleyici güvenlik çalışma kitabı şablonunu ve uygun olabilecek diğer araçları kullanır.
Discovery & Insights tesliminin sonunda, Microsoft teslim kaynakları, belirlenen önerilere ve iyileştirmelere (uyum/boşluk analizi) dayalı olarak gelecekteki çalışmalar için etkinliklerin bir iyileştirme planını oluşturur.
## **Etkileşim Başlangıcı**
Değerlendirmenin başlangıcı şunları içermelidir:  
- Yuvarlak masa tanıtımları
- Katılımcıların teslimat akışı, lojistik, beklentiler, ilgilenilen özel konular ve teslimatlar konusunda net olmalarını sağlamak için kapsam belirleme çağrısının bölümlerini yeniden karma hale getirin  
- Müşteri, Azure'daki amacını ve mimarisini anlamak için CE'ye kapsamlı iş yüküne genel bir bakış sağlamalıdır  
- Azure İzleyici çalışma kitabı dağıtımı ve filtreleme
 Aşağıdaki etkinlikler için arka plan olarak [IPKit](https://aka.ms/waf/wasa)'deki 'Well-Architected Security Assessment - Kickoff.pptx destesini kullanın.
### **Yuvarlak Masa Tanıtımları**
Değerlendirme aşamasının başında, kendinizi, atanan CSA'yı ve CSAM'yi tanıtarak katılımı başlatın. BT operasyonlarının hangi yönünden kimin sorumlu olduğunu ve değerlendirilen iş yükünü anlamak için müşteri paydaşlarından tanıtımlar isteyin.  Çağrıdaki müşteri paydaşlarının sayısına dikkat edin ve gerekirse zaman uğruna bu tanıtımlardan vazgeçin.
### **Kapsam belirleme çağrısının bölümlerini yeniden karma hale getirme**
Katılımcıların teslimat akışı, lojistik, beklentiler, ilgilenilen özel konular ve çıktılar konusunda net olmalarını sağlamak için kapsam belirleme çağrısının bölümlerini yeniden karma hale getirmek için kısa bir süre harcayın. Bu aynı zamanda Soru-Cevap bölümüne yanıt vermek için gereken beklenen müşteri paydaşlarını yinelemek için bir fırsattır.
### **(İsteğe bağlı) İyi Tasarlanmış Çerçeveye Genel Bakış**
WAF'ye, WAF'nin güvenlik ayağına ve bu değerlendirmenin kılavuzuna nasıl uyum sağladığına genel bir bakış sağlamak için bir dizi slayt sağlanmıştır. Müşteriyi WAF güvenliğinin teori ve tasarım ilkelerine dayandırmak için kısa bir süre harcamayı düşünün. WAF'nin iş yükü mimarisine odaklanan içten dışa bir mercek olduğunu ve bir iş yükünün ne kadar iyi tasarlandığına dair hikayenin tek parçası olduğunu öğretin.
### **(İsteğe bağlı) Kurumsal Ölçek / Giriş Bölgelerine Genel Bakış**
Kurumsal ölçekli giriş bölgelerine genel bir bakış sağlamak için bir dizi slayt sağlanmıştır. WAF/CAF ve iş yükü mimarisi (Kurumsal Ölçek) için iniş bölgelerinin rolü ve önemi konusunda müşteriyi dışarıdan içeri mercek altına almak için kısa bir süre harcamayı düşünün. Bu bölüm, ankette müşterinin incelenen iş yükü için giriş bölgesi tasarlayıp tasarlamadığı ve dağıtıp dağıtmadığı sorusu ortaya çıktığında bağlam verecektir.
### **İş Yüküne Genel Bakış**
Müşteri, Azure'daki amacını ve mimarisini anlamak için CE'ye kapsamlı iş yüküne genel bir bakış sağlamalıdır. Paylaşılan mimari belgeyi açmak için zaman ayırın (uygulama amacını, mimariyi, kimlik doğrulamasını ve veri akışlarını anlamak için bir tane varsa). Kapsamlı uygulama/iş yükü hakkında bilgi edinmek için sorular sorun ve uygun olduğu şekilde not alın. Müşteri bir mimari diyagram sağlayamıyorsa, iş yükü tasarımını onlarla birlikte beyaz tahta yapmayı düşünün (yüksek düzey).
### **Azure İzleyici çalışma kitabı dağıtımı ve filtreleme**
Bu değerlendirmenin bir parçası olarak, WAF Güvenliği çalışma kitabının dağıtılması gerekir. Müşteriyi, rapor sayfalarını filtreleyerek kapsamlı iş yükünü sıfıra indirmeye yönlendirin. Bu, iş yükünün kaynaklar, kaynak grupları ve abonelikler arasında nasıl tasarlandığına bağlı olacaktır. Danışman ve Bulut için Microsoft Defender tarafından sunulan önerilerin kapsam dahilindeki iş yüküne yönelik olduğundan emin olmak için kaynak etiketleme üzerinde filtreleme yapılması gerekebilir.  
#### Çalışma Kitabı Önkoşulları
Aşağıdaki Azure kaynak sağlayıcılarının kapsam içi aboneliklere kayıtlı olması gerekir:
- Microsoft.Advisor
- Microsoft.ResourceHealth  
- Microsoft.Güvenlik  
Tüm kapsam içi aboneliklere veya bunların üst yönetim grubuna atanmış Yerleşik Okuyucu rolüne sahip bir bulut hesabı.  
[İsteğe bağlı] Çalışma kitabını şablondan kaydetmek için Katkıda Bulunan rolünü izleyin.  
> [! NOT]
> Çalışma kitabının kaydedilmesi, ortaya çıkardığı içgörüleri görüntülemek ve dışa aktarmak için gerekli değildir. Müşteri çalışma kitabını post engagement özelliğini kullanmaya devam etmek istiyorsa çalışma kitabını şablondan kaydetmek için Katkıda Bulunan rolünü izleyin.
#### Çalışma Kitabı Dağıtım Kılavuzu
Çalışma kitabını Azure İzleyici'ye dağıtmak için aşağıdaki kaynaklar kullanılabilir:
- [JSON Dağıtım kılavuzu](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/workbooks-automate#azure-resource-manager-template-for-deploying-a-workbook-in) - **JSON Şablonu** kullanarak çalışma kitapları oluşturma kılavuzu.
- [ARM Şablonu Dağıtım Kılavuzu](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/workbooks-automate#azure-resource-manager-template-for-deploying-a-workbook-instance) - Çalışma kitabını **ARM Şablonu** olarak dağıtma kılavuzu.
- [Security WorkBook.json](https://microsoft.sharepoint.com/teams/ASDIPRelease/IP%20Release/Forms/AllItems.aspx?viewid=971b6985%2D5ac6%2D47e5%2Da6dc%2D5c0664b149a9&id=%2Fteams%2FASDIPRelease%2FIP%20Release%2FSecure%20Infrastructure%2FAssessment%20Program%2FWell%2DArchitected%20Security%20Assessment%2F4%2DDelivery%20Artifacts%2F1%2DAzureMonitorWorkbook) - Bu çalışma kitabında Bulut ve Azure için Microsoft Defender'dan güvenlikle ilgili çeşitli ayrıntılar sunulacaktır Danışman.
#### İsteğe Bağlı Ağ Güvenliği Panosu Çalışma Kitabı
IPKit ayrıca GitHub'daki [Ağ Güvenlik Panosu](https://aka.ms/DeployNetSecWorkbook) çalışma kitabına bir bağlantı içerir. Bu ek çalışma kitabı, ağ ile ilgili iş yükü kaynakları hakkında ek içgörüler elde etmek için kullanılabilir. Ancak, bu çalışma kitabı **WASA Güvenliği çalışma kitabı gibi filtreleme özellikleri sağlamaz**. Kullanmaya karar verirseniz, **yalnızca kapsamdaki iş yükü kaynaklarına odaklandığınızdan emin olun**. Bu çalışma kitabı müşteri için ek değer ve fayda sağlayabilir.
## Azure İyi Tasarlanmış İnceleme Anketi
İş yükünüzü güvenlik ayağının merceklerinden inceleyin. Değerlendirmeyi gerçekleştirmek için lütfen [Azure İyi Tasarlanmış İnceleme](https://docs.microsoft.com/assessments) web sitesini ziyaret edin.
Görüşmeler, temel amacın kapsamlı Azure iş yükü için müşteriden mümkün olduğunca fazla bilgi ve içgörü elde etmek olduğu etkileşimin kritik bir parçasıdır. Azure İyi Tasarlanmış İnceleme için zengin ve anlamlı yanıtlar toplamak üzere doğru yanıtları sağlamak üzere doğru müşteri paydaşlarına sahip olmak önemlidir.
Bu müşteri görüşmelerinin ruhu, diğer birçok önemli ayrıntıyı kaçırabilecek ikili cevaplar almak için bir sürü soru sormaya çalışmak yerine, kritik alanların her biri hakkında açık konuşmalar yapmaktır. Güçlü yönleri, zorlukları ve fırsatları belirlemeye çalışın.
Değerlendirme sorularını/seçimlerini sadece satır satır okumayın. Onlara sözlerinizle sorun. Bunları örneklerle genişletin, bu sorunun neden önemli olduğu ve etkisinin ne olduğu konusunda bağlam ve arka plan bilgileri sağlayın. Müşterinin Azure iş yükünün ayrıntılarını konuşması ve paylaşması için açık uçlu sorular sorun. Müşteriyi, açıklamalarını görselleştirmek için beyaz tahtayı kullanmaya teşvik edin.
Alınması zor ve kolay kararlar arayın – her iki uç nokta da örgütsel sorunların sonucu olabilir. Konuları zaman kutusuna koyduğunuzdan emin olun ve zorlu tartışmalar için 'otopark' kullanın.
> [! NOT]
> Bir soruyu cevaplamak için gerekli paydaşın müsait olmadığı ve teslimatın bir soruya cevap vermeden devam ettiği durumlar olabilir. Anketi göndermeden önce tüm soruların yanıtlandığından emin olun.  
### Değerlendirmeyi gerçekleştirin ve csv raporunu oluşturun
- [Azure Well-Architected Review](https://docs.microsoft.com/assessments) web sitesine gidin.
- İstendiğinde, B2B hesabınızla (varsa) giriş yapın veya müşterinin kimlik bilgileriyle giriş yapmasını sağlayın. Henüz mevcut değilse bir hesap oluşturmanız gerekebilir.
- Oturum açtıktan sonra, kullanılabilir değerlendirmeler altında Azure İyi Tasarlanmış İnceleme'yi seçin.
- Bunu yaptıktan sonra, size 2 seçenek sunulacak - Yeni bir değerlendirme oluşturun veya bir kilometre taşı oluşturun. Yeni değerlendirme oluştur'u seçin.
- Değerlendirmeye uygun bir ad verin veya sağlanan varsayılan adla devam edin.
- [İsteğe bağlı - **aşağıdaki önemli açıklamaya bakın**] Azure Danışmanı bölümünde, Azure kimlik bilgileriyle oturum açın ve Well-Architected incelemesi için kapsamdaki Azure aboneliklerini seçin. Bu adımı yalnızca bir Azure aboneliğindeki tüm Azure Danışmanı önerilerini raporlara dahil etmek istiyorsanız gerçekleştirin.
- Güvenlik sütununu seçin.
- Her bölümde ve bölüm içinde sunulan seçeneklerde müşteri ile zaman geçirin. Bu tartışmadaki ilgili notları aşağıdaki not metin kutusundan yakalayabilirsiniz. (Bu notlar henüz raporlarda gösterilmediğinden bu notları OneNote'ta veya başka bir sistemde yakalamaya çalışın)
- Değerlendirmeyi gönderdikten sonra, değerlendirme sonuçları ve puanları size sunulacaktır.
- Değerlendirme için csv raporunu indirmek üzere CSV'ye Aktar seçeneğini bulun.
> [! NOT]
> Müşteriyle her öneriye girmek için yeterli zaman olmayabilir, bu nedenle her kategoride kaç önerinin gözden geçirileceği ve açıklama ekleneceği konusunda takdirinizi kullanın.
> [! ÖNEMLİ]
> Azure Danışmanı tümleştirmesi, Azure ticari bulut kiracı hesapları **yalnızca** için desteklenir ve önerilerin CSV çıktı raporuna otomatik olarak eklenmesiyle teslimatın raporlama bölümüne verimlilik getirebilir. Bu tümleştirme yalnızca, bu tümleştirme özelliğindeki sınırlı filtreleme kaldıraçları kullanılarak iş yükü kapsamı başarıyla filtrelenebildiğinde dikkate alınmalıdır.  
## İçgörüler Günü 1-2
İçgörüler Günleri, Microsoft kaynağının ve müşterinin hem Azure İyi Tasarlanmış İnceleme'den hem de Azure İzleyici güvenlik çalışma kitabından içgörüleri incelemesi için yeterli zaman sağlamayı amaçlamaktadır.  İyi tasarlanmış her değerlendirmenin, Microsoft Azure İyi Tasarlanmış Çerçeve'deki belirli kiracıyla hizalanmış kendi kritik odak alanları vardır. Aşağıdaki alt bölümlerde, başarılı bir teslimat sağlamak için keşif ve öngörü günleri hakkında daha ayrıntılı bilgi verilmektedir.
### Keşfedilen Veri Analizi
Öngörüler aşamasının bir parçası olarak ilk etkinlik, Azure İyi Tasarlanmış İnceleme'den toplanan verileri analiz etmektir. Azure İyi Tasarlanmış Gözden Geçirme değerlendirme sonuçları, iyileştirme fırsatlarını tanımlamak için yapılandırılmış ve düzenlenmiştir ve CSV dışarı aktarma işleminde kategorilere ayrılmıştır. Her kategori, elde edilen puana göre sıralanır. Her bir öneriyi müşteriye ve belirlenen sorunları hafifletmeye nasıl devam etmeleri gerektiğini açıklayın.
Bir öneri bir Azure güvenlik çözümünün (ör. Bulut için Microsoft Defender, Azure İlkesi, Azure Blueprints, Azure Güvenlik Duvarı, Web Uygulaması Güvenlik Duvarı vb.) etkinleştirilmesini içeriyorsa, müşterinin iş yükü güvenliğini artırmadaki değerini ve yerini anlamasını sağlamak için bu teknolojileri ve özellikleri tanıtmak veya göstermek için zaman ayırın.
## Azure İzleyici Güvenlik Çalışma Kitabı
Azure İzleyici güvenlik çalışma kitabı dağıtımı ve iş yükü filtreleme başlangıç oturumunda tamamlanmış olmalıdır.  Müşteriyle birlikte gözden geçirilecek birden çok rapor sayfası vardır. Teslim kaynağı, değerlendirme için en alakalı içgörüleri içeren panolara ve rapor sayfalarına odaklanmalıdır.
Çalışma kitabı, bu değerlendirme için önemli bilgiler sağlayan aşağıdaki sayfaları içerir:
#### Güvenlik ve Uyumluluk
- Genel güvenlik puanını ve abonelik güvenlik puanını gözden geçirin.
- Güvenlik puanının nasıl hesaplandığını açıklayın [Bulut için Microsoft Defender'da güvenlik puanı | Microsoft Docs](https://docs.microsoft.com/en-us/azure/defender-for-cloud/secure-score-security-controls).
- Her kontrol alanını ve her kontrol alanı için dahil edilen politikalara karşı kaynak uyumluluğunu gözden geçirin.
- Önerilerden kontrol alanlarına olan bağlantıyı ve bunların güvenlik puanı üzerindeki etkilerini gözden geçirin, paylaşın, tartışın. [Güvenlik kontrolleri ve önerileri | Microsoft Docs](https://docs.microsoft.com/en-us/azure/defender-for-cloud/secure-score-security-controls#security-controls-and-their-suggestations).
- Soru-Cevap oturumu ve raporlama için içgörüleri dışa aktarın.
#### Bulut Uyarıları için Microsoft Defender
Uyarılar, kapsam içi aboneliklerde Microsoft Cloud Defender'ın etkinleştirilmesini gerektirir.
- Aktif uyarılarla her grubu ve kaynağı gözden geçirin.
- İş yükündeki kaynaklara karşı uyarıları gözden geçirin, paylaşın, tartışın. [Uyarılar Referansı] (https://docs.microsoft.com/en-us/azure/defender-for-cloud/alerts-reference).
- Soru-Cevap ve raporlama için uyarıları dışa aktarın.
#### Mevzuat Güvenliği ve Uyumluluğu
Denetim Çerçeveleri, Azure-Security-Benchmark dışında bu denetim çerçevelerinin eklenebilmesi için Microsoft Cloud Defender'ın kapsam içi aboneliklerde etkinleştirilmesini gerektirir.  
- İş yüküyle ilgili her uyumluluk standardını gözden geçirin.
- İş yükündeki kaynaklar için mevzuat uyumluluğunu gözden geçirin, paylaşın, tartışın [Öğretici: Mevzuat uyumluluğunuzu geliştirme](https://docs.microsoft.com/en-us/azure/defender-for-cloud/regulatory-compliance-dashboard).
#### Danışman
- Danışman sayfasının, güvenli puan kontrol alanlarının bir parçası olup olmadıklarına bakılmaksızın tüm aktif önerilerin tam envanterine sahip olduğunu açıklayın.
- Güvenlik ve uyumluluk sayfasında yer almayan önerileri gözden geçirin, paylaşın, tartışın.
- Soru-Cevap oturumu ve raporlama için içgörüleri dışa aktarın.

