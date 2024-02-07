# [ EBS Tester Tools V 0.1 ] Kullanım Kılavuzu

## 1. Giriş

- **Amaç:** Bu program, Tester ve web scraping işlemlerini otomatize etmek isteyenler için tasarlanmıştır.
- **Sürüm:** V0.1

## 2. Kurulum

- **Platform:** Program sadece Windows üzerinde çalışır.
- **Kurulum Adımları:**
  - İlgili .zip dosyasını dışarı çıkartın.
  - EBSTesterTools.exe dosyasını çift tıklayarak çalıştırın (Tak-Çalıştır gibi).

## 3. Temel Kullanım

- **Tarayıcı Başlatma:**
  - Programı çalıştırdıktan sonra tarayıcıyı başlatmak için uygun seçeneği kullanın.

- **Bağlantı Kurma:**
  - Tarayıcı başlatıldıktan sonra bağlantı kurma işlemlerini gerçekleştirin.

- **Otomatize Ayarlar:**
  - Programın kendine özgü bir dil kullanarak test aşamalarını otomatize etmek için Otomatize Ayarlar bölümünden gerekli komutları girin.

## 4. Örnek Senaryolar

### Senaryo 1: Arama ve Veri Çekme İşlemi

-  url~https://www.bulurum.com/
- bekleme~2000
- Userveri~//*[@onkeypress='return(checkEnterKeypressWhatHeader(event));'],kuruyemiş~0
- bekleme~2000
- Userveri~//*[@onkeypress='return(checkEnterKeypressWhatHeader(event));'],Beykoz~1
- bekleme~2000
- mouseover~//*[@class='searchbtn_tr']~0
- bekleme~1500
- mousetiklama~//*[@class='searchbtn_tr']~0
- bekleme~1500
- javascript~for (let index = 0; index < 11; index++) { phoneTextClick(index); }
- bekleme~1500
- javascript~var txt_firmaadi = document.getElementsByClassName("CompanyName"); var txt_Telno = document.getElementsByClassName("PhonesBoxBig"); var firmaadi = []; var telno = []; for (let index = 0; index < txt_firmaadi.length; index++) { var companyName = txt_firmaadi[index].innerText; var No = txt_Telno[index].innerText; firmaadi.push(companyName); telno.push(No); } var csvContent = "Firma Adı,Firma Telefonu\n"; for (var i = 0; i < firmaadi.length; i++) { csvContent += firmaadi[i] + "," + telno[i] + "\n"; } var blob = new Blob([csvContent], { type: "text/csv" }); var link = document.createElement("a"); link.href = window.URL.createObjectURL(blob); link.download = "data.csv"; document.body.appendChild(link); link.click(); document.body.removeChild(link);

## Kullanım Videosu

[![Kullanım Videosu](https://img.youtube.com/vi/Jyh47sz3ToU/0.jpg)](https://www.youtube.com/watch?v=Jyh47sz3ToU)


## 5. Hata Ayıklama ve Sorun Giderme

- Şu an için belirtilen bir hata ayıklama ve sorun giderme bölümü yok.

## 6. Katkıda Bulunma

- Hataları ve önerileri GitHub üzerinden bildirebilirsiniz.

## 7. Lisans

- Program ücretli bir programdır ve kapalı kaynak kodludur.

## 8. İletişim

- Herhangi bir iletişim bilgisi belirtilmemiştir.

## 9. Değişiklik Kaydı

- Şu an için belirtilen bir değişiklik kaydı bölümü yok.
