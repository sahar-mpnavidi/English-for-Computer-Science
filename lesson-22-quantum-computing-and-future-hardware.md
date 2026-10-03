# Lesson 22: Quantum Computing and Future Hardware

## Level: B2–C1
## Time: 90–120 minutes

> **درس ۲۲ — رایانش کوانتومی و سخت‌افزار آینده**
> **نکتهٔ گرامری:** وارونگی (inversion) · قید منفی در آغاز جمله و جابه‌جایی فعل کمکی · وارونگی شرطی و وارونگی مکانی
> **متن درس:** ۲۹۰۹ واژه (۳۳ پاراگراف) | **واژگان کلیدی:** ۱۲۴ واژه | **باند سطح:** B2–C1 (پیشرفته)

---

### 1. Lesson Objectives / اهداف درس

- تفاوت بیت کلاسیک و کیوبیت را توضیح دهید و نقش برهم‌نهی، دامنه و فاز را بیان کنید.
- مراحل تصحیح خطا در سامانه‌های کوانتومی را شرح دهید و نسبت کیوبیت منطقی به فیزیکی را تحلیل کنید.
- خانواده‌های سخت‌افزار کوانتومی و شرایط محیطی آن‌ها را با واژگان دقیق نام ببرید.
- گلوگاه‌های سخت‌افزار امروز (تراشه، بسته‌بندی، پهنای باند حافظه و توان حرارتی) را بیان کنید.
- پیامدهای رمزنگاری پساکوانتومی را برای یک سازمان توضیح دهید و دو اقدام عملی پیشنهاد کنید.
- وارونگی را در نوشتار فنی به‌کار ببرید و جملهٔ وارونه را به شکل عادی بازنویسی کنید.

---

### 2. Key Vocabulary / واژگان کلیدی

> تلفظ‌ها بر پایهٔ انگلیسی آمریکایی و در قالب IPA نوشته شده‌اند.

**جدول ۱ — کیوبیت و مفاهیم بنیادی (Qubits and Fundamental Concepts)**

| فارسی | تلفظ | Definition (EN) | Example (EN) | English |
|---|---|---|---|---|
| کوانتومی | /ˈkwɑːntəm/<br>کوانتُم | About the physics of very small systems. | Quantum behaviour appears at a tiny scale. | quantum |
| کیوبیت | /ˈkjuːbɪt/<br>کیوبیت | The unit of quantum information. | One qubit holds two amplitudes at once. | qubit |
| بیت کلاسیک | /ˈklæsɪkl bɪt/<br>کلَسیکَل بیت | The ordinary bit that holds zero or one. | A classical bit is either on or off. | classical bit |
| رقم دودویی | /ˈbaɪnəri ˈdɪdʒɪt/<br>بایْنِری دیجیت | One digit in base two. | Every byte is eight binary digits. | binary digit |
| منطق بولی | /ˈbuːliən ˈlɑːdʒɪk/<br>بولِیَن لاجیک | Logic that works with true and false. | Boolean logic is the base of every gate. | boolean logic |
| گیت منطقی | /ˈlɑːdʒɪk ɡeɪt/<br>لاجیک گِیت | A small circuit that performs one logical step. | One logic gate switches a small voltage. | logic gate |
| برهم‌نهی | /ˌsuːpərpəˈzɪʃn/<br>سوپِرپُزیشِن | Holding several states at the same time. | A superposition disappears when it is measured. | superposition |
| درهم‌تنیدگی | /ɪnˈtæŋɡlmənt/<br>این‌تَنگِلمِنت | A shared state between two particles. | Entanglement cannot be described locally. | entanglement |
| واهمدوسی | /ˌdiːkoʊˈhɪrəns/<br>دیکوهیرِنس | The loss of quantum information to the environment. | Decoherence ends the computation quietly. | decoherence |
| بی‌واهمدوسی | /ˌdiːkoʊˈhɪrəns friː/<br>دیکوهیرِنس فری | Naturally protected against decoherence. | A decoherence free subspace needs no active repair. | decoherence free |
| دامنه | /ˈæmplɪtuːd/<br>اَمپلیتیود | The size of one part of a quantum state. | The amplitude decides the probability. | amplitude |
| فاز | /feɪz/<br>فِیز | The angle that makes interference possible. | A phase shift changed the final answer. | phase |
| گیت کوانتومی | /ˈkwɑːntəm ɡeɪt/<br>کوانتُم گِیت | One operation on one or two qubits. | A quantum gate must be reversible. | quantum gate |
| یکانی | /ˈjuːnəteri/<br>یونِتِری | Preserving the total probability of all answers. | Every operation of a circuit is unitary. | unitary |
| اندازه‌گیری | /ˈmeʒərmənt/<br>مِژِرمِنت | Reading the state and ending the superposition. | The measurement returned zero nine times in ten. | measurement |
| فروپاشی | /kəˈlæps/<br>کُلاپْس | The sudden end of a superposition. | The collapse gives one ordinary answer. | collapse |
| تابع موج | /ˈweɪv ˈfʌŋkʃn/<br>وِیو فانکشِن | The mathematical description of a quantum state. | The wave function holds one number per answer. | wave function |
| اسپین | /spɪn/<br>اسپین | A quantum property that behaves like a small magnet. | The spin of one electron can hold a qubit. | spin |
| کیوبیت اسپینی | /spɪn ˈkjuːbɪt/<br>اسپین کیوبیت | A qubit stored in the spin of a particle. | A spin qubit can be built in silicon. | spin qubit |
| شبیه‌ساز | /ˈsɪmjəleɪtər/<br>سیمیولِیتِر | Software that runs a circuit on a classical computer. | The simulator agreed with the theory. | simulator |
| همسان‌ساز | /ˈemjəleɪtər/<br>اِمْیولِیتِر | A copy of a device, including its noise. | The emulator reproduced the real error rate. | emulator |
| نوفهٔ آماری | /ʃɑːt nɔɪz/<br>شات نویْز | The scatter that comes from a finite number of measurements. | Shot noise falls when the run is repeated. | shot noise |
| رانش کالیبراسیون | /ˌkæləˈbreɪʃn drɪft/<br>کَلیبرِیشِن دریفت | The slow movement of settings during a day. | Calibration drift was larger than the effect. | calibration drift |
| حجم کوانتومی | /ˈkwɑːntəm ˈvɑːljuːm/<br>کوانتُم وَلْیوم | One number that combines size and quality. | Quantum volume refused to grow with the qubit count. | quantum volume |
| دقت گیت | /ɡeɪt fɪˈdeləti/<br>گِیت فیدِلِتی | How close an operation is to the ideal one. | Gate fidelity was reported as 99.9 percent. | gate fidelity |
| شمار کیوبیت | /ˈkjuːbɪt kaʊnt/<br>کیوبیت کاؤنٹ | How many qubits a machine contains. | The qubit count doubled in two years. | qubit count |
| کاهش خطا | /ˈerər ˌmɪtɪˈɡeɪʃn/<br>اِرِر میتِگِیشِن | Techniques that improve an answer without protection. | Error mitigation made the result readable. | error mitigation |
| قضیهٔ همانندسازی | /noʊ ˈkloʊnɪŋ ˈθɪərəm/<br>نو کلونینگ ثیِرِم | A rule that forbids copying an unknown quantum state. | The no cloning theorem protects key distribution. | no cloning theorem |
| برتری کوانتومی | /ˈkwɑːntəm ədˈvæntɪdʒ/<br>کوانتُم اَدوَنتیج | Doing a task faster than a classical machine. | Quantum advantage was claimed for one narrow task. | quantum advantage |
| چیرگی کوانتومی | /ˈkwɑːntəm suːˈpreməsi/<br>کوانتُم سوپرِمِسی | The strongest claim of quantum speed-up. | Quantum supremacy is a contested phrase. | quantum supremacy |
| آمادهٔ کوانتوم | /ˈkwɑːntəm ˈredi/<br>کوانتُم رِدی | Prepared for the day when quantum machines matter. | A quantum ready service has already replaced one algorithm. | quantum ready |

**جدول ۲ — سخت‌افزار کوانتومی و تصحیح خطا (Quantum Hardware and Error Correction)**

| فارسی | تلفظ | Definition (EN) | Example (EN) | English |
|---|---|---|---|---|
| سرماشناسی | /ˌkraɪoʊˈdʒenɪk/<br>کرایوجِنیک | Working at extremely low temperatures. | The cryogenic part of the lab has its own budget. | cryogenic |
| سردافزار | /ˈkraɪoʊstæt/<br>کرایوستَت | The container that keeps the sample cold. | The cryostat was opened once a week. | cryostat |
| یخچال رقیق‌ساز | /daɪˈluːʃn rɪˈfrɪdʒəreɪtər/<br>دای‌لوشِن ریفریجِرِیتِر | A fridge that reaches a few millikelvin. | The dilution refrigerator needs a team of two to open. | dilution refrigerator |
| میلی‌کلوین | /ˈmɪlikelvɪn/<br>میلی‌کِلوین | A thousandth of a degree above absolute zero. | The chip runs at twenty millikelvin. | millikelvin |
| ابررسانا | /ˌsuːpərkənˈdʌktɪŋ/<br>سوپِرکاندَکتینگ | Conducting with no resistance at low temperature. | A superconducting qubit is fast and cold. | superconducting |
| یون به‌دام‌افتاده | /træpt ˈaɪɑːn/<br>ترَپْت آی‌اُن | An ion held in place by electric fields. | A trapped ion stays accurate for a long time. | trapped ion |
| فوتونی | /foʊˈtɑːnɪk/<br>فُتونیک | Using light as the carrier of information. | A photonic qubit is easy to send and hard to store. | photonic |
| توپولوژیک | /ˌtɑːpəˈlɑːdʒɪk/<br>توپُلاجیک | Protected by its shape rather than by control. | A topological qubit aims at a lower error rate. | topological |
| اتم خنثی | /ˈnuːtrəl ˈætəm/<br>نوترَل اَتَم | An atom without a net charge, held by lasers. | Neutral atom arrays can be arranged in a grid. | neutral atom |
| بازپخت‌ساز | /əˈniːlər/<br>اَنیلِر | A machine that solves problems by cooling a physical system. | The annealer is a special-purpose machine. | annealer |
| محفظهٔ خلأ | /ˈvækjuːm ˈtʃeɪmbər/<br>وَکیوم چِیمبِر | A space with almost no air inside. | The vacuum chamber must not be opened in a hurry. | vacuum chamber |
| حفاظ تشعشعی | /ˌreɪdiˈeɪʃn ˈʃiːldɪŋ/<br>رِیدیِیشِن شیلدینگ | A barrier against outside radiation. | Radiation shielding protects the coherence time. | radiation shielding |
| چرخهٔ گرمایی | /ˈθɜːrml ˈsaɪklɪŋ/<br>ثرِمال سایکلینگ | Repeated warming and cooling. | Thermal cycling slowly breaks the joints. | thermal cycling |
| خلوص مواد | /məˈtɪriəlz ˈpjʊrəti/<br>مَتِریَلز پیورِتی | How clean the material really is. | Materials purity decides the experiment. | materials purity |
| ناخالصی جزئی | /treɪs ɪmˈpjʊrəti/<br>ترِیس ایمپیورِتی | A very small amount of an unwanted element. | One trace impurity ruined the whole wafer. | trace impurity |
| تصحیح خطا | /ˈerər kəˈrekʃn/<br>اِرِر کُرِکشِن | Protecting information against errors. | Error correction needs more hardware than the calculation. | error correction |
| کیوبیت منطقی | /ˈlɑːdʒɪkl ˈkjuːbɪt/<br>لاجیکَل کیوبیت | A protected qubit built from many physical ones. | One logical qubit may need a thousand physical qubits. | logical qubit |
| کیوبیت فیزیکی | /ˈfɪzɪkl ˈkjuːbɪt/<br>فیزی‌کَل کیوبیت | One real qubit inside the machine. | The physical qubit is the unit that is counted in a datasheet. | physical qubit |
| تحمل‌پذیری خطا | /fɔːlt ˌtɑːlərəˈbɪləti/<br>فُلت تالِرَبِلیتی | Working correctly even when parts fail. | Fault tolerance is the goal of the whole field. | fault tolerance |
| رمز سطح | /ˈsɜːrfɪs koʊd/<br>سِرفِس کُد | A standard layout for error correction. | The surface code is drawn on a two-dimensional grid. | surface code |
| نشانگان | /ˈsɪndroʊm/<br>سیندروم | The result of a check that reveals an error. | The syndrome says where an error happened, not what was stored. | syndrome |
| نرخ خطای منطقی | /ˈlɑːdʒɪkl ˈerər reɪt/<br>لاجیکَل اِرِر رِیت | The error rate of a protected qubit. | The logical error rate fell by half. | logical error rate |
| سرباز | /ˈoʊvərhed/<br>اووِرهِد | The extra work that protection costs. | The overhead is the price of a reliable qubit. | overhead |
| زمان همدوسی | /koʊˈhɪrəns taɪm/<br>کوهیرِنس تایم | How long a state survives before it is lost. | A longer coherence time allows more operations. | coherence time |
| وفاداری | /fɪˈdeləti/<br>فیدِلِتی | How closely the result matches the ideal. | The fidelity of the operation was measured twice. | fidelity |
| توزیع کلید کوانتومی | /ˈkwɑːntəm kiː dɪstrɪˈbjuːʃn/<br>کوانتُم کی دیستریبوشِن | Sharing a key with quantum guarantees. | Quantum key distribution warns when it is observed. | quantum key distribution |
| توزیع کلید | /kiː dɪstrɪˈbjuːʃn/<br>کی دیستریبوشِن | The problem of giving two parties the same key. | Key distribution is the oldest problem in cryptography. | key distribution |
| تجزیه به عوامل | /ˈfæktərɪŋ/<br>فَکتِرینگ | Writing a number as a product of smaller ones. | Factoring is easy to check and hard to do. | factoring |
| تحلیل رمز | /krɪpˈtænələsɪs/<br>کریپ‌تَنَلِسیس | Attacking an encryption system. | Cryptanalysis with a large machine is the real worry. | cryptanalysis |
| رمزنگاری | /krɪpˈtɑːɡrəfi/<br>کریپتوگرَفی | The science of protecting messages. | Cryptography has to change before the machine exists. | cryptography |
| پساکوانتومی | /ˌpoʊst ˈkwɑːntəm/<br>پوست کوانتُم | Designed to resist a quantum attack. | Post quantum standards are already published. | post quantum |

**جدول ۳ — تراشه، ساخت و بسته‌بندی (Chip, Fabrication, and Packaging)**

| فارسی | تلفظ | Definition (EN) | Example (EN) | English |
|---|---|---|---|---|
| سیلیسیم | /ˈsɪlɪkən/<br>سیلیکُن | The element that almost every chip is made of. | Silicon is cheap and extremely well understood. | silicon |
| نیمه‌رسانا | /ˌsemikənˈdʌktər/<br>سِمی‌کانداکتِر | A material that can conduct or block. | A semiconductor is useful because it can be controlled. | semiconductor |
| ترانزیستور | /trænˈzɪstər/<br>ترَنزیستِر | The switch that every processor is built from. | One modern chip holds billions of transistors. | transistor |
| گرهٔ فرایند | /ˈprɑːses noʊd/<br>پراسِس نود | One generation of manufacturing technology. | Each process node promised more speed. | process node |
| نانومتر | /ˈnænoʊmiːtər/<br>نانومیتِر | A billionth of a metre. | The gate is now a few nanometres wide. | nanometer |
| آنگستروم | /ˈæŋstrəm/<br>آنگسترُم | A tenth of a nanometre. | The next steps are measured in angstroms. | angstrom |
| لیتوگرافی | /lɪˈθɑːɡrəfi/<br>لیتوگرَفی | Drawing the pattern of a chip with light. | Lithography is the most expensive tool in the plant. | lithography |
| فوتولیتوگرافی | /ˌfoʊtoʊlɪˈθɑːɡrəfi/<br>فوتولیتوگرَفی | Lithography that uses light on a sensitive layer. | Photolithography prepares the surface before etching. | photolithography |
| حکاکی | /ˈetʃɪŋ/<br>اِچینگ | Removing material with a chemical or a plasma. | Etching removes what the pattern does not protect. | etching |
| لایه‌گذاری | /ˌdepəˈzɪʃn/<br>دِپُزیشِن | Adding a thin layer of material. | Deposition builds the layers that carry the current. | deposition |
| کاشت یون | /ˈaɪɑːn ˌɪmplænˈteɪʃn/<br>آی‌اُن ایمپلَنتِیشِن | Shooting ions into a surface. | Ion implantation places the dopants precisely. | ion implantation |
| آلایش | /ˈdoʊpɪŋ/<br>دوپینگ | Adding impurities to change how silicon behaves. | Doping turns silicon into a useful conductor. | doping |
| ویفر | /ˈweɪfər/<br>وِیفِر | The round slice of silicon that chips are made on. | One wafer holds hundreds of chips. | wafer |
| بازده ویفر | /ˈweɪfər jiːld/<br>وِیفِر ییلد | The share of chips on a wafer that work. | Wafer yield decides the profit of the product. | wafer yield |
| افت بازده | /jiːld lɔːs/<br>ییلد لاس | The share that is thrown away. | A yield loss of five percent is a serious problem. | yield loss |
| ساخت | /ˌfæbrɪˈkeɪʃn/<br>فَبریکِیشِن | The whole process of making a chip. | Fabrication takes three months from wafer to package. | fabrication |
| کارخانهٔ تراشه | /ˈfaʊndri/<br>فاوندری | A plant that makes chips for other companies. | The foundry offers three different processes. | foundry |
| اتاق تمیز | /kliːn ruːm/<br>کلین روم | A room with almost no dust in the air. | A clean room is cleaner than an operating theatre. | clean room |
| کنترل آلودگی | /kənˌtæməˈneɪʃn kənˈtroʊl/<br>کُنتَمِنِیشِن کانترول | Keeping dust and chemicals out. | Contamination control is a full-time discipline. | contamination control |
| طول گیت | /ɡeɪt leŋθ/<br>گِیت لِنگث | The size of the part that switches the transistor. | A shorter gate length means a faster switch. | gate length |
| مقیاس‌دهی ترانزیستور | /trænˈzɪstər ˈskeɪlɪŋ/<br>ترَنزیستِر اسکِیلینگ | Making the switch smaller each generation. | Transistor scaling has slowed at the smallest sizes. | transistor scaling |
| کوچک‌سازی گره | /noʊd ʃrɪŋk/<br>نود شرینک | Moving to a smaller manufacturing process. | Node shrink alone no longer doubles performance. | node shrink |
| قانون مور | /mʊrz lɔː/<br>مورز لا | The observation that transistor counts doubled regularly. | Moore's law was a forecast that became a plan. | Moore's law |
| پس از مور | /poʊst mʊr/<br>پوست مور | The period in which that rhythm no longer holds. | Post Moore computing looks for gains in packaging. | post Moore |
| ریزتراشه | /ˈtʃɪplət/<br>چیپ‌لِت | One small die that is combined with others. | A chiplet can use the best process for its job. | chiplet |
| بسته‌بندی پیشرفته | /ədˈvænst ˈpækɪdʒɪŋ/<br>اَدوَنست پَکِجینگ | Joining several dies into one package. | Advanced packaging is where the competition moved. | advanced packaging |
| یکپارچه‌سازی ناهمگون | /ˌhetərəˈdʒiːniəs ˌɪntɪˈɡreɪʃn/<br>هِتِرُجینیِس اینتِگرِیشِن | Putting different kinds of parts on one package. | Heterogeneous integration mixes logic and memory. | heterogeneous integration |
| روی‌هم‌چینی قالب | /daɪ ˈstækɪŋ/<br>دای استَکینگ | Putting one die on top of another. | Die stacking shortens the wires between two layers. | die stacking |
| اتصال هیبریدی | /ˈhaɪbrɪd ˈbɑːndɪŋ/<br>هایبرید بان‌دینگ | Joining two surfaces without solder bumps. | Hybrid bonding allows a very dense connection. | hybrid bonding |
| واسط | /ɪnˈtɜːrpɑːzər/<br>این‌تِرپازِر | A layer that carries wires between dies. | The interposer carries thousands of connections. | interposer |
| زیرلایهٔ شیشه‌ای | /ɡlæs ˈsʌbstreɪt/<br>گلَس سابس‌ترِیت | A glass base that is flatter than plastic. | A glass substrate keeps the package flat. | glass substrate |

**جدول ۴ — سخت‌افزار آینده و چشم‌انداز (Future Hardware and Outlook)**

| فارسی | تلفظ | Definition (EN) | Example (EN) | English |
|---|---|---|---|---|
| سامانه روی تراشه | /ˈsɪstəm ɑːn tʃɪp/<br>سیستِم آن چیپ | A whole product on one die. | A system on chip saves power and space. | system on chip |
| آرایهٔ گیت قابل برنامه‌ریزی | /fiːld prəˈɡræməbl ɡeɪt əˈreɪ/<br>فیلد پروگرَمَبُل گِیت اَرِی | A chip that can be rewired after it is made. | A field programmable gate array is used for prototypes. | field programmable gate array |
| مدار مجتمع اختصاصی | /ˌæplɪˈkeɪʃn spəˈsɪfɪk ˌɪntɪɡreɪtɪd ˈsɜːrkɪt/<br>اَپلیکِیشِن سپِسیفیک اینتِگرِیتِد سِرکِت | A chip designed for exactly one task. | An application specific integrated circuit is fast and inflexible. | application specific integrated circuit |
| مجموعه‌دستور | /ɪnˈstrʌkʃn set/<br>این‌اس‌تراکشِن سِت | The list of operations that a processor understands. | A narrow instruction set can be made very efficient. | instruction set |
| هستهٔ تانسوری | /ˈtensər kɔːr/<br>تِنسِر کور | A unit built for matrix arithmetic. | The tensor core does one calculation extremely well. | tensor core |
| آرایهٔ سیستولیک | /sɪˈstɑːlɪk əˈreɪ/<br>سیستالیک اَرِی | A grid of units that passes data step by step. | A systolic array never sends intermediate results to memory. | systolic array |
| روی‌هم‌چینی سه‌بعدی | /θriː dɪˈmenʃənl ˈstækɪŋ/<br>تری دیمِنشِنَل استَکینگ | Building a chip in several layers. | Three dimensional stacking made the package shorter. | three dimensional stacking |
| میان‌سیلیسیمی | /θruː ˈsɪlɪkən ˈvaɪə/<br>ثرو سیلیکُن وای‌اِی | A vertical wire that passes through silicon. | A through silicon via connects two stacked layers. | through silicon via |
| دیوار حافظه | /ˈmeməri wɔːl/<br>مِمُری وال | The gap between fast processors and slow memory. | The memory wall is now the main limit. | memory wall |
| رایانش نزدیک حافظه | /nɪr ˈmeməri kəmˈpjuːtɪŋ/<br>نیِر مِمُری کُمپیوتینگ | Doing small calculations beside the storage. | Near memory computing saves a long trip. | near memory computing |
| ممریستور | /ˈmemrɪstər/<br>مِمریستِر | A device that remembers a resistance after power is removed. | A memristor behaves like a synapse. | memristor |
| اسپین‌ترونیک | /spɪnˈtrɑːnɪks/<br>اسپین‌ترونیکس | Computing with the magnetic state of a material. | Spintronics promises storage that never forgets. | spintronics |
| نورومورفیک | /ˌnʊroʊˈmɔːrfɪk/<br>نورومورفیک | Hardware that imitates the style of a brain. | Neuromorphic chips work with events, not with clocks. | neuromorphic |
| فوتونیک سیلیسیمی | /ˈsɪlɪkən fəˈtɑːnɪks/<br>سیلیکُن فُتونیکس | Sending data as light inside a chip. | Silicon photonics moves data with less energy. | silicon photonics |
| اپتیک هم‌بسته | /koʊ ˌpækɪdʒd ˈɑːptɪks/<br>کو پَکِجْد اُپتیکس | Placing the laser beside the processor. | Co packaged optics shortens the optical path. | co packaged optics |
| بهره‌وری انرژی | /ˈenərdʒi ɪˈfɪʃnsi/<br>اِنِرجی اِفیشِنسِی | Useful work for each unit of electricity. | Energy efficiency decides the size of a data centre. | energy efficiency |
| کارایی به ازای هر وات | /pərˈfɔːrməns pər wɑːt/<br>پِرفورمَنس پِر وات | Performance divided by the power used. | The new design doubled performance per watt. | performance per watt |
| توان طراحی حرارتی | /ˈθɜːrml dɪˈzaɪn ˈpaʊər/<br>ثرِمال دیزاین پاوِر | The maximum heat that a package may produce. | Thermal design power is a ceiling, not a target. | thermal design power |
| گرمای هدررفته | /weɪst hiːt/<br>وِیست هیت | Heat that a system throws away. | Waste heat can warm a building instead. | waste heat |
| بازاستفاده از گرما | /hiːt riːˈjuːs/<br>هیت ری‌یوس | Using that heat for something useful. | Heat reuse turns a cost into a service. | heat reuse |
| رایانش برگشت‌پذیر | /rɪˈvɜːrsəbl kəmˈpjuːtɪŋ/<br>ریوِرسَبُل کُمپیوتینگ | Computing in a way that can be undone. | Reversible computing avoids the cost of erasing a bit. | reversible computing |
| معماری دامنه‌محور | /doʊˈmeɪn spəˈsɪfɪk ˈɑːrkɪtektʃər/<br>دومِین سپِسیفیک آرکیتِکچِر | A design built for one kind of workload. | A domain specific architecture trades flexibility for efficiency. | domain specific architecture |
| رایانش شتاب‌یافته | /əkˈseləreɪtɪd kəmˈpjuːtɪŋ/<br>اَکسِلِرِیتِد کُمپیوتینگ | Using special hardware beside a general processor. | Accelerated computing grew faster than general-purpose computing. | accelerated computing |
| اگزاسکیل | /ˈeksə skeɪl/<br>اِکسَسکِیل | A machine that passes a billion billion operations per second. | The exascale line was crossed in 2022. | exascale |
| مجموعهٔ محک | /ˈbentʃmɑːrk swiːt/<br>بِنچمارک سویْت | A group of programs that measure real performance. | The benchmark suite is still being written. | benchmark suite |
| چابکی رمزنگاری | /ˈkrɪptoʊ əˈdʒɪləti/<br>کریپتو اَجیلِتی | Being ready to replace one algorithm with another. | Crypto agility is cheaper than a migration. | crypto agility |
| برداشت امروز، رمزگشایی فردا | /ˈhɑːrvɪst naʊ diːˈkrɪpt ˈleɪtər/<br>هارویست ناو دیکریپت لِیتِر | Storing encrypted data for a future machine to open. | Harvest now decrypt later is why the change is urgent. | harvest now decrypt later |
| نقشهٔ راه | /ˈroʊdmæp/<br>رودمَپ | A plan with dates and milestones. | The roadmap lists logical rather than physical qubits. | roadmap |
| چرخهٔ هیاهو | /haɪp ˈsaɪkl/<br>هایپ سایکُل | The pattern of hope and disappointment around a technology. | Every technology passes through a hype cycle. | hype cycle |
| شبیه‌سازی کوانتومی | /ˈkwɑːntəm ˌsɪmjəˈleɪʃn/<br>کوانتُم سیمیولِیشِن | Using a quantum machine to study another quantum system. | Quantum simulation was the first motivation of the field. | quantum simulation |
| علم مواد | /məˈtɪriəlz ˈsaɪəns/<br>مَتِریَلز سایِنس | The study of how materials behave. | Materials science is the first real customer. | materials science |

---

### 3. Reading / متن اصلی

**عنوان متن: Machines That Must Stay Cold and Quiet (ماشین‌هایی که باید سرد و بی‌صدا بمانند)**

**[1]** Rarely has a technology been praised so loudly on the strength of so few working examples. Quantum computing is real research, and it is also a field where a single published number can move a budget. Shirin is a physics student who spends her weeks beside a machine that must stay colder than space, and Dariush is a chip engineer who spends his weeks fighting heat of a much more ordinary kind. Their two systems have nothing in common except one property that shapes every decision around them: they are fragile.

**[2]** A classical bit holds one of two values, and a binary digit is the smallest unit of information that an ordinary computer works with. Every processor above it is a clever arrangement of boolean logic, built from millions of logic gates that switch a small voltage on and off. This design is robust: a bit that is flipped by a cosmic ray is simply copied again, and nobody notices. The same property explains why an ordinary computer can be dropped on a table and still boot in the morning.

**[3]** A qubit does not work that way. While it is not measured, it holds a superposition of both values at once, and its state is described by a wave function with two numbers for each possible answer. Those numbers are an amplitude and a phase, and the phase is what allows interference between the possible paths through a computation. Interference is the engine of every quantum algorithm: the wrong answers cancel, and the right answer adds up.

**[4]** A second qubit makes possible entanglement, in which two particles share one state and can no longer be described separately. The cost of this power is that any measurement destroys the superposition: the wave function collapses into one ordinary answer, and the experiment is over. Some hardware stores the qubit in the spin of an electron, and a spin qubit built in silicon is one of the most promising designs precisely because it borrows a manufacturing line that already exists.

**[5]** Computation itself is done with a quantum gate, which is a small operation that must be unitary, meaning that it preserves the total probability of all answers. The quality of that operation is its gate fidelity, and it is measured in parts per thousand rather than in perfect units. Two standard summaries of a machine are its qubit count and its quantum volume, which is a single number that combines size and quality, because a machine with many unreliable qubits is worth less than a smaller reliable one.

**[6]** The enemy has a name. Decoherence is the loss of quantum information to the surrounding world, and every design decision is a fight against it: a shorter coherence time means fewer operations before the state is gone. Some designs aim at a decoherence free subspace, which is a corner of the state space that is naturally protected. In practice the laboratory also fights smaller enemies: shot noise, which is the statistical scatter of a finite number of measurements, and calibration drift, which is the slow movement of every parameter away from the value it had when the team arrived in the morning. The team keeps a written log of that drift, because a curve that moves is not yet a result.

**[7]** Error correction is the answer, and it is expensive. A logical qubit is a protected unit that is built from many physical qubits, and the surface code is the standard layout for doing it. The trick is a syndrome measurement, which is a check that looks at the neighbours of a qubit without looking at the qubit itself, and the logical error rate falls as the code grows. The overhead is the price: a useful logical qubit may need a thousand physical ones, and the number decides whether a machine is small or merely expensive. Fault tolerance is the point at which adding more hardware makes the result better rather than worse, and error mitigation is a cheaper, weaker alternative that improves an answer without protecting it.

**[8]** There is a threshold hidden in that arithmetic. Below it, more qubits help; above it, more qubits only add more ways to fail. No wonder, then, that laboratories publish fidelity curves rather than promises: what a reader wants to know is whether the curve is on the right side of the line.

**[9]** The hardware families are different answers to the same question. A superconducting qubit is fast and must be cooled to millikelvin temperatures. A trapped ion is slower and more accurate, and it can be held in a vacuum for a long time. A photonic qubit carries information in light, which is convenient for communication and awkward for storage. A topological qubit is designed so that small errors cannot disturb the state at all, and a neutral atom can be arranged into large regular arrays with lasers. A spin qubit borrows the silicon transistor, and an annealer solves a different kind of problem by cooling a physical system towards a low-energy state.

**[10]** Not only is the processor itself exotic, but the building around it is also a machine: a cryogenic system with a cryostat and a dilution refrigerator, held at a few millikelvin, inside a vacuum chamber, behind radiation shielding, and designed so that the thermal cycling of a warm-up does not break a joint. So sensitive is the equipment that a passing lorry can be seen in the data, and materials purity is a full-time job, because a trace impurity in a sample can ruin a week of measurements.

**[11]** Nobody outside a laboratory reaches this hardware directly. A team writes a circuit, an automatic pipeline compiles it, and the machine is used through cloud access. A simulator can run the same circuit on a classical computer while the design is being tested, and an emulator reproduces the behaviour of a real device, including its noise, so that a student can practise without waiting for a two-day slot on the fridge. That queue is measured in weeks, and a badly designed job can consume a whole slot for nothing.

**[12]** Cryptography is where the field touches ordinary life. Factoring a large number is easy to check and very hard to do, which is the foundation of most public-key systems, and cryptanalysis with a large quantum computer is the reason for the panic. Post quantum algorithms, and especially lattice based schemes, are being standardised now, because a modern threat is to harvest now and decrypt later: an encrypted message of today can be stored and opened when the machine exists. Key distribution has a quantum version too, and quantum key distribution is attractive because the no cloning theorem forbids making a perfect copy of an unknown state; a weaker implementation can still leak through a side channel, so crypto agility, which means being able to replace an algorithm quickly, is the practical answer.

**[13]** The applications that are most often named are simulations rather than calculations. A quantum simulation of a molecule is the original motivation of the whole field, because nature is quantum and a quantum machine speaks its language. Materials science and chemistry are the natural customers, followed by an optimization problem such as a routing or a portfolio problem, and by the variational methods that try to use today's imperfect hardware for those tasks.

**[14]** Around the research sits a market. Every technology passes through a hype cycle, and quantum computing is far enough along to have produced its own winter of disappointed expectations. Investment continues, but a serious roadmap now mentions the number of logical qubits and the error rate rather than the number of physical ones. The words quantum advantage and quantum supremacy are both used for the moment when a quantum machine beats a classical machine at a task, and both of them are contested. Little does a headline know about the difference: a hundred-qubit chip is impressive in a press release and useless in a calculation, and the honest benchmark suite for the field is still being written. A service that calls itself quantum ready has usually replaced one algorithm, and that is a start.

**[15]** Dariush works at the other end of the same science. His chips are not exotic; they are made in enormous numbers, and the problem is that they are becoming difficult to feed. Feeding a chip means giving it data and power, and both of those deliveries have become harder than the arithmetic itself.

**[16]** The foundation is silicon, a semiconductor that can be made to conduct or to block, and the transistor is the switch that made everything else possible. For fifty years the industry followed a rhythm: a process node got smaller every two years, the gate length shortened, and the number of transistors doubled. That rhythm was named Moore's law, and transistor scaling is now at the point where a node is measured in nanometers and the next steps are counted in angstroms. Node shrink still continues, but post Moore computing means that the gains now come from packaging and design as much as from the switch itself.

**[17]** Every chip begins as a wafer. Lithography draws the pattern with light, photolithography prepares the surface, and etching removes what is not wanted, while deposition adds the thin layers that carry the current. Ion implantation and doping place the impurities that give silicon its useful properties, and all of it happens inside a fabrication plant, or foundry, in a clean room where contamination control is the main religion. The economics are brutal: wafer yield decides the profit, and a yield loss of a few percent can turn a good product into a bad one.

**[18]** Since a single large chip is expensive to build and hard to yield, the industry moved to the chiplet: several small dies placed close together and joined by advanced packaging. Heterogeneous integration lets a designer choose the best process for each part, die stacking and hybrid bonding shorten the connections, and an interposer or a glass substrate carries thousands of wires between neighbours. Two techniques are worth naming: three dimensional stacking, and the through silicon via that connects one layer of silicon to the next. The reward is real, and the difficulty is real too, because a package with six dies has six chances to fail.

**[19]** The oldest wall in computing is still standing. The memory wall describes the growing gap between a processor that can add numbers quickly and a memory that cannot deliver them quickly enough, and the answer is to move work towards the data: near memory computing puts a small calculation next to the storage, and every designer talks about the latency budget of a request rather than the peak speed of a core.

**[20]** Three new devices are trying to change the rules rather than the numbers. A memristor keeps a resistance after the power is removed, which makes it a candidate for storage that behaves like a synapse. Spintronics uses the magnetic state of a material instead of a charge, and neuromorphic hardware imitates the sparse, event-driven style of a brain. Reversible computing goes further and asks whether a computation can be undone, because erasing a bit has a thermodynamic cost. None of these devices is faster than silicon at everything; each one is faster at one small thing.

**[21]** Light is the other candidate. Silicon photonics sends data as light inside a chip, co packaged optics puts the laser next to the processor, and optical computing tries to do part of the arithmetic with interference rather than with transistors. Nothing here is new; what is new is that the manufacturing has finally become good enough to be boring.

**[22]** Energy is the constraint that decides the design. Every generation is judged by its energy efficiency, and by performance per watt rather than by the highest clock rate, because thermal design power is a hard ceiling in a building with a fixed electricity supply. Waste heat is now an asset: heat reuse sends it into a district heating network, and the older air cooling of a data centre is being replaced by liquid cooling and, in some designs, immersion cooling. A machine that cannot be cooled cannot be sold, however clever its design is.

**[23]** The architecture of an ordinary device has changed just as much. A system on chip puts the whole product on one die, and a designer may choose between a field programmable gate array, which can be reprogrammed, and an application specific integrated circuit, which cannot but is far more efficient. Inside, a tensor core or a systolic array does one operation extremely well: a stream of multiply-and-add steps that never leaves the chip, and the instruction set of the machine has been reduced to serve that stream. This is what domain specific architecture means, and it is the reason accelerated computing has grown faster than general-purpose computing. A machine that crosses the exascale line reports its speed in exaflops, and the distance between a laboratory record and a useful workload has never been larger.

**[24]** Reliability is the last unglamorous subject. A new part is pushed through reliability testing and a burn-in period, because electromigration slowly moves metal inside a wire and every device has a wear out point. Endurance is the number of writes that a memory can survive, and a user who learns that number only after a failure has learned it too late. The lesson is not that devices fail, but that the failure arrives long after the report that promised it would not.

**[25]** Shirin's first experiment failed for a reason that had nothing to do with physics. So carefully had the team calibrated the machine on Sunday that they decided not to repeat the calibration on Monday, and the calibration drift of that single day moved a phase by a small amount. Had the phase been checked, the two runs would have agreed. Not until the data were plotted on the same axis did the pattern appear, and only then did anybody think of the temperature in the corridor outside the laboratory.

**[26]** What she learned is written in the paper she now gives to new students. No measurement is a fact on its own; it is a fact with a time, a temperature, and a calibration attached to it. Hardly had the team finished the correction when a second drift appeared, and this time nobody was surprised.

**[27]** Dariush's project began with a request that sounded simple: double the memory bandwidth of an accelerator without increasing the power. Not only was the existing package already at its thermal limit, but the wires between the dies were also the bottleneck. His first proposal was a larger interposer, and his second was a different arrangement of chiplets. Neither of them was accepted on paper, because both of them had to be tested in a package that costs more than a car.

**[28]** The test failed in a way that everyone recognised. Under a synthetic load, one corner of the package became hotter than the rest, and the clock slowed down to protect itself. So uneven was the heat that the measured performance was lower than the specification of the slower part it was meant to replace. No sooner had the team seen the thermal map than they understood the real problem: the layout was optimised for wire length and not for heat.

**[29]** What the two of them share is a style of thinking, and it is not really about technology. Both fields are dominated by noise, by calibration, and by the difference between a demonstration and a product. Not once did either of them say that the hardware was the easy part, and both of them measure before they argue.

**[30]** A list of the usual mistakes fits on one page. The first is comparing a physical qubit with a logical one, which is like comparing a brick with a house. The second is quoting a peak number from a datasheet as if it were the performance of a real program. The third is forgetting the cost of data movement, which is now larger than the cost of the arithmetic in many workloads. The fourth is treating a laboratory record as a product roadmap.

**[31]** A student who wants to work here should learn three things in this order. Learn the classical foundation first, because a quantum algorithm is a modification of a classical one and a chip is still a chip. Then learn to measure, because a number without its conditions is not evidence. Then learn to read a paper critically, because the sentence that matters is rarely the one in the title.

**[32]** What should be measured is also worth writing down, and the two lists are almost the same. For a quantum machine: gate fidelity, coherence time, the logical error rate, and the number of logical qubits that a benchmark actually used. For a classical one: performance per watt, energy per operation, memory bandwidth, and the thermal envelope in which the number was obtained. Seldom is a specification complete without the condition under which it was measured.

**[33]** Neither field will be finished soon, and that is the last honest sentence of this chapter. Only after the noise has been measured and the packaging has been designed does a machine become a product, and by then the next generation has already been announced. Rarely does a technology arrive in the shape that its first description promised; what arrives is a smaller, more specific improvement that somebody can actually use.

*(۲۹۰۹ واژه — ۳۳ پاراگراف)*

---

### 4. Persian Translation / ترجمه فارسی

**الف) واژه‌های دشوار و معادل آن‌ها**

| واژه / عبارت | معادل پیشنهادی | نکتهٔ ترجمه |
|---|---|---|
| qubit | کیوبیت | «بیت کوانتومی» هم درست است؛ در یک متن یکی را انتخاب کنید و در نخستین کاربرد شکل دیگر را در پرانتز بیاورید. |
| superposition | برهم‌نهی | «فوق‌موقعیت» ترجمهٔ ماشینی و نادرست است؛ این واژه در فیزیک معادل جاافتاده دارد. |
| entanglement | درهم‌تنیدگی | «درهم‌پیچیدگی» هم دیده می‌شود؛ شکل رایج در متن‌های فارسی «درهم‌تنیدگی» است. |
| decoherence | واهمدوسی | «از‌هم‌دوسی» و «بی‌همدوسی» هم به کار می‌رود؛ یک شکل را ثابت نگه دارید. |
| amplitude / phase | دامنه / فاز | «دامنه» اندازه و «فاز» زاویه است؛ ترجمهٔ «فاز» به «مرحله» خطای رایجی است. |
| unitary | یکانی | در ریاضیات «یکانی» معادل جاافتاده است؛ «واحدی» یا «تک‌واحدی» را به کار نبرید. |
| collapse | فروپاشی | «فروپاشی تابع موج» اصطلاح استاندارد است؛ «سقوط» معنا را نمی‌رساند. |
| spin qubit | کیوبیت اسپینی | «اسپین» را ترجمه نکنید؛ «چرخش» در این معنا نادرست است. |
| simulator / emulator | شبیه‌ساز / همسان‌ساز | تفاوت را در پرانتز توضیح دهید: شبیه‌ساز مدل نظری را اجرا می‌کند و همسان‌ساز رفتار واقعی دستگاه را بازمی‌سازد. |
| cryogenic / cryostat | سرماشناسی / سردافزار | «کرایوژنیک» در صنعت رایج است؛ «سردافزار» برای *cryostat* گویاست و با «یخچال» اشتباه نمی‌شود. |
| dilution refrigerator | یخچال رقیق‌ساز | «رقیق‌سازی» بخشی از سازوکار سرمایش است؛ حذف آن، نام دستگاه را بی‌معنا می‌کند. |
| millikelvin | میلی‌کلوین | عدد را به فارسی بنویسید و در پرانتز معادل انگلیسی را نگه دارید؛ «k» لاتین را داخل متن فارسی نگذارید. |
| trapped ion | یون به‌دام‌افتاده | «یون محبوس» هم درست است؛ «تله‌یونی» در متن دانشگاهی ثقیل است. |
| topological | توپولوژیک | «توپولوژیکی» رایج است؛ منظور این است که پایداری از ساختار هندسی می‌آید، نه از کنترل دقیق. |
| fault tolerance | تحمل‌پذیری خطا | «خطاپذیری» و «تحمل خطا» هم درست‌اند؛ در متن فنی به‌جای «مقاوم به خرابی» از این ترکیب استفاده کنید. |
| surface code | رمز سطح | «کد سطح» هم رایج است؛ *code* در اینجا رمز تصحیح خطا است، نه رمز عبور. |
| syndrome | نشانگان | «سندروم» بار پزشکی دارد؛ در تصحیح خطا «نشانگان» یا «الگوی نشانه» را بنویسید. |
| overhead | سرباز | «سربار» هم رایج است؛ در متن دانشگاهی «سرباز» دقیق‌تر است و با «هزینهٔ اضافی» توضیح داده می‌شود. |
| yield | بازده | «بازده ویفر» یعنی سهم چیپ‌های سالم روی هر ویفر؛ «تولید» معنا را عوض می‌کند. |
| chiplet | ریزتراشه | «چیپلت» در صنعت رایج است؛ باید روشن شود که یک قالب کوچک است، نه یک تراشهٔ کامل. |
| interposer | واسط | «لایهٔ واسط» گویاتر است؛ این قطعه فقط یک بستر نیست، هزاران سیم را حمل می‌کند. |
| memory wall | دیوار حافظه | «دیوارهٔ حافظه» تحت‌اللفظی و نادرست است؛ منظور شکاف میان سرعت پردازنده و تحویل داده است. |
| performance per watt | کارایی به ازای هر وات | نسبت را با «کارایی هر وات» کوتاه کنید؛ «توان بر وات» ترجمهٔ معکوس است. |
| thermal design power | توان طراحی حرارتی | سرواژهٔ TDP را در نخستین کاربرد در پرانتز بیاورید؛ این عدد سقف است، نه هدف. |
| exascale | اگزاسکیل | «مقیاس اگزا» گویاست؛ *flops* را در پرانتز نگه دارید، چون یکا است. |
| roadmap | نقشهٔ راه | «نقشهٔ راه» تصویب‌شده است؛ «نقشهٔ جاده» ترجمهٔ تحت‌اللفظی و نامناسب برای متن فنی است. |

**ب) نکات ترجمه**

۱. **وارونگی را در فارسی بازسازی نکنید، بلکه تأکید را منتقل کنید:** *Never has a laboratory tool been so sensitive* ← «هیچ‌گاه ابزار آزمایشگاهی این‌قدر حساس نبوده است». جابه‌جا کردن فعل در فارسی لازم نیست؛ جای قید در آغاز جمله تأکید را می‌رساند.
۲. **وارونگی شرطی را با «اگر» برگردانید:** *Had the phase been checked, the two runs would have agreed* ← «اگر فاز بررسی شده بود، دو اجرا هم‌خوان می‌شدند». معادل انگلیسی را با *if* هم می‌توان نوشت.
۳. **قیدهای منفی را با کلیدواژه‌های دقیق فارسی بیاورید:** *rarely* ← «به‌ندرت»، *seldom* ← «کمتر پیش می‌آید»، *scarcely* ← «به‌سختی»، *no sooner ... than* ← «به‌محض ... که».
۴. **واژه‌های فنی را با معادل دقیق بیاورید:** *to decohere* ← «واهمدوس شدن»، *to calibrate* ← «کالیبره کردن»، *to anneal* ← «بازپخت کردن»، *to fabricate* ← «ساختن در فرایند تولید».
۵. **واحدها را به فارسی بنویسید و یکا را دست‌نخورده بگذارید:** «۲۰ میلی‌کلوین» و «۲ نانومتر» درست است؛ «۲۰ mK» داخل متن فارسی نگذارید.
۶. **از ترجمهٔ فارسی‌نما بپرهیزید:** *spin qubit* ← «کیوبیت اسپینی» (نه «کیوبیت چرخشی»)، *dilution refrigerator* ← «یخچال رقیق‌ساز» (نه «یخچال رقت»).
۷. **سرواژه‌ها را یکدست نگه دارید:** TDP، FPGA، ASIC و QKD را ترجمه نکنید؛ در نخستین کاربرد معادل فارسی را در پرانتز بیاورید.
۸. **ترتیب صفت و اسم را رعایت کنید:** *a cryogenic dilution refrigerator* ← «یخچال رقیق‌ساز سرماشناسی»؛ آوردن هر صفت به‌صورت جداگانه عبارت را نامفهوم می‌کند.

---

### 5. Comprehension Check / درک مطلب

**الف) چهارگزینه‌ای — ده سؤال**

1. What does a qubit hold before it is measured?
   a) one of two values, exactly like a classical bit
   b) a superposition of both values at once
   c) the result of the previous measurement

2. What destroys a superposition?
   a) any measurement of the qubit
   b) a long coherence time
   c) a unitary operation

3. Why is error correction expensive?
   a) because it needs a classical computer beside the machine
   b) because it doubles the clock speed of the processor
   c) because one logical qubit may need a thousand physical qubits

4. What is the threshold in that arithmetic?
   a) the point below which adding more qubits helps
   b) the temperature of the dilution refrigerator
   c) the highest gate fidelity that a device can reach

5. Why must this hardware be cooled to millikelvin temperatures?
   a) because the software is written for low temperatures
   b) because a superconducting qubit only works when it is cold
   c) because the lasers would otherwise be too hot

6. What is the purpose of an emulator?
   a) to cool the processor between two runs
   b) to replace the quantum machine in production
   c) to reproduce the behaviour of a real device, including its noise

7. Why is "harvest now and decrypt later" a threat?
   a) because encrypted data can be copied in a single second
   b) because a message stored today can be opened when the machine exists
   c) because quantum key distribution is not yet standardised

8. What is the memory wall?
   a) the growing gap between fast processors and slow memory delivery
   b) the limit on how many chips fit on one wafer
   c) the highest number of transistors that can be printed

9. Why did Dariush's test fail?
   a) because the interposer was too expensive
   b) because the clock speed was too high for the process node
   c) because one corner of the package became hotter than the rest

10. What is performance per watt used for?
   a) to measure the physical size of a chip
   b) to compare the price of two processors
   c) to judge a design when electricity and cooling are limited

**ب) صحیح یا غلط — ده سؤال**

1. A phase is what allows interference between the possible paths. (..........)
2. Gate fidelity is normally reported in perfect units. (..........)
3. Quantum volume combines size and quality in one number. (..........)
4. A longer coherence time allows more operations before the state is lost. (..........)
5. A syndrome measurement reads the stored value of the qubit. (..........)
6. Fault tolerance means that adding more hardware makes the result better. (..........)
7. Quantum key distribution is protected by the no cloning theorem. (..........)
8. Moore's law was an observation that became a plan for the industry. (..........)
9. A chiplet is one large die that replaces several small ones. (..........)
10. In the text, the heat in the package was uneven, and the clock slowed down. (..........)

**پ) پاسخ کوتاه — شش سؤال**

1. Why does the text describe a classical bit as "robust"?
2. What is the difference between a physical qubit and a logical qubit?
3. Why is error mitigation described as "a cheaper, weaker alternative"?
4. Why does the text say that the laboratory building is itself a machine?
5. What is the difference between a simulator and an emulator, in the words of paragraph [11]?
6. Why is post-quantum work urgent even though a large quantum computer does not exist yet?

**ت) ایدهٔ اصلی — دو سؤال**

۱. ایدهٔ اصلی متن کدام جمله است؟

a) Two very different kinds of hardware — quantum processors and ordinary chips — are both limited by noise, heat, and measurement, so a professional measures before arguing.
b) A surface code is drawn on a two-dimensional grid and protects one logical qubit.
c) Dariush doubled the memory bandwidth of an accelerator in his second proposal.

۲. پاراگراف [18] بیشتر دربارهٔ چه چیزی است؟

a) How lithography draws the pattern of a chip with light.
b) How the chiplet, advanced packaging, and the interposer answer the cost of one large die.
c) How the memory wall moves work towards the data.

**ث) تطبیق — دو جدول**

**جدول ۱:** هر واژه (۱ تا ۵) را به معنی درست آن (الف تا ه) وصل کنید.

| # | Word | | Meaning |
|---|---|---|---|
| 1 | superposition | الف | a device that remembers a resistance after power is removed |
| 2 | memristor | ب | holding several states at the same time |
| 3 | syndrome | پ | the result of a check that reveals an error |
| 4 | interposer | ت | a layer that carries wires between dies |
| 5 | heat reuse | ث | using waste heat for something useful |

**جدول ۲:** هر واژه (۱ تا ۵) را به معنی درست آن (الف تا ه) وصل کنید.

| # | Word | | Meaning |
|---|---|---|---|
| 1 | cryostat | الف | the share of chips on a wafer that work |
| 2 | chiplet | ب | the container that keeps the sample cold |
| 3 | angstrom | پ | hardware that imitates the style of a brain |
| 4 | wafer yield | ت | one small die that is combined with others |
| 5 | neuromorphic | ث | a tenth of a nanometre |

---

### 6. Vocabulary Practice / تمرین واژگان

**الف) جای خالی — بیست سؤال**

از واژه‌های داخل کادر استفاده کنید. هر واژه یک بار.

> **واژه‌ها:** superposition · entanglement · decoherence · amplitude · quantum gate · unitary · measurement · collapse · coherence time · gate fidelity · logical qubit · physical qubit · syndrome · overhead · surface code · cryostat · millikelvin · wafer · chiplet · interposer

1. Holding several states at the same time is called .......... .
2. A shared state between two particles is .......... .
3. The loss of quantum information to the surrounding world is .......... .
4. The size of one part of a quantum state is its .......... .
5. One operation on one or two qubits is a .......... .
6. An operation that preserves the total probability is .......... .
7. Reading the state and ending the superposition is a .......... .
8. The sudden end of a superposition is called .......... .
9. How long a state survives before it is lost is the .......... .
10. How close an operation comes to the ideal one is its .......... .
11. A protected qubit that is built from many real qubits is a .......... .
12. One real qubit inside the machine is a .......... .
13. The result of a check that reveals an error is the .......... .
14. The extra work that protection costs is the .......... .
15. A standard layout for error correction is the .......... .
16. The container that keeps the sample cold is the .......... .
17. A thousandth of a degree above absolute zero is a .......... .
18. The round slice of silicon that chips are made on is a .......... .
19. One small die that is combined with others is a .......... .
20. A layer that carries wires between dies is an .......... .

**ب) وصل کردن — ده سؤال**

هر واژه را به معنی درست آن وصل کنید.

| # | Word | | Meaning |
|---|---|---|---|
| 1 | semiconductor | الف | drawing the pattern of a chip with light |
| 2 | transistor | ب | a material that can conduct or block |
| 3 | lithography | پ | the gap between fast processors and slow memory |
| 4 | etching | ت | the switch that every processor is built from |
| 5 | doping | ث | removing material with a chemical or a plasma |
| 6 | foundry | ج | being ready to replace one algorithm with another |
| 7 | memory wall | چ | adding impurities to change how silicon behaves |
| 8 | exascale | ح | a plant that makes chips for other companies |
| 9 | hype cycle | خ | a machine that passes a billion billion operations per second |
| 10 | crypto agility | د | the pattern of hope and disappointment around a technology |

**پ) جمله‌سازی — ده سؤال**

با هر مورد یک جمله بنویسید. موضوع همهٔ جمله‌ها سخت‌افزار است.

1. یک جمله با *Never* در آغاز و **وارونگی** بنویسید. موضوع: نرخ خطای منطقی
2. یک جمله با *Rarely* و وارونگی بنویسید. موضوع: دقت گیت
3. یک جمله با *Not only ... but also* و وارونگی بنویسید. موضوع: هزینهٔ سرمایش
4. یک جمله با *Only after ...* و وارونگی بنویسید. موضوع: کالیبراسیون
5. یک جمله با *No sooner ... than* بنویسید. موضوع: رانش کالیبراسیون
6. یک جمله با **وارونگی شرطی** (*Had ...* / *Were ...*) بنویسید. موضوع: اگر بستهٔ تراشه خنک‌تر بود
7. یک جمله با *So + صفت* و وارونگی بنویسید. موضوع: نوفهٔ آماری
8. یک جمله با *Under no circumstances* بنویسید. موضوع: خاموش کردن یخچال
9. دو جمله بنویسید: در یکی *Little did ... know* و در دیگری *Hardly had ... when* بیاید
10. دو توصیهٔ محتاطانهٔ وارونه بنویسید: یکی با *Never* و یکی با *Seldom*

**ت) واژه‌سازی: پیشوند و پسوند — یک تمرین**

پیشوند در **ابتدای** واژه و پسوند در **پایان** واژه می‌آید و معنای آن را تغییر می‌دهد:

| پیشوند / پسوند | معنی | نمونه |
|---|---|---|
| nano- | نانو، یک میلیاردم | meter ← nanometer |
| thermo- | گرما | dynamic ← thermodynamic |
| electro- | الکتریکی | migration ← electromigration |
| photo- | نور | lithography ← photolithography |
| ultra- | فراتر، بسیار | sensitive ← ultra-sensitive |
| -ic | صفت ساختن | electron ← electronic |

با افزودن پیشوند یا پسوند درست، واژهٔ مناسب بسازید.

1. meter ← .......... (نانومتر)
2. dynamic ← .......... (وابسته به گرما و کار)
3. migration ← .......... (مهاجرت الکتریکی)
4. lithography ← .......... (فوتولیتوگرافی)
5. sensitive ← .......... (بسیار حساس)
6. electron ← .......... (الکترونیکی)

---

### 7. Grammar Focus / نکتهٔ گرامری

**موضوع: وارونگی (inversion)**

**توضیح فارسی:**

در جملهٔ خبری انگلیسی، فعل کمکی پیش از فاعل نمی‌آید. **وارونگی** یعنی همین ترتیب، مانند جملهٔ پرسشی، عوض می‌شود تا جمله **تأکید** بگیرد. این ساختار در نوشتار فنی برای هشدار، محدودیت و نتیجه‌گیری زیاد به کار می‌رود.

**۱) پس از قید منفی یا محدودکننده در آغاز جمله:** *never, rarely, seldom, hardly, scarcely, little, nowhere, no sooner, not only, not until, under no circumstances*.
*Rarely has a tool been so sensitive.* / *Not only is the qubit fragile, but it is also expensive to cool.*

**۲) پس از *only* + قید:** *Only then did the team publish.* / *Only after the calibration did the numbers agree.* اما اگر *only* به **فاعل** اشاره کند، وارونگی نمی‌آید: *Only the manager approved the change.*

**۳) با *so* و *such*:** *So sensitive is the equipment that a lorry appears in the data.* / *Such was the noise that no signal survived.*

**۴) وارونگی شرطی:** به‌جای *if*، فعل کمکی به ابتدای جمله می‌آید: *Had the phase been checked, the two runs would have agreed.* (*Should you need a slot, book it early.* هم همان ساخت است.)

**۵) وارونگی مکانی:** پس از قید مکان، فعل پیش از فاعل می‌آید: *In the cryostat sat four chips.*

**دو نکتهٔ مهم:** ① در زمان حال یا گذشتهٔ ساده که فعل کمکی وجود ندارد، *do/does/did* اضافه می‌شود: *Rarely do we repeat a calibration.*؛ ② وارونگی پس از قید تأکیدی می‌آید، نه در هر جملهٔ خبری.

دو خطای رایج فارسی‌زبانان: ① جا انداختن فعل کمکی ✗ *Never I have seen such noise* ← درست: *Never have I seen such noise*؛ ② وارونگی پس از *only* که به فاعل اشاره دارد ✗ *Only the manager did approve it* ← درست: *Only the manager approved it.*

**جدول ۱ — قیدهای منفی و وارونگی:**

| قید | ساخت | نمونه |
|---|---|---|
| Never / Rarely / Seldom | قید + فعل کمکی + فاعل + فعل | Never have I seen such noise. |
| Hardly / Scarcely | Hardly had + فاعل + p.p. ... when | Hardly had we started when the alarm sounded. |
| No sooner ... than | No sooner had + فاعل + p.p. ... than | No sooner had the run finished than the drift returned. |
| Not only ... but also | Not only + کمکی + فاعل + ... | Not only is the chip hot, but it is also slow. |
| Not until / Little / Nowhere | Not until + جمله + کمکی + فاعل | Not until we plotted both runs did we see the pattern. |
| Under no circumstances | Under no circumstances + کمکی + فاعل | Under no circumstances should the fridge be switched off. |

**جدول ۲ — only، so / such و وارونگی شرطی:**

| ساخت | نمونه | نکته |
|---|---|---|
| Only then | Only then did the team publish the result. | پس از only + قید، وارونگی لازم است |
| Only after + جمله | Only after the calibration did the numbers agree. | ✗ Only after the calibration the numbers agreed. |
| Only + فاعل | Only the security officer approved the change. | وارونگی نمی‌آید |
| So + صفت | So uneven was the heat that the clock slowed down. | برای تأکید بر صفت |
| Such | Such was the noise that no signal survived. | برای تأکید بر اسم |
| وارونگی شرطی | Had the package been cooler, ... / Were the fridge warmer, ... / Should you need a slot, ... | به‌جای if، بدون تغییر معنا |

**جدول ۳ — وارونگی مکانی و خطاهای رایج:**

| مورد | نمونه |
|---|---|
| وارونگی مکانی | In the cryostat sat four chips. |
| بدون فعل کمکی | Rarely do we repeat a calibration on the same day. |
| ✗ غلط | Never I have seen such noise. → Never have I seen such noise. |
| ✗ غلط | No sooner we finished than the drift returned. → No sooner had we finished than the drift returned. |

**پنج مثال از دنیای کامپیوتر:**

1. Rarely has a technology been praised so loudly on so few examples.
2. Not only is the qubit fragile, but it is also expensive to cool.
3. No sooner had the calibration finished than the drift returned.
4. Had the package been cooler, the clock would not have slowed down.
5. So uneven was the heat that the measured performance fell below the specification.

**تمرین‌ها — چهل سؤال**

**الف) با شکل وارونهٔ درست کامل کنید (۱ تا ۱۴).**

1. Never .......... (I / see) such a clean signal before.
2. Rarely .......... (a machine / need) so much care.
3. Not only .......... (the qubit / be) fragile, but it is also expensive to cool.
4. No sooner .......... (the run / finish) than the drift returned.
5. Hardly .......... (we / start) when the temperature alarm sounded.
6. Only after the calibration .......... (the numbers / agree).
7. Only then .......... (the team / publish) the result.
8. Under no circumstances .......... (the fridge / be switched off).
9. So sensitive .......... (the equipment / be) that a lorry appears in the data.
10. .......... (the phase / check) earlier, the two runs would have agreed.
11. .......... (the package / be) cooler, the clock would not have slowed down.
12. Should you .......... (need) a slot on the machine, book it in advance.
13. Little .......... (we / know) that the drift was already in the data.
14. Nowhere in the datasheet .......... (the condition / be) mentioned.

**ب) با قید داده‌شده و وارونگی بازنویسی کنید (۱۵ تا ۲۰).**

15. *(هرگز)* The laboratory has never been so quiet.
16. *(به‌ندرت)* A machine needs so much care.
17. *(نه‌تنها)* The chip is hot, and it is also slow.
18. *(به‌محض ... که)* The run finished, and the drift returned immediately.
19. *(فقط پس از)* The calibration was done, and then the numbers agreed.
20. *(به‌هیچ‌وجه)* The fridge must not be switched off.

**پ) شکل درست را انتخاب و جمله را کامل کنید (۲۱ تا ۲۶).**

21. Rarely .......... (we repeat / do we repeat) a calibration on the same day.
22. No sooner had the run finished .......... (when / than) the drift returned.
23. Only after the plot .......... (we saw / did we see) the pattern.
24. .......... (Had / Have) the phase been checked, the two runs would have agreed.
25. Not only .......... (the chip is / is the chip) hot, but it is also slow.
26. Never .......... (I have / have I) seen a cleaner signal.

**ت) خطای هر جمله را اصلاح کنید (۲۷ تا ۳۲).**

27. Never I have seen such noise.
28. No sooner we finished than the drift returned.
29. Only after the calibration the numbers agreed.
30. So sensitive the equipment is that a lorry appears in the data.
31. Hardly we had started when the alarm sounded.
32. Only the manager did approve the change.

**ث) تبدیل و جمله‌سازی (۳۳ تا ۳۶).**

33. این جملهٔ شرطی را با وارونگی بنویسید: *If the package had been cooler, the clock would not have slowed down.*
34. این جمله را با *Only after* تأکید کنید: *The team published the result after the third run.*
35. این جمله را با *Not until* بازنویسی کنید: *We saw the pattern only when we plotted both runs.*
36. این جمله را با وارونگی مکانی بازنویسی کنید: *Four chips sat in the cryostat.*

**ج) تمرین آزاد (۳۷ تا ۴۰).**

37. یک جمله با *Never* و وارونگی دربارهٔ یک تجربهٔ آزمایشگاهی خودتان بنویسید.
38. یک جملهٔ وارونهٔ شرطی با *Had* بنویسید که یک اشتباه گذشته را فرض کند.
39. یک جمله با *So ... that* و وارونگی بنویسید. موضوع: گرمای بستهٔ تراشه
40. یک هشدار دو جمله‌ای بنویسید که در یکی *Under no circumstances* و در دیگری *Only after* آمده باشد.

---

### 8. Key Sentences Translation / ترجمهٔ جمله‌های کلیدی

**انگلیسی ← فارسی (۱۰ جمله)**

1. Rarely has a technology been praised so loudly on so few examples.
2. Not only is the qubit fragile, but it is also expensive to cool.
3. No sooner had the calibration finished than the drift returned.
4. Had the package been cooler, the clock would not have slowed down.
5. So uneven was the heat that the measured performance fell below the specification.
6. Only after the error rate had been plotted did the team believe the result.
7. Under no circumstances should the dilution refrigerator be switched off.
8. Little did the investors know that the logical qubit count was still one.
9. Not until the wafer yield was measured did the real cost of the chip appear.
10. Never before had a datasheet been read so carefully.

**فارسی ← انگلیسی (۱۰ جمله)**

1. به‌ندرت ابزار آزمایشگاهی این‌قدر حساس بوده است.
2. نه‌تنها برهم‌نهی شکننده است، بلکه اندازه‌گیری آن را از بین می‌برد.
3. به‌محض اینکه کالیبراسیون تمام شد، رانش بازگشت.
4. اگر فاز بررسی شده بود، دو اجرا هم‌خوان می‌شدند.
5. تنها پس از اندازه‌گیری بازده ویفر بود که هزینهٔ واقعی تراشه معلوم شد.
6. به‌هیچ‌وجه نباید یخچال رقیق‌ساز را خاموش کرد.
7. کمتر کسی می‌دانست که شمار کیوبیت‌های منطقی هنوز یک است.
8. تنها پس از آن بود که تیم نتیجه را منتشر کرد.
9. چنان ناموزون بود که یک گوشهٔ بسته داغ‌تر از همه‌جا شد.
10. هرگز پیش از این، نرخ خطای منطقی این‌قدر پایین نبوده است.

---

### 9. Writing Task / تمرین نگارش

**موضوع: A Measurement I Could Not Repeat — اندازه‌گیری که نتوانستم تکرار کنم**

یک اندازه‌گیری واقعی را انتخاب کنید که **خودتان** انجام داده‌اید و نتوانسته‌اید دوباره تکرارش کنید: زمان بارگذاری یک برنامه، مصرف برق یک دستگاه، نتیجهٔ یک آزمایش دانشگاهی، یا زمان پردازش یک مجموعه‌داده. سپس دربارهٔ آن بنویسید:

- چه چیزی را اندازه گرفتید و در چه شرایطی؟ (ساعت، دما، نسخهٔ نرم‌افزار، تعداد دستگاه)
- چه چیزی در آن اندازه‌گیری **ثبت نشد** و بعداً مهم شد؟
- اگر آن شرایط ثبت شده بود، چه چیزی عوض می‌شد؟
- **چه چیزی را هرگز نباید فرض گرفت** و چه چیزی را تنها پس از اندازه‌گیری می‌توان گفت؟
- یک جملهٔ محتاطانه بنویسید که محدودیت اندازه‌گیری خودتان را بپذیرد.

**شرایط نگارش:**

- نوشته بین **۲۰۰ تا ۳۰۰ واژه** باشد.
- دست‌کم **۴ جملهٔ وارونه** داشته باشد؛ در میان آن‌ها یکی با قید منفی (*Never / Rarely*)، یکی با *Only after* یا *Only then* و یکی با **وارونگی شرطی** (*Had ...*) بیاید.
- دست‌کم **۲ اصطلاح ربطی** از این فهرست به‌کار ببرید: *however*, *therefore*, *even so*, *as a result*.
- دست‌کم **۸ واژه** از جدول‌های واژگان بخش ۲ استفاده شود.

---

### 10. Mini Project / پروژهٔ کوچک

**انشا (نیمه‌تحقیقی): زنجیرهٔ توان و گرما در یک سامانهٔ واقعی**

یک سامانهٔ سخت‌افزاری را انتخاب کنید که **خودتان** با آن کار می‌کنید (لپ‌تاپ شخصی، کامپیوتر آزمایشگاه، سرور یک کارگاه، یا پردازندهٔ داخل یک دستگاه صنعتی) و گزارش کوتاهی بنویسید:

- **سامانه:** چه کاری انجام می‌دهد، چه کسی از آن استفاده می‌کند و چند ساعت در روز روشن است؟
- **شکل دستی:** زنجیرهٔ توان و گرما را روی کاغذ بکشید: برق ← منبع تغذیه ← پردازنده ← گرماگیر ← محیط. روی هر پیکان یک عدد بنویسید (وات، دما، یا سرعت باد).
- **جدول دستی مقایسه:** جدولی با چهار سطر بکشید و دو راه‌حل بهبود را مقایسه کنید (مثلاً خنک‌کنندهٔ بهتر در برابر پردازندهٔ کم‌مصرف‌تر): هزینه، اثر بر کارایی، صدا و فضا، نگه‌داری.
- **گلوگاه:** کدام محدودیت اول از همه ظاهر می‌شود — توان طراحی حرارتی، پهنای باند حافظه، یا دیوار حافظه؟ با یک عدد آن را ثابت کنید.
- **اندازه‌گیری:** یک عدد را پیش از بهبود و یک عدد را پس از آن گزارش کنید و شرایط هر اندازه‌گیری را بنویسید.
- **جمله‌های گرامری:** پنج جملهٔ وارونه بنویسید، شامل یک وارونگی شرطی و یک جمله با *No sooner ... than* یا *Only after*.

**شرایط نگارش:**

- گزارش را **دست‌نویس روی کاغذ** بنویسید و در **جلسهٔ بعد** به مدرس تحویل دهید.
- دست‌کم **۲۵۰ واژه** باشد.
- دست‌کم **۵ جملهٔ وارونه** و **۲ جمله** با *might* یا *could* (لحن محتاطانه) داشته باشد.
- طرح دستی زنجیرهٔ توان و جدول دستی مقایسه در گزارش باشد.
- دست‌کم **۱۲ واژه** از جدول‌های واژگان بخش ۲ در گزارش به‌کار رفته باشد.

**واژه‌های یاری‌دهنده:** thermal design power · energy efficiency · performance per watt · waste heat · heat reuse · memory wall · process node · chiplet · advanced packaging · benchmark suite · coherence time · gate fidelity

---

### 11. Did You Know? / آیا می‌دانستید؟

1. **The first transistor was demonstrated in late 1947, and it was about the size of a paperclip.**
   نخستین ترانزیستور در اواخر ۱۹۴۷ ساخته و نمایش داده شد و تقریباً به اندازهٔ یک گیرهٔ کاغذ بود.

2. **The first integrated circuit followed in 1958, and the first microprocessor appeared in 1971 with roughly 2,300 transistors inside it.**
   نخستین مدار مجتمع در ۱۹۵۸ ساخته شد و نخستین ریزپردازنده در ۱۹۷۱ با حدود ۲٬۳۰۰ ترانزیستور عرضه شد.

3. **In 1965, an engineer observed that the number of components on a chip was doubling about every year, and he revised the figure to two years a decade later.**
   در سال ۱۹۶۵ مهندسی مشاهده کرد که شمار اجزای یک تراشه حدوداً هر سال دو برابر می‌شود و یک دهه بعد همان عدد را به دو سال اصلاح کرد.

4. **In 1961, a physicist argued that erasing a single bit must produce a minimum amount of heat, and reversible computing still starts from that idea.**
   در سال ۱۹۶۱ فیزیکدانی استدلال کرد که پاک کردن یک بیت باید حداقلی از گرما تولید کند و رایانش برگشت‌پذیر هنوز از همان ایده آغاز می‌شود.

5. **A superconducting qubit was first demonstrated in 1999, and it required a temperature close to absolute zero.**
   نخستین کیوبیت ابررسانا در سال ۱۹۹۹ نمایش داده شد و دمایی نزدیک به صفر مطلق لازم داشت.

6. **In 2019, a research group claimed quantum advantage on a single sampling task, and within a year classical methods had narrowed that claim considerably.**
   در سال ۲۰۱۹ یک گروه پژوهشی برتری کوانتومی را در یک تک‌وظیفهٔ نمونه‌گیری ادعا کرد و کمتر از یک سال بعد روش‌های کلاسیک آن ادعا را بسیار محدود کردند.

7. **In late 2024, a research group reported that its error correction had passed the threshold, so that adding physical qubits lowered the logical error rate instead of raising it.**
   در اواخر ۲۰۲۴ یک گروه پژوهشی گزارش داد که تصحیح خطای آن از آستانه گذشته است؛ به این معنا که افزودن کیوبیت فیزیکی نرخ خطای منطقی را پایین می‌آورد، نه بالا.

8. **Industry surveys in 2023 reported that most users of quantum hardware reached it through the cloud rather than owning a machine.**
   بررسی‌های صنعتی در ۲۰۲۳ گزارش کردند که بیشتر کاربران سخت‌افزار کوانتومی از طریق فضای ابری به آن دسترسی داشتند، نه با مالکیت دستگاه.
