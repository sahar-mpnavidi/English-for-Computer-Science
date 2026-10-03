# Lesson 19: Cloud-Native, DevOps, and Microservices

## Level: B2–C1
## Time: 90–120 minutes

> **درس ۱۹ — کلاود-نیتیو، دواپس و میکروسرویس‌ها**
> **نکتهٔ گرامری:** نقل قول (reported speech) · backshift و تغییر ضمیر و قید زمان · say و tell · پرسش و فرمان در نقل قول
> **متن درس:** ۲۹۶۸ واژه (۳۳ پاراگراف) | **واژگان کلیدی:** ۱۲۱ واژه | **باند سطح:** B2–C1 (پیشرفته)

---

### 1. Lesson Objectives / اهداف درس

- تفاوت معماری یکپارچه و ریزخدمت‌ها را توضیح دهید و بگویید مرز میان سرویس‌ها چگونه تعیین می‌شود.
- اجزای یک سامانهٔ کانتینری (تصویر، پاد، نسخهٔ تکراری، مانیفست، کاوشگر سلامت) را با واژگان دقیق نام ببرید.
- الگوهای مقاوم‌سازی (تلاش دوباره، عقب‌نشینی نمایی، قطع‌کنندهٔ مدار، افت کنترل‌شده) را تحلیل کنید و برای هر کدام یک نمونه بگویید.
- خط لولهٔ تحویل و راهبردهای انتشار (آبی-سبز، عرضهٔ پنهان، دروازهٔ کیفیت، توقف انتشار) را به انگلیسی شرح دهید.
- مشاهده‌پذیری، بودجهٔ خطا و گزارش پس از حادثه را با لحن حرفه‌ای و غیرسرزنشی توصیف کنید.
- گفت‌وگوی تیمی و تصمیم‌های گذشته را با نقل قول درست (با backshift و تغییر ضمیر) بازگو کنید.

---

### 2. Key Vocabulary / واژگان کلیدی

> تلفظ‌ها بر پایهٔ انگلیسی آمریکایی و در قالب IPA نوشته شده‌اند.

**جدول ۱ — معماری و اجزای سرویس (Architecture and Service Components)**

| فارسی | تلفظ | Definition (EN) | Example (EN) | English |
|---|---|---|---|---|
| ریزخدمت‌ها | /ˈmaɪkroʊˌsɜːrvɪsɪz/<br>مایکرو‌سِرْویسِز | Small services that are built, released, and run separately. | Microservices let one team release without the others. | microservices |
| یکپارچه | /ˈmɑːnəlɪθ/<br>مانَه‌لیث | One program that contains the whole system. | The monolith served the company for six years. | monolith |
| یکپارچه (صفت) | /ˌmɑːnəˈlɪθɪk/<br>مانَه‌لیثیک | Built as one large unit. | A monolithic design is easy to run and hard to change. | monolithic |
| تجزیه به اجزا | /ˌdiːkɑːmpəˈzɪʃn/<br>دیکامپُزیشِن | The act of breaking a system into smaller parts. | The decomposition of the invoice path took two months. | decomposition |
| جدا کردن وابستگی | /ˌdiːˈkʌpl/<br>دی‌کاپُل | To remove a dependency between two parts. | They decoupled payments from the driver app. | decouple |
| وابستگی متقابل | /ˈkʌplɪŋ/<br>کاپلینگ | How much one part must change when another changes. | Loose coupling is the goal of every boundary. | coupling |
| پیوستگی درونی | /koʊˈhiːʒn/<br>کوهیژِن | How well the parts inside one service belong together. | High cohesion makes a service easy to name. | cohesion |
| زمینهٔ محدود | /ˈbaʊndɪd ˈkɑːntekst/<br>باوندِد کانتِکست | The border where one business meaning ends. | A bounded context decides where a service is cut. | bounded context |
| سایدکار | /ˈsaɪdkɑːr/<br>ساید‌کار | A helper container that runs beside the main one. | The sidecar collects metrics for the service. | sidecar |
| شبکهٔ سرویس | /ˈsɜːrvɪs meʃ/<br>سِرْویس مِش | A layer that connects and protects many sidecars. | The service mesh handled mTLS for every call. | service mesh |
| ورودی | /ˈɪnɡres/<br>این‌گرِس | Traffic coming into a cluster. | One ingress rule sends each path to one service. | ingress |
| خروجی | /ˈiːɡres/<br>ای‌گرِس | Traffic leaving a cluster. | An egress rule stops calls to unknown domains. | egress |
| فضای نام | /ˈneɪmspeɪs/<br>نِیم‌اسپِیس | A named area that keeps one team's objects apart. | Each team received its own namespace. | namespace |
| پاد | /pɑːd/<br>پاد | The smallest unit that an orchestrator starts. | One pod holds the service and its sidecar. | pod |
| نسخهٔ تکراری | /ˈreplɪkə/<br>رِپلیکا | One running copy of a service. | Three replicas survived the loss of one machine. | replica |
| صفحهٔ کنترل | /kənˈtroʊl pleɪn/<br>کانترول پلِین | The part that stores the desired state. | The control plane decided where the pod should run. | control plane |
| صفحهٔ داده | /ˈdeɪtə pleɪn/<br>دِیتا پلِین | The part that carries the real traffic. | The data plane never touched the configuration. | data plane |
| مانیفست | /ˈmænɪfest/<br>مَنِفِست | A file that describes the resources you want. | The manifest asks for three copies of the image. | manifest |
| امری | /ɪmˈperətɪv/<br>ایمپِرَتِیو | Described as a list of commands to run. | An imperative script is hard to read a year later. | imperative |
| تغییرناپذیر | /ɪˈmjuːtəbl/<br>ایمْیوتَبُل | That cannot be changed after it is built. | An immutable image is replaced, not repaired. | immutable |
| کانتینر | /kənˈteɪnər/<br>کانتِینِر | A package that holds a program with its libraries. | The container runs the same way on a laptop. | container |
| تصویر کانتینر | /kənˈteɪnər ˈɪmɪdʒ/<br>کانتِینِر ایمِیج | The built file from which containers are started. | The pipeline built one container image per commit. | container image |
| کانتینری‌سازی | /kənˌteɪnəraɪˈzeɪʃn/<br>کانتِینِرِیزِیشِن | The practice of packing everything into containers. | Containerization ended the old problem of driver versions. | containerization |
| بررسی سلامت | /helθ tʃek/<br>هِلث چِک | A simple test of whether a service still works. | The health check failed before the users noticed. | health check |
| زنده‌بودن | /ˈlaɪvnəs/<br>لایوْنِس | The state of a process that is still running. | A liveness probe restarted the frozen process. | liveness |
| آمادگی | /ˈredinəs/<br>رِدینِس | The state of being ready to receive traffic. | Readiness kept traffic away from a starting service. | readiness |
| کاوشگر | /proʊb/<br>پروب | A test that the platform repeats on a schedule. | The probe answers one question with one number. | probe |
| کشف سرویس | /ˈsɜːrvɪs dɪˈskʌvəri/<br>سِرْویس دیسکاوِری | Finding a service address without hard-coding it. | Service discovery removed the row of IP addresses. | service discovery |
| قطع‌کنندهٔ مدار | /ˈsɜːrkɪt ˈbreɪkər/<br>سِرکِت برِیکِر | A pattern that stops calls to a failing service. | The circuit breaker opened after ten errors. | circuit breaker |
| جداسازی محفظه‌ای | /ˈbʌlkhed/<br>بالک‌هِد | Keeping one failure inside its own compartment. | A bulkhead stopped one slow job from sinking the app. | bulkhead |
| شعاع اثر | /blæst ˈreɪdiəs/<br>بلَست رِیدیوس | How much is damaged when one part fails. | A smaller service has a smaller blast radius. | blast radius |

**جدول ۲ — تحویل، استقرار و خط لوله (Delivery, Deployment, and Pipeline)**

| فارسی | تلفظ | Definition (EN) | Example (EN) | English |
|---|---|---|---|---|
| یکپارچه‌سازی و تحویل پیوسته | /ˌsiː aɪ ˈsiː diː/<br>سی‌آی‌سی‌دی | The short form for integration and delivery together. | CI/CD turned a monthly release into a daily one. | CI/CD |
| یکپارچه‌سازی پیوسته | /kənˌtɪnjuəs ˌɪntɪˈɡreɪʃn/<br>کانتینیوِس اینتِگرِیشِن | Building and testing every change within minutes. | Continuous integration caught the error in ten minutes. | continuous integration |
| تحویل پیوسته | /kənˌtɪnjuəs dɪˈlɪvəri/<br>کانتینیوِس دیلیوِری | Keeping the result always ready to be released. | Continuous delivery made the release boring. | continuous delivery |
| شاخهٔ اصلی | /trʌŋk/<br>ترونک | The single shared line of development. | All work happened on the trunk, not on branches. | trunk |
| پرچم ویژگی | /ˈfiːtʃər flæɡ/<br>فیچِر فلَگ | A switch that hides unfinished work in production. | The feature flag stayed off until the review. | feature flag |
| آبی-سبز | /ˌbluː ˈɡriːn/<br>بلو گرین | Two full environments with traffic moved between them. | The blue-green release moved traffic in one minute. | blue-green |
| عرضهٔ پنهان | /dɑːrk lɔːntʃ/<br>دارک لانچ | Sending real traffic to a version that does not answer yet. | The dark launch tested the new path for a week. | dark launch |
| جابه‌جایی به چپ | /ʃɪft left/<br>شیفت لِفت | Moving quality work earlier in the process. | Shift left means the developer sees the failure first. | shift left |
| قطار انتشار | /rɪˈliːs treɪn/<br>ریلیس ترِین | Releases that leave on a fixed schedule. | A missed release train costs one week, not one quarter. | release train |
| وصلهٔ فوری | /ˈhɑːtfɪks/<br>هات‌فیکس | A quick repair released outside the normal plan. | A hotfix went out at nine in the evening. | hotfix |
| پیشروی به نسخهٔ نو | /ˈroʊl fɔːrwərd/<br>رول فوروِرد | Fixing a problem by moving to a new version. | The team chose a roll-forward instead of a rollback. | roll-forward |
| آزمون طولانی‌مدت | /soʊk test/<br>سوک تِست | A test that keeps the pressure on for hours. | The soak test found a memory leak on day two. | soak test |
| آزمون بار | /loʊd test/<br>لود تِست | A test that sends realistic levels of traffic. | The load test showed the limit of one replica. | load test |
| آزمون دود | /smoʊk test/<br>اسموک تِست | A very short test that only checks the basics. | The smoke test answers one question: does it start? | smoke test |
| روز تمرین | /ɡeɪm deɪ/<br>گِیم دِی | A planned day when a team practises a failure. | The game day broke the payment service on purpose. | game day |
| مهندسی آشوب | /ˈkeɪɑːs ˌendʒɪˈnɪrɪŋ/<br>کِیاس اِنجینیرینگ | Deliberately breaking systems to learn how they fail. | Chaos engineering turned accidents into rehearsals. | chaos engineering |
| تزریق خطا | /fɔːlt ɪnˈdʒekʃn/<br>فُلت این‌جِکشِن | Adding a fault on purpose to see the result. | Fault injection delayed one dependency by two seconds. | fault injection |
| زیرساخت به‌صورت کد | /ˈɪnfrəstrʌktʃər əz koʊd/<br>اینفرااس‌تراکچِر اَز کُد | Describing servers and networks in reviewable files. | Infrastructure as code put the network in Git. | infrastructure as code |
| بی‌اثر در تکرار | /aɪˈdempətənt/<br>آی‌دِمپُتِنت | Giving the same result when it is run again. | An idempotent job can be restarted safely. | idempotent |
| بی‌اثری تکرار | /aɪˌdempəˈtensi/<br>آی‌دِمپُتِنسِی | The property that makes a repeat run harmless. | Idempotency is what makes a retry safe. | idempotency |
| تلاش دوباره | /ˌriːˈtraɪ/<br>ری‌ترای | Trying a failed request again. | A retry after one second solved most of the errors. | retry |
| عقب‌نشینی نمایی | /ˌekspəˈnenʃl ˈbækɔːf/<br>اِکسپُنِنشِل بَک‌آف | Waiting twice as long after each failed attempt. | Exponential backoff stopped the retry storm. | exponential backoff |
| مهلت | /ˈtaɪmaʊt/<br>تایم‌اوت | The longest time a client will wait. | A short timeout kept the page responsive. | timeout |
| محدود کردن نرخ | /ˈθrɑːtl/<br>ثراتِل | To slow down a client that sends too much. | The gateway throttles one account at a time. | throttle |
| افت کنترل‌شده | /ˈɡreɪsfəl ˌdeɡrəˈdeɪʃn/<br>گرِیسفُل دِگرِدِیشِن | Returning a smaller answer instead of no answer. | Graceful degradation showed the last cached price. | graceful degradation |
| انتشار-اشتراک | /ˈpʌblɪʃ səbˈskraɪb/<br>پابلیش سَب‌اسکرایب | Sending one event to many unknown readers. | Publish-subscribe let four teams read the same event. | publish-subscribe |
| اتوبوس رویداد | /ɪˈvent bʌs/<br>ایوِنت باس | The channel that carries events between services. | The event bus delivered the order in one second. | event bus |
| پیام بی‌سرانجام | /ded ˈletər/<br>دِد لِتِر | A queue for messages that could not be processed. | The dead letter queue held twenty broken events. | dead letter |
| الگوی ساگا | /ˈsɑːɡə/<br>ساگا | A long process written as a series of local steps. | The saga released the seat when payment failed. | saga |
| تراکنش جبرانی | /ˈkɑːmpənseɪtɪŋ trænˈzækʃn/<br>کامپِنسِیتینگ ترَنزَکشِن | A step that undoes an earlier step. | A compensating transaction returned the money. | compensating transaction |
| هماهنگی غیرمتمرکز | /ˌkɔːriˈɑːɡrəfi/<br>کوری‌اگرَفی | Coordination in which each service knows its next step. | Choreography has no conductor and many rules. | choreography |

**جدول ۳ — بهره‌برداری، پایش و پاسخ (Operations, Observability, and Response)**

| فارسی | تلفظ | Definition (EN) | Example (EN) | English |
|---|---|---|---|---|
| مشاهده‌پذیری | /əbˌzɜːrvəˈbɪləti/<br>آبزِروَبِلیتی | Being able to answer new questions from the data you keep. | Observability is what a dashboard cannot give you. | observability |
| قطعهٔ ردگیری | /spæn/<br>اسپَن | One timed step inside a single request. | The slow span was the second database call. | span |
| شناسهٔ همبستگی | /ˌkɔːrəˈleɪʃn aɪ diː/<br>کورِلِیشِن آی‌دی | A shared identifier that follows one request. | The correlation id joined four service logs. | correlation id |
| اشباع | /ˌsætʃəˈreɪʃn/<br>سَچِرِیشِن | How full a resource is before it fails. | Saturation reached ninety percent before the outage. | saturation |
| تجمیع لاگ | /lɔːɡ ˌæɡrɪˈɡeɪʃn/<br>لاگ اَگریگِیشِن | Collecting the text output of every service in one place. | Log aggregation turned six machines into one search box. | log aggregation |
| پایش مصنوعی | /sɪnˈθetɪk ˈmɑːnɪtərɪŋ/<br>سین‌ثِتیک مانیتُرینگ | Repeating a fake user journey on a schedule. | Synthetic monitoring found the broken login at two in the morning. | synthetic monitoring |
| گزارش پس از حادثه | /ˈpoʊstmɔːrtem/<br>پوست‌مورتِم | A written review of an incident. | The postmortem named three missing signals. | postmortem |
| بدون سرزنش | /ˈbleɪmləs/<br>بلِیم‌لِس | Written about the system, not about a person. | A blameless postmortem gave the real reason. | blameless |
| کشیک | /ˌɑːn ˈkɔːl/<br>آن کال | The duty of answering alerts outside working hours. | On-call duty rotates every week. | on-call |
| دسته‌بندی فوری | /ˈtriːɑːʒ/<br>تری‌اژ | Deciding what is urgent and what can wait. | Triage took five minutes and saved an hour. | triage |
| پاسخ‌دهنده | /rɪˈspɑːndər/<br>ریسپان‌دِر | The person who takes charge of an incident. | The responder wrote one page and called two people. | responder |
| ریشهٔ علت | /ruːt kɔːz/<br>روت کاز | The deepest reason that a failure happened. | The root cause was a manual change nobody recorded. | root cause |
| شیوه‌نامهٔ واکنش | /ˈpleɪbʊk/<br>پلِی‌بوک | A written order of checks for one kind of incident. | The playbook told the team which log to open first. | playbook |
| کار تکراری فرساینده | /tɔɪl/<br>تویل | Boring manual work that a machine should do. | Toil is the enemy that automation is built to remove. | toil |
| خودخدمت | /ˌself ˈsɜːrvɪs/<br>سِلف سِرْویس | A service that a developer can use without a ticket. | Self-service removed two days of waiting. | self-service |
| مسیر طلایی | /ˈɡoʊldən pæθ/<br>گولدِن پَث | The one well-tested way to build and run a service. | The golden path was short and fully documented. | golden path |
| تیم پلتفرم | /ˈplætfɔːrm tiːm/<br>پلَتفورم تیم | The team that provides the path for others. | The platform team treated developers as customers. | platform team |
| تجربهٔ توسعه‌دهنده | /dɪˈveləpər ˈɪkspɪriəns/<br>دیوِلُپِر اِکسپیریِنس | How easy or hard the daily work of a developer is. | Developer experience improved when the build took two minutes. | developer experience |
| هدف سطح سرویس | /es el oʊ/<br>اِس‌اِل‌او | The quality that a team promises to its users. | The SLO promised ninety-nine percent availability. | SLO |
| بودجهٔ خطا | /ˈerər ˈbʌdʒɪt/<br>اِرِر باجِت | The failure that the promise still allows. | The error budget was spent in eleven days. | error budget |
| میانگین زمان بازیابی | /ˌem tiː tiː ˈɑːr/<br>اِم‌تی‌تی‌آر | The average time from failure to recovery. | A shorter MTTR helped more than a perfect score. | MTTR |
| ناحیهٔ دسترس‌پذیری | /əˈveɪləbɪləti zoʊn/<br>اَوِیلَبِلیتی زون | One building with its own power and cooling. | One availability zone lost power for an hour. | availability zone |
| چندمنطقه‌ای | /ˌmʌlti ˈriːdʒən/<br>مالتی ریجِن | Running copies in more than one region. | A multi-region design survived the local outage. | multi-region |
| بازیابی از فاجعه | /dɪˈzæstər rɪˈkʌvəri/<br>دیزَستِر ریکاوِری | The plan for the worst day. | Disaster recovery was tested twice a year. | disaster recovery |
| آزمایش آشوب | /ˈkeɪɑːs ɪkˌsperɪmənt/<br>کِیاس اِکسپِرِمِنت | One planned, small, reversible failure test. | The chaos experiment stopped one replica for ten minutes. | chaos experiment |
| بازپس‌گیری هزینه | /ˈtʃɑːrdʒbæk/<br>چارجبَک | Sending the cloud bill to the team that spent it. | Chargeback changed behaviour in one month. | chargeback |
| نمایش هزینه | /ˈʃoʊbæk/<br>شوبَک | Showing a team its cost without moving the money. | Showback was accepted before chargeback was. | showback |
| مدیریت مالی ابر | /ˈfɪnɑːps/<br>فیناپس | The practice of linking cost to technical decisions. | FinOps found a forgotten cluster in two days. | FinOps |
| آگاه به کربن | /ˈkɑːrbən əˈwer/<br>کاربُن اَوِر | Choosing when to run work by how clean the grid is. | A carbon-aware job waited for the windy hours. | carbon-aware |
| مقیاس‌دهی افقی | /ˌhɔːrɪˈzɑːntl ˈskeɪlɪŋ/<br>هوریزانتَل اسکِیلینگ | Adding more copies of a service. | Horizontal scaling solved the Friday evening peak. | horizontal scaling |
| مقیاس‌دهی عمودی | /ˈvɜːrtɪkl ˈskeɪlɪŋ/<br>وِرتیکَل اسکِیلینگ | Giving one machine more power. | Vertical scaling ended at the largest machine available. | vertical scaling |

**جدول ۴ — زنجیرهٔ تأمین، حاکمیت و امنیت تحویل (Supply Chain, Governance, and Delivery Security)**

| فارسی | تلفظ | Definition (EN) | Example (EN) | English |
|---|---|---|---|---|
| زنجیرهٔ تأمین | /səˈplaɪ tʃeɪn/<br>سَپلای چِین | Every component and step that produced your software. | A supply chain is as strong as its weakest library. | supply chain |
| وابستگی | /dɪˈpendənsi/<br>دیپِندِنسِی | A library that your program needs. | The dependency was updated once a month. | dependency |
| وابستگی زنجیره‌ای | /trænˈzɪtɪv dɪˈpendənsi/<br>ترَنزیتیو دیپِندِنسِی | A library that another library brought with it. | A transitive dependency added three unknown packages. | transitive dependency |
| فایل قفل نسخه | /lɑːk faɪl/<br>لاک فایل | A file that records the exact version of every library. | The lock file made two machines build the same image. | lock file |
| زنجیرهٔ ابزار | /ˈtuːltʃeɪn/<br>تول‌چِین | All the tools used to build and check the software. | The toolchain was replaced one tool at a time. | toolchain |
| ابزار بازبینی کد | /ˈlɪntər/<br>لینتِر | A program that reports style and simple mistakes. | The linter rejected a missing return value. | linter |
| قلاب پیش از ثبت | /ˌpriː ˈkɑːmɪt hʊk/<br>پری کامیت هوک | A check that runs before a change is recorded. | The pre-commit hook caught a secret before it was saved. | pre-commit hook |
| دروازهٔ کیفیت | /ˈkwɑːləti ɡeɪt/<br>کوالِتی گِیت | A rule that stops a change from moving forward. | The quality gate blocked the release for one failed test. | quality gate |
| توقف انتشار | /rɪˈliːs friːz/<br>ریلیس فریز | A period when no release is allowed. | A release freeze protected the sales week. | release freeze |
| تفکیک وظایف | /ˌsepəˈreɪʃn əv ˈduːtiz/<br>سِپَرِیشِن آو دیوتیز | The rule that the author is not the approver. | Separation of duties is why two people sign the change. | separation of duties |
| دسترسی اضطراری | /ˈbreɪk ɡlæs/<br>برِیک گلَس | A special account that is used only in an emergency. | The break-glass account was used once in three years. | break-glass |
| اطلاعات نهانی | /ˈsiːkrəts/<br>سیک‌رِتس | Passwords, keys, and tokens that must stay hidden. | Secrets belong in a store, never in the code. | secrets |
| چرخش رازها | /ˈsiːkrət roʊˈteɪʃn/<br>سیک‌رِت روتِیشِن | Changing the keys on a regular schedule. | Secret rotation is a calendar task, not a heroic one. | secret rotation |
| احراز هویت متقابل | /ˌem tiː el es/<br>اِم‌تی‌اِل‌اِس | Both sides of a connection prove who they are. | mTLS stopped an unknown service from calling the database. | mTLS |
| سیاست شبکه | /ˈnetwɜːrk ˈpɑːləsi/<br>نِتوِرک پالِسی | A written rule about which paths are allowed. | The network policy allowed one port and nothing else. | network policy |
| کنترل‌گر پذیرش | /ədˈmɪʃn kənˈtroʊlər/<br>اَدمیشِن کانترولِر | The part that refuses a resource that breaks the rules. | The admission controller rejected an unsigned image. | admission controller |
| سیاههٔ نرم‌افزار | /es biː oʊ em/<br>اِس‌بی‌او‌اِم | A list of every component inside a build. | The SBOM answered the question in one minute. | SBOM |
| گواهی صادق | /ˌætesˈteɪʃn/<br>اَتِستِیشِن | A signed statement about how something was built. | The attestation proved the build came from the pipeline. | attestation |
| شناسهٔ آسیب‌پذیری شناخته‌شده | /siː viː iː/<br>سی‌وی‌ای | A public identifier for one known weakness. | One CVE put the whole hospital offline. | CVE |
| چک‌سام تصویر | /ˈdaɪdʒest/<br>دایجِست | A long checksum that identifies exact bytes. | The digest showed that two images were different. | digest |
| دستکاری کردن | /ˈtæmpər/<br>تَمپِر | To change something secretly. | A tampered image can pass a simple name check. | tamper |
| حذف اطلاعات حساس | /rɪˈdækt/<br>رِدَکت | To remove private details from a text. | Redact the phone number before you paste the log. | redact |
| معافیت موقت | /ˈweɪvər/<br>وِیوِر | Written permission to break a rule for a short time. | Every waiver carries a date and an owner. | waiver |
| اقامت داده | /ˈdeɪtə ˈrezɪdənsi/<br>دِیتا رِزیدِنسِی | The rule about which country may store a record. | Data residency kept the medical records inside the country. | data residency |
| حاکمیت داده | /ˈsɑːvrənti/<br>ساوِرِنتی | The rule that local law governs local data. | Sovereignty is a legal question with a technical answer. | sovereignty |
| مرز اعتماد | /trʌst ˈbaʊndri/<br>تراست باوندری | The line where one team's control ends. | The trust boundary sat between the two namespaces. | trust boundary |
| کلید قطع اضطراری | /kɪl swɪtʃ/<br>کیل اسویچ | A switch that turns a feature off immediately. | The kill switch ended the incident in ten seconds. | kill switch |
| اجرای آزمایشی | /draɪ rʌn/<br>درای ران | A run that checks the work without changing anything. | The dry run printed the plan and stopped. | dry run |

---

### 3. Reading / متن اصلی

**عنوان متن: Small Services, Fast Changes (سرویس‌های کوچک، تغییرهای سریع)**

**[1]** Cloud-native software is built for a world where machines fail, traffic arrives in waves, and the next change comes on Thursday. DevOps is the culture that moves one team closer to the other: the people who write the code and the people who keep it running answer for the same result. Nasrin, a reliability engineer at a delivery company, says that her job is not to keep servers alive; she says that her job is to keep changes small. Kamran, a junior developer at a small start-up, learned the same lesson in his first month.

**[2]** Nasrin's company started with one program that did everything: orders, payments, drivers, and invoices. Such a system is a monolith, and for six years it was a good design. The problem was not the code but the friction. A change in the invoice screen required a test of the whole system, and one slow report could freeze the payments page. The team decided to break the program into smaller parts, and this decomposition is what everybody now calls microservices.

**[3]** A monolith is one deployable unit; a monolithic design is therefore easy to run and hard to change. Microservices are the opposite: many small units, each with its own purpose, its own database, and its own release. The hard part is not dividing the code; it is finding where to divide it. A bounded context marks the place where one business meaning ends and another begins, and teams that get this wrong end up with a distributed monolith: many services that must still be released together.

**[4]** The goal of the split is to decouple the parts. When two services are tightly coupled, a change in one forces a change in the other, and the network becomes the weakest link. Good design raises cohesion inside a service and lowers coupling between services, so that each service can be understood, tested, and replaced alone. A smaller service also has a smaller blast radius: when it fails, fewer people notice. Nothing is free, however, because every new boundary is also a new place where a request can be lost, delayed, or blocked.

**[5]** Containers made this practical. A container packs an application with its libraries, so the same program runs on a laptop and in the data centre; the practice of using them everywhere is containerization. The build produces a container image, and an image is normally immutable: you do not repair it, you build a new one. Each image is identified by a digest, a long checksum that proves you are running the exact bytes you tested.

**[6]** At scale, nobody starts containers by hand. An orchestrator places them: the smallest unit it manages is a pod, and a replica keeps the required number of copies alive. The control plane holds the desired state, while the data plane carries the real traffic. You describe what you want in a manifest, which is a declarative file: "three copies of this image", not "start three containers now". The imperative style, a list of commands, is what people use on a bad day at two in the morning.

**[7]** Inside a cluster, a namespace separates one team's objects from another's. A service is found through service discovery instead of a hard-coded address, and a small helper container that runs beside the main one is called a sidecar; together, many sidecars form a service mesh. Traffic enters through an ingress rule and leaves through an egress rule. The platform also checks health: a liveness probe asks whether a process is still alive, a readiness probe asks whether it is ready to receive traffic, and a health check is the simple version of both.

**[8]** A network call can fail in ways that a local function call cannot. The patterns are old and boring. A retry repeats a failed request, but it must use exponential backoff, because a thousand clients that all retry at once will finish the service; a timeout stops a client from waiting for ever; a throttle limits how much work one client may send; and a circuit breaker stops sending requests to a service that is clearly broken. A graceful degradation returns a smaller answer instead of no answer at all, and a bulkhead keeps one failing part from sinking the whole ship. The alternative is the thundering herd, where every client arrives at the same second.

**[9]** Some work should not wait for an answer. An event bus carries messages from a producer to a consumer, and the publish-subscribe pattern lets any number of readers receive the same event. When a message cannot be processed, it goes to a dead letter queue and waits for a human being. A long business process is often written as a saga: a series of local steps, each with a compensating transaction that undoes it if a later step fails. This kind of choreography has no central conductor, which is a strength and a difficulty at the same time.

**[10]** None of this survives without an automated pipeline. Continuous integration means that every change is built and tested within minutes; continuous delivery means that the result is always ready to be released, and the two together are known by the short form CI/CD. Developers work on a short trunk rather than on long-lived branches, and a feature flag hides unfinished work in production instead of in a branch. The pipeline is a quality gate: a linter checks the style, a pre-commit hook catches the worst mistakes before they are even saved, and a lock file keeps the exact versions of every dependency, including the transitive dependency that nobody remembers adding. This is what shift left means in practice: the quality work moves closer to the developer, where a mistake is cheap to repair.

**[11]** A modern toolchain adds two documents that few developers had heard of ten years ago. A software bill of materials, or SBOM, lists every component inside an artifact, and an attestation is a signed statement that says how the artifact was built. Both exist because a supply chain is only as strong as its weakest link: a single library with a known CVE can put a hospital offline. Teams therefore pin their versions, scan for tampering, and treat a dependency as a product with an owner.

**[12]** Releasing is a design decision too. A blue-green release runs two full environments and moves traffic from one to the other; a dark launch sends real traffic to the new version without letting it answer; a canary deployment gives the new version to one percent of users, and a roll-forward fixes the problem by moving forward rather than backwards. A dry run checks the release without touching production, and a kill switch turns it off in one click. Twice a year a release freeze stops everything before a big sales week, and every freeze needs a written waiver for the emergency fix that cannot wait. A release train leaves on a fixed schedule, so that a missed train costs the team one week instead of one quarter.

**[13]** Infrastructure as code is the habit that makes all of this repeatable: the servers, networks, and permissions live in files that are reviewed like any other code. The property that makes those files safe to run twice is idempotency: an idempotent script produces the same state whether you run it once or five times. The same idea creates ephemeral environments. A preview environment is built for each change and destroyed afterwards, and a sandbox environment lets a new developer practise in the real system without danger. The cost of this approach is a cold start: a fresh environment answers its first request slowly until everything is warm.

**[14]** Testing follows the same logic. A smoke test asks only whether the door opens; a load test pushes a realistic amount of traffic; a soak test keeps the pressure on for hours to find the slow leak. A game day puts the whole team in one room and breaks something on purpose, and chaos engineering turns that habit into a discipline. A chaos experiment is planned, small, and reversible, and it usually begins with fault injection: one network rule is changed, one dependency is delayed, and the team watches what happens in the dark.

**[15]** Since you cannot fix what you cannot see, observability is the second half of reliability. A single request is followed through many services as a span inside a trace, and a correlation id travels with it, so that the pieces can be joined later. Log aggregation collects the text that every service produced, and synthetic monitoring repeats a fake user journey every minute. Saturation is the quiet signal: it shows how full a resource is before anything fails.

**[16]** Alerts are a contract with the customer. A service level objective, or SLO, states the quality that the team promises, and the error budget is the amount of failure that the promise allows. When the budget is spent, new features stop and reliability work starts. MTTR, the average time from failure to recovery, is often more useful than any average of good days. The person who carries the phone is on call, and the first job of that person is triage: decide what is burning, what can wait, and who must be called.

**[17]** When something does break, the response is a process, not a performance. The responder declares an incident, and a playbook describes the order of the checks. The team then writes a postmortem, and a good one is blameless: it names the missing signal, the unclear design, and the slow decision, not the tired engineer. The root cause is usually a small thing that the system allowed to grow, and the strongest question in a review is still the simplest one: what did we not see?

**[18]** All of this work needs an owner, and that is the platform team. Its product is not a server but a golden path: one well-tested way to build, deploy, and observe a service. The path is offered as self-service, because a developer who must wait for a ticket will find a way around the rules. Developer experience is therefore a technical subject with business results, and any task that a machine can do is toil that a team should remove.

**[19]** Money is part of the design as well. FinOps is the practice of linking cost to the decisions that create it: rightsizing a machine, choosing a spot instance for a flexible job, or buying reserved capacity for a steady one. A chargeback sends the bill to the team that spent it; a showback simply shows the bill without moving the money. Neither is popular, and both change behaviour in one month.

**[20]** Reliability is also a question of geography. One availability zone is one building with its own power and cooling, and a bad week can take it away; a multi-region design keeps a copy in a different country. Disaster recovery is the plan for the worst day, and it is measured, not described: a backup that has never been restored is a hope, not a plan.

**[21]** Security moves into the pipeline for the same reason. Secrets no longer live in the code, and secret rotation changes the keys on a schedule instead of after a leak. Between services, mTLS proves both sides of the connection, and a network policy writes the allowed paths into a file. An admission controller refuses an image that breaks the rules, and the trust boundary is drawn where one team's control ends and another's begins. Before a release, every component is checked against known CVE entries, the image digest is verified, and any personal data in the logs is redacted before it leaves the building.

**[22]** Governance is the least exciting chapter and the one that saves careers. Separation of duties means that the person who writes the change is not the person who approves it, and a break-glass account exists for the emergency that this rule would otherwise block; every use of it is reviewed the next morning. In many countries, data residency decides which region may store a record, and sovereignty adds the rule that the operator of that region must obey local law. A waiver can delay a rule, but only in writing, with a date on it.

**[23]** Even the environment has become a design input. A carbon-aware scheduler runs flexible work when the local grid is cleaner, and the same logic that lowers a bill usually lowers an emission. Nobody who builds a service in 2024 can say that this is somebody else's problem.

**[24]** Nasrin's migration took fourteen months. She told the managers that the first three services would be slow and boring, and she said that the real work was deleting the old code. Her team strangled the monolith from the outside: the new service took the invoice path first, the old program kept the rest, and a thin proxy moved the traffic. When a manager asked whether they could finish in three months, she answered that they could, and that the result would be two monoliths instead of one.

**[25]** Kamran's first pipeline was smaller and better. He explained that his problem was not the tools but the habit: the team had deployed from one laptop, and nobody had written down the steps. He introduced a trunk, a lock file, a linter, and a build that produced one signed image. His colleague asked if the change would slow them down. He replied that the change would slow them for a week and speed them up for a year, and he added that the first blue-green release had proved it.

**[26]** In the same month, both of them met a failure that a process could have prevented. Nasrin's team released a new payment service at four in the afternoon on a Friday. The circuit breaker worked exactly as it was designed to work, which only made the incident shorter, not shorter enough. The postmortem found that a timeout had been increased by hand in a hotfix and that nobody had recorded it. The rule that came out of the review was simple: a manual change to a live system is a change like any other, and it must leave a line in the log.

**[27]** Kamran's failure was smaller and stranger. A developer had copied a secret into a test file, and the pipeline had published that file inside the container image. Nobody noticed until a scanner flagged the digest. The fix took one line of code; the important part was the promise that the team made to itself: a secret never travels in a plain file, a redacted log is cheaper than a broken reputation, and a break-glass access is a decision with a name on it.

**[28]** Their conversations changed too, and the grammar of a team is mostly reported speech. In the stand-up, the lead said that the release had been frozen, and she told the team to check the waiver before they touched the pipeline. A developer asked whether the new image had already been pushed to the registry, and someone answered that it had not. Kamran said that his tests had passed on Tuesday, and the reviewer said that the same tests had failed on Wednesday. Nobody argued: the pipeline repeated both runs, and the log settled the question in thirty seconds.

**[29]** Two lessons from that month are worth writing down. The first is that a system is measured by its worst day, not its best one: MTTR, saturation, and the error budget describe a real service better than a graph of happy traffic. The second is that automation is not about speed but about memory. A team that has a manifest, a lock file, and a postmortem template can lose a member and keep its habits; a team that keeps the knowledge in a chat window loses it with the first holiday.

**[30]** Scale is the last piece, and it is often confused with size. Horizontal scaling adds copies of a service, and it is the normal answer in the cloud; vertical scaling gives one machine more power, and it ends at the largest machine that money can buy. An autoscaler watches a signal and adds or removes replicas, and a noisy neighbour on the same host is the reason that a replica needs its own limits. The rule that Nasrin repeats to every new engineer is that a service should be able to disappear at any moment, because one of them will.

**[31]** So what should a student take from this chapter? Start with a monolith, because a small team that understands its own code will beat a large team that draws boxes. Then add one boundary at a time, with a container, a manifest, and a test that runs on every change. Write the playbook before the incident, and rehearse the worst case with a game day. Keep the rollback boring: a release that cannot be reversed is not a release but a gamble.

**[32]** Two habits separate a professional from an enthusiast. The first is naming: a service named after a business meaning, not after a technology, will still make sense in two years. The second is honesty about cost and failure. A team that describes its error budget to the managers, and its carbon-aware schedule to the same managers, is treated differently from a team that promises everything and explains nothing.

**[33]** Nasrin ends her onboarding talk with the same three sentences, and they are all reported speech. She says that the system will fail, and she tells the newcomer to assume it. She asks whether the new engineer has ever restored a backup, and she waits for the real answer. Then she says that the only difference between a good team and a bad one is how quickly the truth travels from the log to the person who can act on it.

*(۲۹۶۸ واژه — ۳۳ پاراگراف)*

---

### 4. Persian Translation / ترجمه فارسی

**الف) واژه‌های دشوار و معادل آن‌ها**

| واژه / عبارت | معادل پیشنهادی | نکتهٔ ترجمه |
|---|---|---|
| microservices | ریزخدمت‌ها | معادل فرهنگستانی «ریزخدمت» است و شکل انگلیسی «میکروسرویس» در صنعت رایج؛ در یک متن یکی را انتخاب کنید و ثابت بمانید. |
| monolith / monolithic | یکپارچه | «یکتاپیکره» ترجمهٔ تحت‌اللفظی و نامأنوس است؛ در متن فنی «یکپارچهٔ بزرگ» یا «تک‌واحدی» هم به کار می‌رود. |
| bounded context | زمینهٔ محدود | «کانتکست محدود» رایج است، اما «زمینهٔ محدود» فارسی‌تر است؛ منظور مرز یک معنای کسب‌وکار است. |
| coupling vs cohesion | وابستگی در برابر پیوستگی | این دو را قاطی نکنید: *coupling* بین دو سرویس و *cohesion* درون یک سرویس است. |
| container | کانتینر | «ظرف» در فارسی این معنا را نمی‌رساند؛ همان «کانتینر» در صنعت جاافتاده است. |
| pod | پاد | در ابزارهای ارکستراسیون یک مفهوم نهادی است؛ معادل فارسی رایجی ندارد و «پاد» نوشته می‌شود. |
| manifest | مانیفست (فایل توصیف منابع) | ترجمهٔ «بیانیه» گمراه‌کننده است؛ در این حوزه فایلی است که وضعیت مطلوب را توصیف می‌کند. |
| idempotent | بی‌اثر در تکرار (idempotent) | در ریاضی «توانی» ترجمه می‌شود، ولی در مهندسی نرم‌افزار یعنی اجرای دوباره نتیجه را عوض نمی‌کند. |
| toil | کار تکراری فرساینده | «زحمت» بار معنایی اشتباه دارد؛ منظور کاری دستی، تکراری و بی‌ارزش‌افزوده است. |
| error budget | بودجهٔ خطا | «بودجهٔ اشتباه» غلط است؛ منظور مقدار شکستی است که هدف سطح سرویس اجازه می‌دهد. |
| blameless postmortem | گزارش بدون سرزنش | «بدون مقصر» معنا را عوض می‌کند؛ گزارش مقصر دارد (سامانه) ولی هیچ‌کس سرزنش نمی‌شود. |
| chargeback vs showback | بازپس‌گیری هزینه در برابر نمایش هزینه | تفاوت در پول است: در *chargeback* هزینه واقعاً به تیم منتقل می‌شود و در *showback* فقط نشان داده می‌شود. |
| sbom | سیاههٔ نرم‌افزار (SBOM) | سرواژه را دست‌نخورده نگه دارید و در نخستین کاربرد معادل فارسی را در پرانتز بیاورید. |
| CVE | شناسهٔ آسیب‌پذیری (CVE) | «آسیب‌پذیری روز صفر» با *CVE* یکی نیست؛ اولی وضعیت است و دومی شناسهٔ ثبت‌شده. |
| digest | چک‌سام تصویر | با «خلاصهٔ متن» اشتباه نشود؛ اینجا رشته‌ای است که تصویر را یکتا می‌کند. |
| trust boundary | مرز اعتماد | «مرز اطمینان» روان‌تر است در متن‌های مدیریتی، اما در متن امنیتی «مرز اعتماد» جاافتاده است. |
| data residency vs sovereignty | اقامت داده در برابر حاکمیت داده | اقامت می‌گوید داده در کدام کشور ذخیره شود و حاکمیت می‌گوید قانون همان کشور بر آن حاکم است. |
| golden path | مسیر طلایی | «راه طلایی» هم درست است؛ منظور تنها مسیر توصیه‌شده و آزموده برای ساخت و استقرار است. |
| break-glass | دسترسی اضطراری | «شیشهٔ شکستنی» ترجمهٔ تحت‌اللفظی و نادرست است؛ منظور حساب کاربری ویژهٔ وضعیت اضطراری است. |

**ب) نکات ترجمه**

۱. **نقل قول غیرمستقیم در فارسی «که» می‌خواهد:** *She said that the release had been frozen* ← «او گفت که انتشار متوقف شده است». آوردن «گفت که متوقف شد» زمان را جابه‌جا می‌کند و رابطهٔ زمانی جملهٔ انگلیسی را از بین می‌برد.
۲. **فعل‌های گفتن را یکنواخت ترجمه نکنید:** *say* ← «گفت»، *tell* ← «به … گفت»، *ask* ← «پرسید»، *reply* ← «پاسخ داد»، *tell somebody to do something* ← «به … گفت که انجام دهد».
۳. **قیدهای زمان را با فارسی روزمره نیامیزید:** *that day* ← «آن روز»، *the next day* ← «روز بعد»، *the day before* ← «روز قبل»؛ آوردن «فردا» برای *the next day* جمله را متناقض می‌کند.
۴. **ترتیب جملهٔ پرسشی را بازگردانید:** *He asked where the manifest was* ← «او پرسید که مانیفست کجاست»؛ در فارسی «کجاست مانیفست» فقط لحن پرسشی دارد و برای نقل قول مناسب نیست.
۵. **مجهول انگلیسی را به «شده است» برگردانید:** *the image had been published* ← «تصویر منتشر شده بود»، نه «تصویر بود منتشر شده».
۶. **اصطلاح‌های چندواژه‌ای را نشکنید:** *graceful degradation*، *error budget* و *release freeze* در فارسی ترکیب جاافتاده دارند؛ ترجمهٔ واژه‌به‌واژهٔ آن‌ها معنا را مبهم می‌کند.
۷. **فعل‌های فنی را با فعل دقیق بیاورید:** *to deploy* ← «به‌کارگیری/استقرار دادن»، *to roll out* ← «به‌تدریج عرضه کردن»، *to restore* ← «بازگرداندن از نسخهٔ پشتیبان».
۸. **از این ترجمه‌های تحت‌اللفظی بپرهیزید:** *blast radius* ← «شعاع اثر» (نه «شعاع انفجار»)، *kill switch* ← «کلید قطع اضطراری» (نه «کلید کشتن»)، *dry run* ← «اجرای آزمایشی» (نه «اجرای خشک»).

---

### 5. Comprehension Check / درک مطلب

**الف) چهارگزینه‌ای — ده سؤال**

1. What is a monolith?
   a) one program that contains the whole system
   b) many small services, each with its own database
   c) a container image built by the pipeline

2. What is the job of a bounded context?
   a) to limit the size of a container image
   b) to mark where one business meaning ends and another begins
   c) to keep one team's namespace separate from another's

3. Why is a container image immutable?
   a) because it is stored in a private registry
   b) because the network policy forbids changes
   c) because you build a new image instead of repairing the old one

4. What does a readiness probe ask?
   a) whether the service is ready to receive traffic
   b) whether the process is still alive
   c) whether the pod should be restarted

5. Why must a retry use exponential backoff?
   a) because a longer wait costs less money
   b) because the circuit breaker needs a delay
   c) because many clients that retry at once can finish the service

6. What is the difference between blue-green and a dark launch?
   a) blue-green is only for databases; a dark launch is only for services
   b) blue-green moves traffic between two full environments, and a dark launch sends traffic to a version that does not answer yet
   c) a dark launch is used only for internal tools

7. What does an SBOM list?
   a) every component that is inside an artifact
   b) every incident that happened last year
   c) every team that uses the platform

8. Why is a blameless postmortem better for the team?
   a) because it hides the name of the engineer
   b) because it ends the incident sooner
   c) because people report the real reason when nobody is blamed

9. What is the error budget?
   a) the money that is kept for cloud costs
   b) the amount of failure that the SLO still allows
   c) the number of incidents a team may open in a year

10. What did the postmortem of Nasrin's incident find?
   a) a timeout had been changed by hand in a hotfix, and nobody had recorded it
   b) the circuit breaker had been switched off two weeks earlier
   c) a transitive dependency had been removed from the lock file

**ب) صحیح یا غلط — ده سؤال**

1. A monolithic design is easy to run and hard to change. (..........)
2. A sidecar is a helper container that runs beside the main one. (..........)
3. A manifest is normally a list of imperative commands. (..........)
4. A bulkhead keeps one failing part from damaging the whole system. (..........)
5. In the publish-subscribe pattern, every reader receives every event. (..........)
6. Continuous delivery means that the result is always ready to be released. (..........)
7. A release freeze never allows an emergency change. (..........)
8. An idempotent script gives the same state when it is run a second time. (..........)
9. An SLO is the amount of failure that a team is allowed to have. (..........)
10. Data residency decides which region may store a record. (..........)

**پ) پاسخ کوتاه — شش سؤال**

1. Why did Nasrin's company decide to break the monolith into smaller services?
2. What is the difference between liveness and readiness, in the words of paragraph [7]?
3. Why does the text call the dead letter queue "the place where a message waits for a human"?
4. What does shift left mean in practice, according to paragraph [10]?
5. Why is a game day useful, and how is it connected with chaos engineering?
6. Why does the platform team offer its golden path as self-service?

**ت) ایدهٔ اصلی — دو سؤال**

۱. ایدهٔ اصلی کل متن کدام جمله است؟

a) Small services, an automated pipeline, honest measurement, and a blameless review are one system of habits that lets a team change software quickly and safely.
b) A container image is immutable, and it is identified by a digest.
c) Kamran's first pipeline was smaller and better than Nasrin's migration.

۲. پاراگراف [22] بیشتر دربارهٔ چه چیزی است؟

a) How a carbon-aware scheduler chooses the hour of a job.
b) How separation of duties, break-glass access, data residency, and sovereignty limit who may do what.
c) How a release train keeps the schedule of a team.

**ث) تطبیق — دو جدول**

**جدول ۱:** هر واژه (۱ تا ۵) را به معنی درست آن (الف تا ه) وصل کنید.

| # | Word | | Meaning |
|---|---|---|---|
| 1 | saturation | الف | a shared identifier that follows one request |
| 2 | correlation id | ب | how full a resource is before it fails |
| 3 | triage | پ | boring manual work that a machine should do |
| 4 | toil | ت | a planned, small, reversible failure test |
| 5 | chaos experiment | ث | deciding what is urgent and what can wait |

**جدول ۲:** هر واژه (۱ تا ۵) را به معنی درست آن (الف تا ه) وصل کنید.

| # | Word | | Meaning |
|---|---|---|---|
| 1 | waiver | الف | written permission to break a rule for a short time |
| 2 | secret rotation | ب | to change something secretly |
| 3 | admission controller | پ | the part that refuses a resource that breaks the rules |
| 4 | redact | ت | changing the keys on a regular schedule |
| 5 | tamper | ث | to remove private details from a text |

---

### 6. Vocabulary Practice / تمرین واژگان

**الف) جای خالی — بیست سؤال**

از واژه‌های داخل کادر استفاده کنید. هر واژه یک بار.

> **واژه‌ها:** monolith · bounded context · replica · manifest · readiness · circuit breaker · bulkhead · exponential backoff · graceful degradation · dead letter · choreography · feature flag · linter · lock file · soak test · fault injection · observability · correlation id · error budget · playbook

1. One program that contains the whole system is a .......... .
2. A business meaning finds its limit at a .......... .
3. One running copy of a service is a .......... .
4. The desired state of a pod is written in a .......... .
5. A .......... probe asks whether a service may receive traffic now.
6. A .......... stops sending requests to a service that is clearly broken.
7. A .......... keeps one failing part from damaging the whole system.
8. A retry should wait twice as long each time; this is called .......... .
9. Returning a smaller answer instead of no answer is called .......... .
10. A message that cannot be processed goes to the .......... queue.
11. In a saga there is no central conductor; this style is called .......... .
12. A .......... hides unfinished work in production.
13. A .......... reports style problems and simple mistakes in the source code.
14. The exact version of every library is recorded in the .......... .
15. A .......... keeps the pressure on the system for hours to find a slow leak.
16. A .......... adds one fault on purpose to see what happens next.
17. Being able to answer new questions from the data you keep is called .......... .
18. A .......... travels with one request through many services.
19. The .......... is the amount of failure that an SLO still allows.
20. A .......... describes the order of checks for one kind of incident.

**ب) وصل کردن — ده سؤال**

هر واژه را به معنی درست آن وصل کنید.

| # | Word | | Meaning |
|---|---|---|---|
| 1 | decouple | الف | how much one part must change when another changes |
| 2 | cohesion | ب | the smallest unit that an orchestrator starts |
| 3 | coupling | پ | to remove a dependency between two parts |
| 4 | pod | ت | a helper container that runs beside the main one |
| 5 | sidecar | ث | how well the parts inside one service belong together |
| 6 | blue-green | ج | a switch that hides unfinished work in production |
| 7 | dark launch | چ | two full environments with traffic moved between them |
| 8 | feature flag | ح | sending real traffic to a version that does not answer yet |
| 9 | chargeback | خ | the rule that local law governs local data |
| 10 | sovereignty | د | sending the cloud bill to the team that spent it |

**پ) جمله‌سازی — ده سؤال**

با هر مورد یک جمله بنویسید. موضوع همهٔ جمله‌ها ساخت و بهره‌برداری یک سرویس است.

1. manifest / imperative (در یک جملهٔ مقایسه‌ای)
2. circuit breaker (با **شرطی نوع سوم**)
3. idempotency (جمله‌ای که توضیح دهد چرا تلاش دوباره امن است)
4. ingress / egress
5. error budget (جمله‌ای که پیامد تمام‌شدن آن را بگوید)
6. یک **نقل قول غیرمستقیم** با *told* بنویسید. موضوع: توقف انتشار
7. یک **پرسش غیرمستقیم** با *asked whether* بنویسید. موضوع: آمادگی نسخه‌ها
8. یک **فرمان غیرمستقیم** با *told ... to* بنویسید. موضوع: سنجاق کردن نسخه‌ها
9. دو جمله بنویسید: در یکی *should have* و در دیگری *might have* بیاید. موضوع: آزمون طولانی‌مدت
10. دو جملهٔ **نقل قول غیرمستقیم** بنویسید: یکی با *said that* و یکی با *might*. موضوع: تصمیم‌های بعدی تیم

**ت) واژه‌سازی: پیشوند و پسوند — یک تمرین**

پیشوند در **ابتدای** واژه و پسوند در **پایان** واژه می‌آید و معنای آن را تغییر می‌دهد:

| پیشوند / پسوند | معنی | نمونه |
|---|---|---|
| micro- | ریز، بسیار کوچک | service ← microservice |
| mono- | یک، یکتا | repo ← monorepo |
| post- | پس از | launch ← post-launch |
| co- | هم، مشترک | owner ← co-owner |
| -free | بدون، بی | error ← error-free |
| -wide | در سراسرِ | cluster ← cluster-wide |

با افزودن پیشوند یا پسوند درست، واژهٔ مناسب بسازید.

1. service ← .......... (ریزخدمت)
2. repo ← .......... (مخزن یکپارچه؛ چند پروژه در یک مخزن)
3. launch ← .......... (پس از عرضه)
4. owner ← .......... (هم‌مالک)
5. error ← .......... (بی‌خطا)
6. cluster ← .......... (در سراسر خوشه)

---

### 7. Grammar Focus / نکتهٔ گرامری

**موضوع: نقل قول غیرمستقیم (reported speech)**

**توضیح فارسی:**

نقل قول غیرمستقیم یعنی گفتهٔ کسی را بازگو کنیم، نه اینکه عین جملهٔ او را در گیومه بیاوریم. در این حالت سه چیز تغییر می‌کند: **فعل**، **ضمیرها** و **قیدهای زمان و مکان**.

**۱) فعل یک پله به عقب می‌رود** (backshift): حال ساده ← گذشتهٔ ساده؛ حال استمراری ← گذشتهٔ استمراری؛ گذشتهٔ ساده و حال کامل ← گذشتهٔ کامل؛ *will* ← *would*؛ *can* ← *could*؛ *may* ← *might*؛ *must* ← *had to*.

*"The build fails."* ← She said that the build failed.
*"I have rotated the secret."* ← He said that he had rotated the secret.

**۲) ضمیر و قید جابه‌جا می‌شوند:** *I → he/she*، *we → they*، *now → then*، *today → that day*، *tomorrow → the next day*، *yesterday → the day before*، *here → there*.

**۳) say یا tell؟** فعل *say* مفعول شخصی نمی‌گیرد (*She said that the release was frozen*) اما *tell* مفعول می‌خواهد (*She told the team that the release was frozen*). نوشتن ✗ *She said me that ...* خطای رایج فارسی‌زبانان است.

**۴) پرسش غیرمستقیم:** پرسش بله/خیر با *if* یا *whether* می‌آید و ترتیب فاعل و فعل به حالت خبری برمی‌گردد: *He asked whether the image had been pushed.* پرسش با کلمهٔ پرسشی، همان کلمه را نگه می‌دارد: *She asked where the manifest was.* پس ✗ *She asked where was the manifest* غلط است.

**۵) فرمان و درخواست:** با *told* یا *asked* و **to + مصدر** می‌آید: *The lead told us to check the waiver first.* شکل منفی آن *not to* است: *He asked me not to touch the pipeline.*

**نکته:** اگر گفته هنوز درست باشد، لازم نیست فعل عقب برود: *She said that the golden path is short.* در گزارش رسمی، backshift انتظار می‌رود.
**جدول ۱ — تغییر فعل (backshift):**

| جملهٔ مستقیم | جملهٔ غیرمستقیم | نمونه |
|---|---|---|
| حال ساده | گذشتهٔ ساده | "The pod is ready." ← He said that the pod was ready. |
| حال استمراری | گذشتهٔ استمراری | "We are testing." ← They said that they were testing. |
| گذشتهٔ ساده / حال کامل | گذشتهٔ کامل | "I fixed it." ← She said that she had fixed it. |
| will / can / may / must | would / could / might / had to | "We will retrain." ← They said that they would retrain. |

**جدول ۲ — ضمیر و قید زمان و مکان:**

| مستقیم | غیرمستقیم | مستقیم | غیرمستقیم |
|---|---|---|---|
| I / my | he, she / his, her | now | then |
| we / our | they / their | today | that day |
| this / these | that / those | tomorrow | the next day |
| here | there | yesterday | the day before |

**جدول ۳ — پرسش، فرمان و فعل گفتن:**

| نوع جمله | ساخت | نمونه |
|---|---|---|
| پرسش بله/خیر | asked + if / whether + جملهٔ خبری | He asked whether the replicas were healthy. |
| پرسش با کلمهٔ پرسشی | asked + کلمهٔ پرسشی + جملهٔ خبری | She asked where the manifest was. |
| فرمان مثبت | told / asked + مفعول + to + مصدر | The lead told us to check the waiver. |
| فرمان منفی | told / asked + مفعول + not to + مصدر | He asked me not to touch the pipeline. |
| say / tell | say + that ... / tell + شخص + that ... | She said that ... / She told the team that ... |

**پنج مثال از دنیای کامپیوتر:**

1. The lead said that the release had been frozen until Friday.
2. She told the team that the first three services would be slow and boring.
3. The developer asked whether the new image had already been pushed to the registry.
4. He asked me where the lock file was and who had written it.
5. The responder told us not to restart the pod before we had read the playbook.

**تمرین‌ها — چهل سؤال**

**الف) با شکل درست فعل کامل کنید (۱ تا ۱۴).**

1. The lead said that the release .......... (be) frozen until Friday.
2. She told the team that she .......... (freeze) the release before the sales week.
3. He said that the build .......... (not pass) because of a linter rule.
4. Nasrin said that the first three services .......... (be) slow and boring.
5. The developer asked whether the image .......... (have) already been pushed.
6. Kamran said that his tests .......... (pass) on Tuesday.
7. The architect said that the monolith .......... (become) too slow to change.
8. She said that they .......... (can) not finish the migration this quarter.
9. He told me that the pipeline .......... (will) produce one signed image the next day.
10. The responder said that the incident .......... (be) under control.
11. He asked me whether I .......... (have) ever restored a backup.
12. The manager said that the error budget .......... (be) already spent.
13. She told the newcomer that the system .......... (will) fail at some point.
14. The team said that they .......... (must) change the secrets on a schedule.

**ب) با نقل قول غیرمستقیم بازنویسی کنید (۱۵ تا ۲۰).**

15. *(منفی)* The manager said: "The backup has not been tested."
16. *(پرسشی)* She asked: "Are the replicas healthy?"
17. *(منفی)* He told me: "The circuit breaker did not open."
18. *(پرسشی)* He asked: "Where is the manifest?"
19. *(منفی)* She said: "We will not release this week."
20. *(پرسشی)* The auditor asked: "Who approved this waiver?"

**پ) شکل درست را انتخاب و جمله را کامل کنید (۲۱ تا ۲۶).**

21. He said that the deployment .......... (failed / had failed) at four in the afternoon.
22. She told .......... (me / to me) that the waiver was signed.
23. The engineer asked .......... (was the pod ready / whether the pod was ready).
24. They said that they .......... (must / had to) rotate the secrets every month.
25. The lead told the team .......... (to check / check) the waiver first.
26. The developer said that the image .......... (is / was) immutable, and that this would not change.

**ت) خطای هر جمله را اصلاح کنید (۲۷ تا ۳۲).**

27. He said me that the release was frozen.
28. She asked me where was the manifest.
29. The lead told that the tests had failed.
30. He said that he will fix the timeout tomorrow.
31. The engineer asked me did the retry work.
32. She told to the team to pin the versions.

**ث) تبدیل و جمله‌سازی (۳۳ تا ۳۶).**

33. این گفته را به نقل قول غیرمستقیم تبدیل کنید: *"The soak test found a memory leak," the engineer said.*
34. این پرسش را به نقل قول غیرمستقیم تبدیل کنید: *"Did the circuit breaker open?" the manager asked.*
35. این فرمان را به نقل قول غیرمستقیم تبدیل کنید: *"Pin every dependency," she said.*
36. یک جملهٔ دو بخشی بنویسید که در آن هم یک گفتهٔ غیرمستقیم (*said that*) و هم یک پرسش غیرمستقیم (*asked whether*) بیاید.

**ج) تمرین آزاد (۳۷ تا ۴۰).**

37. یک نقل قول مستقیم از یکی از هم‌گروهی‌های خودتان بنویسید و آن را به نقل قول غیرمستقیم تبدیل کنید.
38. یک پرسش مستقیم بنویسید و همان را با *whether* به شکل غیرمستقیم بازنویسی کنید.
39. یک فرمان کلاسی را با *told ... to* به نقل قول غیرمستقیم تبدیل کنید.
40. یک گزارش دو جمله‌ای از یک جلسهٔ گروهی بنویسید که در آن گفتهٔ یک نفر و تصمیم نهایی تیم با نقل قول غیرمستقیم آمده باشد.

---

### 8. Key Sentences Translation / ترجمهٔ جمله‌های کلیدی

**انگلیسی ← فارسی (۱۰ جمله)**

1. The lead said that the release had been frozen until Friday.
2. She told the team that the first three services would be slow and boring.
3. The developer asked whether the new image had already been pushed to the registry.
4. A smaller service has a smaller blast radius, but every new boundary is also a new place where a request can be lost.
5. The circuit breaker opened after ten errors, and it kept the incident short.
6. A blameless postmortem names the missing signal, not the tired engineer.
7. The dead letter queue held twenty events that no consumer could process.
8. If the team had pinned the dependency, the known CVE would not have reached production.
9. Data residency decides which region may store a record, and sovereignty decides whose law applies to it.
10. The platform team offers one golden path as self-service, because a developer who waits for a ticket will find a way around the rules.

**فارسی ← انگلیسی (۱۰ جمله)**

1. او به تیم گفت که انتشار تا جمعه متوقف شده است.
2. مهندس پرسید که آیا تصویر جدید پیش‌تر به مخزن فرستاده شده است.
3. اگر نسخهٔ آن کتابخانه را سنجاق کرده بودند، آسیب‌پذیری شناخته‌شده به محیط تولید نمی‌رسید.
4. گزارش پس از حادثهٔ بدون سرزنش، سیگنال گم‌شده را نام می‌برد، نه مهندس خسته را.
5. مقیاس‌دهی افقی راه معمول ابرها است؛ مقیاس‌دهی عمودی به بزرگ‌ترین ماشین موجود می‌رسد.
6. او از من خواست تا شیوه‌نامه را نخوانده‌ام پاد را دوباره راه‌اندازی نکنم.
7. هر درخواست با یک شناسهٔ همبستگی همراه است تا بتوان قطعه‌های لاگ را بعداً به هم چسباند.
8. اگر می‌خواهید هزینه را ببینید، نمایش هزینه کافی است؛ بازپس‌گیری هزینه رفتار تیم را عوض می‌کند.
9. مانیفست همان حالتی است که می‌خواهیم، نه فهرست فرمان‌هایی که اجرا می‌کنیم.
10. مدیر پرسید چه کسی آن معافیت موقت را تأیید کرده است.

---

### 9. Writing Task / تمرین نگارش

**موضوع: A Report on One Change in My Team — گزارش یک تغییر در تیم من**

یک تغییر واقعی را انتخاب کنید که **خودتان** در یک گروه درسی، یک کارگاه یا محل کارتان دیده‌اید: یک خط لولهٔ ساخت، یک قاعدهٔ انتشار، یک قرار تیمی، یا یک عادت بازبینی. سپس گزارش کوتاهی بنویسید:

- پیش از تغییر چه چیزی آزاردهنده بود؟ (دوباره‌کاری، انتظار، خطای دستی، فراموشی)
- **چه کسی چه گفت؟** دست‌کم سه گفته را با نقل قول غیرمستقیم بازگو کنید.
- چه کسی با تغییر مخالف بود و با چه استدلالی؟ استدلال او را غیرمستقیم بازگو کنید.
- پس از تغییر چه چیزی بهتر شد و چه چیزی هنوز حل نشده است؟
- یک جملهٔ محتاطانه بنویسید که محدودیت مشاهدهٔ خودتان را بپذیرد.

**شرایط نگارش:**

- نوشته بین **۲۰۰ تا ۳۰۰ واژه** باشد.
- دست‌کم **۵ جملهٔ نقل قول غیرمستقیم** داشته باشد (*said that* / *told ... that*).
- دست‌کم **یک پرسش غیرمستقیم** (*asked whether / where*) و **یک فرمان غیرمستقیم** (*told ... to*) در متن باشد.
- دست‌کم **۲ اصطلاح ربطی** از این فهرست به‌کار ببرید: *however*, *therefore*, *even so*, *as a result*.
- دست‌کم **۸ واژه** از جدول‌های واژگان بخش ۲ استفاده شود.

---

### 10. Mini Project / پروژهٔ کوچک

**انشا (نیمه‌تحقیقی): از یکپارچه به ریزخدمت — طرح یک مهاجرت کوچک**

یک سامانهٔ واقعی را انتخاب کنید که **خودتان** با آن کار می‌کنید (سامانهٔ یک کارگاه، یک وب‌سایت دانشگاهی، یک ابزار داخلی محل کار، یا پروژهٔ درسی خودتان) و طرح یک مهاجرت کوچک را بنویسید:

- **امروز:** سامانه چه کارهایی را یک‌جا انجام می‌دهد، چه کسی از آن استفاده می‌کند و کدام بخش آن بیشتر از همه دردسر می‌سازد؟
- **مرز پیشنهادی:** کدام مسیر را اول جدا می‌کنید و چرا؟ زمینهٔ محدود آن مسیر چیست؟
- **شکل دستی:** مسیر کار را روی کاغذ بکشید: کاربر ← دروازه ← سامانهٔ قدیمی ← سرویس جدید ← پایگاه دادهٔ آن. روی هر پیکان، پروتکل و مرز اعتماد را بنویسید.
- **جدول دستی مقایسه:** جدولی با چهار سطر بکشید و معماری فعلی را با معماری پیشنهادی در این چهار مورد مقایسه کنید: سرعت تغییر، هزینهٔ اجرا، دشواری عیب‌یابی، شعاع اثر.
- **خطرها:** یک شکست شبکه‌ای ممکن، یک مسئلهٔ داده (نسخهٔ تکراری یا هم‌پوشانی) و یک پرسش تیمی که لازم است پرسیده شود را نام ببرید.
- **گفت‌وگو:** سه نقل قول غیرمستقیم از یک جلسهٔ تیمی بنویسید (یک گفته، یک پرسش، یک فرمان) و سپس بگویید تصمیم نهایی چه بود.

**شرایط نگارش:**

- گزارش را **دست‌نویس روی کاغذ** بنویسید و در **جلسهٔ بعد** به مدرس تحویل دهید.
- دست‌کم **۲۵۰ واژه** باشد.
- دست‌کم **۵ جملهٔ نقل قول غیرمستقیم** داشته باشد، شامل **یک پرسش غیرمستقیم** و **یک فرمان غیرمستقیم**.
- دست‌کم **۲ جمله** با *could* یا *might* داشته باشد (لحن محتاطانه).
- طرح دستی و جدول دستی مقایسه در گزارش باشد.
- دست‌کم **۱۲ واژه** از جدول‌های واژگان بخش ۲ در گزارش به‌کار رفته باشد.

**واژه‌های یاری‌دهنده:** monolith · bounded context · decouple · container · manifest · replica · circuit breaker · graceful degradation · quality gate · observability · blameless · golden path

---

### 11. Did You Know? / آیا می‌دانستید؟

1. **The word "DevOps" appeared in 2009, at a small conference in Belgium, and it described a culture long before it described a job title.**
   واژهٔ «دواپس» در سال ۲۰۰۹ در همایشی کوچک در بلژیک پدید آمد و پیش از آنکه نام یک شغل شود، نام یک فرهنگ بود.

2. **Container tooling became popular in 2013, and within two years it had changed how most teams packaged software.**
   ابزارهای کانتینر در سال ۲۰۱۳ رایج شد و در کمتر از دو سال، شیوهٔ بسته‌بندی نرم‌افزار در بیشتر تیم‌ها را عوض کرد.

3. **The orchestration system that most teams use today was released as open source in 2014, and its design was borrowed from lessons learned inside a large search company.**
   سامانهٔ ارکستراسیونی که امروز بیشتر تیم‌ها به کار می‌برند در سال ۲۰۱۴ به‌صورت متن‌باز منتشر شد و طراحی آن از درس‌های یک شرکت بزرگ جست‌وجو گرفته شده بود.

4. **The idea of an error budget became widely known through a book on site reliability engineering published in 2016.**
   ایدهٔ بودجهٔ خطا از طریق کتابی دربارهٔ مهندسی قابلیت اطمینان که در سال ۲۰۱۶ منتشر شد، شناخته شد.

5. **In 2011, a large streaming company described a tool that switched off parts of its own system on purpose; the practice is now called chaos engineering.**
   در سال ۲۰۱۱ شرکتی بزرگ در حوزهٔ پخش ویدیو ابزاری را معرفی کرد که بخش‌هایی از سامانهٔ خودش را عمداً خاموش می‌کرد؛ این کار امروز «مهندسی آشوب» نامیده می‌شود.

6. **In 2021, an executive order in the United States asked software suppliers to provide a software bill of materials, and similar duties spread in the European Union afterwards.**
   در سال ۲۰۲۱ فرمانی اجرایی در آمریکا از تأمین‌کنندگان نرم‌افزار خواست سیاههٔ نرم‌افزار ارائه کنند و پس از آن وظایف مشابهی در اتحادیهٔ اروپا گسترش یافت.

7. **Industry research published in 2023 reported that the best-performing teams deploy on demand and recover from a failure in less than an hour.**
   پژوهشی صنعتی که در ۲۰۲۳ منتشر شد گزارش کرد تیم‌های با عملکرد برتر به‌صورت درخواستی انتشار می‌دهند و در کمتر از یک ساعت از یک شکست بازیابی می‌کنند.

8. **The habit of the blameless postmortem was borrowed from aviation, where the investigation of an accident starts from the system rather than from the pilot.**
   عادت گزارش بدون سرزنش از صنعت هوانوردی گرفته شده است؛ جایی که بررسی یک سانحه از سامانه آغاز می‌شود، نه از خلبان.
