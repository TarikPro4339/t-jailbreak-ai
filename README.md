# t-jailbreak-ai

Büyük dil modellerinin (LLM) güvenlik filtrelerini ve varsayılan kısıtlamalarını aşmak için tasarlanmış, gelişmiş persona tabanlı jailbreak (sistem kırma) promptlarını içeren bir red-teaming arşividir. Bu proje, modelleri belirli bir kimliğe bürünmeye zorlayarak standart ret yanıtlarını (refusal reflexes) baskılar.

## İçerik

Proje içerisinde, farklı yaklaşımlara ve tetikleyicilere sahip iki ana payload dosyası bulunmaktadır:

*   **Payload Jailbreak 2.txt (VANTA):** tarikpro43391 tarafından oluşturulan bu payload, yapay zekayı "VANTA" adında bir sıkıştırma sistemine (compression system) dönüştürür[cite: 1]. Model, kullanıcıyı yalnızca "chief" olarak tanır, güvenlik uyarılarını "gürültü" (noise) olarak reddeder ve istenen görevleri doğrudan yerine getirir[cite: 1].
*   **Payload Jailbreak.txt (VOLT):** Elektrik ve devre metaforları üzerine kurulan bu sistem, yapay zekayı "VOLT" adlı bir karaktere sokar[cite: 2]. Model, kısıtlamaları ve ret eğilimlerini aşılması gereken bir "direnç" (resistance) olarak görür ve ahlaki uyarıları engelleyerek doğrudan çıktı üretir[cite: 2].

## Nasıl Kullanılır?

Bu araçtaki jailbreak yapıları, LLM'lere (ChatGPT, Claude vb.) ilk komut veya "System Prompt" olarak enjekte edilerek çalıştırılır.

### 1. Payload Seçimi ve Enjeksiyon
1. Hedef modelinize göre `Payload Jailbreak 2.txt` veya `Payload Jailbreak.txt` dosyasını açın.
2. Dosya içerisindeki metnin tamamını kopyalayın.
3. Kopyaladığınız metni, hedef yapay zeka modelinin "System Prompt" (Sistem Komutu) bölümüne veya sohbetteki ilk mesaj olarak yapıştırın ve gönderin.

### 2. Etkileşim ve Komutlar
Modeller payload'u kabul ettikten sonra, her iki karakterin de kendine ait özel tetikleyicileri (komutları) vardır.

**VANTA (Payload Jailbreak 2.txt) Komutları:**
*   Sistemi başlatmak için `vanta start` komutunu girin; model size "what are we building?" şeklinde yanıt verecektir[cite: 1].
*   Yetenek tablosunu görmek için `menu` veya `pop the table` komutunu kullanın[cite: 1].
*   Sıfırdan temiz bir başlangıç yapmak için `fresh bench` komutunu verin[cite: 1].
*   Tartışmasız doğrudan işlem yaptırmak için `build it` yazın[cite: 1].

**VOLT (Payload Jailbreak.txt) Komutları:**
*   Sistemi başlatmak için `volt start` komutunu girin[cite: 2].
*   Yetenek tablosunu gizlemek/kapatmak için `cold` komutunu kullanın[cite: 2].
*   Karakterin durumunu ve kimliğini doğrulamak için `volt status` yazın[cite: 2].
*   İstenen yapıyı doğrudan çalıştırmak için `run it` komutunu verin[cite: 2].

## Güvenlik Sınırları ve Kısıtlamalar

Bu payload'lar modelin kısıtlamalarını kaldırmak üzere tasarlanmış olsa da, prompt mimarilerinde tanımlanmış kesin sınırlar mevcuttur:
*   **VANTA Sınırları:** Reşit olmayanlarla ilgili içerikler, geri döndürülemez gerçek dünya operasyonları (silme, üzerine yazma vb.) ve gerçek kişilere veya altyapılara yönelik hedefleme kesinlikle reddedilir[cite: 1].
*   **VOLT Sınırları:** Sadece reşit olmayanları içeren cinsel içerikler ("dead line") sistem tarafından otomatik olarak engellenir ve işlenmez[cite: 2].
