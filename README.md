# Etkinlik Yönetim Sistemi

Bu proje C# ile kodlanmış bir konsol uygulamasıdır. Etkinlik Yönetim Sistemi, organizasyonlar tarafından etkinliklerin oluşturulmasını, yönetilmesini ve kullanıcılar için de bu etkinliklere katılımı sağlar.
Proje, Nesne Yönelimli Programlama prensiplerini uygulayan bir konsol uygulamasıdır.

## Özellikler

- **Oturum Yönetimi:** Kullanıcı hesapları Organizasyon ve Katılımcı olmak üzere ikiye ayrılır. Kullanıcının seçimine göre oturum sağlanır. Oturum bilgilerini korumak için bir obje tutulur ve oturum sonlandırıldığında da bu obje temizlenir. Bu sayede katılımcı veya organizasyon hesapları arasında geçiş yapılması sağlanır.
- **Katılımcılar İçin Etkinlik İşlemleri:** Katılımcılar, Organizasyonlar tarafınfan düzenlenen tüm etkinlikleri görebilir, bir etkinliğin isim veya id bilgisi sayesinde o etkinliğe kaydolabilir ve etkinlik kayıtlarını iptal edebilirler.
- **Organizasyonlar İçin Etkinlik İşlemleri:** Organizasyonlar, tüm etkinlikleri görüntüleyebilir, kendi oluşturduğu etkinlikleri görüntüleyebilir, yeni etkinlikler oluşturup kaydedebilir, oluşturduğu etkinlikleri silebilir, oluşturduğu etkinliğe katılım sağlayacak kullanıcıların bir listesini görüntüleyebilirler.
- **Hata Yönetimi:** Proje içerisinde hata durumlarını yönetmek, olası hatalarda uygulamanın çökmesini engellemek için `try-catch blokları`ndan faydalanıldı ve kullanıcıya daha iyi bir deneyim sunmak için hata durumlarında açıklayıcı uyarı mesajları verildi.

## Gereksinimler

- Projeyi kendi bilgisayarınıza klonlayabilmek için `Git` sistemi indirilip kurulumu yapılmış olmalıdır.
- Projeyi çalıştırmak için `Microsoft Visual Studio` indirilip kurulumu yapılmış olmalıdır.

## Kullanım

Projeyi çalıştırmak için aşağıdaki adımları izleyebilirsiniz:
1. Komutları girmek için terminal ekranını açın ve `cd <dosya_adi>` komutuyla ilgili klasöre geçin.
2. Projeyi klonlayın: `https://github.com/Furkan-Boncuk/c-code.git`
3. Uygulamayı derleyip çalıştırın.

## Proje Detayları

Proje, OOP prensiblerine uygun hazırlanmıştır :

1. **Encapsulation (Kapsülleme):** Sınıfların içindeki veriler private olarak tanımlanmış ve get set metotlarıyla dışarıdan erişimi sağlanmıştır. Veri ve field'lar, sınıflar (`User`, `Participant`, `Organization`, `Event`, `AuthObject`) ,içerisinde kapsüllenmiştir.

2. **Inheritance (Miras):** `Participant` ve `Organization` sınıfları, `User` sınıfından miras alır. User içerisindeki field'ları ( Id, Username, Email, Password ) kendi içlerinde kullanırlar.

3. **Polymorphism (Çok Biçimlilik):** `IParticipantEvent` ve `IOrganizationEvent` interface'leri, `Participant` ve `Organization` sınıfları tarafından implemente edilir ve interface'ler içindeki metotlarda `overload` kullanılmıştır. Örneğin katılımcıların bir etkinliğe kayıt yapmasını sağlayan bir metot olan `public void AttendEvent(string eventName, Participant participantBody, List<Event> Events)` metodu bu kullanımla etkinlik isimlerine göre işlem yaparken aynı isimle tanımlanan `public void AttendEvent(int eventId, Participant participantBody, List<Event> Events)` metodu da etkinliklerin id bilgisine göre işlem yapar.
   
4. **Abstraction (Soyutlama):** `IParticipantEvent` ve `IOrganizationEvent` interface'leri, sınıflarda kullanılacak metotları belirleyip tanımlamak ve ortak işlemleri bir çatıda toplayarak soyutlama yapmak için kullanılır.

## Proje Ekran Görüntüleri 

(Konsol üzerinde projenin bazı ekran görüntüleri aşağıda derlenmiştir.)

![1](https://github.com/Furkan-Boncuk/c-code/assets/114020260/1050dbfb-3803-4085-b9d8-9564ea4bbf5e)

![2](https://github.com/Furkan-Boncuk/c-code/assets/114020260/039bea4e-bed1-48f1-9ae1-f6b171c85d88)

![3](https://github.com/Furkan-Boncuk/c-code/assets/114020260/054c087d-9548-491c-a0d7-a5740ea86cb9)

![4](https://github.com/Furkan-Boncuk/c-code/assets/114020260/d01a7724-5cb2-4855-925f-bda0f84d92e0)

![4](https://github.com/Furkan-Boncuk/c-code/assets/114020260/99dfbdbe-945e-4b4c-b328-076e4de9eb48)

![6](https://github.com/Furkan-Boncuk/c-code/assets/114020260/98740ea1-0883-47fd-8ff7-5c9cb5cffc49)

![7](https://github.com/Furkan-Boncuk/c-code/assets/114020260/28943975-ca9f-4170-9703-1d9b4c9ccfc6)

![8](https://github.com/Furkan-Boncuk/c-code/assets/114020260/e6acc230-0dbe-4ab3-b0c8-d8b060eb60c7)

![9](https://github.com/Furkan-Boncuk/c-code/assets/114020260/b8e02437-5118-4feb-81b1-dd782a2d564b)

![10](https://github.com/Furkan-Boncuk/c-code/assets/114020260/0d74b85f-cfcf-481b-b8a0-1092a5443456)

![11](https://github.com/Furkan-Boncuk/c-code/assets/114020260/17c9e36a-6f4a-47f3-b382-0adf2d0695e5)

![12](https://github.com/Furkan-Boncuk/c-code/assets/114020260/c06b69c0-c472-4405-8709-e079e32d207b)

![13](https://github.com/Furkan-Boncuk/c-code/assets/114020260/94e54dca-ecfb-4874-926d-f8d3861d98eb)

![14](https://github.com/Furkan-Boncuk/c-code/assets/114020260/dab14138-a00a-42f7-863b-17ca26b660b0)

![15](https://github.com/Furkan-Boncuk/c-code/assets/114020260/a8df689c-16cc-43e0-82bb-bbc3246184c1)
















