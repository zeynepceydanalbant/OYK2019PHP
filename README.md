# Özgür Yazılım Yaz Kampı PHP Sınıfı Ders Notları


![Mustafa Akgül Özgür Yazılım Kampı](https://kamp.linux.org.tr/2019/yaz/wp-content/themes/oyk-wp-theme/assets/images/oyk2019logo.png)
## 20.07.2019 Birinci Gün Notları
Komut|Açıklama
---|---
`sudo apt install paket-ismi`|Bu komut ile sistemimize ubuntu depolarında bulunan her paketi kurabiliriz. 
`sudo apt remove paket-ismi`|Bu komut ile istediğimiz paketi silebiliriz. 
`sudo apt update`|Paket listesini günceller.
`sudo apt upgrade`|Sistemde kurulu paketleri günceller.

### Paket yöneticileri (apt, yum, dnf, pkg)
- Paket yükleme işlemleri kolaylaşır.
- Paket kaldırma işlemleri kolaylaşır.
- Var olan paketlerin güncelleme işlemleri kolaylaşır.
- Sistemde yüklü olan/olmayan paketleri listeleme işi kolaylaşır.
- Programların çalışması için gerekli olan diğer programların yönetimi kolaylaşır.

### Çekirdek
Çekirdek, bilgisayarda donanım (hardware) ve yazılım (software) arasındaki bağlantıyı sağlayan arabirime verilen isimdir. 

Linux işletim sisteminin çekirdeğinin diğer işletim sistemlerinin pek çoğundan farkı, çekirdek kaynak kodunun GPL (GENERAL PUBLIC LICENSE) lisansı altında açık kaynak kodlu, diğer bir deyişle isteyen herkes tarafından yapılandırılabilir, hatta daha üst düzey kullanıcılar için değiştirilebilir olmasıdır. 
#### Debian Nedir?
**Debian**, günümüze kadar ulaşmış ve hala sayısız kullanıcı tarafından kullanılan GNU/Hurd, GNU/Linuxgibi farklı çekirdek seçeneklerine bağlı özgür bir Linux dağıtımıdır. 

#### Red Hat Nedir?
Red Hat, Türkçesiyle Kırmızı Şapka, başta açık kaynak kodlu yazılımlar olmak üzere Linux tabanlı çalışan en gelişmiş ve profesyonelleşmiş yazılım şirketlerinden biridir. 

### RFC (Request for Comment) Nedir?
1969 yılından günümüze kadar ortaya koyulan standartların saklandığı döküman arşividir.TCP/IP standartları, Request For Comment(RFC) denilen dökümanlar içinde yayınlanmıştır. RFC’lerde internetin işleyişi açıklanır. 

### Betik Dili Nedir?
Betik dili, web sayfalarında dinamik içerik sağlamak ve kullanıcıyla iletişim kurmak için kullanılan, istemci tarafında çalışan bir dildir.

### CGI Nedir?
CGI (Common Gateway Interface), Web Servisleri ile bu servislerin dışındaki programlar arasında etkileşim (ortak çalışma) platformu oluşturmak için geliştirilmiş bir standarttır. CGI, aslında bir programdır. Web'in statik yapısına, HTML kodu içinden çağrılan CGI programları dinamik bir nitelik kazandırmaktadır. 
(Kaynak: http://www.bilisimterimleri.com/bilgisayar_bilgisi/bilgi/68.html TODO: Yukarıdaki geçici bir açıklama. Kaynaktan derle ve değiştir.) 

### IP Nedir?
İnternet Protokolü ya da orijinal adıyla Internet Protocol isim tamlamasının kısaltması olan IP; internet üzerinden gerçekleştirilen tüm işlemlerde tıpkı bir imza gibi belirleyici rol oynuyor. IP numarası ya da IP adresi için bir diğer benzetme de parmak izi. 

### Apache Nedir?
Apache, dünyadaki web sitelerinin %46’sına gücünü veren açık kaynak kodlu, ücretsiz bir web sunucusu yazılımıdır. 

### MySQL? MariaDB?

MySQL, altı milyondan fazla sistemde yüklü bulunan çoklu iş parçacıklı, çok kullanıcılı, hızlı ve sağlam bir veri tabanı yönetim sistemidir.
MariaDB, ilişkisel veritabanı sistemi olan MySQL'in kaynak kodundan türemiş, GNU Genel Kamu Lisansı altında dağıtılarak ücretsiz olarak kullanılabilen, geliştirilmesi ve bakımı topluluk tarafından sürdürülen veritabanıdır.

### Servis Nedir?
Belirli bir görevi yerine getirebilmek için arka planda çalışan ve kullanıcının uygulamayla olan ilişkisini etkilemeyen işlemler için kullanılan sınıftır.




## 4.gün
### Atom aracılığıyla Git serivisine bağlanmak 
İlk önce SSH anahtarının GitHub (veya kullanacağımız başka bir Git servisi) üzerinde kayıtlı olması gerekiyor. [SSH anahtarını nasıl buluyoruz?](https://github.com/nuriakman/PHP-Egitimi/blob/master/konular/ayarlar.sshkey.md) sorusunun cevabı burada. 
(Tabi bunlardan önce bilgisayarımızda Git konfigürasyonlarının yapılmış olması gerekiyor. 

TODO: Başlığı tamamla. 

## 5.gün
### PHP Komutları

- file_get_contents : Dosyadan direkt olarak içeriği sayfaya çekip, gösterir. 
- file: Dosyada bulunan içeriği dizi olarak çekip satır satır gösterir. 
- print_r($array) : Dizileri yazdırmak için kullanılan fonksiyon.
- explode("ayırıcı", variable) : Değişkeni ilk parametredeki karaktere göre patlatır ve bir dizi oluşturur. 
- implode("birleştirici", dizi): Diziyi ilk parametredeki karaktere göre birleştirir ve bir karaktere atar. 
Not: Ayırıcı ve birleştirici gibi ifadeler ,;.- gibi karakterlerdir.
- die("") : İşlemi bitirir ve bitirirken yazı yazdırabilir. 
- md5($str) : Bu ifade dosyanın veya ifadenin parmak izini çıkarmak için kullanılır. Şifreleme yapmak için veya bir veri türünü orjinali ile kıyaslamak için kullanılır. 
- sha1($str) : md5 gibi verinin parmak izini çıkartır. md5'in istatistiksel olarak (çok düşük bir ihtimal de olsa) aynısının var olma ihtimali varken sha1'i de böyle bir ihtimal yoktur. 

###### git reset --hard : Bu komut ile Git'ten "git pull" ile çektiğimiz ve düzenlediğimiz dosyayı, düzenlemeden önceki haline döndürebiliriz. 

- sudo chmod g+w isimler.txt

#### Kaçış Karakterleri
- \n new line
- \r return 
- \t tab 
