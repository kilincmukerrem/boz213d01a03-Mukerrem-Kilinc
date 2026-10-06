# Açık Kaynak GitHub Lisans Sözleşmeleri Nelerdir ve Hangi Durumda Hangi Sözleşmeler Kullanılır
Açık kaynak ortamında bir yazılımın kaynak kodunun GitHub üzerinde erişilebilir olması, o kodun yasal olarak serbestçe kullanılabileceği anlamına gelmez. Bir depoya (repository) açıkça bir lisans eklenmediğinde, varsayılan olarak katı telif hakkı (All Rights Reserved) geçerlidir. Bu durumda diğer kullanıcılar GitHub Hizmet Şartları uyarınca kodu görüntüleyebilir veya çatallayabilir (fork); ancak projeyi ticari amaçla kullanamaz, değiştiremez veya dağıtamaz.

Yazılım geliştiriciler, projelerinin hukuki çerçevesini belirlemek için Open Source Initiative (OSI) tarafından onaylanmış ve GitHub'ın choosealicense.com aracılığıyla sunduğu standart açık kaynak sözleşmelerini tercih eder.



## Lisans Türleri ve Karşılaştırma Tablosu
Açık kaynak lisansları temel olarak iki ana grupta toplanır:

* **İzin Verici (Permissive) Lisanslar:** Kullanıcıya minimum kısıtlama getirir; kodun kapalı kaynaklı ve ticari projelerde kullanılmasına izin verir.

* **Telif Haklı / Paylaşımcı (Copyleft) Lisanslar:** Kod üzerinde yapılan değişikliklerin ve türetilen yazılımların da aynı lisans koşullarıyla açık kaynak olarak paylaşılmasını zorunlu tutar.

| Lisans Adı | Lisans Türü | Değiştirilen Kodu Açma Zorunluluğu | Ticari Kullanım | Patent Koruması | Temel Ayırt Edici Şartı |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **MIT** | İzin Verici *(Permissive)* | Yok | Serbest | Yok | Orijinal telif hakkı ve lisans metninin korunması yeterlidir. |
| **Apache 2.0** | İzin Verici *(Permissive)* | Yok | Serbest | Var *(Açık patent hibesi)* | Katkıda bulunanların patent davası açmasını engeller, ticari markayı korur. |
| **BSD 3-Clause** | İzin Verici *(Permissive)* | Yok | Serbest | Yok | Proje sahibinin adı, izinsiz reklam ve tanıtımlarda kullanılamaz. |
| **GNU GPLv3** | Güçlü Copyleft | **Var** *(Tüm türetilen projeler GPLv3 olmak zorunda)* | Serbest | Var | Kod kapalı kaynaklı yazılımlarla birleştirilip ticarileştirilemez. |
| **GNU AGPLv3** | Ağ Tabanlı Copyleft | **Var** *(Ağ/Bulut üzerinden sunulsa dahi geçerli)* | Serbest | Var | Yazılım bir SaaS/bulut hizmeti olarak çalıştırıldığında dahi kaynak kodu açılmalıdır. |
| **GNU LGPLv3** | Zayıf Copyleft | **Kısmi** *(Yalnızca kütüphanenin kendisi değiştirilirse)* | Serbest | Var | Kütüphane kapalı kaynaklı bir projeye harici olarak bağlanabilir (dinamik linkleme). |
| **Mozilla (MPL 2.0)** | Dosya Bazlı Copyleft | **Kısmi** *(Sadece MPL ile yazılmış dosyalarda)* | Serbest | Var | Değişiklikler dosya düzeyinde takip edilir; projenin geri kalanı kapalı kalabilir. |
| **The Unlicense / CC0** | Kamu Malı *(Public Domain)* | Yok | Serbest | Yok | Tüm haklardan feragat edilir, atıf zorunluluğu dahi aranmaz. | 


## Farklı Durumlara Göre Hangi Sözleşme Kullanılmalı?
* **Geniş Kitlelere Yayılma ve Kolay Entegrasyon (Örn. Araçlar, Yardımcı Kütüphaneler)**
  * **Lisans:** MIT License
  * **Neden:** Kodun şirketler tarafından kapalı kaynaklı ürünlere dahil edilmesine izin verir. En yaygın ekosistem uyumluluğuna sahiptir.
  
* **Kurumsal Projeler ve Patent Güvencesi (Örn. Framework'ler, Altyapı Yazılımları)**
  * **Lisans:** Apache License 2.0
  * **Neden:** Katkıda bulunanların telif veya patent hakkı iddia ederek dava açmasını engeller; ticari markanın korunmasını sağlar.
* **Topluluğun Kod Paylaşımını Zorunlu Kılma (Örn. Masaüstü Uygulamaları, Çekirdek Sistemler)**
  * **Lisans:** GNU GPLv3
  * **Neden:** Kodun değiştirilip ticarileştirilerek kapatılmasını engeller; türetilen her ürünün açık kaynak kalmasını teminat altına alır.
* **Bulut ve SaaS Hizmetleri (Örn. Web API'leri, Ağ Tabanlı Platformlar)**
  * **Lisans:** GNU AGPLv3
  * **Neden:** Standart GPL'deki "kodun dağıtımı" şartı ağ üzerinden sunulan hizmetleri kapsamayabilir. AGPL, SaaS mimarisinde dahi kaynak kodun istemcilere açılmasını şart koşar.
* **Dinamik Bağlanan Kütüphaneler (Örn. C/C++ DLL/SO Paketleri)**
  * **Lisans:** GNU LGPLv3 veya Mozilla Public License 2.0
  * **Neden:** Kapalı kaynak projelerin kütüphaneyi çağırmasına imkân tanırken, kütüphanenin kendi kaynak kodunda yapılan geliştirmeleri koruma altına alır.
* **Haklardan Tamamen Feragat Etme (Örn. Şablonlar, Konfigürasyon Dosyaları)**
  * **Lisans:** The Unlicense veya CC0 1.0 Universal
  * **Neden:** Proje tamamen kamu malı haline getirilir, atıf zorunluluğu kalkar.

# Kaynakça
* [GitHub Lisanslama Dokümantasyonu](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository)
* [GitHub Resmi Lisans Seçim Portalı](https://choosealicense.com/licenses/)
* [Open Source Initiative (OSI Onaylı Lisans Listesi)](https://opensource.org/licenses)



