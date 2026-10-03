# Lesson 9: How Computer Networks Work

## Level: B1
## Time: 90–120 minutes

> **درس ۹ — شبکه‌های کامپیوتری چگونه کار می‌کنند**
> **نکتهٔ گرامری:** حال کامل (present perfect) · for / since · تفاوت با گذشتهٔ ساده
> **متن درس:** ۱۵۷۶ واژه (۳۰ پاراگراف) | **واژگان کلیدی:** ۹۰ واژه | **باند سطح:** B1 (متوسط)

---

### 1. Lesson Objectives / اهداف درس

- اجزای یک شبکه (کارت شبکه، سوئیچ، روتر، مودم، نقطهٔ دسترسی) را نام ببرید و کار هر یک را توضیح دهید.
- تفاوت شبکهٔ محلی (LAN)، شبکهٔ گسترده (WAN) و اینترنت را در چند جمله بیان کنید.
- با واژگان بستهٔ داده، پروتکل، نشانی IP و توپولوژی، مسیر حرکت داده در شبکه را توضیح دهید.
- کیفیت یک شبکه را با واژگان توان عبوری، تأخیر، ازدحام و زمان کارکرد توصیف کنید.
- با حال کامل از تجربه‌ها و کارهای تازه‌تمام‌شده صحبت کنید و آن را با گذشتهٔ ساده مقایسه کنید.

---

### 2. Key Vocabulary / واژگان کلیدی

> تلفظ‌ها بر پایهٔ انگلیسی آمریکایی و در قالب IPA نوشته شده‌اند.

**جدول ۱ — اجزای شبکه (Network Components)**

| فارسی | تلفظ | Definition (EN) | Example (EN) | English |
|---|---|---|---|---|
| شبکهٔ محلی | /læn/<br>لَن | A network inside one building or one place. | A LAN covers one office. | LAN |
| شبکهٔ گسترده | /wæn/<br>وان | A network that covers cities or countries. | A WAN connects many LANs. | WAN |
| گره | /noʊd/<br>نود | One device that is connected to a network. | Every device in a network is a node. | node |
| ایستگاه کاری | /ˈwɜːrksteɪʃn/<br>وِرک‌استیشن | A computer for one person at work. | A node can be a workstation. | workstation |
| دروازه | /ˈɡeɪtweɪ/<br>گِیت‌وِی | The device that joins your network to another. | The gateway connects the subnet. | gateway |
| نقطهٔ دسترسی | /ˈækses pɔɪnt/<br>اَکسِس پوینت | A device that gives wireless access. | An access point sends radio waves. | access point |
| کارت شبکه | /nɪk/<br>نیک | A card that joins a device to a network. | Every device needs a NIC. | NIC |
| نشانی فیزیکی | /mæk əˈdres/<br>مَک اَدْرِس | The fixed address of a network card. | The switch reads the MAC address. | MAC address |
| نشانی شبکه | /ˌaɪ ˈpiː əˈdres/<br>آی‌پی اَدْرِس | The address of a device in an IP network. | Every node needs an IP address. | IP address |
| زیرشبکه | /ˈsʌbnet/<br>ساب‌نت | A smaller part of an IP network. | A subnet keeps one office together. | subnet |
| اِترنت | /ˈiːθərnet/<br>اِثِرنِت | The common technology for wired networks. | An Ethernet cable has two connectors. | Ethernet |
| فیبر نوری | /ˈfaɪbər/<br>فایبِر | A thin glass line that carries light. | An optical fibre is very fast. | fibre |
| مس | /ˈkɑːpər/<br>کاپِر | The brown metal inside a normal cable. | Copper cable is cheap. | copper |
| اتصال‌دهنده | /kəˈnektər/<br>کانِکتِر | The small part that joins two cables. | A cable has a connector at each end. | connector |
| هاب | /hʌb/<br>هاب | An old device that repeats every frame. | An old hub caused many collisions. | hub |
| پل شبکه | /brɪdʒ/<br>بریج | A device that joins two networks. | A bridge joins two small networks. | bridge |
| تقویت‌کننده | /rɪˈpiːtər/<br>ریپیتِر | A device that makes a signal strong again. | A repeater helps a weak signal. | repeater |
| آنتن | /ænˈtenə/<br>اَنتِنـا | A part that sends and receives radio waves. | The NIC has a small antenna. | antenna |
| دکل | /ˈtaʊər/<br>تاوِر | A tall structure for radio signals. | A mobile tower carries the signal. | tower |
| ماهواره | /ˈsætəlaɪt/<br>سَتِلایت | A machine in space that sends signals. | A satellite reaches a remote village. | satellite |
| ستون فقرات شبکه | /ˈbækboʊn/<br>بَک‌بون | The main, high-speed part of a network. | The backbone joins the big buildings. | backbone |
| نقطهٔ پایانی | /ˈendpɔɪnt/<br>اِندپوینت | The device that sends or receives data. | The frame goes to one endpoint. | endpoint |
| رابط | /ˈɪntərfeɪs/<br>اینتِرفِیس | The point where a device joins a network. | The interface has an IP address. | interface |
| بستر انتقال | /ˈmiːdiəm/<br>میدیوم | The way that data travels. | Copper and air are two media. | medium |
| فرکانس | /ˈfriːkwənsi/<br>فریکوئنسی | How many waves pass in one second. | The frequency changes the range. | frequency |
| توپولوژی | /təˈpɑːlədʒi/<br>تِپالاجی | The shape or plan of a network. | A star is a common topology. | topology |
| ستاره‌ای | /stɑːr/<br>اِستار | A shape with one central device. | In a star topology one switch is central. | star |
| حلقه‌ای | /rɪŋ/<br>رینگ | A shape where the nodes form a circle. | In a ring topology the nodes form a circle. | ring |
| توری | /meʃ/<br>مِش | A shape where every node joins many others. | A mesh network is very resilient. | mesh |
| بخش شبکه | /ˈseɡmənt/<br>سِگمِنت | One part of a divided network. | You can configure a logical segment. | segment |

**جدول ۲ — داده، پروتکل و کارهای شبکه (Data, Protocols and Network Actions)**

| فارسی | تلفظ | Definition (EN) | Example (EN) | English |
|---|---|---|---|---|
| بستهٔ داده | /ˈpækɪt/<br>پَکِت | A small piece of data that travels alone. | The data travels in small packets. | packet |
| پروتکل، قرارداد | /ˈproʊtəkɔːl/<br>پروتِکال | A set of rules for communication. | A protocol is a set of rules. | protocol |
| تی‌سی‌پی/آی‌پی | /ˌtiː siː ˈpiː aɪ piː/<br>تی‌سی‌پی‌آی‌پی | The main family of internet protocols. | Every device on the internet uses TCP/IP. | TCP/IP |
| اچ‌تی‌تی‌پی | /ˌeɪtʃ tiː tiː ˈpiː/<br>اچ‌تی‌تی‌پی | The protocol that moves web pages. | HTTP moves the pages of the web. | HTTP |
| اچ‌تی‌تی‌پی امن | /ˌeɪtʃ tiː tiː piː ˈes/<br>اچ‌تی‌تی‌پی اِس | The same protocol with encryption. | HTTPS uses encryption. | HTTPS |
| دی‌ان‌اس | /ˌdiː en ˈes/<br>دی‌اِن‌اِس | The service that finds IP addresses by name. | DNS finds the address of a name. | DNS |
| نام دامنه | /doʊˈmeɪn neɪm/<br>دومِین نِیم | The name of a website, like example.com. | DNS resolves a domain name. | domain name |
| قالب داده | /freɪm/<br>فرِیم | One unit of data on a local network. | A switch reads every frame. | frame |
| سرآیند | /ˈhedər/<br>هِدِر | The first part of a packet with its address. | The header carries the addresses. | header |
| محتوای بسته | /ˈpeɪloʊd/<br>پِیلود | The real data inside a packet. | The payload carries the real data. | payload |
| مسیریابی | /ˈruːtɪŋ/<br>روتینگ | Choosing the way for the packets. | Routing is the work of the router. | routing |
| دست‌دهی | /ˈhændʃeɪk/<br>هَندشِیک | The first exchange before a connection. | A handshake starts a connection. | handshake |
| توان عبوری | /ˈθruːpʊt/<br>ثروپوت | The real amount of data in one second. | Throughput is measured in megabits. | throughput |
| تأخیر | /ˈleɪtənsi/<br>لِیتِنسی | The time for one packet to travel. | Latency is measured in milliseconds. | latency |
| لرزش تأخیر | /ˈdʒɪtər/<br>جیتِر | A delay that changes all the time. | Jitter is a problem for video calls. | jitter |
| پینگ | /pɪŋ/<br>پینگ | A command that shows the delay. | A ping shows the latency. | ping |
| افت بسته | /lɔːs/<br>لاس | The packets that never arrive. | Packet loss makes a link slow. | loss |
| ازدحام | /kənˈdʒestʃən/<br>کانجِسچِن | Too much traffic at the same time. | Congestion happens at peak hours. | congestion |
| برخورد داده | /kəˈlɪʒn/<br>کولیزِن | Two frames that meet on one line. | An old hub caused collisions. | collision |
| پخش همگانی | /ˈbrɔːdkæst/<br>برادکست | To send to all the nodes at once. | Two points broadcast on one frequency. | broadcast |
| انتقال دادن | /trænsˈmɪt/<br>ترَنسِمیـت | To send data through a medium. | Too many nodes transmit at once. | transmit |
| تحویل دادن | /dɪˈlɪvər/<br>دیلیوِر | To bring data to the right place. | The router delivers the packets. | deliver |
| رمزگشایی کردن | /diːˈkrɪpt/<br>دیکریپت | To read a message that was in code. | Only the receiver can decrypt it. | decrypt |
| احراز هویت کردن | /ɔːˈθentɪkeɪt/<br>اُثِنتِیکِیت | To check who a user really is. | Programs authenticate the users. | authenticate |
| تبدیل نام به نشانی | /rɪˈzɑːlv/<br>ریزالو | To change a domain name into an IP address. | DNS resolves a domain name. | resolve |
| مسیر | /ruːt/<br>رویـت | The way that a packet goes. | The router chooses the best route. | route |
| پرش | /hɑːp/<br>هاپ | One step from one router to the next. | The packet goes to the next hop. | hop |
| پیکربندی کردن | /kənˈfɪɡjər/<br>کانفیگیـر | To set the options of a device. | You can configure a logical segment. | configure |
| اندازه‌گیری کردن | /ˈmeʒər/<br>مِژِر | To find the size or the amount of something. | We measure the throughput. | measure |
| بزرگ شدن | /skeɪl/<br>اِسکِیل | To grow and still work well. | A good design can scale to ten thousand nodes. | scale |

**جدول ۳ — کیفیت، امنیت و صفت‌های شبکه (Quality, Security and Network Adjectives)**

| فارسی | تلفظ | Definition (EN) | Example (EN) | English |
|---|---|---|---|---|
| قابل اعتماد | /rɪˈlaɪəbl/<br>ریلایِبُل | Working well almost every time. | The internal network is reliable. | reliable |
| سیمی | /ˈwaɪərd/<br>وایِرد | Connected with a cable. | Ethernet is a wired technology. | wired |
| پهن‌باند | /ˈbrɔːdbænd/<br>برادبَند | A fast connection with a wide band. | A broadband line has high throughput. | broadband |
| نوری | /ˈɑːptɪkl/<br>آپتیکَل | Working with light. | An optical fibre is very fast. | optical |
| آنالوگ | /ˈænəlɔːɡ/<br>اَنالاگ | With a signal that changes like a wave. | An old analog line cannot do this. | analog |
| فیزیکی | /ˈfɪzɪkl/<br>فیزیکَل | Real and touchable. | The NIC has a physical connector. | physical |
| مجازی | /ˈvɜːrtʃuəl/<br>ویرچوال | Not real, but working like the real thing. | A modern network is also virtual. | virtual |
| ارتقا دادن | /ˌʌpˈɡreɪd/<br>آپگرِید | To change something for a better one. | She has upgraded her workstation. | upgrade |
| زمان از کار افتادگی | /ˈdaʊntaɪm/<br>داون‌تَیم | The time when a system does not work. | Downtime costs money. | downtime |
| زمان کارکرد | /ˈʌptaɪm/<br>آپ‌تَیم | The time when a system works. | The uptime is more than 99 percent. | uptime |
| قطعی | /ˈaʊtɪdʒ/<br>اوتِیج | A longer period without service. | An outage lasted two hours. | outage |
| گلوگاه | /ˈbɑːtəlnek/<br>باتِل‌نِک | A part that slows the whole system. | The network becomes a bottleneck. | bottleneck |
| عیب، خطا | /fɔːlt/<br>فالت | Something that is not working right. | If one route has a fault, another helps. | fault |
| افزونگی | /rɪˈdʌndənsi/<br>ریداندِنسی | Extra parts so a fault is not serious. | Redundancy keeps the system alive. | redundancy |
| تاب‌آور | /rɪˈzɪliənt/<br>ریزیلیِنت | Able to work again after a problem. | A mesh network is very resilient. | resilient |
| محدود | /ˈlɪmɪtɪd/<br>لیمیتِد | Not very big or not very much. | A limited budget is not a big problem. | limited |
| اختصاصی | /ˈdedɪkeɪtɪd/<br>دِدیکِیتِد | Only for one user or one job. | A dedicated line has a higher price. | dedicated |
| اوج | /piːk/<br>پیک | The busiest time. | At peak hours the latency grows. | peak |
| معمول، نمونه‌ای | /ˈtɪpɪkl/<br>تیپیکَل | Like most others. | A typical uptime is 99 percent. | typical |
| ثابت | /ˈkɑːnstənt/<br>کانستَنت | Not changing. | The delay is not constant. | constant |
| متغیر | /ˈveriəbl/<br>وِریَبُل | Changing all the time. | Jitter is a variable latency. | variable |
| تداخل امواج | /ˌɪntərˈfɪrəns/<br>اینتِرفیرِنس | Two signals that disturb each other. | Interference from other devices is common. | interference |
| مانع | /ˈɑːbstəkl/<br>آبستِکُل | Something that stops or weakens a signal. | Obstacles such as walls reduce the signal. | obstacle |
| فاصله | /ˈdɪstəns/<br>دیستَنس | The space between two places. | Copper is good for short distances. | distance |
| نزدیک | /ˌnɪrˈbaɪ/<br>نیربای | Not far away. | Two nearby points can interfere. | nearby |
| دور | /rɪˈmoʊt/<br>ریموت | Far away. | A satellite reaches a remote village. | remote |
| داخلی | /ɪnˈtɜːrnl/<br>اینتِرنال | Inside one place. | The internal network is fast. | internal |
| مرکزی | /ˈsentrəl/<br>سِنتِرال | In the middle, joining the parts. | One central switch joins the buildings. | central |
| توزیع‌شده | /dɪˈstrɪbjuːtɪd/<br>دیستریبیتِد | Spread over many places. | The servers are distributed. | distributed |
| مقیاس‌پذیر | /ˈskeɪləbl/<br>اِسکِیلَبُل | Able to grow bigger without problems. | A good design is scalable. | scalable |

---

### 3. Reading / متن اصلی

**عنوان متن: The Invisible Roads (جاده‌های نامرئی)**

**[1]** A network is a group of computers that are connected together. With a network, we can send a file from one computer to another, use the same printer, and share an internet connection. Networks are everywhere: at home, at a university, and in every office. They are the physical and logical base of the modern world.

**[2]** The smallest network is a LAN: a local area network inside one building or one room. The largest is a WAN: a wide area network that covers cities or countries. The internet itself is not one network; it is a network of networks. A WAN usually connects many LANs together.

**[3]** Every device in a network is a node. A node can be a workstation, a server, a printer, or even a phone. One node can be a client that asks for data, and another node can be a server that gives data. This is the client–server model, and most services on the internet use it.

**[4]** How does a computer join a network? Every device needs an interface: a network interface card or NIC. The NIC has a physical connector for a cable and an antenna for wireless signals. It also has a unique MAC address, a kind of serial number that the device keeps for its whole life.

**[5]** What is the medium of a network? The medium is the way that data travels: a copper cable, an optical fibre, or the air. Copper cable is cheap, and it is good for short distances. An optical fibre carries light, so it is very fast and it works over long distances. Wireless networks use radio waves through the air.

**[6]** Ethernet is the most common technology in wired networks. An Ethernet cable has a small connector at each end, and it goes into a port on the NIC. Wired connections are usually faster and more stable than wireless ones, but you cannot move your laptop far from the cable.

**[7]** Wireless networks are different. A wireless access point sends and receives radio waves, and a device with an antenna can connect to it. The frequency of the signal is important: 2.4 GHz travels further, and 5 GHz is faster but shorter. Obstacles such as thick walls reduce the signal.

**[8]** How do devices find each other inside a LAN? A switch connects the nodes of one LAN. It reads the MAC address in every frame and sends the frame only to the correct endpoint. This is much better than an old hub, which sent every frame to every node and caused many collisions.

**[9]** A bridge joins two small networks, and a repeater makes a weak signal strong again so it can travel a longer distance. A modern repeater is often simple: you put it in a room with a weak signal, and it repeats the wireless signal for the whole house.

**[10]** What connects your home to the internet? A modem. The modem changes the signal from the telephone line or the cable network into a digital signal for your devices. It is the gateway between your LAN and your internet provider, and it usually has a port for the WAN side.

**[11]** A router is more intelligent than a modem. The router joins two or more networks and chooses the best route for every packet. Routing is the work of the router: it looks at the IP address and sends the packet to the next hop on the way.

**[12]** Data never travels as one big piece. The sender divides the data into small packets. Every packet has a header with the address of the sender and the address of the destination, and a payload that carries the real data. The packets can travel by different routes, and the receiver puts them together again.

**[13]** This method is called packet switching, and it is very strong. If one route has a fault, the router can deliver the packets by another way. A network with a second path is more resilient, and this idea is called redundancy. In a big network, redundancy keeps the whole system alive.

**[14]** How do the packets know where to go? Every device in an IP network needs an IP address, like a postal address. An IPv4 address has four numbers between 0 and 255. Because the world has more devices than addresses, the newer IPv6 uses much longer addresses and can support almost unlimited nodes.

**[15]** A subnet is a smaller part of a network. In one LAN, a subnet can keep all the computers of one office together. The interface of each device has an address inside the subnet, and the gateway connects the subnet to the wider network.

**[16]** A protocol is a set of rules for communication. Without protocols, two devices cannot understand each other. The most important family of protocols is TCP/IP, and every device on the internet uses it. TCP divides the data and checks that every packet arrives; IP moves the packets between networks.

**[17]** Other protocols do other jobs. HTTP moves the pages of the web, and HTTPS does the same job with encryption. SMTP sends email. DNS is the address book of the internet: it resolves a domain name into an IP address, because people remember names better than numbers.

**[18]** When you open a page, several things happen in a second. Your device sends a request to the DNS server and receives an IP address. Then it sends packets to that address, and the server sends the answer back. This short conversation at the start of a connection is called a handshake.

**[19]** The shape of a network is its topology. In a star topology, every node connects to one central switch; this is the most common design today. In a ring topology, the nodes form a circle. In a mesh topology, every node connects to many other nodes, so the network is very resilient.

**[20]** How fast is a network? Throughput is the real amount of data that moves in one second, and it is usually measured in megabits or gigabits. A broadband connection at home can have a throughput of 100 megabits per second; a fibre line in a university can be much higher.

**[21]** Latency is different from throughput. Latency is the delay: the time that one packet needs to travel from the sender to the receiver. It is measured in milliseconds, and a ping shows the latency. Jitter is a variable latency: the delay is not constant, and this is a problem for video calls.

**[22]** Congestion happens when too many nodes transmit at the same time. The network becomes a bottleneck, and some packets are lost. Packet loss makes a connection slow and unreliable. At peak hours, the average latency of a home network can become two or three times higher than usual.

**[23]** How do we measure the quality of a network? Uptime is the time that the network works, and downtime is the time that it does not work. An outage is a longer period without service, and it costs money. A private, dedicated line has a higher price, but it gives a typical uptime of more than 99 percent.

**[24]** In a university, a central switch joins the buildings, and many access points give wireless coverage in every classroom. The internal network is fast and reliable, and the external line to the internet provider is a fibre connection. Faults are rare, but the network team checks the logs and the interfaces every week.

**[25]** A modern network is also virtual in many places. You can configure a logical segment without a new cable, upgrade the equipment, or add a second line. A limited budget is not always a big problem: a good design is scalable, and it can scale from ten nodes to ten thousand nodes. Networks are the hidden backbone of everything that we do online.

**[26]** Wireless networks have their own vocabulary. A mobile tower or a satellite can carry a signal to a remote village where no cable exists. The radio signal becomes weaker with distance, and interference from other devices is common. If two access points are nearby, they can broadcast on the same frequency and disturb each other.

**[27]** A modern network can also be distributed: the servers are not in one central room but in many places. Security work is part of the design. Programs authenticate the users, and strong encryption means that other people cannot read the data. If a message is encrypted, only the correct receiver can decrypt it. An old analog telephone line cannot do this.

**[28]** What tools does a network engineer use? The ping command shows whether a remote node answers. A command like ipconfig or ifconfig shows the IP address and the subnet of your interface. If a device cannot get an address, the DHCP service usually gives it a new one automatically. Then the engineer can measure the throughput and check the logs for faults.

**[29]** Security is different in a network. A firewall at the gateway stops dangerous traffic before it enters the LAN. A VPN encrypts the data between a remote worker and the office, so an open public network is less dangerous. Companies also divide a big network into segments, because a smaller inside network is easier to protect.

**[30]** Networks are not magic. They are nodes, cables, radio waves, and rules. A small home network and a huge university network use the same ideas: addresses, packets, protocols, and a clear design. If you understand these four ideas, you can understand every network, from a phone hotspot to the backbone of the internet.

*(۱۵۷۶ واژه — ۳۰ پاراگراف)*

---

### 4. Persian Translation / ترجمه فارسی

**ترجمهٔ پاراگراف‌های کلیدی:**

**[۱]** شبکه گروهی از کامپیوترهاست که به هم وصل شده‌اند. با یک شبکه می‌توانیم فایلی را از یک کامپیوتر به کامپیوتر دیگر بفرستیم، از یک چاپگر مشترک استفاده کنیم و یک اتصال اینترنت را به اشتراک بگذاریم. شبکه‌ها همه‌جا هستند: در خانه، در دانشگاه و در هر دفتری. آن‌ها پایهٔ فیزیکی و منطقی جهان امروزند.

**[۲]** کوچک‌ترین شبکه یک LAN است: شبکهٔ محلی درون یک ساختمان یا یک اتاق. بزرگ‌ترین آن یک WAN است: شبکهٔ گسترده‌ای که شهرها یا کشورها را پوشش می‌دهد. خودِ اینترنت یک شبکه نیست؛ شبکه‌ای از شبکه‌هاست. یک WAN معمولاً بسیاری از LANها را به هم وصل می‌کند.

**[۸]** دستگاه‌ها درون یک LAN چگونه یکدیگر را پیدا می‌کنند؟ یک سوئیچ گره‌های یک LAN را به هم وصل می‌کند. نشانی فیزیکی (MAC) را در هر قالب می‌خواند و قالب را فقط به نقطهٔ پایانی درست می‌فرستد. این بسیار بهتر از یک هاب قدیمی است که هر قالب را به هر گره می‌فرستاد و برخوردهای زیادی ایجاد می‌کرد.

**[۱۱]** روتر از مودم هوشمندتر است. روتر دو یا چند شبکه را به هم می‌پیوندد و بهترین مسیر را برای هر بستهٔ داده انتخاب می‌کند. مسیریابی کار روتر است: به نشانی شبکه (IP) نگاه می‌کند و بسته را در مسیر به پرش بعدی می‌فرستد.

**[۱۲]** داده هرگز به‌صورت یک قطعهٔ بزرگ سفر نمی‌کند. فرستنده داده را به بسته‌های کوچک تقسیم می‌کند. هر بسته یک سرآیند با نشانی فرستنده و نشانی مقصد دارد و یک محتوای بسته که دادهٔ واقعی را حمل می‌کند. بسته‌ها می‌توانند از مسیرهای مختلف بروند و گیرنده دوباره آن‌ها را کنار هم می‌گذارد.

**[۱۶]** پروتکل مجموعه‌ای از قواعد برای ارتباط است. بدون پروتکل‌ها، دو دستگاه نمی‌توانند یکدیگر را بفهمند. مهم‌ترین خانوادهٔ پروتکل‌ها TCP/IP است و هر دستگاه روی اینترنت از آن استفاده می‌کند. TCP داده را تقسیم می‌کند و بررسی می‌کند که هر بسته برسد؛ IP بسته‌ها را میان شبکه‌ها جابه‌جا می‌کند.

**[۲۰]** شبکه چقدر سریع است؟ توان عبوری، مقدار واقعی داده‌ای است که در یک ثانیه جابه‌جا می‌شود و معمولاً با مگابیت یا گیگابیت اندازه‌گیری می‌شود. یک اتصال پهن‌باند در خانه می‌تواند توان عبوری ۱۰۰ مگابیت بر ثانیه داشته باشد؛ یک خط فیبر در دانشگاه می‌تواند بسیار بیشتر باشد.

**[۲۱]** تأخیر با توان عبوری متفاوت است. تأخیر یعنی دیرکرد: زمانی که یک بسته لازم دارد تا از فرستنده به گیرنده برسد. با میلی‌ثانیه اندازه‌گیری می‌شود و پینگ تأخیر را نشان می‌دهد. لرزش تأخیر، تأخیری متغیر است: دیرکرد ثابت نیست و این برای تماس تصویری مشکل است.

**خلاصهٔ فارسی متن:**

این درس نشان می‌دهد داده در شبکه چگونه از نقطه‌ای به نقطهٔ دیگر می‌رسد. شبکه‌ها در دو مقیاس اصلی دسته‌بندی می‌شوند: شبکهٔ محلی (LAN) درون یک ساختمان و شبکهٔ گسترده (WAN) میان شهرها و کشورها؛ اینترنت خود شبکه‌ای از شبکه‌هاست. هر دستگاه یک گره است و برای پیوستن به شبکه به کارت شبکه (NIC) با نشانی فیزیکی (MAC) و نشانی شبکه (IP) نیاز دارد. داده از بستر انتقال (کابل مسی، فیبر نوری یا امواج رادیویی) عبور می‌کند.

داده به بسته‌های کوچک تقسیم می‌شود؛ هر بسته سرآیند و محتوای بسته دارد و بسته‌ها می‌توانند از مسیرهای متفاوت بروند (سوئیچ‌کردن بسته). روتر بهترین مسیر را انتخاب می‌کند و سوئیچ قالب‌ها را درون LAN به نقطهٔ پایانی درست می‌فرستد. پروتکل‌ها این ارتباط را ممکن می‌کنند: TCP/IP ستون اصلی است، HTTP و HTTPS صفحه‌های وب را جابه‌جا می‌کنند و DNS نام دامنه را به نشانی IP تبدیل می‌کند.

کیفیت شبکه با معیارهایی سنجیده می‌شود: توان عبوری (مقدار واقعی داده در ثانیه)، تأخیر و پینگ، لرزش تأخیر، افت بسته، ازدحام در ساعت‌های اوج، و زمان کارکرد در برابر زمان از کار افتادگی. افزونگی و طراحی چندمسیره شبکه را تاب‌آور می‌کند و توپولوژی‌های ستاره‌ای، حلقه‌ای و توری شکل‌های رایج شبکه‌اند. در پایان، امنیت شبکه با دیوار آتش، رمزنگاری، احراز هویت و تقسیم شبکه به بخش‌ها تأمین می‌شود؛ طراحی مقیاس‌پذیر و مجازی به شبکه اجازه می‌دهد از ده گره تا ده‌ها هزار گره رشد کند.

---

### 5. Comprehension Check / درک مطلب

**الف) چهارگزینه‌ای — ده سؤال**

1. What is the smallest kind of network?
   a) a WAN
   b) a LAN
   c) the internet

2. What does a NIC have?
   a) a physical connector and an antenna
   b) a mouse and a keyboard
   c) a battery and a charger

3. Which medium is very fast over long distances?
   a) copper cable
   b) an optical fibre
   c) a telephone line

4. What does a switch read in every frame?
   a) the MAC address
   b) the payload
   c) the password

5. What is the work of a router?
   a) to change the signal into a digital signal
   b) to choose the best route for every packet
   c) to send every frame to every node

6. Why was an old hub worse than a switch?
   a) because it was too fast
   b) because it sent every frame to every node and caused collisions
   c) because it needed fibre

7. What does DNS do?
   a) it moves web pages
   b) it resolves a domain name into an IP address
   c) it encrypts the connection

8. What is latency?
   a) the real amount of data in one second
   b) the time that one packet needs to travel
   c) the number of nodes in a network

9. What happens at peak hours?
   a) the network becomes a bottleneck and some packets are lost
   b) the uptime becomes 100 percent
   c) the frequency becomes higher

10. Why do companies divide a big network into segments?
   a) because a smaller inside network is easier to protect
   b) because segments are cheaper than cables
   c) because segments make the latency zero

**ب) صحیح یا غلط — ده سؤال**

1. The internet is one single network. (..........)
2. An optical fibre carries light. (..........)
3. A wired connection is usually more stable than a wireless one. (..........)
4. A modem is more intelligent than a router. (..........)
5. Data travels in small packets, not in one big piece. (..........)
6. Redundancy makes a network less resilient. (..........)
7. IPv6 uses longer addresses than IPv4. (..........)
8. Jitter is a delay that never changes. (..........)
9. A dedicated line has a higher price but a high uptime. (..........)
10. A scalable design can grow from ten nodes to ten thousand nodes. (..........)

**پ) پاسخ کوتاه — شش سؤال**

1. What are three things that people can do with a network?
2. What is the difference between a node and an endpoint?
3. Why do the packets of one message travel by different routes?
4. What are the four things inside every packet that this lesson describes? *(header, payload, source address, destination address)*
5. Why is jitter a problem for video calls?
6. What does the DHCP service do?

**ت) ایدهٔ اصلی — دو سؤال**

۱. ایدهٔ اصلی کل متن کدام جمله است؟

a) A network is nodes, media, and rules: packets travel by routes, protocols make sense of them, and design decides the quality and the security.
b) IPv6 can support almost unlimited nodes.
c) An old hub caused many collisions.

۲. پاراگراف [۲۱] بیشتر دربارهٔ چه چیزی است؟

a) Latency and jitter are delays, and they are different from throughput.
b) Uptime and downtime measure the quality of a network.
c) A ping command shows whether a node answers.

**ث) تطبیق — دو جدول**

**جدول ۱:** هر واژه (۱ تا ۵) را به معنی درست آن (الف تا ه) وصل کنید.

| # | Word | | Meaning |
|---|---|---|---|
| 1 | topology | الف | too much traffic at the same time |
| 2 | protocol | ب | the shape or plan of a network |
| 3 | congestion | پ | the main, high-speed part of a network |
| 4 | backbone | ت | extra parts so a fault is not serious |
| 5 | redundancy | ث | a set of rules for communication |

**جدول ۲:** هر واژه (۱ تا ۵) را به معنی درست آن (الف تا ه) وصل کنید.

| # | Word | | Meaning |
|---|---|---|---|
| 1 | resolve | الف | to send to all the nodes at once |
| 2 | broadcast | ب | to read a message that was in code |
| 3 | decrypt | پ | to change a domain name into an IP address |
| 4 | authenticate | ت | to set the options of a device |
| 5 | configure | ث | to check who a user really is |

---

### 6. Vocabulary Practice / تمرین واژگان

**الف) جای خالی — بیست سؤال**

از واژه‌های داخل کادر استفاده کنید. هر واژه یک بار.

> **واژه‌ها:** LAN · WAN · node · gateway · access point · NIC · MAC address · IP address · subnet · Ethernet · fibre · repeater · antenna · backbone · interface · medium · frequency · topology · packet · header · bottleneck

1. A .......... covers one building, and a .......... covers many cities.
2. Every device that is connected to a network is a .......... .
3. The .......... joins your subnet to the wider network.
4. A wireless .......... sends and receives radio waves in a room.
5. Every device needs a .......... to join a network.
6. The switch reads the .......... in every frame.
7. Every node in an IP network needs an .......... .
8. A .......... is a smaller part of a network.
9. .......... is the most common technology in wired networks.
10. An optical .......... carries light and works over long distances.
11. A .......... makes a weak signal strong again.
12. The NIC has a small .......... for radio waves.
13. The main, high-speed part of a big network is the .......... .
14. The .......... of a device is the point where it joins the network.
15. Copper cable, fibre, and air are three kinds of .......... .
16. The .......... of the signal decides the range and the speed.
17. The shape or plan of a network is its .......... .
18. The sender divides the data into small .......... .
19. Every packet has a .......... with the addresses of the sender and the destination.
20. At peak hours the network becomes a .......... .

**ب) وصل کردن — ده سؤال**

هر واژه را به معنی درست آن وصل کنید.

| # | Word | | Meaning |
|---|---|---|---|
| 1 | throughput | الف | the packets that never arrive |
| 2 | latency | ب | the time when a system works |
| 3 | jitter | پ | the real amount of data in one second |
| 4 | loss | ت | a longer period without service |
| 5 | uptime | ث | a delay that changes all the time |
| 6 | downtime | ج | the time for one packet to travel |
| 7 | outage | چ | the time when a system does not work |
| 8 | bottleneck | ح | able to work again after a problem |
| 9 | resilient | خ | to grow and still work well |
| 10 | scale | د | a part that slows the whole system |

**پ) جمله‌سازی — ده سؤال**

با هر واژه یک جملهٔ انگلیسی **در حال کامل** بنویسید. هر جمله دست‌کم ۶ واژه داشته باشد و به تجربه یا کار تازه‌تمام‌شده اشاره کند.

1. configure
2. upgrade
3. measure
4. transmit
5. deliver
6. authenticate
7. decrypt
8. resolve
9. reset *(برای روتر)*
10. check *(برای ثبت‌ها / logs)*

**ت) واژه‌سازی: پیشوند و پسوند — یک تمرین**

پیشوند در **ابتدای** واژه و پسوند در **پایان** واژه می‌آید و معنای آن را تغییر می‌دهد:

| پیشوند / پسوند | معنی | نمونه |
|---|---|---|
| -work | کار، ساختار | net ← network |
| trans- | از این سو به آن سو | mit ← transmit |
| broad- | گسترده، پهن | band ← broadband |
| -age | اسم ساختن (فرایند یا چیز) | pack ← package |
| mega- | یک میلیون برابر | bit ← megabit |
| giga- | یک میلیارد برابر | bit ← gigabit |

با افزودن پیشوند یا پسوند درست، واژهٔ مناسب بسازید.

1. net ← .......... (شبکه)
2. mit ← .......... (انتقال دادن)
3. band ← .......... (پهن‌باند)
4. pack ← .......... (بستهٔ نرم‌افزاری یا بستهٔ داده)
5. bit ← .......... (یک میلیون بیت)
6. bit ← .......... (یک میلیارد بیت)

---

### 7. Grammar Focus / نکتهٔ گرامری

**موضوع: حال کامل (present perfect) · for / since · تفاوت با گذشتهٔ ساده**

**توضیح فارسی:**

**حال کامل** با *have / has* + **قسمت سوم فعل** (past participle) ساخته می‌شود و برای چهار کار به کار می‌رود: ① **تجربه** در زندگی: *I have used a fibre connection.* ② کاری که **همین حالا تمام شده** و نتیجه‌اش مهم است: *The network has stopped.* ③ وضعیتی که از گذشته **تا حال ادامه دارد**: *I have worked in this team for two years.* ④ همراه *just, already, yet, ever, never*: *The packets have just arrived. / Have you finished yet?*

**for و since:** با *for* مدت زمان را می‌گوییم (*for three years*) و با *since* نقطهٔ شروع را (*since 2022*).

**منفی و سؤالی:** *I have not (haven't) configured the switch. / She has not (hasn't) seen this error.* سؤالی: *Have you ever used a VPN? / Has the router delivered the packets?* پاسخ کوتاه: *Yes, I have. / No, it hasn't.*

**تفاوت با گذشتهٔ ساده:** گذشتهٔ ساده زمان **مشخص** دارد (*I configured the router yesterday. / She joined the team in 2023.*)؛ حال کامل زمان مشخص ندارد و به حال مربوط است (*I have configured the router. / She has been in the team for two years.*). پس با *yesterday, last week* از گذشتهٔ ساده و با *already, yet, ever, never* از حال کامل استفاده می‌کنیم.

**قسمت سوم فعل‌های بی‌قاعده** را باید حفظ کرد: *be → been*, *do → done*, *go → gone*, *see → seen*, *write → written*, *take → taken*, *give → given*, *send → sent*, *find → found*, *build → built*, *break → broken*, *lose → lost*, *speak → spoken*.

دو خطای رایج فارسی‌زبانان: ① استفاده از گذشتهٔ ساده به‌جای قسمت سوم («I have saw» ← ~~have saw~~ / *have seen*)؛ ② آوردن *has* با فاعل جمع («They has finished» ← ~~They has~~ / *They have finished*).

**جدول ۱ — ساختار حال کامل:**

| ضمیر فاعلی | مثبت | منفی |
|---|---|---|
| I / you / we / they | I have (I've) configured the router. | I have not (haven't) configured it. |
| he / she / it | She has (She's) upgraded the switch. | She has not (hasn't) upgraded it. |

**جدول ۲ — سؤالی و پاسخ کوتاه:**

| پرسش | پاسخ کوتاه |
|---|---|
| Have you ever used a VPN? | Yes, I have. / No, I haven't. |
| Has the network stopped again? | Yes, it has. / No, it hasn't. |
| Have they measured the latency? | Yes, they have. / No, they haven't. |

**جدول ۳ — for / since و تفاوت با گذشتهٔ ساده:**

| نشانه | نمونه |
|---|---|
| for + مدت | I have worked in this lab for two years. |
| since + نقطهٔ شروع | The lab has had a fibre line since 2022. |
| just / already / yet | The packets have just arrived. · Have you finished yet? |
| گذشتهٔ ساده (زمان مشخص) | I configured the router yesterday. |
| حال کامل (بدون زمان مشخص) | I have configured the router. |

**پنج مثال از دنیای کامپیوتر:**

1. I have configured three subnets this week.
2. She has already upgraded her workstation.
3. The engineer has measured the throughput.
4. Have you ever used a satellite connection?
5. We have not received any packets since nine o'clock.

**تمرین‌ها — چهل سؤال**

**الف) جمله‌ها را با حال کامل کامل کنید (۱ تا ۱۴).**

1. I .......... (configure) the new router.
2. She .......... (upgrade) her workstation.
3. They .......... (install) a new switch.
4. The network .......... (stop) three times today.
5. We .......... (measure) the throughput.
6. He .......... (transmit) the packets.
7. I .......... (use) this VPN before.
8. The server .......... (deliver) all the packets.
9. You .......... (change) the subnet.
10. Our team .......... (test) the fibre line.
11. They .......... (solve) the congestion problem.
12. The engineer .......... (authenticate) the user.
13. We .......... (check) the logs.
14. My laptop .......... (connect) to the wrong access point.

**ب) جمله‌ها را منفی کنید (۱۵ تا ۲۰).**

15. I .......... (not / finish) the configuration.
16. She .......... (not / see) this error before.
17. The network .......... (not / return) to normal.
18. We .......... (not / receive) any packets.
19. He .......... (not / configure) the gateway.
20. They .......... (not / upgrade) the repeater.

**پ) جمله‌ها را سؤالی کنید یا پاسخ کوتاه بدهید (۲۱ تا ۲۶).**

21. .......... you ever .......... (use) a fibre connection? *(سؤالی)*
22. .......... the network .......... (stop) again? *(سؤالی)*
23. .......... she .......... (check) the interface? *(سؤالی)*
24. Have you configured the subnet? — Yes, .......... .
25. Has the router delivered the packets? — No, .......... .
26. Have they measured the latency? — Yes, .......... .

**ت) قسمت سوم این فعل‌ها را بنویسید (۲۷ تا ۳۴).**

27. see → .......... 
28. write → .......... 
29. take → .......... 
30. build → .......... 
31. break → .......... 
32. choose → .......... 
33. speak → .......... 
34. lose → .......... 

**ث) گذشتهٔ ساده یا حال کامل؟ شکل درست را بنویسید (۳۵ تا ۳۸).**

35. I .......... (configure) the router yesterday.
36. I .......... (already / configure) the router.
37. She .......... (join) the network team in 2023.
38. She .......... (be) in the network team for two years.

**ج) با for یا since کامل کنید (۳۹ تا ۴۰).**

39. We have used this switch .......... three years.
40. The lab has had a fibre line .......... 2022.

---

### 8. Key Sentences Translation / ترجمهٔ جمله‌های کلیدی

**انگلیسی ← فارسی (۱۰ جمله)**

1. A LAN covers one building, and a WAN covers many cities.
2. Every packet has a header with the address of the destination.
3. The router chooses the best route for every packet.
4. DNS resolves a domain name into an IP address.
5. A switch reads the MAC address and sends the frame to one endpoint.
6. Congestion happens when too many nodes transmit at the same time.
7. Latency is measured in milliseconds, and a ping shows it.
8. We have measured the throughput of the fibre line.
9. The engineer has not configured the gateway yet.
10. Have you ever used a mesh network?

**فارسی ← انگلیسی (۱۰ جمله)**

1. هر دستگاه در شبکه یک گره است.
2. سوئیچ قالب‌ها را درون LAN می‌فرستد.
3. روتر بهترین مسیر را انتخاب می‌کند.
4. ازدحام در ساعت‌های اوج پیش می‌آید.
5. ما توان عبوری را اندازه‌گیری کرده‌ایم.
6. من تا حالا از وی‌پی‌ان استفاده نکرده‌ام.
7. آیا تو در این آزمایشگاه کار کرده‌ای؟
8. شبکه از ساعت نه قطع شده است.
9. افزونگی شبکه را تاب‌آور می‌کند.
10. آن‌ها سوئیچ را ارتقا داده‌اند.

---

### 9. Writing Task / تمرین نگارش

**موضوع: My Experience with Networks — تجربهٔ من با شبکه‌ها**

یک نوشتهٔ کوتاه بنویسید و در آن توضیح دهید چه تجربه‌ای با شبکه‌ها داشته‌اید. این موارد را بگنجانید:

- چه نوع شبکه‌ای را خودتان راه‌اندازی یا پیکربندی کرده‌اید؟ (شبکهٔ خانه، اتصال کابل، تنظیم روتر، نقطهٔ دسترسی)
- چه چیزی درست پیش نرفت و شما چه کردید؟ (سیگنال ضعیف، ازدحام، مهلت، قطعی)
- چه مهارتی در این مسیر به دست آورده‌اید؟
- یک برنامه یا هدف برای آینده در این زمینه.

**شرایط نگارش:**

- نوشته بین **۱۲۰ تا ۲۰۰ واژه** باشد.
- دست‌کم **۵ جمله** در **حال کامل** بنویسید (با *for*, *since*, *already*, *yet* یا *ever*).
- دست‌کم **۲ جمله** در **گذشتهٔ ساده** با زمان مشخص داشته باشد.
- دست‌کم **۱۰ واژه** از جدول‌های واژگان بخش ۲ استفاده شود.

---

### 10. Mini Project / پروژهٔ کوچک

**انشا (نیمه‌تحقیقی): گزارش یک شبکهٔ واقعی**

یک شبکهٔ واقعی را که خودتان از آن استفاده می‌کنید انتخاب کنید: شبکهٔ خانه، خوابگاه، آزمایشگاه دانشگاه، یا شبکهٔ کتابخانه. دربارهٔ آن یک گزارش کوتاه بنویسید و این بخش‌ها را بیاورید:

- **نقشه:** یک **شکل دستی ساده** از شبکه بکشید و در آن گره‌ها، سوئیچ یا روتر، مودم و نقطه‌های دسترسی را مشخص کنید.
- **اجزا:** کدام بخش سیمی و کدام بخش بی‌سیم است؟ چه رسانه‌ای استفاده شده (مس، فیبر، امواج رادیویی)؟
- **اندازه‌گیری:** اگر می‌توانید، با فرمان «ping» یک نشانی معتبر تأخیر را اندازه بگیرید و عدد را بنویسید؛ در غیر این صورت فرض کنید و بنویسید.
- **کیفیت:** کجا سیگنال ضعیف است، چه ساعت‌هایی ازدحام هست، و آیا تا حالا قطعی داشته‌اید؟
- **پیشنهادها:** سه پیشنهاد بنویسید که کیفیت این شبکه را بهتر می‌کند.

**شرایط نگارش:**

- گزارش را **دست‌نویس روی کاغذ** بنویسید و در **جلسهٔ بعد** به مدرس تحویل دهید.
- دست‌کم **۲۰۰ واژه** باشد (بدون احتساب شکل).
- دست‌کم **۶ جمله** با **حال کامل** و **۳ جمله** با **گذشتهٔ ساده** داشته باشد.
- دست‌کم **۱۲ واژه** از جدول‌های واژگان بخش ۲ در گزارش باشد.

**واژه‌های یاری‌دهنده:** node · gateway · access point · subnet · throughput · latency · congestion · uptime · outage · wired · wireless · repeater

---

### 11. Did You Know? / آیا می‌دانستید؟

1. **The first message on the ARPANET in 1969 crashed after two letters: the engineers wanted to write "LOGIN", but the system stopped after "LO".**
   نخستین پیام روی آرپانت در سال ۱۹۶۹ پس از دو حرف از کار افتاد: مهندسان می‌خواستند «LOGIN» بنویسند، اما سیستم پس از «LO» متوقف شد.

2. **IPv4 offers about 4.3 billion addresses, and they ran out in the 2010s; IPv6 offers about 340 undecillion addresses.**
   IPv4 حدود ۴٫۳ میلیارد نشانی دارد که در دههٔ ۲۰۱۰ تمام شدند؛ اما IPv6 حدود ۳۴۰ آندیسیلیون نشانی فراهم می‌کند.

3. **Light in an optical fibre travels at about two thirds of its speed in a vacuum, so a ping to the other side of the world usually takes 100 to 200 milliseconds.**
   نور در فیبر نوری با حدود دو سوم سرعتش در خلأ حرکت می‌کند؛ پس پینگ به آن سوی جهان معمولاً ۱۰۰ تا ۲۰۰ میلی‌ثانیه است.

4. **DNS is one of the oldest services on the internet: it was designed in 1983, and the whole system still works on the same idea.**
   DNS یکی از قدیمی‌ترین سرویس‌های اینترنت است: در سال ۱۹۸۳ طراحی شد و کل سامانه هنوز با همان ایده کار می‌کند.

5. **The first web page, published in 1991, is still online, and it was only a simple text about the web project itself.**
   نخستین صفحهٔ وب که در سال ۱۹۹۱ منتشر شد، هنوز آنلاین است و فقط متنی ساده دربارهٔ خودِ پروژهٔ وب بود.

6. **A packet usually passes through 10 to 20 routers — that is, 10 to 20 "hops" — before it arrives at a server in another country.**
   یک بسته معمولاً پیش از رسیدن به سروری در کشور دیگر از ۱۰ تا ۲۰ روتر می‌گذرد؛ یعنی ۱۰ تا ۲۰ «پرش».

7. **The newest Wi-Fi standard, from 2024, can reach theoretical speeds of about 46 gigabits per second — about 10,000 times faster than the first Wi-Fi in 1997.**
   جدیدترین استاندارد وای‌فای از سال ۲۰۲۴ می‌تواند به سرعت نظری حدود ۴۶ گیگابیت در ثانیه برسد؛ حدود ۱۰ هزار برابر سریع‌تر از نخستین وای‌فای در ۱۹۹۷.

8. **The word "router" was used for network devices from the 1970s; before that, a router was a tool for cutting wood.**
   واژهٔ «router» از دههٔ ۱۹۷۰ برای دستگاه‌های شبکه به کار رفت؛ پیش از آن، روتر ابزاری برای بریدن چوب بود.
