<h1 align="center">Temel Network (Ağ) Notları</h1>

<p>&nbsp;</p>

## Network (Ağ) Nedir?

Network kısaca iki veya daha fazla cihazın belirli kurallar (protokoller) içerisinde ilerişim kurabilen cihazların oluşturmuş olduğu genel yapıdır. 

<p>&nbsp;</p><p>&nbsp;</p>

## Domain, Hosting, SubDomain, Name Server 

### Domain
Domain, kısaca tanımı alan adıdır. Her website aslında bir IP adresine sahiptir ancak bunları girmek yerine daha kişiselleştirilmiş ve özelleştirilmiş olan domain adlarını alırlar. Örnek vermek gerekirse "yildizskylab.com" bu bir domaindir. 

### SubDomain
SubDomain, herhangi bir alan adının bir alt alan adı olarak geçmektedir, bir alan adının altına istediğiniz kadar subdomain açabilmeniz mümkündür. Örnek vermek gerelirse "skysec.yildizskylab.com" adresinde bulunan "skysec" ibaresi bir SubDomain'dir.

### SubFolder (SubDirectory)
Bir alan adı altında yer alan bir alt klasörü temsil etmektedir. Örnek vermek gerekirse "yildizskulab.com/register" da bulunan "/register" kısmı bir SubFolder'dır. 

### Hosting
Kısaca barındırma/depolama hizmetidir. Sitenizde yayınlanacak olan sayfaları, fotoğrafları, belgeleri vb. içerikleri barındırmaya yarar. 

Kullanıcı bilgisayarında neden barındıramayız gibi bir soru sorabilirsiniz, sitenizin erişilebilir olması adına sürekli açık bir bilgisayara ihtiyaç duyulmaktadır, burada hosting hizmeti devreye girmektedir; eğer sitenizi kişisel/kullanıcı bilgisayarına kurmuş olsaydınız bilgisayar kapatıldığı zaman siteniz içerisindeki hiçbir belge, veri, dosyaya vb. ulaşılabilir olmayacaktı; hosting bu problemi ortadan kaldırmaktadır. 

### Name Server

NS (name server), bilgisayarlar tarafından kendisine yapılan domain adresi sorgularına cevap veren bir sunucu türüdür. Hosting hizmeti aldığınız şirket tarafından domaininize atanır ve domaininizle IP adresiniz arasındaki bağı oluşturur. 

Name Server adresi örneği:

ns1.yildizskylab.com
ns2.yildizskylab.com

<p>&nbsp;</p><p>&nbsp;</p>

## Ağ donanımlarına giriş
### İnternet kartı(NIC)

Cihazların internete erişmelerini sağlar, IP ve MAC adresleri bilgilerini tutar. 
[NIC ile ilgili güzel bir kaynak](https://longline.com.tr/network-interface-card-nic-nedir/)
<br>

### Switch

Birçok cihazın kablolu ve/veya kablosuz biçimde internete bağlanmasını sağlar; kendi aralarında haberleşmesini mümkün kılar. 
OSI katman modelinde ikinci katman olan Veri İletim (Data Link Layer) katmanında çalışır; yeni dağıtıcılarda ise OSI'ın ikinci katmanı olan Data Link Layer'da (Veri İletim) çalışabilir.
<br>

### Modem

Cihazları tek bir ağa bağlar ve o cihazların kablolu veya kablosuz olarak internete erişmesinden sorumludur;Ağ olarak LAN kullanır. 

Modemlerin belirli bir admin paneli bulunmaktadır ve genelde arama motoruna `192.168.1.1` ve/veya `localhost` yazarak erişilir, admin paneline erişmek için modemin LAN ağında bulunmanız gerekmektedir.
<br>

### Bridge

İki bilgisayar ağını birbirine bağlayan ağ cihazıdır.
[Bridge hakkinda yazilmis guzel bir kaynak](https://tr.wikipedia.org/wiki/A%C4%9F_k%C3%B6pr%C3%BCs%C3%BC)
<br>

### Hub

Sinyalleri güçlendirip, kabloya iletir.
[Burda basit bir anlatıma detaylı ve güzel bir kaynak bulunuyor, bakmanızı öneririm](https://networkgiller.wordpress.com/hub/)
<br>

### Firewall

Network paketlerinin içeriniğinin incelendiği (okunduğu ve bir tehlike içerip içermediğinin kontrolü sağlanır.) kısımdır. Eğer bir tehlike içeriyorsa bloklar, erişim izinlerini denetlemeden sorumludur. İki türe ayrılır, Yapılarına ve mimarilerine göre. 

[Daha ayrıntılı bir kaynağa ihtiyaç duyarsanız](https://www.vargonen.com/blog/firewall-guvenlik-duvari-nedir/#:~:text=Sunucular%C4%B1n%C4%B1zda%2C%20network%20altyap%C4%B1n%C4%B1zda%20ve%20ki%C5%9Fisel,(g%C3%BCvenlik%20duvar%C4%B1)%20ad%C4%B1%20verilmektedir.)

<p>&nbsp;</p><p>&nbsp;</p>

## Temel Network bilgisi

### LAN(Local Area Network)
Sınırlı alandaki internete bağlanan cihazları birbirine bağlayan ağdır. Yani aynı evde bulunan bilgisayar, telefon gibi cihazları tek bir modem üzerine bağlandığı zaman bu bir LAN ağı olur.
`IP Örneği: 192.168.1.1`
Modem bunu HOST ID Numarasını atar. Yani bilgisyar `192.168.1.2` adresinde ise telefon `192.168.1.3` adresindedir.

LAN IP Adresinizi öğrenmek için **Windows cihazlarda** Windows + R tuşlarına aynı anda basarak açılan alana **“CMD”** yazın ve **“Enter”** tuşuna basın. **“ipconfig”** yazıp **“Enter”** tuşuna basın, bu şekilde Local IP adresinize ulaşırsınız (daha ayrıntılı bilgi için ise **"ipconfig /all "** yazabilirsiniz); **Linux tabanlı cihazlarda** ise ctrl+alt+t ile terminale ulaşabilir **"ifconfig"** yaıp **"Enter"** tuşuna basın, bu şekilde Local IP adresinize ulaşırsınız (daha ayrıntılı bilgi için ise **"ipconfig -a "** yazabilirsiniz).

<br>

### MAN (Metropolitan Area Network)

Bir şehir veya büyük bir yerleşkede bulunan ağdır. LAN'lar (Local Area Network) arasındaki bağlantıyı kurmaktadır. İnternet ve WAN (Wide Area Network) için bağlantı hizmetleri sunar.
<br>

### WAN (Wide Area Network)

Dünya çapındaki cihazların birbirine bağlanmasını sağlayan ağdır.
WAN IP Adresinizi arama motorunuza **"what's my ip"** yazarak öğrenebilirsiniz 
<br>

### DNS (Domain Name System)

DNS, internette bulunan tüm bileşenleri sınıflayan, bu bileşenlerin IP adreslerini adlandıran ve bu bileşenler arasında bağ kuran sistemin kendisidir. Bu işi yapan sunuculara DNS denir. 

Dünya üzerinde sadece 13 adet **ROOT DNS** vardır, bu ana DNS tüm trafiği kontrol etmektedir. Yerel lokasyonlarda da birçok hosting şirketine ait sayısız DNS serverları sadece 13 adet olan **ROOT DNS** serverlarıyla sürekli iletişim halindedir.

#### DNS'in Nasıl Çalışır? 

Bu işlemi bir örnek ile anlatmak gerekirse, bir telefon numaralarını hafızamızda tutamadığımız için telefon rehberimize o numaraya ait bir isim tanımlamaya benzer. Telefon rehberi 'tarayıcı', kayıtlı isimler 'domain', telefon numarasını 'IP Adresi', bu telefon numarası ile size ulaşılmasını sağlayan operatöre 'DNS', o numaranın kullanıldığı cihaza 'Hosting', sim karta da 'NameServer Adresi' olarak varsayabiliriz.

Bu sistem sayesinde tarayıcıya 'domain' bilgisi girilir, o 'domain' barındırıldığı 'hostinge' ait bir 'nameserver' bilgileri üzerinden websitesine erişim sağlar. 

Eğer 'DNS' istemi olmasaydı websitelerine, bulundukları sunucuda tanımlanan IP adresleri ile ulaşılması gerekirdir. 

Adresleri sınıflayarak bağlı bulundukları 'nameserverları' kayıt altında tutan bu sunucular sayesinde birden fazla domain akılda kalabilmektedir. 
<br>

### OSI Referans Modeli

OSI (Open Systems Interconnection) modelini ISO (International Organization for Standardization) geliştirmiştir. Amacı cihazların birbirleri ile nasıl iletişim kuracaklarını tanımlamaktır; 7 Katmandan oluşmaktadır. 
Bunlar:
L-1 Physical(Fiber, Wirelees vb..), 
L-2 Data Link(Ethernet, Switch vb..), 
L-3 Network(IP,ICMP), 
L-4 Transport(TCP, UDP), 
L-5 Session(API,Sockets),
L-6 Presentation(SSL,SSH,FTP vb.),
L-7 Application(HTTP, FTP, IRC, DNS, SSH)

#### OSI Referans Modeli Katmalnalrının Özellikleri: 

L-1 Physical Layer:
Fiziksel katman (ayrıca modelin ilk katmanı olarak bilinir) verinin kablo üzerinde alacağı yapıyı tanımlar. Veriler bit olarak iletilir. Bu katman bir ve sıfırların nasıl elektrik, ışık veya radyo sinyallerine çevrileceğini ve aktarılacağını tanımlar. Gönderen tarafta fiziksel katman bir ve sıfırları elektrik sinyallerine çevirip kabloya yerleştirirken, alıcı tarafta fiziksel katman kablodan okuduğu bu sinyalleri tekrar bir ve sıfır haline getirir. 

Fiziksel katman veri bitlerinin alıcıya kullanılan medya ile (kablo, fiber optik ve radyo sinyalleri) üzerinden nasıl gönderileceğini tanımlar. Veri iletiminin mümkün olabilmesi için **iki tarafın aynı kurallar üzerinde tanımlanmış olması gerekir**.

L-2 Data Link Layer:

*Tabspace* Veri bağlantısı katmanı iki alt bölüme ayrılır: 
*Tabspace**Tabspace* Media Access Control (MAC) 
*Tabspace**Tabspace* Logical Link Control (LLC)

*Tabspace**Tabspace* MAC alt katmanı, veriyi hata kontrol kodu (CRC), alıcı ve gönderenin MAC adresleri ile beraber paketler ve Physical Layer'a aktarır. Alıcı tarafta da bu işlemlerin tam tersi yapılır ve veriyi, veri bağlantısı içindeki ikinci alt katman olan LLC'ye aktarma görevi yine MAC alt katmanına aittir.

*Tabspace**Tabspace* LLC alt katmanı bir üst katman olan ağ katmanı için geçiş görevi görür. Protokole özel mantıksal portlar oluşturur(Service Access Points, SAPs). Böylece kaynak makinada ve hedef makinada aynı protokoller iletişime geçebilir(örneğin TCP/IP<-->TCP/IP). LLC ayrıca veri paketlerinden bozuk gidenlerin(veya karşı taraf için alınanların) tekrar gönderilmesinden sorumludur. Flow Control yani alıcının işleyebileğinden fazla veri paketi gönderilerek boğulmasının engellenmesi de LLC'nin görevidir.

*Tabspace**Tabspace* Ağlarda bulunan çerçeve tipleri şöyledir:

*Tabspace**Tabspace* 802.2  Ethernet II
*Tabspace**Tabspace* 802.3  Ethernet
*Tabspace**Tabspace* 802.4  Token Bus
*Tabspace**Tabspace* 802.5  Token Ring

*Tabspace**Tabspace* Ayrıca switch (anahtar) 2.katmanda çalışan bir cihazdır. Çünkü 2. katmanda tanımlı MAC adreslerini algılayabilirler ve bir porttan gelen veri paketini (yine elektrik sinyalleri halinde) sadece gerekli olan porta (o porttaki makinanın MAC adresini bildiği için) yollayabilirler. 


L-3 Network Layer:

Network Layer'da veri paketine farklı bir ağa gönderilmesi gerektiğinde yönlendiricilerin kullanacağı bilginin eklendiği katmandır. Bu katmanda veriler paket olarak taşınır. Bu katman sayesinde veri router aracılığıyla yönlendirmesi sağlanır. 

Network Layer'da iki istasyon arasında en ekonomik yoldan verinin iletimi kontrol edilir. Bu katman sayesinde verinin yönlendiriciler (router) aracılığıyla yönlendirilmesi sağlanır.
Ağ aşamasında mesajlar adreslenir ayrıca mantıksal adresler fiziksel adreslere çevirilir; bu aşamada ağ trafiği, yönlendirme gibi işlemler de yapılır(Kısaca switching and routing teknolojisi bu katmanda çalışır).
**Internetworking, error handling (hata işleme), congestion control ve packet sequencing (paket sıralama)** ve **'TCP/IP', 'IPX', 'AppleTalk' gibi farklı ***ağ protokolleri*** bu katmanda çalışır.**

L-4 Transport Layer:
Transport Layer üst katmanlardan gelen veriyi ağ paketi boyutunda parçalara böler. 

**TCP, UDP, SPX protokolleri bu katmanda çalışır. Bu protokoller hata kontrolü gibi görevleri de yerine getirir**.

Transport Layer'da veriler segment halinde taşınır; üst katmanlara taşıma servisi sağlar, ayrıca ağın servis kalitesini artırır (QoS – Quality of Service). Aynı zamanda bu layer verinin verinin uçtan uca iletimini sağlar bu verilerin hata kontrolü ve zamanında ulaşıp ulaşmadığı kontrol edilir. Ayrıca Transport Layer veriyi üst katmanlara taşıma görevi yapar.


L-5 Session Layer:
Session Layer'da iki bilgisayardaki uygulama arasındaki bağlantının yapılması, kullanılması ve bitilmesi işlemleri yapılır. Bir bilgisayar birden fazla bilgisayarlarla aynı anda iletişim halinde olduğunda, gerektiğinde doğru bilgisayarla birebir iletişime geçmesini sağlar. 

**NetBIOS, RPC, Named Pipes ve Sockets gibi protokoller bu katmanda çalışır**.

L-6 Presentation Layer:
Presentation Layer'ın en önemli görevi gönderilen verinin alıcı bilgisayar tarafından anlaşılacak şekilde çevrilmesidir. Bu sayede **farklı programların birbirlerinin verisini kullanabilmesi mümkün olur**.

Presentation Layer, Application Layer'a verileri gönderir ve sonrasında bu layer'da verinin yapısı, biçimi ile ilgili düzenlemeler yapılır ve verinin formatı belirlenir (verinin şifrelenmesi, açılması, sıkıştırılması da bu katmanda yapılır).

**GIF, JPEG, TIFF, EBCDIC, ASCII vb. bu katmanda çalışır**.

L-7 Application Layer:
Uygulama katmanı bilgisayar uygulaması ile ağ arasında bir arabirim sağlar. OSI katmanları arasında sadece bu katman diğer katmanlara servis sağlamaz. Uygulamaların ağ üzerinde çalışması sağlanır.
Uygulama katmanı ağ servisini kullanacak olan programdır. Bu katman kullanıcıların gereksinimini karşılar. "SSH", "Telnet", "FTP", "TFTP", "SMTP", "SNMP", "HTTP", "DNS" protokolleri ve "tarayıcılar" bu katmanda çalışır. E-posta ve database gibi uygulamalar bu katman aracılığıyla yapılır.

<br>

### Port
Özetle her uygulama belirli bir portdan sunulur. Bilgisayarda "65536" Port bulunmaktadır.
[Hangi PORT'un ne işe yaradığını öğrenebileceğiniz güzel bir kaynak](https://www.sistemim.com/donan%C4%B1m-makaleleri/116-hangi-port-ne-ise-yarar)

[Fiziksel PORT'lar ile ilgili guzel bir kaynak](https://forum.donanimhaber.com/bilgisayardaki-baglanti-portlari-ve-gorevleri--31333235)
<br>

### TCP/IP Modeli

TCP/IP'de yollanan veriler katmanlara göre paketlenir ve kollanır, alıcıya ulaşınca bu paketleri tek tek açılıp veriler ulaştırılır. Her katmanda verinin türüne göre belirli protokoller görev yapmaktadıe. OSI referans modelindeki 7 katmana karşılık TCP/IP’de 4 katman mevcuttur; Application (Uygulama), Transport (Taşıma), Internet, Network Interface (Ağ Arayüzü). 

L-1 Network Interface Layer (Ağ Arayüzü Katmanı)
L-2 Internet Layer (İnternet Katmanı)
L-3 Transport Layer (Taşıma Katmanı)
L-4 Application Layer (Uygulama Katmanı)

#### TCP/IP Katmalnalrının Özellikleri: 
L-1 Network Interface Layer (Ağ Arayüzü Katmanı)
Network Interface Layer'da verinin kablo üzerinde alacağı yapıyı tanımlayarak bir ve sıfırların fiziksel olarak görüntülenmesi sağlanır. Ethernet, Network Interface Layer kullanılan ve iletiminin fiziksel görünümünü sağlayan en yaygın kablolu yerel ağ teknolojisidir.

*Tabspace* Ethernet üç alt katmana sahiptir:
*Tabspace**Tabspace* LLC (Logic Link Control Layer- Mantıksal Bağlantı Kontrolü) 
*Tabspace**Tabspace* MAC (Media Access Control-Ortam Erişim Kontrolü) 
*Tabspace**Tabspace* Pyhsical(Fiziksel)

*Tabspace**Tabspace* LLC alt katmanında, Internet Layer'ındaki frame’in hangi protokolle geldiğini belirleyerek, iletimin  MAC’e geçişini sağlar. MAC alt katmanında, hedef ve kaynak mac adresleri eklenir. LLC ve MAC, datagrama kendi başlıklarını ekleyerek tam frame yapısını oluştururlar. Fiziksel alt katman ise bu frame'i elektrik sinyaline(kablolu ağda) ya da elektromanyetik dalgalara(kablosuz ağda) dönüştürür.

L-2 Internet Layer (İnternet Katmanı)
Internet Layer'da hedef ve/veya kaynak IP Adresleri veriye eklenerek verinin hangi bilgisayara gönderileceği belirlenir; gönderilen paket Datagram* halini alır. "IP", "ICMP", "IGMP", "ARP" protokolleri bu katmanda çalışmaktadır.

L-3 Transport Layer (Taşıma Katmanı)
Trasnport Layer'da verinin ne şekilde gönderildiğini gösterir. TCP  (Transmission Control Protocol) ve UDP (User Datagram Protocol) protokolleri bu katmanda çalışır. 
TCP ve UDP iletim sırasında veriye içinde bazı kontrol bilgilerinin bulunduğu bir başlık (header) ekler. TCP, kayıpsız veri gönderimi sağlayabilmek için kullanılan protokoldür. Gönderilen veriler için özel bir TCP kabul paketi (TCP ACK) gönderilir ve gelmiş olan paketlerin doğruluğu kontrol edilir. Gönderen taraf, kabul gelmediği sürece pakedi tekrar gönderir, böylece gönderim sağlanmış olur. TCP’de veri iletimi için iki bilgisayar arasında Three-Way Handshake (Üç Zamanlı El Sıkışma) bağlantısı kurulur. 

L-4 Application Layer (Uygulama Katmanı)
Application Layer'da veriyi göndermek isteyen uygulama ve kullandığı dosya biçimi bulunarak gönderilen verinin  türüne göre  farklı protokoller çalıştırılır (HTTP,  SMTP, FTP, Telnet, vs.); programlarla transport protokollerinin portlar aracılığıyla haberleşmesi sağlanır. Bu portlar numaralandırılmış (HTTP:80, FTP:21 vb.) standart uygulamalardır ve transport layer'a gelen paket içeriğinin türünün anlaşılmasında rol oynar.


<p>&nbsp;</p><p>&nbsp;</p>

## İletim
### Unicast
Cihazdan cihaza (cihazlar arası) yapılan iletim türüdür. 
<br>

### Multicast
Cihazdan bellirli cihazlara yapılan iletim türüdür.
<br>

### Broadcast
Cihazdan ortak ağdaki tüm cihazlara yapılan iletim türüdür.

<p>&nbsp;</p><p>&nbsp;</p>

## Network ID, Host ID ve IP Sınıfları
### Network ID
Aynı alt ağda bulunan (örneğin evlerde) cihazları (bilgisayarlar vs.) temsil edensınıf adresidir. IP Adresinin ilk üç kısmı Network IP olarak adlandırılır.
<br>

### Host ID
Evlerimizde kullandığımız IP nin son kısmı Host ID olarak adlandırılır.

[IP Sınıf Ararlıkları ile ilgili güzel bir yazı](https://www.ugureskici.com/notlarim-makalelerim/ip-sinif-araliklari)
<p>&nbsp;</p><p>&nbsp;</p>


## Ağ servislerinden bazıları
### DHCP
Ağda olan ve bir network ile çalışan cihazlara otomatik IP Adres ve DNS ataması yapar. Ağa misafir biri geldiğinde ona otomatik olarak 8 günlüğüne yetki verir. 
Not: Yetki süresi default olarak 8 gündür fakat bu süre artırıp azaltılabilir.

### NAT

Cihazlar internete bağlanmak için Public bir IP adresine ihtiyaç duyarlar fakat Public IP adresleri sayıyla sınırlıdır (3.3 Milyar IPv4 IP Adresi). Günümüzde telefonlarımızdan tutun ev eşyaları bile internete erişebilirken bu sayı çok az kalmaktadır. Bu yüzden internet hizmet sağlayıcıları her bir aboneye tek bir Public IP adresi atarlar. Sonuç olarak tek bir cihaz yerine bir çok cihaz aynı Public IP adresini kullanabilmesi için NAT kullanılır, iç ağda her cihaza yeni bir IP (LAN) verilir fakat bu durum sadece iç ağda geçerlidir. WAN'da ise tek bir Public IP kullanılır.

[Daha ayrıntılı bilgi için bu kaynağı okumanızı öneririm](https://turk.net/blog/internet-hizi/nat-nedir/)

<br>

Tebrikler! Eğer bütün yazıyı okuduysan artık temel olarak 

Sorularınız olursa benimle iletişime geçmekten çekinmeyiniz; iletişim adreslerim:

[Mail'den İletişim için Tıklayınız](mailto:ahmetimalf2@gmail.com)
[LinkedIn](https://www.linkedin.com/in/ahmetburakimal/)



<p>&nbsp;</p><p>&nbsp;</p>