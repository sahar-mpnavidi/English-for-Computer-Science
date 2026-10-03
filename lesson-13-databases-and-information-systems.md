# Lesson 13: Databases and Information Systems

## Level: B1
## Time: 90–120 minutes

> **درس ۱۳ — پایگاه داده و سیستم‌های اطلاعاتی**
> **نکتهٔ گرامری:** مجهول (passive voice) · حال ساده، گذشتهٔ ساده و حال کامل مجهول · مجهول با افعال وجهی
> **متن درس:** ۱۶۸۰ واژه (۳۰ پاراگراف) | **واژگان کلیدی:** ۹۰ واژه | **باند سطح:** B1 (متوسط)

---

### 1. Lesson Objectives / اهداف درس

- اجزای یک پایگاه داده (جدول، سطر، ستون، رکورد، کلید اصلی، نمایه) را به انگلیسی توضیح دهید.
- تفاوت پایگاه دادهٔ رابطه‌ای و noSQL، انبار داده و دریاچهٔ داده را بیان کنید.
- جمله‌های مجهول در حال ساده، گذشتهٔ ساده و حال کامل بسازید و آن‌ها را به معلوم تبدیل کنید.
- با افعال وجهی مجهول (*must be validated*) قاعده و الزام بنویسید.
- دادهٔ خوب و بد را توصیف کنید (دقیق، تازه، معتبر، تکراری، کهنه) و راه بهبود آن را بگویید.

---

### 2. Key Vocabulary / واژگان کلیدی

> تلفظ‌ها بر پایهٔ انگلیسی آمریکایی و در قالب IPA نوشته شده‌اند.

**جدول ۱ — پایگاه داده و ساختار داده (Database and Data Structure)**

| فارسی | تلفظ | Definition (EN) | Example (EN) | English |
|---|---|---|---|---|
| پایگاه داده | /ˈdeɪtəbeɪs/<br>دیتابِیس | An organized collection of data that can be searched. | Almost every service is built on a database. | database |
| جدول | /ˈteɪbl/<br>تِیبُل | A set of rows and columns with the same rules. | Data is kept in tables. | table |
| سطر | /roʊ/<br>رو | One line of data in a table. | Each row is called a record. | row |
| ستون | /ˈkɑːləm/<br>کالُم | One field of every record in a table. | A column is one field of the record. | column |
| رکورد | /ˈrekərd/<br>رِکورد | One complete line of related values. | A new record is inserted. | record |
| کلید اصلی | /ˈpraɪmeri kiː/<br>پرایمِری کی | The unique value that finds one row. | Every table should have a primary key. | primary key |
| کلید خارجی | /ˈfɔːrən kiː/<br>فورِن کی | A column that points to another table. | A foreign key relates two tables. | foreign key |
| نمایه | /ˈɪndeks/<br>ایندِکس | A small structure that makes searching fast. | An index is built on the search columns. | index |
| قید محدودکننده | /kənˈstreɪnt/<br>کانسترِینت | A rule that the data must follow. | A constraint can also be added. | constraint |
| رابطهٔ داده | /rɪˈleɪʃnʃɪp/<br>ریلِیشِن‌شیپ | A link between two entities. | A relationship is drawn as a line. | relationship |
| موجودیت | /ˈentəti/<br>اِنتِتی | One kind of thing that is stored. | Every entity becomes a table. | entity |
| ویژگی | /ˈætrɪbjuːt/<br>اَتِریبوت | One property of an entity. | Every attribute becomes a column. | attribute |
| نرمال‌سازی | /ˌnɔːrmələˈzeɪʃn/<br>نورمَلایزِیشن | Removing repeated data from tables. | With normalization, a name is written once. | normalization |
| تراکنش | /trænˈzækʃn/<br>ترَنزَکشِن | A group of changes that succeed or fail together. | A transaction must all succeed or all fail. | transaction |
| تریگر، راه‌انداز | /ˈtrɪɡər/<br>تریگِر | A small program that runs by itself after a change. | A trigger runs after an update. | trigger |
| نما | /vjuː/<br>ویو | A saved query that looks like a table. | A view looks like a table. | view |
| توالی، شمارنده | /ˈsiːkwəns/<br>سیکوِنس | A counter that gives the next number. | A sequence gives the next number. | sequence |
| نوشیکو‌ال | /ˌnoʊ ˈes kjuː el/<br>نوشی‌کوال | A database that is not strictly relational. | Some systems use noSQL databases. | noSQL |
| مجموعه‌داده | /ˈdeɪtəset/<br>دیتاسِت | One collection of data for analysis. | The same dataset is read by many reports. | dataset |
| انبار داده | /ˈwerhaʊs/<br>وِرهاوس | A large database built for reporting. | A warehouse is built for reading. | warehouse |
| ناهنجاری داده | /əˈnɑːməli/<br>اَنومَلی | A value that does not follow the rule. | An anomaly is found by mapping the rows. | anomaly |
| یکپارچگی | /ɪnˈteɡrəti/<br>اینتِگریتی | The state where every rule is respected. | Integrity means that every rule is respected. | integrity |
| نگاشت | /ˈmæpɪŋ/<br>مَپینگ | Matching one value or field to another. | It is found by mapping every row to a pattern. | mapping |
| دریاچهٔ داده | /ˈdeɪtə leɪk/<br>دیتا لِیک | A store of raw data for later use. | A data lake keeps raw data. | data lake |
| بُعد داده | /dɪˈmenʃn/<br>دیمِنشِن | One point of view for analysis. | A dimension gives the point of view. | dimension |
| تجمیع | /ˈæɡrɪɡət/<br>اَگریگِت | A result made from many rows. | An aggregate turns many rows into one number. | aggregate |
| شمارش | /kaʊnt/<br>کاوْنت | A number of rows. | The result can be counted. | count |
| جمع | /sʌm/<br>سام | The total of many numbers. | A sum turns many rows into one number. | sum |
| درون‌حافظه‌ای | /ˌɪn ˈmeməri/<br>این مِموری | Kept in the memory, not on a disk. | An in-memory database answers in microseconds. | in-memory |
| جاسازی‌شده | /ɪmˈbedɪd/<br>اِمبرِدِد | Built inside another program. | An embedded database lives inside a program. | embedded |

**جدول ۲ — کارهای پایگاه داده (Database Actions)**

| فارسی | تلفظ | Definition (EN) | Example (EN) | English |
|---|---|---|---|---|
| درج کردن | /ɪnˈsɜːrt/<br>اینسِرت | To add a new record. | A new record is inserted. | insert |
| بازیابی کردن | /rɪˈtriːv/<br>ریتـریو | To get data back from the database. | A value cannot be retrieved. | retrieve |
| ماندگار کردن | /pərˈsɪst/<br>پِرسیست | To store data so that it stays. | It was never persisted. | persist |
| بی‌نام‌سازی کردن | /əˈnɑːnɪmaɪz/<br>اَنانیمایز | To remove the name from personal data. | Personal details are anonymized. | anonymize |
| نرمال‌سازی کردن | /ˈnɔːrməlaɪz/<br>نورمَلایز | To remove repeated data from tables. | A table should be normalized. | normalize |
| معکوس نرمال‌سازی | /ˌdiːˈnɔːrməlaɪz/<br>دینورمَلایز | To add controlled repetition for speed. | Sometimes a table is denormalized on purpose. | denormalize |
| خرد کردن داده | /ʃɑːrd/<br>شارد | To split a large dataset across machines. | A large dataset can be sharded. | shard |
| دادهٔ اولیه ریختن | /siːd/<br>سیـد | To fill a new table with starting data. | The first rows were seeded from a list. | seed |
| خروجی گرفتن | /dʌmp/<br>دامپ | To copy a whole database to a file. | A dump is taken every night. | dump |
| تبدیل شکل داده | /trænsˈfɔːrm/<br>ترَنسفُرم | To change the shape of data. | The data is cleaned and transformed. | transform |
| اعتبارسنجی کردن | /ˈvælɪdeɪt/<br>وَلیـدِیت | To check that data follows the rules. | Every field must be validated. | validate |
| محدود کردن | /rɪˈstrɪkt/<br>ریستریکت | To allow only some people or values. | Access is restricted. | restrict |
| تأیید کردن | /əˈpruːv/<br>اَپروو | To say that something is acceptable. | The report was approved by the department. | approve |
| نمودار | /ˈdaɪəɡræm/<br>دایَگرَم | A drawing that shows parts and links. | A good diagram makes the rules visible. | diagram |
| نگاشت کردن | /mæp/<br>مَپ | To match one thing to another. | Every attribute is mapped to one column. | map |
| مرتبط کردن | /rɪˈleɪt/<br>ریلِیت | To show how two things are connected. | The table relates the two entities. | relate |
| واکشی کردن | /fetʃ/<br>فِتچ | To get rows from the database. | The rows are fetched. | fetch |
| جستن در جدول | /lʊk ʌp/<br>لوک آپ | To find one record by its key. | A record can be looked up by its primary key. | look up |
| لغو کردن (تراکنش) | /əˈbɔːrt/<br>اَبورت | To stop a transaction completely. | The transaction is aborted. | abort |
| پاک‌سازی کامل | /pɜːrdʒ/<br>پِرج | To delete data completely and for ever. | Old data is purged. | purge |
| مقدار پیش‌فرض | /dɪˈfɔːlt/<br>دیفالت | The value that is used when nothing is given. | A record is created without a default value. | default |
| آبشاری | /kæˈskeɪd/<br>کَـسکِید | An action that follows another action. | Its children are removed by a cascade rule. | cascade |
| تطبیق دادن | /ˈrekənsaɪl/<br>رِکَنسایل | To check that two sets of numbers agree. | The numbers were reconciled with the old reports. | reconcile |
| نمونه‌برداری | /ˈsæmpl/<br>سَمپُل | To take a small part of the data. | A careful sample of rows shows the problems. | sample |
| طبقه‌بندی کردن | /ˈklæsɪfaɪ/<br>کلَسِفای | To put things into groups. | The numbers are classified into groups. | classify |
| ثبت کردن داده | /ˈkæptʃər/<br>کَپچِر | To record data when it arrives. | Raw data is captured from many places. | capture |
| دریافت و وارد کردن | /ɪnˈdʒest/<br>اینجِست | To bring data into a system. | Then it is ingested into a staging area. | ingest |
| بازسازی کردن | /ˌriːˈbɪld/<br>ریبیلد | To build something again. | Every table is rebuilt from the dump. | rebuild |
| خلاصه‌سازی کردن | /ˈsʌməraɪz/<br>سامَرایز | To make a short version of something. | The data is summarized in one report. | summarize |
| نمایش بصری دادن | /ˈvɪʒuəlaɪz/<br>ویژوالایز | To show data as a picture or a chart. | The numbers are visualized in one chart. | visualize |

**جدول ۳ — صفت‌ها و مفاهیم اطلاعاتی (Adjectives and Information Concepts)**

| فارسی | تلفظ | Definition (EN) | Example (EN) | English |
|---|---|---|---|---|
| رابطه‌ای | /rɪˈleɪʃənl/<br>ریلِیشِنَل | Built from tables that are related. | It is relational: the tables are related. | relational |
| ساختاریافته | /ˈstrʌktʃərd/<br>سْتراکچِرد | With a known place for every value. | Structured data sits in known places. | structured |
| بی‌ساختار | /ʌnˈstrʌktʃərd/<br>آن‌ستْراکچِرد | With no fixed shape or table. | A data lake keeps unstructured data. | unstructured |
| اتمی، تجزیه‌ناپذیر | /əˈtɑːmɪk/<br>اَتَمیک | Happening completely or not at all. | Every change is atomic. | atomic |
| کهنه | /steɪl/<br>ستِیل | Old and no longer correct. | A value may be stale. | stale |
| تازه | /freʃ/<br>فرِش | New and recently updated. | Its numbers must be fresh. | fresh |
| پراکنده | /ˈskætərd/<br>اِسکَتِرد | Spread over many places. | A scattered file system keeps many copies. | scattered |
| متمرکز | /ˈsentrəlaɪzd/<br>سِنتِرَلایزد | Kept in one place. | A centralized warehouse keeps one copy. | centralized |
| حساس | /ˈsensətɪv/<br>سِنسِتیو | That must be protected carefully. | Sensitive data is never stored as simple text. | sensitive |
| محرمانه | /ˌkɑːnfɪˈdenʃl/<br>کانفیدِنشَل | Private and not for everybody. | Confidential data is hashed or encrypted. | confidential |
| بی‌نام | /əˈnɑːnɪməs/<br>اَنانیمِس | With no name attached. | An anonymous record is useful for analytics. | anonymous |
| قابل رهگیری | /ˈtreɪsəbl/<br>ترِیسَبُل | Possible to follow from start to end. | Every change must be traceable. | traceable |
| تراکنشی | /trænˈzækʃənl/<br>ترَنزَکشِنَل | Built for many small, safe changes. | A transactional system must know who did what. | transactional |
| تحلیلی | /ˌænəˈlɪtɪkl/<br>اَنَلِیتیکَل | Used for studying numbers. | Its numbers are analytical. | analytical |
| تاریخی | /hɪˈstɔːrɪkl/<br>هیستوریکَل | About the past. | Its data is historical. | historical |
| زمان واقعی | /ˈriːəl taɪm/<br>ریـل تایم | Updated at the same moment. | A real-time report is updated while data arrives. | real-time |
| مشتق | /dɪˈraɪvd/<br>دِرایود | Calculated from other values. | A derived value is calculated. | derived |
| خام | /rɔː/<br>رَو | Not cleaned or changed yet. | Raw data is captured from many places. | raw |
| ناخالص، کثیف | /ˈdɜːrti/<br>دِرتی | Wrong or incomplete. | Dirty data is incomplete or simply wrong. | dirty |
| دقیق | /ˈækjərət/<br>اَکیورَت | Correct and close to the truth. | Its data must be accurate. | accurate |
| کهنه و از رده خارج | /ˌaʊtˈdeɪtɪd/<br>اوت‌دِیتِد | Too old to be useful. | A date may be outdated. | outdated |
| تکراری | /ˈduːplɪkət/<br>دوپلیکِت | Appearing more than once. | A row may be duplicated. | duplicate |
| یکتا | /juˈniːk/<br>یونیـک | Existing only once. | A primary key is a unique value. | unique |
| معتبر | /ˈvælɪd/<br>وَلیـد | Following the rules. | Its data must be valid. | valid |
| اجباری | /ˈmændətɔːri/<br>مَندَتوری | That you must fill in. | Some fields are mandatory. | mandatory |
| اختیاری | /ˈɑːpʃənl/<br>آپشِنَل | That you may leave empty. | Others are optional. | optional |
| شفاف | /trænsˈpærənt/<br>ترَنسپَرِنت | Easy to see and explain. | A transparent process can be explained. | transparent |
| حاکمیت داده | /ˈɡʌvərnəns/<br>گاوِرنَنس | The rules about who may use data. | Data governance decides who may see what. | governance |
| پاسخ‌گویی | /əˌkaʊntəˈbɪləti/<br>اَکاوْنتَبِلیتی | Being responsible for your work. | Accountability means somebody is responsible. | accountability |
| بینش | /ˈɪnsaɪt/<br>اینسایت | A useful understanding from data. | The data is turned into an insight. | insight |

---

### 3. Reading / متن اصلی

**عنوان متن: A Set of Promises (مجموعه‌ای از وعده‌ها)**

**[1]** A database is an organized collection of data that is stored in one place and can be searched quickly. An information system is bigger: it is the database plus the programs, the rules, and the people. Almost every modern service is built on a database, from a small shop to a university.

**[2]** Data is kept in tables. A table has columns and rows, and each row is called a record. One column is one field of the record: a name, an email, or a date. The same rules are used for every row, so a table is a very regular place.

**[3]** How is one row found between a million rows? Every table should have a primary key: a unique value such as a student number. A foreign key is a column that points to a key in another table, so two tables can be related without copying the data.

**[4]** Every entity in the world becomes a table, and every attribute becomes a column. Every attribute is mapped to one column, and the same value is never stored twice. A relationship between two entities is drawn as a line in a diagram: one student can take many courses, and one course can be taken by many students. A good diagram makes the rules visible.

**[5]** How are tables made safe and regular? With normalization: repeated data is removed and moved into its own table, so a name is written once. A constraint can also be added, for example a rule that no two rows may have the same value. Sometimes a table is denormalized on purpose, to make reading faster.

**[6]** What happens when the data is dirty? Dirty data is incomplete, inconsistent, or simply wrong: a date is outdated, a row is duplicated, or a value is stale. Integrity means that every rule is respected. Some fields are mandatory, and others are optional. Bad data is usually more expensive than no data.

**[7]** How is data used? A query is written and sent to the database. The rows that are needed are fetched, and the result can be counted, summed, or grouped. One record can be looked up by its primary key. An aggregate such as a count or a sum turns a thousand rows into one number that a manager can read.

**[8]** Why are some databases fast? Because an index is built on the columns that are searched most. The index is a small copy of the data, and it can be searched very quickly. When an index is used, a query is answered in milliseconds; when it is not used, the whole table is read.

**[9]** Several changes are often made together. A transaction is a group of changes that must all succeed or all fail. If something goes wrong, the transaction is aborted and the old values are restored; if everything is correct, the changes are committed. This is why a bank transfer is never half-done.

**[10]** These four promises are called ACID. Every change is atomic: it happens completely or not at all. The data is kept consistent, one transaction is isolated from another, and the result is stored durably, so it survives a crash. A database that cannot promise this is not used for money.

**[11]** Where does big data come from? Raw data is captured from many places: a form, a sensor, a payment, or a log. Then it is ingested into a staging area, cleaned, validated, and transformed before it is loaded into a warehouse. This pipeline is often called ETL.

**[12]** A warehouse is built for reading, not for everyday writing. Its data is historical, and its numbers are analytical: the same dataset is read by many reports. A data lake is different: raw, unstructured data is simply kept there until somebody needs it. Both are used by large companies.

**[13]** How are the numbers explained? A dimension gives the point of view: time, place, or product. Then the data can be aggregated, summarized, and turned into an insight. A diagram or a chart helps because a picture is understood faster than a table. A good report shows one clear idea.

**[14]** Not every table is a table. A view is a saved query that looks like a table, so the same result is not written twice. A trigger is a small program that runs by itself after a change, and a sequence gives the next number for a new record. These tools are used to keep data separate and safe.

**[15]** Some systems use noSQL databases. Their data is not kept in a strict table: documents, key values, or graphs are stored instead. They became popular because a very large dataset can be sharded across many machines, and an in-memory database can answer in microseconds. An embedded database may live inside one program.

**[16]** How is data protected? Sensitive and confidential data is never stored as a simple text: it is hashed or encrypted. Personal details are anonymized before they are shared, so a name cannot be linked to a person. Old data is purged or moved to an archive, and a dump of the whole database is taken every night.

**[17]** Rules and people are also part of the system. Data governance decides who may see what, and every change must be traceable, so an audit can follow it. A clear policy of accountability means that somebody is always responsible. Access is restricted, and the schema is documented before it is changed.

**[18]** A university information system is a good example. Students are registered in one table, courses are listed in another, and grades are written in a third table that relates the two. A report is generated at the end of every term, and the results are checked before they are published.

**[19]** Mina built a small database for the library of her department. Each book is stored in one row, and each borrower is stored in another table. The first rows were seeded from a list of books. When a book is borrowed, a new record is inserted, and when it is returned, the record is updated. Every table is rebuilt from the dump when something goes wrong.

**[20]** Then the old data was loaded and the numbers were reconciled with the paper records. A few rows were duplicated, so the dataset was cleaned again. One date was outdated and another was missing, so the source was checked. Finally the report was approved by the department.

**[21]** How should a database be designed? The rules must be written before the tables are built, and every field must be validated when it is entered. A table should be normalized unless there is a good reason, and an index should be added only when a query needs it. Nothing should be deleted before it is archived.

**[22]** What happens when a query is sent? First it is parsed and checked against the schema. Then a plan is chosen: an index may be used, or the whole table may be read. The rows are fetched, the aggregate is calculated, and the answer is returned. If the same query is repeated, the result may be cached.

**[23]** Where does the database live today? It is often run in the cloud, and the same data is copied to three or four machines, so that one failure does not stop the service. A transaction may be routed to the nearest copy, and a slow query is usually optimized first. Capacity is added when the dataset grows.

**[24]** Privacy is a legal duty now. Personal data must be protected, and consent must be recorded before the data is collected. Records are anonymized or aggregated when the individual is not needed, and a purge is scheduled for everything that has become useless. An analytics team may see a summary, but not a name.

**[25]** Which data should be trusted? Only the data that has been checked. A report is read differently when its source is known, and every number should be traceable to one row. If two systems give two answers, the disagreement must be explained, not hidden.

**[26]** What are the common mistakes? A table is created without a primary key, so duplicate rows are inserted. An index is forgotten, so a simple query becomes slow. A backup is never tested, so nobody knows if the data can be restored. Most of these problems are found by a careful diagram, not by a fast server.

**[27]** What will change? More data will be collected and more decisions will be made by programs, so the rules must be written down more carefully. Small databases will still be used, because a simple table is often enough. The skill that will never be outdated is the ability to ask a clear question.

**[28]** A database is not a box of files; it is a set of promises. Data is stored once and found quickly. Changes are made safely, and every change is traceable. Numbers are cleaned before they are trusted. When these promises are kept, the information system is a quiet, useful machine.

**[29]** Not every problem has a simple answer. An anomaly is a value that does not follow the rule, and it is found by mapping every row to a pattern. Sometimes a value cannot be retrieved because it was never persisted, and sometimes a record is created without a default value. A careful sample of rows shows most of these problems. When a key is deleted, its children are removed by a cascade rule, so nothing is left behind; and the numbers are classified into groups and visualized in one chart.

**[30]** Which words describe a good database? It is relational when its tables are related to each other, and structured when every value sits in a known place. Its data must be accurate and valid, and its numbers must be fresh, not stale. A centralized warehouse keeps one copy; a scattered file system keeps many. An anonymous record is useful for analytics, but a transactional system must know who did what. A transparent process can be explained in one minute, and a real-time report is updated while the data is still arriving. A derived value is calculated, not entered.

*(۱۶۸۰ واژه — ۳۰ پاراگراف)*

---

### 4. Persian Translation / ترجمه فارسی

**ترجمهٔ پاراگراف‌های کلیدی:**

**[۱]** پایگاه داده مجموعه‌ای سازمان‌یافته از داده است که در یک جا ذخیره می‌شود و می‌توان آن را سریع جست‌وجو کرد. یک سیستم اطلاعاتی بزرگ‌تر است: پایگاه داده به‌علاوهٔ برنامه‌ها، قاعده‌ها و افراد. تقریباً هر سرویس امروزی روی یک پایگاه داده ساخته شده است، از یک فروشگاه کوچک تا یک دانشگاه.

**[۵]** جدول‌ها چگونه ایمن و منظماند؟ با نرمال‌سازی: دادهٔ تکراری حذف و به جدول خودش منتقل می‌شود، پس یک نام یک بار نوشته می‌شود. یک قید محدودکننده هم می‌توان اضافه کرد، مثلاً قاعده‌ای که دو سطر نباید مقدار یکسان داشته باشند. گاهی جدولی به‌عمد معکوس نرمال‌سازی می‌شود تا خواندن سریع‌تر شود.

**[۹]** چند تغییر اغلب با هم انجام می‌شوند. تراکنش گروهی از تغییرهاست که باید همه موفق شوند یا همه شکست بخورند. اگر چیزی اشتباه شود، تراکنش لغو می‌شود و مقادیر قدیمی بازمی‌گردند؛ اگر همه‌چیز درست باشد، تغییرها ثبت می‌شوند. به همین دلیل انتقال بانکی هیچ‌وقت نیمه‌کاره نمی‌ماند.

**[۱۱]** دادهٔ انبوه از کجا می‌آید؟ دادهٔ خام از جاهای زیادی ثبت می‌شود: یک فرم، یک حس‌گر، یک پرداخت یا یک لاگ. بعد در یک ناحیهٔ آماده‌سازی دریافت می‌شود، پاک می‌شود، اعتبارسنجی و تبدیل می‌شود و سپس در انبار داده بارگذاری می‌شود. این مسیر را اغلب ETL می‌نامند.

**[۱۶]** داده چگونه محافظت می‌شود؟ دادهٔ حساس و محرمانه هرگز به‌صورت متن ساده ذخیره نمی‌شود: به‌صورت درهم‌ساز یا رمزنگاری‌شده نگه‌داری می‌شود. جزئیات شخصی پیش از اشتراک‌گذاری بی‌نام‌سازی می‌شوند، پس یک نام به یک شخص قابل پیوند نیست. دادهٔ قدیمی پاک‌سازی کامل می‌شود یا به بایگانی می‌رود و هر شب یک خروجی از کل پایگاه داده گرفته می‌شود.

**[۲۱]** پایگاه داده چگونه باید طراحی شود؟ قاعده‌ها باید پیش از ساختن جدول‌ها نوشته شوند و هر فیلد هنگام ورود اعتبارسنجی شود. جدول باید نرمال باشد مگر دلیل خوبی وجود داشته باشد و نمایه فقط وقتی اضافه شود که یک پرس‌وجو به آن نیاز دارد. هیچ چیز نباید پیش از بایگانی شدن حذف شود.

**[۳۰]** کدام واژه‌ها یک پایگاه دادهٔ خوب را توصیف می‌کنند؟ وقتی جدول‌هایش به هم مرتبط باشند رابطه‌ای است و وقتی هر مقدار جای مشخصی داشته باشد ساختاریافته. دادهٔ آن باید دقیق و معتبر باشد و عددهایش تازه، نه کهنه. یک انبار دادهٔ متمرکز یک رونوشت نگه می‌دارد؛ یک سامانهٔ فایل‌های پراکنده رونوشت‌های زیادی. یک رکورد بی‌نام برای تحلیل مفید است، اما یک سامانهٔ تراکنشی باید بداند چه کسی چه کاری کرد. یک فرایند شفاف در یک دقیقه توضیح‌پذیر است و یک گزارش زمان واقعی همان‌طور که داده می‌رسد به‌روز می‌شود. یک مقدار مشتق محاسبه می‌شود، نه وارد.

**خلاصهٔ فارسی متن:**

پایگاه داده مجموعه‌ای سازمان‌یافته از داده است و سیستم اطلاعاتی، آن پایگاه به‌علاوهٔ برنامه‌ها، قاعده‌ها و افراد. داده در جدول‌ها نگه‌داری می‌شود؛ جدول از ستون‌ها و سطرها (رکوردها) ساخته شده و هر ستون یک فیلد است. کلید اصلی یک سطر را یکتا پیدا می‌کند، کلید خارجی دو جدول را بدون رونوشت داده به هم مرتبط می‌کند و رابطه‌ها در یک نمودار رسم می‌شوند. هر موجودیت جدول و هر ویژگی ستون می‌شود؛ نرمال‌سازی دادهٔ تکراری را حذف می‌کند و قیدهای محدودکننده و قواعد یکپارچگی، داده را منظمان نگه می‌دارند. گاهی جدول به‌عمد معکوس نرمال‌سازی می‌شود تا خواندن سریع‌تر باشد.

پرس‌وجو نوشته و فرستاده می‌شود، رکوردها با کلید اصلی جستن‌شده و ردیف‌ها واکشی می‌شوند؛ نمایه‌ها جست‌وجو را سریع می‌کنند و تجمیع (شمارش و جمع) هزاران سطر را به یک عدد تبدیل می‌کند. تراکنش‌ها با وعده‌های ACID (اتمی، سازگار، جدا، پایدار) از نیمه‌کاره ماندن داده جلوگیری می‌کنند. دادهٔ خام از جاهای مختلف ثبت و در ناحیهٔ آماده‌سازی دریافت، پاک، اعتبارسنجی و تبدیل می‌شود تا در انبار داده بارگذاری شود؛ دریاچهٔ داده دادهٔ بی‌ساختار را برای بعد نگه می‌دارد. نما، تریگر و توالی ابزارهای کمکی‌اند و پایگاه‌های noSQL با خرد کردن داده و پردازش درون‌حافظه‌ای به دادهٔ بسیار بزرگ پاسخ می‌دهند.

امنیت و حاکمیت داده با بی‌نام‌سازی، محدود کردن دسترسی، رهگیری‌پذیری، پاسخ‌گویی و قاعده‌های رضایت تأمین می‌شود. کیفیت داده با واژه‌های دقیق، معتبر، تازه، خام، ناخالص، کهنه، تکراری و یکتا سنجیده می‌شود و طراحی خوب یعنی قاعده‌ها پیش از ساخت جدول‌ها نوشته شوند. در پایان، متن نتیجه می‌گیرد که پایگاه داده «مجموعه‌ای از وعده‌ها» است: داده یک بار ذخیره و سریع یافت می‌شود، تغییرها ایمن و رهگیری‌پذیرند و عددها پیش از اعتماد، پاک‌سازی می‌شوند.

---

### 5. Comprehension Check / درک مطلب

**الف) چهارگزینه‌ای — ده سؤال**

1. What is an information system?
   a) only the tables
   b) a box of files
   c) the database plus the programs, the rules, and the people

2. What is a record?
   a) one column of a table
   b) one row of a table
   c) one index

3. What does a primary key do?
   a) it finds one row with a unique value
   b) it makes the table slower
   c) it points to another table

4. What does normalization do?
   a) it adds more copies of a name
   b) it deletes the primary key
   c) it removes repeated data

5. Which value is described as "stale"?
   a) a value that is too old to be correct
   b) a value that is very fresh
   c) a value that is confidential

6. Why can a query be answered in milliseconds?
   a) because the data is anonymous
   b) because an index is used
   c) because the table is small

7. What happens when a transaction fails?
   a) half of the changes are kept
   b) the whole database is deleted
   c) it is aborted and the old values are restored

8. What is the difference between a warehouse and a data lake?
   a) a lake is built for reporting
   b) a lake keeps raw unstructured data for later use
   c) a warehouse keeps no data at all

9. What must be recorded before personal data is collected?
   a) consent
   b) a dump
   c) a dimension

10. Why is a duplicate row a problem?
   a) because it is a cascade rule
   b) because two rows say the same thing and the numbers may be wrong
   c) because it makes the table longer, which is always good

**ب) صحیح یا غلط — ده سؤال**

1. A foreign key is a column that points to another table. (..........)
2. A constraint is a rule that the data must follow. (..........)
3. Raw data is already clean and validated. (..........)
4. An in-memory database can answer in microseconds. (..........)
5. Sensitive data is usually stored as a simple text. (..........)
6. Every change in a protected system must be traceable. (..........)
7. A view is a saved query that looks like a table. (..........)
8. A purge keeps the data for ever. (..........)
9. A transactional system must know who did what. (..........)
10. A derived value is entered by the user. (..........)

**پ) پاسخ کوتاه — شش سؤال**

1. What are the four promises of ACID, in the words of the text?
2. What are the steps of the ETL pipeline in paragraph [11]?
3. Why is an index useful, and what is the cost of building one?
4. What is the difference between a view and a trigger?
5. What does a dimension give to a report?
6. Why must every number in a report be traceable to one row?

**ت) ایدهٔ اصلی — دو سؤال**

۱. ایدهٔ اصلی کل متن کدام جمله است؟

a) A database is a set of promises: data is stored once and found quickly, every change is safe and traceable, and numbers are trusted only after they are cleaned.
b) An in-memory database answers in microseconds.
c) Mina built a small database for the library.

۲. پاراگراف [۲۶] بیشتر دربارهٔ چه چیزی است؟

a) The common mistakes in database design and how a careful diagram finds them.
b) How to write a certificate.
c) How big data is captured from sensors.

**ث) تطبیق — دو جدول**

**جدول ۱:** هر واژه (۱ تا ۵) را به معنی درست آن (الف تا ه) وصل کنید.

| # | Word | | Meaning |
|---|---|---|---|
| 1 | entity | الف | a small program that runs by itself after a change |
| 2 | attribute | ب | one kind of thing that is stored |
| 3 | trigger | پ | a value that does not follow the rule |
| 4 | anomaly | ت | a saved query that looks like a table |
| 5 | view | ث | one property of an entity |

**جدول ۲:** هر واژه (۱ تا ۵) را به معنی درست آن (الف تا ه) وصل کنید.

| # | Word | | Meaning |
|---|---|---|---|
| 1 | stale | الف | with no name attached |
| 2 | fresh | ب | too old to be useful |
| 3 | outdated | پ | new and recently updated |
| 4 | anonymous | ت | the value that is used when nothing is given |
| 5 | default | ث | old and no longer correct |

---

### 6. Vocabulary Practice / تمرین واژگان

**الف) جای خالی — بیست سؤال**

از واژه‌های داخل کادر استفاده کنید. هر واژه یک بار.

> **واژه‌ها:** database · table · row · column · record · primary key · foreign key · index · constraint · relationship · entity · attribute · normalization · transaction · trigger · view · noSQL · dataset · warehouse · integrity

1. A .......... is an organized collection of data that can be searched.
2. Data is kept in a .......... with columns and rows.
3. Each .......... is called a record.
4. One .......... is one field of the record.
5. A new .......... is inserted when a book is borrowed.
6. Every table should have a .......... with a unique value.
7. A .......... points to a key in another table.
8. An .......... is built on the columns that are searched most.
9. A .......... can be added, for example a rule about two rows.
10. A .......... between two entities is drawn as a line.
11. Every .......... becomes a table.
12. Every .......... becomes a column.
13. With .......... repeated data is removed.
14. A .......... is a group of changes that succeed or fail together.
15. A .......... runs by itself after a change.
16. A .......... is a saved query that looks like a table.
17. Some systems use .......... databases without a strict table.
18. The same .......... is read by many reports.
19. A .......... is built for reading, not for everyday writing.
20. .......... means that every rule is respected.

**ب) وصل کردن — ده سؤال**

هر واژه را به معنی درست آن وصل کنید.

| # | Word | | Meaning |
|---|---|---|---|
| 1 | insert | الف | to copy a whole database to a file |
| 2 | retrieve | ب | to get rows from the database |
| 3 | persist | پ | to bring data into a system |
| 4 | anonymize | ت | to add a new record |
| 5 | shard | ث | to split a large dataset across machines |
| 6 | dump | ج | to store data so that it stays |
| 7 | ingest | چ | to remove the name from personal data |
| 8 | rebuild | ح | to check that two sets of numbers agree |
| 9 | reconcile | خ | to get data back from the database |
| 10 | fetch | د | to build something again |

**پ) جمله‌سازی — ده سؤال**

با هر واژه یک جملهٔ **مجهول** بنویسید (با *be* + قسمت سوم فعل) و سپس آن را به معلوم تبدیل کنید.

1. store *(حال ساده)*
2. build *(گذشتهٔ ساده)*
3. validate *(حال ساده)*
4. insert *(گذشتهٔ ساده)*
5. anonymize *(حال ساده)*
6. delete *(حال کامل)*
7. optimize *(با must)*
8. summarize *(حال ساده)*
9. visualize *(حال کامل)*
10. restrict *(حال ساده)*

**ت) واژه‌سازی: پیشوند و پسوند — یک تمرین**

پیشوند در **ابتدای** واژه و پسوند در **پایان** واژه می‌آید و معنای آن را تغییر می‌دهد:

| پیشوند / پسوند | معنی | نمونه |
|---|---|---|
| un- | نقیض | structured ← unstructured |
| non- | بدون، نقیض | relational ← non-relational |
| -al | صفت ساختن از اسم | relation ← relational |
| -ity | اسم ساختن از صفت | integral ← integrity |
| -able | «شدنی» | trace ← traceable |
| -ous | صفت ساختن از اسم | anomaly ← anomalous |

با افزودن پیشوند یا پسوند درست، واژهٔ مناسب بسازید.

1. structured ← .......... (بی‌ساختار)
2. relation ← .......... (رابطه‌ای)
3. integral ← .......... (یکپارچگی)
4. trace ← .......... (قابل رهگیری)
5. anomaly ← .......... (ناهنجار)
6. relational ← .......... (غیررابطه‌ای)

---

### 7. Grammar Focus / نکتهٔ گرامری

**موضوع: مجهول (passive voice)**

**توضیح فارسی:**

در جملهٔ **معلوم**، فاعل کار را انجام می‌دهد: *The system stores the data.* در جملهٔ **مجهول**، خودِ کار و نتیجه مهم است و فاعل واقعی یا ناشناخته است یا لازم نیست نام برده شود: *The data is stored by the system.*

**ساخت مجهول:** فعل *be* در زمان مناسب + **قسمت سوم فعل** (past participle): ① **حال ساده مجهول:** *am / is / are* + p.p. → *The data is stored in a table.* ② **گذشتهٔ ساده مجهول:** *was / were* + p.p. → *The index was built last night.* ③ **حال کامل مجهول:** *have / has been* + p.p. → *The record has been deleted.* ④ **مجهول با افعال وجهی:** *must / should / can / will* + *be* + p.p. → *The query must be optimized.* / *The report will be published tomorrow.*

اگر بخواهیم فاعل واقعی را بگوییم، با **by** می‌آید: *The report was written by Mina.* در نوشتهٔ فنی، *by* اغلب حذف می‌شود، چون ابزار یا سامانه مهم نیست: *Every field is validated.*

**کجا مجهول به کار می‌رود؟** ① وقتی فاعل ناشناخته است (*The password was stolen.*) ② وقتی فاعل مهم نیست (*The tables are checked every night.*) ③ وقتی خودِ کار و نتیجه مهم است (*All records must be validated.*) در فارسی هم مجهول با «شدن» ساخته می‌شود («ذخیره می‌شود»)، بنابراین این ساختار برای شما آشناست؛ فقط دقت کنید که در انگلیسی **قسمت سوم** فعل به کار برود.

دو خطای رایج فارسی‌زبانان: ① فراموش کردن فعل *be* («The data stored in a table» ← ~~The data stored~~ / *The data **is** stored*)؛ ② استفاده از گذشتهٔ ساده به‌جای قسمت سوم («is wrote» ← ~~is wrote~~ / *is written*؛ «was build» ← ~~was build~~ / *was built*).

**جدول ۱ — ساخت مجهول در زمان‌ها:**

| زمان | ساختار | نمونه |
|---|---|---|
| حال ساده | am / is / are + p.p. | The data is stored in a table. |
| گذشتهٔ ساده | was / were + p.p. | The index was built last night. |
| حال کامل | have / has been + p.p. | The record has been deleted. |
| با افعال وجهی | must / should / can / will + be + p.p. | The query must be optimized. |

**جدول ۲ — معلوم و مجهول:**

| معلوم | مجهول |
|---|---|
| The system stores the data. | The data is stored by the system. |
| The developer built the index. | The index was built by the developer. |
| The team has deleted the record. | The record has been deleted by the team. |
| The analyst will summarize the results. | The results will be summarized. |

**جدول ۳ — چه وقت مجهول به کار می‌رود؟**

| موقعیت | نمونه |
|---|---|
| فاعل ناشناخته است | The password was stolen. |
| فاعل مهم نیست | The tables are checked every night. |
| خودِ کار مهم است | All records must be validated. |
| فاعل مهم است (با by) | The schema was designed by the architect. |

**پنج مثال از دنیای کامپیوتر:**

1. Personal data is protected by the law.
2. The old records were deleted last week.
3. The index has been rebuilt since the migration.
4. Every field must be validated before it is entered.
5. The results will be published at the end of the term.

**تمرین‌ها — چهل سؤال**

**الف) جمله را مجهول کنید (۱ تا ۱۴).**

1. The data .......... (store) in a table.
2. The index .......... (build) last night.
3. Every record .......... (check) by the system.
4. The tables .......... (create) by the developer.
5. The query .......... (send) to the server.
6. The old records .......... (delete) last week.
7. Personal data .......... (protect) by the law.
8. The schema .......... (design) in three days.
9. The reports .......... (generate) every morning.
10. The password .......... (change) yesterday.
11. The dataset .......... (clean) before the analysis.
12. The results .......... (summarize) in one table.
13. The warehouse .......... (rebuild) last month.
14. The transaction .......... (abort) by the system.

**ب) با حال کامل مجهول کامل کنید (۱۵ تا ۲۰).**

15. The record .......... (delete).
16. The index .......... (rebuild).
17. The tables .......... (normalize).
18. The data .......... (anonymize).
19. The reports .......... (generate).
20. The schema .......... (change).

**پ) با افعال وجهی مجهول کامل کنید (۲۱ تا ۲۶).**

21. The query .......... (must / optimize).
22. All records .......... (must / validate).
23. The data .......... (can / retrieve) in one second.
24. The backup .......... (should / test) every month.
25. The results .......... (will / publish) tomorrow.
26. Personal data .......... (must not / share).

**ت) جمله‌ها را از معلوم به مجهول تبدیل کنید (۲۷ تا ۳۲).**

27. The system stores the data. → .......... 
28. Mina wrote the report. → .......... 
29. The team has deleted the record. → .......... 
30. The developer built the index. → .......... 
31. The system anonymizes the data. → .......... 
32. The team will summarize the results. → .......... 

**ث) خطای هر جمله را اصلاح کنید (۳۳ تا ۳۸).**

33. The data stored in a table.
34. The index is build last night.
35. The record has deleted.
36. The query must optimized.
37. The report was wrote by Mina.
38. The tables were create last week.

**ج) جملهٔ مجهول بسازید (۳۹ تا ۴۰).**

39. (passive) The company / protect / personal data → .......... 
40. (passive + modal) The database / must / back up / every night → .......... 

---

### 8. Key Sentences Translation / ترجمهٔ جمله‌های کلیدی

**انگلیسی ← فارسی (۱۰ جمله)**

1. Data is kept in tables, and every row is called a record.
2. A primary key is used to find one row quickly.
3. An index is built on the columns that are searched most.
4. The transaction was aborted, and the old values were restored.
5. Raw data is captured, validated, and transformed before it is loaded.
6. Sensitive data must never be stored as a simple text.
7. Every change must be traceable, so an audit can follow it.
8. The report was approved by the department.
9. A table should be normalized unless there is a good reason.
10. Numbers are cleaned before they are trusted.

**فارسی ← انگلیسی (۱۰ جمله)**

1. داده در جدول‌ها ذخیره می‌شود.
2. نمایه روی ستون‌های جست‌وجوشده ساخته می‌شود.
3. تراکنش توسط سامانه لغو شد.
4. دادهٔ شخصی باید محافظت شود.
5. گزارش توسط بخش تأیید شد.
6. هر فیلد باید اعتبارسنجی شود.
7. رکوردهای قدیمی هفتهٔ گذشته حذف شدند.
8. جدول باید نرمال شود.
9. نتیجه در یک نمودار نمایش داده می‌شود.
10. یک کلید اصلی باید یکتا باشد.

---

### 9. Writing Task / تمرین نگارش

**موضوع: How Data Is Kept in My University — داده در دانشگاه من چگونه نگه‌داری می‌شود**

یک نوشتهٔ کوتاه بنویسید و توضیح دهید در دانشگاه یا محل کار شما داده چگونه نگه‌داری و استفاده می‌شود. این موارد را بگنجانید:

- چه داده‌هایی نگه‌داری می‌شود؟ (دانشجویان، درس‌ها، نمره‌ها، کتاب‌ها، پرداخت‌ها)
- این داده‌ها کجا ذخیره می‌شوند و چه کسی آن‌ها را وارد می‌کند؟
- دو قاعده بنویسید که باید رعایت شود (با مجهول + افعال وجهی).
- یک مشکل کیفیت داده که دیده‌اید (تکراری، کهنه، ناقص) و اینکه چه باید بشود.

**شرایط نگارش:**

- نوشته بین **۱۲۰ تا ۲۰۰ واژه** باشد.
- دست‌کم **۶ جملهٔ مجهول** بنویسید (حال ساده، گذشتهٔ ساده یا حال کامل).
- دست‌کم **۲ جملهٔ مجهول با افعال وجهی** داشته باشد (*must be checked*).
- دست‌کم یک بار فاعل واقعی را با **by** بنویسید.
- دست‌کم **۱۰ واژه** از جدول‌های واژگان بخش ۲ استفاده شود.

---

### 10. Mini Project / پروژهٔ کوچک

**انشا (نیمه‌تحقیقی): گزارش یک پایگاه داده در زندگی من**

یک سامانهٔ واقعی را که خودتان داده در آن وارد می‌کنید انتخاب کنید (سامانهٔ دانشگاه، کتابخانه، اپ بانکی، فروشگاه اینترنتی، ثبت‌نام کلاس) و دربارهٔ آن گزارش کوتاهی بنویسید:

- **داده‌ها:** چه چیزهایی در آن ذخیره می‌شود؟ شش فیلد را فهرست کنید (نام، شمارهٔ دانشجویی، تاریخ، مبلغ…) و بگویید کدام‌ها اجباری و کدام‌ها اختیاری هستند.
- **جدول‌ها و رابطه:** سه جدول حدس بزنید و یک **شکل دستی ساده** بکشید که جدول‌ها را با جعبه و خط نشان دهد؛ برای هر جدول یک کلید اصلی و یک کلید خارجی مشخص کنید.
- **کیفیت داده:** یک نمونه از دادهٔ ناخالص که دیده‌اید بنویسید (تکراری، کهنه، ناقص، نادرست) و بگویید چه باید بشود.
- **امنیت:** کدام داده‌ها حساس یا محرمانه‌اند و چگونه باید محافظت شوند؟
- **قاعده‌ها:** سه قاعده بنویسید: دو مورد با مجهول + فعل وجهی (*must be validated*) و یک مورد با مجهول در حال کامل (*has been checked*).
- **پیشنهادها:** دو پیشنهاد برای بهتر شدن این سامانه بنویسید.

**شرایط نگارش:**

- گزارش را **دست‌نویس روی کاغذ** بنویسید و در **جلسهٔ بعد** به مدرس تحویل دهید.
- دست‌کم **۲۰۰ واژه** باشد (بدون احتساب شکل).
- دست‌کم **۸ جملهٔ مجهول** داشته باشد؛ دو مورد با فعل وجهی مجهول و یک مورد با *by*.
- دست‌کم **۱۲ واژه** از جدول‌های واژگان بخش ۲ در گزارش باشد.

**واژه‌های یاری‌دهنده:** database · table · record · primary key · foreign key · index · constraint · transaction · normalization · dataset · sensitive · validate

---

### 11. Did You Know? / آیا می‌دانستید؟

1. **The relational model was described in 1970, and modern databases still use its ideas about tables, rows, and keys.**
   مدل رابطه‌ای در سال ۱۹۷۰ توصیف شد و پایگاه‌های دادهٔ امروزی هنوز از ایده‌های آن دربارهٔ جدول‌ها، سطرها و کلیدها استفاده می‌کنند.

2. **SQL was standardised in 1986, and it is still the most common language for working with data.**
   زبان SQL در سال ۱۹۸۶ استاندارد شد و هنوز رایج‌ترین زبان برای کار با داده است.

3. **The four letters ACID (atomic, consistent, isolated, durable) have been used since the 1980s to describe safe transactions.**
   چهار حرف ACID (اتمی، سازگار، جدا، پایدار) از دههٔ ۱۹۸۰ برای توصیف تراکنش‌های ایمن به کار می‌رود.

4. **An index can make a query thousands of times faster, but every index also makes writing slower, because it must be updated.**
   یک نمایه می‌تواند پرس‌وجو را هزاران برابر سریع‌تر کند، اما هر نمایه نوشتن را هم کند می‌کند، چون باید به‌روزرسانی شود.

5. **noSQL databases became popular after 2009, when very large websites needed to store data across thousands of machines.**
   پایگاه‌های دادهٔ noSQL پس از سال ۲۰۰۹ رایج شدند، زمانی که وب‌سایت‌های بسیار بزرگ به ذخیرهٔ داده روی هزاران ماشین نیاز داشتند.

6. **According to industry reports in 2023, more than half of companies now keep their most important data in a cloud database.**
   بر پایهٔ گزارش‌های صنعت در سال ۲۰۲۳، بیش از نیمی از شرکت‌ها امروز مهم‌ترین داده‌های خود را در یک پایگاه دادهٔ ابری نگه می‌دارند.

7. **A single modern hard disk can hold more data than the entire Internet could store in 1995.**
   یک دیسک سخت امروزی می‌تواند دادهٔ بیشتری از کل اینترنت در سال ۱۹۹۵ نگه دارد.

8. **Privacy rules such as the GDPR were reported in 2023 to have produced more than a billion euros in fines in total, mostly for data that was not protected properly.**
   بر پایهٔ گزارش‌های ۲۰۲۳، قاعده‌های حریم خصوصی مانند GDPR در مجموع بیش از یک میلیارد یورو جریمه به‌بار آورده‌اند؛ بیشتر برای داده‌ای که درست محافظت نشده بود.
