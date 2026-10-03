# Lesson 20: Advanced Cybersecurity and Zero Trust

## Level: B2–C1
## Time: 90–120 minutes

> **درس ۲۰ — امنیت سایبری پیشرفته و اعتماد صفر**
> **نکتهٔ گرامری:** مجهول پیشرفته (advanced passive) · مجهول در زمان‌های کامل و با افعال وجهی · مجهول گزارشی و ساختار سببی
> **متن درس:** ۳۰۴۵ واژه (۳۳ پاراگراف) | **واژگان کلیدی:** ۱۲۳ واژه | **باند سطح:** B2–C1 (پیشرفته)

---

### 1. Lesson Objectives / اهداف درس

- اصول معماری اعتماد صفر را توضیح دهید و بگویید چرا مرز شبکه به‌تنهایی کافی نیست.
- اجزای کنترل دسترسی (کمترین اختیار، دسترسی در لحظهٔ نیاز، ارتقای موقت) را با واژگان دقیق شرح دهید.
- زنجیرهٔ حمله را مرحله‌به‌مرحله تحلیل کنید و برای هر مرحله یک نشانهٔ قابل تشخیص بنویسید.
- تفاوت پایش، تشخیص و پاسخ را بیان کنید و نقش قواعد تشخیص و تحلیل رفتاری را توضیح دهید.
- لایه‌های رمزنگاری، طبقه‌بندی داده و کنترل‌های حاکمیتی را در یک گزارش کوتاه ارزیابی کنید.
- ساختار مجهول پیشرفته را در نوشتار فنی به‌کار ببرید و آن را با شکل معلوم بازنویسی کنید.

---

### 2. Key Vocabulary / واژگان کلیدی

> تلفظ‌ها بر پایهٔ انگلیسی آمریکایی و در قالب IPA نوشته شده‌اند.

**جدول ۱ — اعتماد صفر و کنترل دسترسی (Zero Trust and Access Control)**

| فارسی | تلفظ | Definition (EN) | Example (EN) | English |
|---|---|---|---|---|
| اعتماد صفر | /ˈzɪroʊ trʌst/<br>زیرو تراست | The rule that nothing inside a network is trusted by position. | Zero trust treats the internal network as hostile. | zero trust |
| ریزقطعه‌بندی | /ˌmaɪkroʊˌseɡmenˈteɪʃn/<br>مایکرو‌سِگمِنتِیشِن | Dividing one network into many very small parts. | Microsegmentation kept the billing server alone. | microsegmentation |
| کمترین اختیار لازم | /liːst ˈprɪvəlɪdʒ/<br>لیست پریوِلِج | Giving only the permissions that the task requires. | Least privilege closed ninety old accounts. | least privilege |
| دسترسی کم‌دوام | /liːst ˈstændɪŋ ˈækses/<br>لیست استَندینگ اَکسِس | Permission that does not stay open after the task. | Least-standing access is the goal of the review. | least-standing access |
| دسترسی در لحظهٔ نیاز | /ˌdʒʌst ɪn ˈtaɪm ˈækses/<br>جاست این تایم اَکسِس | Permission that is created when it is requested. | Just-in-time access expires after two hours. | just-in-time access |
| دسترسی ممتاز | /ˈprɪvəlɪdʒd ˈækses/<br>پریوِلِجْد اَکسِس | The right to change systems and settings. | Privileged access was recorded for every session. | privileged access |
| ارتقای دسترسی | /ˌelɪˈveɪʃn/<br>اِلیوِیشِن | Raising an account to a higher level for a short time. | Elevation is granted for one task at a time. | elevation |
| احراز هویت پله‌ای | /ˈstep ʌp ɔːˌθentɪˈkeɪʃn/<br>استِپ آپ اُثِنتِکِیشِن | Asking for a stronger proof when the risk rises. | A payment change triggers step-up authentication. | step-up authentication |
| بدون‌رمز | /ˈpæswɜːrdləs/<br>پَس‌وِردلِس | Working without a password, using a key instead. | A passwordless login cannot be phished. | passwordless |
| کلید عبور | /ˈpæskiː/<br>پَس‌کی | A private key that stays on the user's device. | A passkey is stored in the device's secure chip. | passkey |
| کلید سخت‌افزاری | /sɪˈkjʊrəti kiː/<br>سِکیورِتی کی | A physical device that proves the user's identity. | One security key replaced six passwords. | security key |
| احراز هویت تطبیقی | /əˈdæptɪv ɔːˌθentɪˈkeɪʃn/<br>اَدَپتیو اُثِنتِکِیشِن | Changing the proof that is required by the risk level. | Adaptive authentication asked a second question. | adaptive authentication |
| راستی‌آزمایی پیوسته | /kənˌtɪnjuəs ˌverɪfɪˈkeɪʃn/<br>کانتینیوِس وِرِیفِکِیشِن | Checking the session again while it is open. | Continuous verification caught the stolen session. | continuous verification |
| وضعیت امنیتی دستگاه | /dɪˈvaɪs ˈpɑːstʃər/<br>دیوایس پاسچِر | The health and settings of a device that connects. | A bad device posture blocked the connection. | device posture |
| اثر انگشت دستگاه | /dɪˈvaɪs ˈfɪŋɡərprɪnt/<br>دیوایس فینگرپرینت | A set of features that identifies one device. | The device fingerprint changed after the upgrade. | device fingerprint |
| زیست‌سنجی رفتاری | /bɪˌheɪvjərəl ˌbaɪoʊˈmetrɪks/<br>بیهِیویُرَل بایومِتریکس | Measuring habits such as typing rhythm. | Behavioural biometrics spotted the odd typing speed. | behavioural biometrics |
| تأمین‌کنندهٔ هویت | /aɪˈdentəti prəˈvaɪdər/<br>آیدِنتِتی پروای‌دِر | The system that authenticates users for others. | The identity provider sent the claims to the app. | identity provider |
| ورود یک‌باره | /ˌsɪŋɡl ˈsaɪn ɑːn/<br>سینگُل ساین آن | One login that opens many applications. | Single sign-on reduced the number of passwords. | single sign-on |
| فدراسیون (هویت) | /ˌfedəˈreɪʃn/<br>فِدِرِیشِن | Trusting identities from another organisation. | Federation joined the clinic and the university. | federation |
| اظهارنامهٔ هویتی | /əˈsɜːrʃn/<br>اَسِرشِن | A signed statement that proves an identity. | The assertion was valid for five minutes. | assertion |
| ادعاهای هویتی | /kleɪmz/<br>کلِیمز | Facts about a user inside a token, such as a role. | The claims named the department and the shift. | claims |
| واگذاری اختیار | /ˌdelɪˈɡeɪʃn/<br>دِلیگِیشِن | Letting one service act for a user. | Delegation was limited to reading one folder. | delegation |
| مرز اختیار | /ˈprɪvəlɪdʒ ˈbaʊndri/<br>پریوِلِج باوندری | The line between ordinary and administrative work. | The privilege boundary was crossed at midnight. | privilege boundary |
| لایهٔ مدیریتی | /ədˌmɪnɪˈstreɪtɪv tɪr/<br>اَدمینیس‌ترِیتیو تیر | The separate world of administrative accounts. | Administrative tier accounts never open email. | administrative tier |
| میزبان پرش | /dʒʌmp hoʊst/<br>جامپ هوست | A server that is used to reach other servers. | Engineers log in through one jump host. | jump host |
| بستیون | /ˈbæstiən/<br>بَستیون | The only door from the office network to the inside. | The bastion recorded every administrative session. | bastion |
| ضبط نشست | /ˈseʃn rɪˈkɔːrdɪŋ/<br>سِشِن ریکور‌دینگ | Recording every action of an administrative session. | Session recording answered the audit question. | session recording |
| حکمرانی دسترسی | /ˈækses ˈɡʌvərnəns/<br>اَکسِس گاوِرنَنس | The rules and reviews that control who has what. | Access governance is a quarterly task. | access governance |
| حق دسترسی | /ɪnˈtaɪtlmənt/<br>این‌تایْتِلمِنت | One specific permission that a user holds. | The review listed every entitlement of the role. | entitlement |
| ترکیب خطرناک | /ˈtɑːksɪk ˌkɑːmbɪˈneɪʃn/<br>تاکسیک کامبینِیشِن | Two permissions that are dangerous together. | Approving a payment and changing the payee is a toxic combination. | toxic combination |
| لغو دسترسی | /ˌrevəˈkeɪʃn/<br>رِوُکِیشِن | Taking a permission or a session away. | Revocation must happen in minutes, not days. | revocation |

**جدول ۲ — تهدیدها و زنجیرهٔ حمله (Threats and the Attack Chain)**

| فارسی | تلفظ | Definition (EN) | Example (EN) | English |
|---|---|---|---|---|
| بازیگر تهدید | /θret ˈæktər/<br>ثرِت اَکتِر | A person or group that attacks systems. | The threat actor stayed quiet for eleven days. | threat actor |
| تهدید پیشرفتهٔ پایدار | /ədˌvænst pərˈsɪstənt θret/<br>اَدوَنست پِرسیستِنت ثرِت | A patient attack that hides for months. | An advanced persistent threat is not in a hurry. | advanced persistent threat |
| تهدید داخلی | /ˈɪnsaɪdər θret/<br>این‌سایدِر ثرِت | An attack that comes from someone with access. | The insider threat was a stolen account, not a person. | insider threat |
| ریسک داخلی | /ˈɪnsaɪdər rɪsk/<br>این‌سایدِر ریسک | The risk that is created by people who are already inside. | Insider risk is reduced by access review. | insider risk |
| سطح حمله | /əˈtæk sɜːrfɪs/<br>اَتَک سِرفِس | Everything that an attacker can try to reach. | The attack surface grew with every new service. | attack surface |
| مسیر حمله | /əˈtæk pæθ/<br>اَتَک پَث | The route from the first weak point to the data. | The attack path passed through one old printer. | attack path |
| حرکت جانبی | /ˈlætərəl ˈmuːvmənt/<br>لَتَرَل مووْمِنت | Moving from one internal machine to another. | Lateral movement was stopped by microsegmentation. | lateral movement |
| ارتقای اختیار (مهاجم) | /ˈprɪvəlɪdʒ ˌeskəˈleɪʃn/<br>پریوِلِج اِسکَلِیشِن | Getting a higher level of access than intended. | Privilege escalation turned a user into an administrator. | privilege escalation |
| تداوم حضور | /pərˈsɪstəns/<br>پِرسیستِنس | The mechanism that keeps an attacker alive. | Persistence survived the restart of the server. | persistence |
| زمان ماندگاری | /ˈdwel taɪm/<br>دوِل تایم | The time between the first entry and the discovery. | The dwell time was measured in months. | dwell time |
| زنجیرهٔ حمله | /ˈkɪl tʃeɪn/<br>کیل چِین | The ordered stages of an intrusion. | The kill chain starts with reconnaissance. | kill chain |
| فرمان و کنترل | /kəˈmænd ənd kənˈtroʊl/<br>کُمَند اَند کانترول | The channel that the attacker uses to give orders. | Command and control was hidden in normal traffic. | command and control |
| سیگنال‌دهی دوره‌ای | /ˈbiːkənɪŋ/<br>بیکُنینگ | A machine that contacts a server at fixed intervals. | Beaconing every ten minutes gave the attacker away. | beaconing |
| دامنه ربایی تایپی | /ˈtaɪpoʊskwɑːtɪŋ/<br>تایپو‌اسکواتینگ | A fake domain that looks like a real address. | Typosquatting copied the payroll page exactly. | typosquatting |
| چاه آبی | /ˈwɔːtərɪŋ hoʊl/<br>واتِرینگ هول | Attacking a website that the target trusts. | A watering hole infected the news site. | watering hole |
| دانلود ناخواسته | /ˈdraɪv baɪ ˈdaʊnloʊd/<br>درایو بای داونلود | Code that runs when a page is opened. | A drive-by download needed no click. | drive-by download |
| بهانه‌سازی | /ˈpriːtekstɪŋ/<br>پری‌تِکس‌تینگ | Inventing a believable reason for a request. | Pretexting turned a support call into a breach. | pretexting |
| فیشینگ تلفنی | /ˈvɪʃɪŋ/<br>ویشینگ | Phishing that is done on a telephone call. | Vishing worked because the voice was familiar. | vishing |
| نفوذ به ایمیل کاری | /ˈbɪznəs ˈiːmeɪl ˌkɑːmprəˈmaɪz/<br>بیزِنِس ایمِیل کامپرُمایز | Taking over a business mailbox to move money. | Business email compromise cost the company a payment. | business email compromise |
| تزریق اعتبارنامه‌ها | /krəˈdenʃl ˈstʌfɪŋ/<br>کرِدِنشِل استافینگ | Replaying passwords that were stolen elsewhere. | Credential stuffing used a list from another breach. | credential stuffing |
| پاشیدن رمز | /ˈpæswɜːrd ˈspreɪɪŋ/<br>پَس‌وِرد اسپرِیینگ | Trying one common password against many accounts. | Password spraying avoided the lockout rule. | password spraying |
| فرسایش احراز دومرحله‌ای | /ˈmʌlti ˈfæktər ˈfætiɡ/<br>مالتی فَکتُر فَتیگ | Breaking a user with repeated approval requests. | Multi-factor fatigue ended with one tired click. | multi-factor fatigue |
| سرقت توکن | /ˈtoʊkən θeft/<br>توکِن ثِفت | Stealing a session token instead of a password. | Token theft works after a password change. | token theft |
| ربودن نشست | /ˈseʃn ˈhaɪdʒækɪŋ/<br>سِشِن های‌جَکینگ | Taking over an open session. | Session hijacking needs no password at all. | session hijacking |
| سرقت کوکی | /ˈkʊki θeft/<br>کوکی ثِفت | Copying the browser cookie that proves a session. | Cookie theft is why sessions must expire. | cookie theft |
| اخاذی دوگانه | /ˈdʌbl ɪkˈstɔːrʃn/<br>دابُل ایکستورشِن | Locking the data and stealing it as well. | Double extortion answered the refusal to pay. | double extortion |
| تنظیم نادرست | /ˌmɪskənfɪɡjəˈreɪʃn/<br>میسکانفیگ‌یورِیشِن | A dangerous setting that was left in place. | One misconfiguration published a storage bucket. | misconfiguration |
| وصله‌نشده | /ˌʌnˈpætʃt/<br>آن‌پَچْت | Still carrying a weakness that a patch would fix. | An unpatched server was the way in. | unpatched |
| فناوری سایه | /ˈʃædoʊ aɪ tiː/<br>شَدو آی‌تی | Tools that a team bought without asking. | Shadow IT put patient data in a private tool. | shadow IT |
| دستگاه مدیریت‌نشده | /ˌʌnˈmænɪdʒd dɪˈvaɪs/<br>آن‌مَنِجْد دیوایس | A device that the company does not control. | An unmanaged device has no posture to check. | unmanaged device |

**جدول ۳ — پایش، تشخیص و پاسخ (Monitoring, Detection, and Response)**

| فارسی | تلفظ | Definition (EN) | Example (EN) | English |
|---|---|---|---|---|
| شکار تهدید | /θret ˈhʌntɪŋ/<br>ثرِت هانتینگ | Searching for an intrusion with a question, not an alert. | Threat hunting started with one strange name. | threat hunting |
| اطلاعات تهدید | /θret ɪnˈtelɪdʒəns/<br>ثرِت اینتِلِجِنس | Information about attackers and their tools. | Threat intelligence arrived as a weekly summary. | threat intelligence |
| نشانگر نفوذ | /ˈɪndɪkeɪtər əv kəmˈproʊmaɪz/<br>ایندیکِیتِر آو کامپرُمایز | A small fact that suggests an intrusion. | The indicator of compromise was one domain. | indicator of compromise |
| قاعدهٔ تشخیص | /dɪˈtekʃn ruːl/<br>دیتِکشِن رول | A query that turns a signal into an alert. | The detection rule was written for beaconing. | detection rule |
| مهندسی تشخیص | /dɪˈtekʃn ˌendʒɪˈnɪrɪŋ/<br>دیتِکشِن اِنجینیرینگ | Testing and maintaining the rules that detect attacks. | Detection engineering retired two useless rules. | detection engineering |
| قاعدهٔ همبستگی | /ˌkɔːrəˈleɪʃn ruːl/<br>کورِلِیشِن رول | A rule that joins several weak signals into one. | The correlation rule joined three small events. | correlation rule |
| منبع لاگ | /lɔːɡ sɔːrs/<br>لاگ سورس | A system that produces log records. | When the log source disappeared, the rule died. | log source |
| تحلیل رفتاری | /bɪˌheɪvjərəl ˌænəˈlɪtɪks/<br>بیهِیویُرَل اَنَلِتیکس | Finding a threat from the way people work. | Behavioural analytics noticed the odd schedule. | behavioural analytics |
| تحلیل رفتار کاربر و موجودیت | /ˌjuːzər ˈentəti bɪˌheɪvjər ˌænəˈlɪtɪks/<br>یوزِر اِنتِتی بیهِیویُر اَنَلِتیکس | One view of every account and machine's habits. | User entity behaviour analytics joined six log sources. | user entity behaviour analytics |
| تشخیص ناهنجاری | /əˈnɑːməli dɪˈtekʃn/<br>اَنُمالی دیتِکشِن | Finding the record that does not fit the pattern. | Anomaly detection flagged three hundred records. | anomaly detection |
| رفتار مبنا | /ˈbeɪslaɪn bɪˈheɪvjər/<br>بِیس‌لاین بیهِیویُر | The normal picture that a system learns first. | The baseline behaviour was built in two weeks. | baseline behaviour |
| سفر ناممکن | /ɪmˈpɑːsəbl ˈtrævl/<br>ایمپاسِبُل ترَوِل | Two logins that no person could have made. | Impossible travel proved that the token was stolen. | impossible travel |
| خستگی هشدار | /əˈlɜːrt ˈfætiɡ/<br>اَلِرت فَتیگ | Losing attention because there are too many alerts. | Alert fatigue made the urgent alert the last one. | alert fatigue |
| پایش پیوسته | /kənˌtɪnjuəs ˈmɑːnɪtərɪŋ/<br>کانتینیوِس مانیتُرینگ | Watching systems all day, not once a quarter. | Continuous monitoring was the first-tier duty. | continuous monitoring |
| مرکز عملیات امنیت | /sɪˈkjʊrəti ˌɑːpəˈreɪʃnz ˈsentər/<br>سِکیورِتی آپِرِیشِنز سِنتِر | The room and team that watch the alerts. | The security operations centre works in three shifts. | security operations centre |
| قهرمان امنیت | /sɪˈkjʊrəti ˈtʃæmpiən/<br>سِکیورِتی چَمپیون | A person in each department who knows both sides. | Each department named one security champion. | security champion |
| مدیریت پرونده | /keɪs ˈmænɪdʒmənt/<br>کِیس مَنِجمِنت | Tracking every alert as a case with an owner. | Case management gave each alert one owner. | case management |
| مسیر ارجاع | /ˌeskəˈleɪʃn pæθ/<br>اِسکَلِیشِن پَث | The order in which people are called. | The escalation path was written on one page. | escalation path |
| مهار حادثه | /kənˈteɪnmənt/<br>کانتِینمِنت | Stopping a problem before it spreads. | Containment was finished before midnight. | containment |
| ریشه‌کنی | /ɪˌrædɪˈkeɪʃn/<br>ایرَدیکِیشِن | Removing the entry point completely. | Eradication removed the malicious inbox rule. | eradication |
| درس‌های آموخته | /ˈlesnz lɜːrnd/<br>لِسِنز لِرند | The notes that a team writes after an incident. | The lessons learned named the missing review. | lessons learned |
| زنجیرهٔ حفظ اثر | /tʃeɪn əv ˈkʌstədi/<br>چِین آو کاستِدی | The record of who held the evidence and when. | The chain of custody was kept for every file. | chain of custody |
| تمرین رومیزی | /ˈteɪbltɑːp ˈeksərsaɪz/<br>تِیبُل‌تاپ اِکسِرسایز | A practice run of a scenario, without real systems. | The tabletop exercise lasted two hours. | tabletop exercise |
| شبیه‌سازی حمله | /əˈtæk ˌsɪmjəˈleɪʃn/<br>اَتَک سیمیولِیشِن | Repeating the attacks of a real actor on purpose. | Attack simulation followed the real kill chain. | attack simulation |
| شبیه‌سازی فیشینگ | /ˈfɪʃɪŋ ˌsɪmjəˈleɪʃn/<br>فیشینگ سیمیولِیشِن | Sending a fake message to teach the staff. | The monthly phishing simulation was not published as a contest. | phishing simulation |
| آزمون نفوذ | /ˌpenəˈtreɪʃn test/<br>پِنِترِیشِن تِست | A paid attempt to break into a system. | The penetration test found one open printer port. | penetration test |
| افشای آسیب‌پذیری | /ˌvʌlnərəˈbɪləti dɪsˈkloʊʒər/<br>وولنِرَبِلیتی دیسکلوژِر | Telling a vendor about a weakness you found. | Vulnerability disclosure starts a clock for the vendor. | vulnerability disclosure |
| افشای مسئولانه | /rɪˈspɑːnsəbl dɪsˈkloʊʒər/<br>ریسپانسِبُل دیسکلوژِر | Reporting a weakness and allowing time to repair it. | Responsible disclosure kept the users safe. | responsible disclosure |
| جایزهٔ کشف آسیب‌پذیری | /bʌɡ ˈbaʊnti/<br>باگ باونتی | A payment for reporting a weakness. | The bug bounty paid for a proof, not a story. | bug bounty |
| تله (هانی‌پات) | /ˈhʌnipɑːt/<br>هانی‌پات | A system that is meant to be attacked. | Any contact with the honeypot is interesting. | honeypot |
| توکن تله | /kəˈneri ˈtoʊkən/<br>کُنِری توکِن | A key or file that nobody should ever open. | The canary token raised an alarm when it was read. | canary token |

**جدول ۴ — رمزنگاری، پیکربندی و حاکمیت (Cryptography, Configuration, and Governance)**

| فارسی | تلفظ | Definition (EN) | Example (EN) | English |
|---|---|---|---|---|
| رمزنگاری سرتاسری | /ˌend tə ˈend ɪnˈkrɪpʃn/<br>اِند تو اِند اینکریپشِن | Protecting a message from one end to the other. | End-to-end encryption protects the conversation itself. | end-to-end encryption |
| رمزنگاری دادهٔ ساکن | /ɪnˈkrɪpʃn ət rest/<br>اینکریپشِن اَت رِست | Protecting the data that is stored on a disk. | Encryption at rest was enabled on every server. | encryption at rest |
| رمزنگاری دادهٔ در انتقال | /ɪnˈkrɪpʃn ɪn ˈtrænzɪt/<br>اینکریپشِن این ترَنزیت | Protecting the data while it travels. | Encryption in transit is the minimum requirement. | encryption in transit |
| مدیریت کلید | /kiː ˈmænɪdʒmənt/<br>کی مَنِجمِنت | Storing, rotating, and destroying cryptographic keys. | Key management decides the real strength of a system. | key management |
| ماژول امنیت سخت‌افزاری | /ˌhɑːrdwer sɪˈkjʊrəti ˈmɑːdʒuːl/<br>هاردوِر سِکیورِتی ماجول | A device that keeps a key that cannot be exported. | The master key never left the hardware security module. | hardware security module |
| سپردهٔ کلید | /kiː ˈeskroʊ/<br>کی اِسکرو | A protected copy of a key, kept for an emergency. | Key escrow is the most dangerous document in the building. | key escrow |
| نمک‌زدن | /ˈsɔːltɪŋ/<br>سال‌تینگ | Adding a random value to each stored password. | Salting stops two equal passwords from matching. | salting |
| گاوصندوق توکن | /ˈtoʊkən vɔːlt/<br>توکِن وُلت | A protected store for tokens and secrets. | The token vault was opened by one service only. | token vault |
| ماسک‌کردن داده | /ˈdeɪtə ˈmæskɪŋ/<br>دِیتا مَسکینگ | Hiding part of a value from some users. | Data masking showed the last four digits. | data masking |
| شبه‌بی‌هویتی‌سازی | /ˌsuːdoʊˌnɪmaɪˈzeɪʃn/<br>سودُ‌نیمِیزِیشِن | Replacing a name with a code that can be reversed. | Pseudonymization kept the study inside the law. | pseudonymization |
| حریم خصوصی از طراحی | /ˈprɪvəsi baɪ dɪˈzaɪn/<br>پریوِسی بای دیزاین | Asking the privacy question before you build. | Privacy by design is cheaper than a fine. | privacy by design |
| طبقه‌بندی داده | /ˈdeɪtə ˌklæsɪfɪˈkeɪʃn/<br>دِیتا کلَسِفیکِیشِن | Deciding which data is sensitive and how it must be treated. | Data classification decided the encryption rule. | data classification |
| سیاست نگه‌داشت | /rɪˈtenʃn ˈpɑːləsi/<br>ریتِنشِن پالِسی | The rule about how long data may be kept. | The retention policy removed three years of records. | retention policy |
| جلوگیری از نشت داده | /ˈdeɪtə lɔːs prɪˈvenʃn/<br>دِیتا لاس پریوِنشِن | Watching for data that leaves in the wrong direction. | Data loss prevention blocked the upload. | data loss prevention |
| اطلاع‌رسانی نفوذ | /briːtʃ ˌnoʊtɪfɪˈkeɪʃn/<br>بریچ نوتِفیکِیشِن | The legal duty to tell people about a breach. | The breach notification deadline was seventy-two hours. | breach notification |
| مدل تهدید | /θret ˈmɑːdl/<br>ثرِت مادِل | A description of what is valuable and who wants it. | The threat model was written in one page. | threat model |
| امن به‌صورت پیش‌فرض | /sɪˈkjʊr baɪ dɪˈfɔːlt/<br>سِکیور بای دیفالت | Safe settings that must be turned off deliberately. | Secure by default is why the port was closed. | secure by default |
| امنیت از مرحلهٔ نخست | /ʃɪft left sɪˈkjʊrəti/<br>شیفت لِفت سِکیورِتی | Moving security work to the beginning of the process. | Shift-left security added one test to the pipeline. | shift-left security |
| مدیریت آسیب‌پذیری | /ˌvʌlnərəˈbɪləti ˈmænɪdʒmənt/<br>وولنِرَبِلیتی مَنِجمِنت | Finding, scoring, and fixing known weaknesses. | Vulnerability management turned a list into a plan. | vulnerability management |
| امتیاز شدت | /səˈverəti skɔːr/<br>سِوِرِتی اسکور | A number that shows how serious a weakness is. | The severity score decided the order of the repairs. | severity score |
| رفع نقص | /rɪˌmiːdiˈeɪʃn/<br>رِمی‌دِیشِن | The work of repairing a weakness. | Remediation was planned for the next window. | remediation |
| کنترل جبرانی | /ˈkɑːmpənseɪtɪŋ kənˈtroʊl/<br>کامپِنسِیتینگ کانترول | A different control when the repair must wait. | A compensating control isolated the old server. | compensating control |
| دفاع لایه‌ای | /dɪˈfens ɪn ˈdepθ/<br>دیفِنس این دِپث | Several independent layers of protection. | Defense in depth assumes that one layer will fail. | defense in depth |
| رانش پیکربندی | /kənˌfɪɡjəˈreɪʃn drɪft/<br>کانفیگ‌یورِیشِن دریفت | Slow movement of a system away from its baseline. | Configuration drift was created by a midnight fix. | configuration drift |
| خط پایهٔ سخت‌سازی | /ˈhɑːrdənɪŋ ˈbeɪslaɪn/<br>هاردِنینگ بِیس‌لاین | The documented secure state of a machine. | The hardening baseline was stored with the image. | hardening baseline |
| محافظت زمان اجرا | /ˈrʌntaɪm prəˈtekʃn/<br>ران‌تایم پروتِکشِن | Watching a process while it is actually running. | Runtime protection stopped the unexpected process. | runtime protection |
| پایش یکپارچگی فایل | /faɪl ɪnˈteɡrəti ˈmɑːnɪtərɪŋ/<br>فایل اینتِگرِتی مانیتُرینگ | Noticing when a system file changes. | File integrity monitoring found the changed binary. | file integrity monitoring |
| نسخهٔ پشتیبان تغییرناپذیر | /ɪˈmjuːtəbl ˈbækʌp/<br>ایمْیوتَبُل بَک‌آپ | A backup that cannot be changed or deleted. | The immutable backup was the reason they recovered. | immutable backup |
| نقطهٔ بازگردانی | /rɪˈstɔːr pɔɪnt/<br>ریستور پویْنت | A saved state that can be restored. | The restore point from Tuesday was used. | restore point |
| بازهٔ وصله | /pætʃ ˈwɪndoʊ/<br>پَچ ویندو | The planned time in which patches are installed. | The patch window was missed twice. | patch window |
| گاوصندوق رازها | /ˈsiːkrəts vɔːlt/<br>سیک‌رِتس وُلت | A safe store for keys and passwords. | The secrets vault removed the key from the code. | secrets vault |

---

### 3. Reading / متن اصلی

**عنوان متن: Nothing Inside the Walls (هیچ‌چیز درون دیوارها امن نیست)**

**[1]** For thirty years, security was drawn as a castle: a strong wall, a guarded gate, and a soft inside. Once a user was inside the network, almost everything was trusted. This model has been replaced by a single sentence that is repeated in every modern design review: **zero trust**. The rule is simple to say and expensive to follow — no request is trusted because of where it comes from. Farid, a security engineer at a teaching hospital, and Leila, an incident responder who is called after a breach, meet the same rule from two different sides.

**[2]** The old model failed for a measurable reason. A single stolen password gave an attacker an ordinary account, and from that account a whole internal network could be explored. The area that an attacker can reach is the attack surface, and the internal one was almost unlimited. The hospital had one flat network, so a laptop in the cafeteria could reach the imaging servers in the basement. This is lateral movement, and it usually begins with privilege escalation: a normal user finds a misconfigured service and becomes a local administrator.

**[3]** Zero trust answers with small borders inside the building. Microsegmentation divides one large network into many small ones, so that a payment terminal can talk to one server and to nothing else. Access is then reduced to what a job actually needs: least privilege means no more than the task requires, least-standing access means the permission disappears after the task ends, and just-in-time access means it is created at the moment it is requested. Even privileged access, the ability to change a system, is granted only through elevation, which is recorded and time-limited, and not by keeping an administrator account open all day.

**[4]** Identity is the new perimeter, and it is managed in one place. The identity provider authenticates the user, and single sign-on gives one session for many applications. Federation lets one organisation trust the identity of another, and the proof that travels between them is an assertion that carries claims — the facts about the user, such as a group or a department. Delegation allows one service to act for a user, and every delegation must have a limit, because a service that can do anything is a permanent back door. Inside the identity system, a privilege boundary separates what an ordinary session may do from what an administrative session may do.

**[5]** Passwords are being removed from the list of trusted factors. A passwordless login uses a passkey that stays on the user's device, and a security key is a small hardware device that cannot be copied by a phishing page. Adaptive authentication raises the requirement when the risk rises, so a login from a new country triggers step-up authentication instead of a simple refusal. Continuous verification checks the state of the session during the day, not only at the door: the device posture is read from an agent, the device fingerprint tells whether the same machine is still in use, and behavioural biometrics compare the rhythm of typing with the user's own habits. When the pattern breaks, the session is closed and the token is revoked.

**[6]** Administration is treated as a separate world. The administrative tier contains the accounts that can change the security system itself, and nobody browses the web with one of them. Engineers reach a server through a jump host, or through a bastion that is the only door to the internal network, and every session on it is under session recording. Revocation is the last and the most important control: when a person leaves, the access must disappear in minutes, not in days.

**[7]** Access governance is the boring work that decides the outcome. Every user holds entitlements, and the dangerous ones are found by looking for a toxic combination, such as the right to approve a payment and the right to change the payee. An access review is repeated every quarter, and a recertification asks the manager to confirm, in writing, that a permission is still needed. The failures are always the same: an orphaned account belongs to nobody, a dormant account has not been used for a year, and privilege creep adds one permission at a time until a help-desk user can change a database. Role-based access control is not a cure by itself, because role explosion turns three roles into three hundred.

**[8]** The threats on the other side are patient. A threat actor may be a criminal group or a government team, and an advanced persistent threat is one that stays for months without making noise. An insider threat comes from a person who already has access; sometimes the person is malicious, and more often the account has simply been stolen. The difference matters, because insider risk is managed with access review, and a stolen account is managed with authentication.

**[9]** An intrusion is usually drawn as a chain. The attack path is the route from the first weak point to the valuable data, the kill chain describes the stages of the operation, and persistence is the mechanism that keeps the attacker alive after a restart. Dwell time is the time between the first entry and the discovery, and it is often measured in months. The first step is frequently a watering hole, which is a trusted website that has itself been infected, or a typosquatting domain that looks like the real address. A drive-by download needs no click and no dialogue: the page simply loads, and the code runs. Then the attacker builds command and control, and the machine begins beaconing at a regular interval, which is exactly the signal that a good detection rule is looking for.

**[10]** Most attacks still enter through a human being, and the methods are only slightly new. Credential stuffing replays passwords from an old breach, and password spraying tries one common password against many accounts, which is why the alert usually arrives as multi-factor fatigue: a user is asked ten times for an approval and accepts one of them. Token theft takes the session rather than the password, session hijacking takes the cookie, and cookie theft works even when the password has already been changed. Pretexting gives a believable reason for a request, vishing is the same trick on a telephone call, and business email compromise is the version that costs companies the most money. The only defence that scales is practice: a phishing simulation is sent to the staff every month, and the report is read by the security champion of each department.

**[11]** When a company is attacked with encryption, the modern demand is double extortion: the data is locked and it is also stolen, so a refusal to pay is answered with a threat of publication. This is why an immutable backup and a restore point are worth more than any negotiation, and why one copy is kept in an air-gapped system. The entry point is still usually the same: an unpatched server, a misconfiguration in a public bucket, or a credential that was never rotated inside a patch window that came and went.

**[12]** Shadow IT is the internal version of the same problem. A team buys a tool with a credit card, an unmanaged device joins the network, and a personal phone is used for a work task. The technical question is whether the device was enrolled in the company system, because a machine that is not enrolled has no device posture to check.

**[13]** Detection is an engineering discipline, not a hobby. Threat hunting starts with a question rather than an alert, and it depends on threat intelligence, which is information about the actors and their tools. An indicator of compromise is a small fact that suggests an intrusion, such as a domain, a file hash, or an unusual schedule. A detection rule turns that fact into a query, and detection engineering keeps the rules honest: every rule is tested, documented, and retired when its log source disappears. A correlation rule joins several weak signals into one strong one.

**[14]** Above the rules sits analysis. Behavioural analytics compares today with the normal picture, and a baseline behaviour is the normal picture itself. The same analysis, applied to every account and machine in one view, is called user entity behaviour analytics. An anomaly detection system may learn that a nurse opens one record per minute, so three hundred records in one hour is impossible travel in the same city, not in another country. The output must be tuned, because alert fatigue defeats a team as reliably as a zero-day.

**[15]** A security operations centre is organised around that flow. Continuous monitoring is the duty of the first tier, and the security champion in each department is the person who knows both the work and the rules. Every alert becomes a case in case management, and a case has a defined escalation path, so that a task follows a person rather than a phone number.

**[16]** Response is a fixed sequence, and it is rehearsed. Containment stops the spread, eradication removes the entry point, and the last step is the hardest: lessons learned are written down while the team is still tired, in a review that blames the system and not the person. Evidence is kept under chain of custody, so that every file has a name, a time, and a signature attached to it. A tabletop exercise is how the sequence is practised: no production system is touched, and a scenario is played out for two hours in one room.

**[17]** Reliability and offence complete the picture. A penetration test is carried out by a person who is paid to break in, and an attack simulation repeats the plausible attacks of a real actor. If a researcher finds something, vulnerability disclosure is the normal path, and responsible disclosure gives the vendor time to repair before anything is published. A bug bounty turns that courtesy into a paid arrangement. After the report, vulnerability management takes over: every finding is scored with a severity score, remediation is planned, and a compensating control is added when the repair must wait. The principle behind this work is defense in depth: several independent layers, so that one failure is not a disaster.

**[18]** Two quiet tools belong to the same family. A honeypot is a server that is designed to be attacked, so that any contact with it is interesting; a canary token is a file or a key that nobody should ever open, and its use is an alarm in itself. Both work on a single assumption: something will be touched.

**[19]** Cryptography closes the layers. End-to-end encryption protects the conversation itself, encryption at rest protects the disk, and encryption in transit protects the wire. Key management is the discipline that keeps all of it alive, and a hardware security module is the device in which a master key is stored, used, and never exported. Key escrow is the arrangement for the day when the only person who knows a key is not available, and it is also the most dangerous document in the building. Salting is the smaller habit that protects a stolen list of passwords: every stored password receives its own random addition, so two users with the same password no longer produce the same hash.

**[20]** On the data side, the work is classification. Data classification decides what must be protected and how, a retention policy decides how long it may be kept, and data loss prevention watches for the moment when it moves in the wrong direction. Data masking and pseudonymization reduce what an analyst can see, and privacy by design means that the question is asked while the system is being designed, not after a letter arrives from a regulator. The breach notification itself is a legal deadline: the regulator and the customers must be told, and the honest paragraph about the affected records is written before the lawyers ask for it.

**[21]** The lower layers of the software are also in scope. Memory safety is the property that stops a buffer overflow from turning data into code, and memory corruption is the class of faults behind the oldest security bugs. Runtime protection watches a process while it runs, file integrity monitoring notices when a system file changes, and a hardening baseline describes the state in which the machine is allowed to run. Configuration drift happens when a live system slowly leaves that baseline, and it is usually created by a hurried fix at midnight. Secure by default and shift-left security are the same idea at two moments: the safe option should be the first option, and the check should run before the release, not after the incident.

**[22]** A secrets vault removes the simplest and most common mistake. The team that stores a key in a private repository has already published it; the vault gives a short-lived credential to a service account and keeps the long-lived secret behind a door that few people can open.

**[23]** Threat modelling is the exercise that ties the rest together. A threat model describes what is valuable and who would want it, an attack tree breaks one goal into the paths that could reach it, and an abuse case writes the story from the attacker's point of view. A design review without a threat model is a list of features with a feeling of safety attached to it.

**[24]** Farid's implementation was described by his own team as unglamorous. He was told that the money would not be given for anything new; he was asked to remove what already existed. The first three months were spent on access review rather than on tools: ninety orphaned accounts were found, two dormant administrator accounts were closed, and one toxic combination was removed from a help-desk role. Not one product was purchased in that quarter, and the hospital's risk was reduced more than it had been by the previous two projects combined.

**[25]** His first incident was small and instructive. A dormant account that belonged to a researcher who had left two years earlier was used at four in the morning. The account was disabled within minutes, and the logs were searched for the entire night. What the team learned was not about the attacker: the account had been found only because the review was repeated, and the failure had been created by a process whose exceptions were never checked.

**[26]** Leila was called at eleven in the evening. A logistics company had been breached, the file servers were being encrypted, and the backups were the only question that mattered. She asked whether the backup was immutable, and the answer was that it was. The restore point from two days earlier was used, and the business lost two days of data instead of two years of it.

**[27]** Her report described an ordinary chain. A payroll page had been cloned with a typosquatting domain, one finance officer had entered a password into it, and the account had been used to read mail for eleven days. Nothing was broken; nothing was encrypted; the intrusion was found by a bank that noticed an unusual transfer. If the payment had been smaller, the dwell time would have been longer. If the inbox rule had been reviewed, the account would have been closed a week earlier.

**[28]** Her lessons went into a table that she now shows in every review. On the left, what was assumed; on the right, what was true. It was assumed that the mailbox was only read by its owner; it was true that a rule had forwarded every invoice to an external address. It was assumed that the password was enough; it was true that no step-up authentication had been required for a payment change. It was assumed that the incident would be detected by the company; it was true that a bank had detected it first.

**[29]** What the two of them recommend is a smaller list than a vendor would prefer. Close the accounts that nobody uses, because they are found by review and not by a scanner. Remove the standing permissions, because a permission that is given once is a permission that stays. Record every administrative session, because the person who means well is not the only person who can log in. Separate the backup from the network, because the last line of defence is a copy that the attacker cannot reach. Practise the worst day in a room, because the sequence of the response should be learned before it is needed.

**[30]** Measurement is the last habit, and it is deliberately humble. A mature team reports the percentage of devices that are enrolled, the number of administrators with a standing elevation, the median time to revocation, and the percentage of alerts that were closed without action. The last number is the honest one: a security team with no false positives and no complaints is a team that is not looking.

**[31]** Three mistakes are repeated in every organisation that starts this work. The first is buying a product instead of closing an account: a platform is installed, and the ninety orphaned accounts are still open a year later. The second is keeping the knowledge in one expert, who is then exhausted by the same three questions. The third is treating security as a project with an end date, although the attack surface grows every time a team deploys on Friday. None of the three is solved by a tool, and all three are solved by a habit.

**[32]** What has changed is the direction of the trust. In the old design, the network was trusted and the user was approved once. In the zero-trust design, the network is treated as hostile, the user is verified again and again, and the permission is given for one task and taken back afterwards. The work is not finished by any single control, because a control that is never reviewed is a permission that is never questioned.

**[33]** Farid ends his training session with a sentence that was given to him by an older engineer. "You will not be judged by the attack that never happened; you will be judged by how quickly you answered, and by how honestly you wrote the report." Security, in the end, is not a wall. It is a habit of asking who is really there, and of writing down the answer.

*(۳۰۴۵ واژه — ۳۳ پاراگراف)*

---

### 4. Persian Translation / ترجمه فارسی

**الف) واژه‌های دشوار و معادل آن‌ها**

| واژه / عبارت | معادل پیشنهادی | نکتهٔ ترجمه |
|---|---|---|
| zero trust | اعتماد صفر | «بدون اعتماد» ترجمهٔ نادرست است؛ ایده این است که هیچ‌چیز بر پایهٔ موقعیت شبکه مورد اعتماد نیست. |
| microsegmentation | ریزقطعه‌بندی | «قطعه‌بندی ریز» هم درست است؛ منظور تقسیم یک شبکه به بخش‌های بسیار کوچک است، نه تقسیم داده به قطعه. |
| least privilege | کمترین اختیار لازم | واژهٔ *privilege* اینجا «اختیار» است، نه «امتیاز»؛ «حداقل دسترسی» هم پذیرفته است. |
| least-standing access | دسترسی کم‌دوام | واژهٔ *standing* به معنای «بی‌پایان و همیشگی» است؛ «دسترسی ایستا» معنا را نمی‌رساند. |
| elevation | ارتقای دسترسی | با «ارتقای شغلی» اشتباه نشود؛ این ارتقا موقت و فنی است. |
| step-up authentication | احراز هویت پله‌ای | «پله‌ای» به معنای بالا رفتن سطح تأیید است، نه رفتن پلهٔ ساختمان. |
| passkey | کلید عبور | در متن‌های فنی اغلب «پَس‌کی» نوشته می‌شود؛ در پرانتز شکل انگلیسی را بیاورید. |
| token | توکن | در این درس توکن نشست است؛ در متن‌های هوش مصنوعی همان واژه یکای متن است. این تفاوت معنایی را در ترجمه روشن کنید. |
| device posture | وضعیت امنیتی دستگاه | «وضعیت» به معنای آوردهٔ امنیتی دستگاه است؛ «قامت دستگاه» ترجمهٔ تحت‌اللفظی و نادرست است. |
| delegation | واگذاری اختیار | با «تعطیل وظایف» اشتباه نشود؛ منظور این است که یک سرویس اجازهٔ عمل به‌جای کاربر را بگیرد. |
| privilege boundary | مرز اختیار | «مرز امتیاز» بی‌معناست؛ این مرز میان نشست عادی و نشست مدیریتی است. |
| entitlement | حق دسترسی | در سیستم‌های حکمرانی دسترسی، هر مجوز مشخص یک *entitlement* است؛ «استحقاق» معنا را منتقل نمی‌کند. |
| toxic combination | ترکیب خطرناک | اصطلاح به دو مجوزی گفته می‌شود که تنهایی بی‌خطر و با هم خطرناک‌اند. |
| dwell time | زمان ماندگاری مهاجم | «زمان اقامت» گمراه‌کننده است؛ این بازه میان ورود اول و کشف نفوذ است. |
| kill chain | زنجیرهٔ حمله | «زنجیرهٔ کشتار» ترجمهٔ تحت‌اللفظی و نامناسب برای متن دانشگاهی است. |
| beaconing | سیگنال‌دهی دوره‌ای | «فانوس‌زنی» بی‌معناست؛ منظور تماس مکرر بدافزار با سرور فرمان است. |
| pretexting | بهانه‌سازی | «پیش‌متن‌سازی» غلط است؛ منظور ساختن بهانه‌ای باورپذیر برای گرفتن اطلاعات است. |
| double extortion | اخاذی دوگانه | هر دو بخش لازم است: قفل کردن داده و دزدیدن آن. |
| compensating control | کنترل جبرانی | «کنترل جبران‌کننده» در متن‌های حسابرسی رایج نیست؛ همین شکل را نگه دارید. |
| configuration drift | رانش پیکربندی | «دریفت» هم در صنعت رایج است؛ منظور فاصله گرفتن تدریجی سامانه از خط پایهٔ امن است. |
| immutable backup | نسخهٔ پشتیبان تغییرناپذیر | «پشتیبان تغییرناپذیر» روان‌تر است؛ معنا این است که مهاجم نمی‌تواند آن را پاک یا رمزگذاری کند. |
| canary token | توکن تله | «قناری» ترجمهٔ استعاری است؛ در پرانتز توضیح دهید: فایل یا کلیدی که هیچ‌کس نباید باز کند. |

**ب) نکات ترجمه**

۱. **مجهول انگلیسی را با ساخت فارسی روان برگردانید:** *the account was disabled* ← «حساب غیرفعال شد»، نه «حساب توسط مدیر غیرفعال شد»؛ در فارسی می‌توان فاعل واقعی را حذف کرد و «توسط» را آن‌جا آورد که خواننده انتظارش را دارد.
۲. **معلوم و مجهول را در فارسی هم‌جنس کنید:** *logs are collected and analysed every night* ← «هر شب گزارش‌ها جمع‌آوری و تحلیل می‌شود»؛ آوردن «می‌شوند» برای هر دو فعل، جمله را سبک‌تر می‌کند.
۳. **مجهول گزارشی را با «گفته می‌شود» برگردانید:** *It is reported that the attack started in March* ← «گزارش شده است که حمله در مارس آغاز شد»؛ *He is believed to have left* ← «باور بر این است که او رفته است».
۴. **واژهٔ *privilege* را درست تشخیص دهید:** در امنیت «اختیار/دسترسی ممتاز» است و در جمله‌های عمومی «امتیاز»؛ ترجمهٔ یکنواخت باعث سوءبرداشت فنی می‌شود.
۵. **اصطلاح‌های سیاسی و حقوقی را با معادل صنعتی بیاورید:** *breach notification* ← «اطلاع‌رسانی نفوذ»، *regulator* ← «نهاد تنظیم‌گر»، *chain of custody* ← «زنجیرهٔ حفظ اثر».
۶. **افعال فنی را با فعل دقیق ترجمه کنید:** *to revoke a token* ← «توکن را باطل کردن»، *to contain an incident* ← «حادثه را مهار کردن»، *to eradicate* ← «ریشه‌کن کردن».
۷. **در تلفظ سرواژه‌ها یکدست بمانید:** *MFA*، *SIEM* و *SOC* در فارسی معمولاً با حروف انگلیسی خوانده می‌شوند؛ آن‌ها را ترجمه نکنید، بلکه نخستین بار توضیح فارسی بدهید.
۸. **از این ترجمه‌های تحت‌اللفظی بپرهیزید:** *honeypot* ← «تله/هانی‌پات» (نه «دیگ عسل»)، *bug bounty* ← «جایزهٔ کشف آسیب‌پذیری» (نه «پاداش حشره»)، *vishing* ← «فیشینگ تلفنی» (نه «ویشینگ کردن»).

---

### 5. Comprehension Check / درک مطلب

**الف) چهارگزینه‌ای — ده سؤال**

1. What does zero trust assume about the internal network?
   a) that it is safe because it is private
   b) that it must be treated as hostile, like any other network
   c) that it is protected by one strong firewall

2. What is least-standing access?
   a) permission that does not stay open after the task has ended
   b) permission that is never reviewed by a manager
   c) permission that is given to every administrator at once

3. Why is a passkey harder to phish than a password?
   a) because it is much longer than a normal password
   b) because it is written down by the user
   c) because the private key never leaves the user's device

4. What triggers step-up authentication?
   a) a rise in the risk level of the login
   b) the end of the working day
   c) a new version of the application

5. What is a toxic combination?
   a) two alerts that arrive at the same second
   b) two permissions that are dangerous together
   c) two log sources with the same name

6. What does dwell time measure?
   a) the time that a backup takes to restore
   b) the length of a security training session
   c) the time between the first entry and the discovery

7. What is beaconing?
   a) sending a monthly report to the regulator
   b) a machine that contacts a server at fixed intervals
   c) copying a file to a backup device every night

8. Why is a canary token useful?
   a) because nobody should ever open it, so its use is an alarm
   b) because it blocks every known attack
   c) because it replaces the need for an access review

9. What does an immutable backup protect against?
   a) a slow network connection during the restore
   b) a user who forgets the password of the backup tool
   c) an attacker who wants to delete or encrypt the backups too

10. What did the bank notice in Leila's case?
   a) an unusual transfer from the company account
   b) a new firewall rule in the payroll system
   c) an unpatched server in the logistics network

**ب) صحیح یا غلط — ده سؤال**

1. In the old castle model, a user inside the network was trusted. (..........)
2. Microsegmentation makes one large network into many small ones. (..........)
3. A jump host is used for browsing the web safely. (..........)
4. An access review is repeated every quarter, and a recertification confirms that a permission is still needed. (..........)
5. Persistence is the mechanism that keeps an attacker alive after a restart. (..........)
6. Credential stuffing tries one common password against many accounts. (..........)
7. A honeypot is a server that is designed to be attacked. (..........)
8. Runtime protection watches a process while it is running. (..........)
9. Key escrow makes a system more secure, because the key is copied. (..........)
10. In this lesson, the account in Farid's incident was found because the access review was repeated. (..........)

**پ) پاسخ کوتاه — شش سؤال**

1. Why did the old castle model fail, in the words of paragraph [2]?
2. What is the difference between least privilege and just-in-time access?
3. Why does the text say that "a service that can do anything is a permanent back door"?
4. How does double extortion change the answer to a ransomware demand?
5. What is the difference between a penetration test, an attack simulation, and a bug bounty?
6. What three mistakes does paragraph [31] describe, and what is the answer to all three?

**ت) ایدهٔ اصلی — دو سؤال**

۱. ایدهٔ اصلی کل متن کدام جمله است؟

a) Zero trust is a habit of verifying every request, closing old accounts, and measuring honestly, rather than a product that is installed once.
b) A honeypot is a server that is designed to be attacked, so any contact with it is interesting.
c) Leila's case was detected by a bank that noticed an unusual transfer.

۲. پاراگراف [13] بیشتر دربارهٔ چه چیزی است؟

a) How encryption at rest protects a disk that is stolen from a server room.
b) How detection is built from intelligence, indicators, rules, and log sources.
c) How a tabletop exercise is practised in one room for two hours.

**ث) تطبیق — دو جدول**

**جدول ۱:** هر واژه (۱ تا ۵) را به معنی درست آن (الف تا ه) وصل کنید.

| # | Word | | Meaning |
|---|---|---|---|
| 1 | entitlement | الف | the time between the first entry and the discovery |
| 2 | dwell time | ب | one specific permission that a user holds |
| 3 | pretexting | پ | the record of who held the evidence and when |
| 4 | chain of custody | ت | inventing a believable reason for a request |
| 5 | salting | ث | adding a random value to each stored password |

**جدول ۲:** هر واژه (۱ تا ۵) را به معنی درست آن (الف تا ه) وصل کنید.

| # | Word | | Meaning |
|---|---|---|---|
| 1 | severity score | الف | a device that keeps a key that cannot be exported |
| 2 | hardware security module | ب | the legal duty to tell people about a breach |
| 3 | breach notification | پ | a number that shows how serious a weakness is |
| 4 | remediation | ت | hiding part of a value from some users |
| 5 | data masking | ث | the work of repairing a weakness |

---

### 6. Vocabulary Practice / تمرین واژگان

**الف) جای خالی — بیست سؤال**

از واژه‌های داخل کادر استفاده کنید. هر واژه یک بار.

> **واژه‌ها:** least-standing access · just-in-time access · step-up authentication · passkey · device posture · delegation · entitlement · toxic combination · revocation · dwell time · beaconing · typosquatting · double extortion · unpatched · threat hunting · indicator of compromise · alert fatigue · containment · chain of custody · immutable backup

1. Permission that disappears after the task has ended is called .......... .
2. Permission that is created at the moment it is requested is called .......... .
3. A login from a new country may trigger .......... .
4. A .......... is a private key that stays on the user's device.
5. The health and the settings of a connecting device are its .......... .
6. Allowing one service to act for a user is called .......... .
7. One specific permission that a user holds is an .......... .
8. The right to approve a payment and the right to change the payee form a .......... .
9. Taking a session away when a person leaves is called .......... .
10. The time between the first entry and the discovery is the .......... .
11. A machine that contacts a server every ten minutes is .......... .
12. A fake domain that copies a real address is called .......... .
13. Locking the data and stealing it as well is .......... .
14. A server that still carries a weakness that a patch would fix is .......... .
15. Searching for an intrusion with a question rather than an alert is .......... .
16. A domain, a hash, or an odd schedule that suggests an intrusion is an .......... .
17. Too many alerts make a team lose attention; this is .......... .
18. Stopping a problem before it spreads is called .......... .
19. The record of who held the evidence and when is the .......... .
20. A backup that cannot be changed or deleted is an .......... .

**ب) وصل کردن — ده سؤال**

هر واژه را به معنی درست آن وصل کنید.

| # | Word | | Meaning |
|---|---|---|---|
| 1 | microsegmentation | الف | the rule that nothing inside a network is trusted by position |
| 2 | zero trust | ب | dividing one network into many very small parts |
| 3 | adaptive authentication | پ | the line between ordinary and administrative work |
| 4 | privilege boundary | ت | changing the proof that is required by the risk level |
| 5 | bastion | ث | the only door from the office network to the inside |
| 6 | session recording | ج | recording every action of an administrative session |
| 7 | honeypot | چ | a system that is meant to be attacked |
| 8 | canary token | ح | a key or a file that nobody should ever open |
| 9 | patch window | خ | the planned time in which patches are installed |
| 10 | secrets vault | د | a safe store for keys and passwords |

**پ) جمله‌سازی — ده سؤال**

با هر مورد یک جمله بنویسید. موضوع همهٔ جمله‌ها امنیت سامانه است.

1. least privilege (با **مجهول**)
2. revocation (با *must be*)
3. beaconing (با *was detected*)
4. double extortion / immutable backup (جمله‌ای که تضاد این دو را نشان دهد)
5. toxic combination (با **مجهول در حال کامل**)
6. یک جمله با **مجهول گزارشی** بنویسید (*It is reported that ...*)
7. یک جمله با **ساخت سببی** بنویسید (*had the account disabled* / *got the logs analysed*)
8. honeypot (با ساخت *get*-passive)
9. دو جمله بنویسید: در یکی *had to be* و در دیگری *should have been* بیاید. موضوع: لغو دسترسی
10. دو جملهٔ مجهول محتاطانه بنویسید: یکی با *must be* و یکی با *might have been*. موضوع: پایش یکپارچگی فایل

**ت) واژه‌سازی: پیشوند و پسوند — یک تمرین**

پیشوند در **ابتدای** واژه و پسوند در **پایان** واژه می‌آید و معنای آن را تغییر می‌دهد:

| پیشوند / پسوند | معنی | نمونه |
|---|---|---|
| counter- | ضد، متقابل | measure ← countermeasure |
| ex- | پیشین، سابق | employee ← ex-employee |
| im- | بی، نقیض (پیش از m/p) | possible ← impossible |
| infra- | زیر، پایه | structure ← infrastructure |
| -en | فعل ساختن از صفت | hard ← harden |
| -resistant | مقاوم در برابر | tamper ← tamper-resistant |

با افزودن پیشوند یا پسوند درست، واژهٔ مناسب بسازید.

1. measure ← .......... (اقدام متقابل، پادکار)
2. employee ← .......... (کارمند پیشین)
3. hard ← .......... (سخت‌سازی کردن)
4. possible ← .......... (ناممکن)
5. structure ← .......... (زیرساخت)
6. tamper ← .......... (مقاوم به دستکاری)

---

### 7. Grammar Focus / نکتهٔ گرامری

**موضوع: مجهول پیشرفته (advanced passive)**

**توضیح فارسی:**

مجهول (*passive*) وقتی به کار می‌آید که **کنندهٔ کار مهم نباشد، ناشناخته باشد، یا نخواهیم نامش را ببریم**؛ در نوشتار فنی و امنیتی این حالت بیشترین کاربرد را دارد، زیرا گزارش باید دربارهٔ سامانه باشد، نه دربارهٔ افراد.

ساخت پایه `be + past participle` است، اما مجهول در متن‌های حرفه‌ای چند شکل پیشرفته دارد:

**۱) در زمان‌های کامل و آینده:** *has been revoked* (حال کامل)، *had been published* (گذشتهٔ کامل)، *will be reviewed* (آینده)، *is being analysed* (حال استمراری).
**۲) با افعال وجهی:** *must be disabled*، *can be exported*، *should have been patched*، *might have been copied*.
**۳) مجهول گزارشی:** *It is reported that ...*، *It was decided that ...* و ساخت *He is believed to have left*.
**۴) مجهول با *get*** (نزدیک به زبان گفتار): *The token got revoked.*
**۵) ساخت سببی:** `have / get + مفعول + past participle` یعنی کار را به دیگری سپردن: *We had the account disabled.*

سه نکتهٔ مهم: ① بسیاری از فعل‌ها مجهول نمی‌شوند؛ نوشتن ✗ *The incident was happened* غلط است، چون *happen* مفعول نمی‌گیرد؛ ② در زمان کامل، *been* فراموش نشود: ✗ *The token has revoked* ← درست: *The token has been revoked*؛ ③ فاعل مجهول در فارسی معمولاً حذف می‌شود: «حساب غیرفعال شد» بهتر از «حساب توسط مدیر غیرفعال شد» است.

در نوشتار فنی، مجهول سه کار انجام می‌دهد: ① مسئولیت را از فرد به سامانه منتقل می‌کند (*The log was rotated.*)؛ ② دستورالعمل را بدون خطاب مستقیم می‌نویسد (*The key must be stored securely.*)؛ ③ در گزارش حادثه ترتیب رخدادها را روشن می‌کند (*The account was disabled before the review began.*). هنگام ترجمه، این ترتیب زمانی را حفظ کنید و فاعل ناشناخته را تنها وقتی برگردانید که واقعاً معلوم باشد.

**جدول ۱ — مجهول در زمان‌ها:**

| زمان | ساخت | نمونه |
|---|---|---|
| حال ساده | is / are + p.p. | The evidence is kept under chain of custody. |
| گذشتهٔ ساده | was / were + p.p. | Two dormant accounts were closed. |
| حال کامل | has / have been + p.p. | The token has been revoked. |
| گذشتهٔ کامل | had been + p.p. | The test data had been published by mistake. |
| آینده | will be + p.p. | Every patch will be installed in the window. |
| حال استمراری | is / are being + p.p. | The logs are being analysed now. |

**جدول ۲ — مجهول با افعال وجهی:**

| ساخت | معنی | نمونه |
|---|---|---|
| must be + p.p. | باید (اجبار) | The key must be stored in the module. |
| can be + p.p. | می‌توان (امکان) | The file can be exported once. |
| should have been + p.p. | باید انجام می‌شد (نقد گذشته) | This weakness should have been patched. |
| might have been + p.p. | شاید انجام شده باشد | The mailbox might have been read for days. |

**جدول ۳ — گزارشی، گفتاری و سببی:**

| ساخت | نمونه | کاربرد |
|---|---|---|
| مجهول گزارشی | It is said that the breach began in March. / He is believed to have left. | گزارش رسمی و خبری |
| مجهول با get | The token got revoked. | زبان گفتار و متن‌های ساده‌تر |
| ساخت سببی | We had the account disabled. / She got the logs analysed. | سپردن کار به دیگری |

**پنج مثال از دنیای کامپیوتر:**

1. The account was disabled within minutes of the alert.
2. Every administrative session has been recorded since January.
3. This weakness should have been patched before the sales week.
4. It is reported that the attack started with one cloned page.
5. Two dormant accounts had been closed only after the review.

**تمرین‌ها — چهل سؤال**

**الف) با شکل مجهول درست فعل کامل کنید (۱ تا ۱۴).**

1. The account .......... (disable) within minutes of the alert.
2. All administrative sessions .......... (record) last quarter.
3. The token .......... (already / revoke) before the user noticed.
4. If the baseline .......... (check) every month, the drift would have been found earlier.
5. Every patch .......... (install) inside the patch window from now on.
6. The evidence .......... (keep) under chain of custody.
7. The suspicious domain .......... (report) by the bank yesterday.
8. The logs .......... (analyse) at this moment.
9. The finding .......... (score) before the meeting.
10. Two dormant accounts .......... (close) last week.
11. The master key .......... (must / store) in the hardware security module.
12. This weakness .......... (should / patch) three months ago.
13. The incident .......... (believe) to have started in March.
14. The alerts .......... (could / tune) much earlier.

**ب) جمله را به شکل منفی یا سؤالی مجهول بنویسید (۱۵ تا ۲۰).**

15. *(منفی)* The account has been disabled.
16. *(سؤالی)* The token was revoked.
17. *(منفی)* The logs were analysed.
18. *(سؤالی)* The backup will be tested.
19. *(منفی)* This rule should have been retired.
20. *(سؤالی)* The device was enrolled.

**پ) شکل درست را انتخاب و جمله را کامل کنید (۲۱ تا ۲۶).**

21. The token .......... (has revoked / has been revoked).
22. The reports .......... (are being reviewed / are reviewing) by the second tier.
23. The incident .......... (was happened / happened) at four in the morning.
24. We .......... (had the account disabled / had the account disable).
25. It .......... (is said / says) that the attack started in March.
26. A compensating control .......... (must be added / must add) while the repair waits.

**ت) خطای هر جمله را اصلاح کنید (۲۷ تا ۳۲).**

27. The incident was happened at four in the morning.
28. The token has revoked by the system.
29. The logs were deleted by someone.
30. The finding should be scored yesterday.
31. The patch was not applied by anybody.
32. The evidence is being keep under chain of custody.

**ث) تبدیل و جمله‌سازی (۳۳ تا ۳۶).**

33. این جمله را به مجهول تبدیل کنید: *The team disabled the account at four in the morning.*
34. این جمله را به معلوم تبدیل کنید: *The rules were retired by the detection engineers.*
35. با ساخت سببی بازنویسی کنید: *Someone analysed the logs for us.*
36. با مجهول گزارشی بازنویسی کنید: *People say that the breach began in March.*

**ج) تمرین آزاد (۳۷ تا ۴۰).**

37. یک جملهٔ مجهول در حال کامل دربارهٔ یک اقدام امنیتی در آزمایشگاه یا محل کار خودتان بنویسید.
38. یک جمله با *should have been* بنویسید که یک اشتباه گذشته را نقد کند.
39. یک جمله با افعال وجهی مجهول (*must be* یا *can be*) بنویسید.
40. یک جملهٔ مجهول گزارشی بنویسید که رفتار یک سامانه را گزارش کند.

---

### 8. Key Sentences Translation / ترجمهٔ جمله‌های کلیدی

**انگلیسی ← فارسی (۱۰ جمله)**

1. The account was disabled within minutes of the alert.
2. Every administrative session has been recorded since January.
3. This weakness should have been patched before the sales week.
4. It is reported that the attack started with one cloned page.
5. Two dormant accounts had been closed only after the review.
6. The evidence is kept under chain of custody, so every file has a name and a time.
7. If the baseline had been checked every month, the configuration drift would have been found earlier.
8. A compensating control must be added while the repair waits.
9. The token got revoked, and the session was closed at once.
10. Nothing was broken; nothing was encrypted; the intrusion was found by a bank.

**فارسی ← انگلیسی (۱۰ جمله)**

1. حساب چند دقیقه پس از هشدار غیرفعال شد.
2. کلید اصلی باید در ماژول امنیت سخت‌افزاری ذخیره شود.
3. اگر نسخهٔ پشتیبان تغییرناپذیر نبود، شرکت دو سال داده را از دست می‌داد.
4. گزارش شده است که حمله در ماه مارس آغاز شده است.
5. آن ضعف باید سه ماه پیش وصله می‌شد.
6. هر تغییر در پیکربندی باید بازبینی شود.
7. توکن باطل شد و نشست بسته شد.
8. دو حساب راکد تنها پس از بازبینی دسترسی بسته شدند.
9. گفته می‌شود که این آسیب‌پذیری از سال گذشته شناخته شده بود.
10. یک کنترل جبرانی افزوده شد تا سامانهٔ قدیمی جدا بماند.

---

### 9. Writing Task / تمرین نگارش

**موضوع: A Security Habit I Would Change — عادتی که در امنیت کار خودم عوض می‌کردم**

یک رویهٔ امنیتی را انتخاب کنید که **خودتان** با آن روبه‌رو شده‌اید: رمز عبور مشترک در یک گروه درسی، یک پوشهٔ عمومی در شبکهٔ دانشگاه، یک فلش‌مموری که بین همه می‌گردد، یا یک حساب قدیمی که هنوز باز است. سپس دربارهٔ آن بنویسید:

- کدام رویه بود و چه کسی از آن آسیب می‌دید؟
- **چه کاری انجام شد؟** جمله‌ها را با ساخت مجهول بنویسید (حساب بسته شد، رمز عوض شد، فایل حذف شد).
- چه چیزی **باید انجام می‌شد** ولی انجام نشد؟ (با *should have been*)
- اگر آن اتفاق یک بار دیگر بیفتد، **چه چیزی باید اضافه شود**؟ (با *must be* یا *can be*)
- یک جملهٔ محتاطانه بنویسید که احتمال خطای ارزیابی خودتان را بپذیرد.

**شرایط نگارش:**

- نوشته بین **۲۰۰ تا ۳۰۰ واژه** باشد.
- دست‌کم **۵ جملهٔ مجهول** داشته باشد؛ در میان آن‌ها **یک مجهول با فعل وجهی** و **یک مجهول در حال کامل** بیاید.
- **یک مجهول گزارشی** (*It is reported that / It was decided that*) در متن باشد.
- دست‌کم **۲ اصطلاح ربطی** از این فهرست به‌کار ببرید: *however*, *therefore*, *even so*, *as a result*.
- دست‌کم **۸ واژه** از جدول‌های واژگان بخش ۲ استفاده شود.

---

### 10. Mini Project / پروژهٔ کوچک

**انشا (نیمه‌تحقیقی): پنجره‌های باز یک سامانهٔ واقعی**

یک سامانهٔ واقعی را انتخاب کنید که **خودتان** با آن کار می‌کنید (سامانهٔ آموزشی دانشگاه، شبکهٔ کارگاه، ابزار داخلی محل کار، یا سامانهٔ یک کسب‌وکار کوچک در خانواده) و یک ارزیابی کوتاه بنویسید:

- **دارایی:** کدام داده ارزشمند است و کدام حساب‌ها به آن دسترسی دارند؟
- **مسیر فرضی حمله:** یک مهاجم از کدام نقطه وارد می‌شود و از آنجا به کجا می‌رود؟
- **شکل دستی:** مسیر بالا را روی کاغذ بکشید و روی هر پیکان یک مرحله و یک نشانهٔ قابل تشخیص بنویسید (ورود، حرکت جانبی، دسترسی به داده).
- **جدول دستی مقایسه:** جدولی با چهار سطر بکشید و کنترل فعلی را با کنترل پیشنهادی مقایسه کنید: هزینه، اثر بر امنیت، زمان لازم برای اجرا، دشواری نگه‌داری.
- **سه اقدام مشخص:** یک حساب که باید بسته شود، یک اختیار که باید موقت شود، و یک گزارش که باید ثبت و بازبینی شود را نام ببرید.
- **جمله‌های گرامری:** پنج جملهٔ **مجهول** بنویسید، شامل یک *should have been* و یک *must be*.

**شرایط نگارش:**

- گزارش را **دست‌نویس روی کاغذ** بنویسید و در **جلسهٔ بعد** به مدرس تحویل دهید.
- دست‌کم **۲۵۰ واژه** باشد.
- دست‌کم **۵ جملهٔ مجهول** و **۲ جمله** با *might have been* یا *could have been* داشته باشد.
- طرح دستی مسیر حمله و جدول دستی مقایسه در گزارش باشد.
- دست‌کم **۱۲ واژه** از جدول‌های واژگان بخش ۲ در گزارش به‌کار رفته باشد.

**واژه‌های یاری‌دهنده:** least privilege · just-in-time access · entitlement · toxic combination · revocation · attack path · lateral movement · dwell time · indicator of compromise · containment · chain of custody · compensating control

---

### 11. Did You Know? / آیا می‌دانستید؟

1. **The expression "zero trust" became popular through an analyst report in 2010, and the idea is often traced back to a 2004 report that argued the network perimeter was already dissolving.**
   عبارت «اعتماد صفر» با گزارشی تحلیلی در سال ۲۰۱۰ رایج شد و ریشهٔ ایده را معمولاً به گزارشی در ۲۰۰۴ برمی‌گردانند که استدلال می‌کرد مرز شبکه از پیش در حال از هم پاشیدن است.

2. **The first research papers on honeypots appeared around 1990, and the whole point of the design was to record an attack instead of preventing it.**
   نخستین مقاله‌های پژوهشی دربارهٔ هانی‌پات حدود سال ۱۹۹۰ منتشر شد و هدف اصلی این طراحی، ثبت حمله بود، نه جلوگیری از آن.

3. **The word "canary" in a canary token comes from the canary words printed in some government documents, which revealed which copy had been leaked.**
   واژهٔ «قناری» در توکن تله از «کلمه‌های قناری» گرفته شده است؛ کلمه‌هایی که در برخی اسناد دولتی چاپ می‌شد تا معلوم شود کدام نسخه لو رفته است.

4. **In 2022, a large technology company reported that a stolen session cookie, and not a password, had been used to enter its internal systems.**
   در سال ۲۰۲۲ شرکتی بزرگ در حوزهٔ فناوری گزارش کرد که برای ورود به سامانه‌های داخلی‌اش از یک کوکی نشست دزدیده‌شده استفاده شده بود، نه از رمز عبور.

5. **The standard behind passkeys was published in 2019, and several large platforms began to offer passkeys to ordinary users in 2022 and 2023.**
   استاندارد پشت کلیدهای عبور در سال ۲۰۱۹ منتشر شد و چند پلتفرم بزرگ در ۲۰۲۲ و ۲۰۲۳ عرضهٔ آن را به کاربران عادی آغاز کردند.

6. **Industry research published in 2023 reported an average of roughly nine months to identify and contain a breach, and shorter times were linked to faster detection rather than to better tools.**
   پژوهشی صنعتی که در ۲۰۲۳ منتشر شد، میانگین زمانی حدود نُه ماه را برای شناسایی و مهار یک نفوذ گزارش کرد و زمان‌های کوتاه‌تر را به تشخیص سریع‌تر نسبت داد، نه به ابزار بهتر.

7. **In 2024, the first post-quantum encryption standards were published, after a public competition that lasted several years.**
   در سال ۲۰۲۴ نخستین استانداردهای رمزنگاری پساکوانتومی منتشر شد؛ پس از مسابقه‌ای عمومی که چند سال طول کشید.

8. **The purple team, in which the attackers and the defenders work in the same room, became a common practice in industry publications after 2018.**
   تیم بنفش — جایی که مهاجمان و مدافعان در یک اتاق کار می‌کنند — از سال ۲۰۱۸ به بعد در نشریه‌های صنعتی به رویه‌ای رایج تبدیل شد.
