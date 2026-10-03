# Lesson 18: Generative AI and Large Language Models

## Level: B2–C1
## Time: 90–120 minutes

> **درس ۱۸ — هوش مصنوعی مولد و مدل‌های زبانی بزرگ**
> **نکتهٔ گرامری:** شرطی نوع سوم (third conditional) · if + had + past participle، would have + past participle · برای گذشتهٔ خیالی و پشیمانی
> **متن درس:** ۲۸۷۷ واژه (۳۳ پاراگراف) | **واژگان کلیدی:** ۱۱۸ واژه | **باند سطح:** B2–C1 (پیشرفته)

---

### 1. Lesson Objectives / اهداف درس

- توضیح دهید یک مدل زبانی بزرگ چگونه متن تولید می‌کند و «توکن» و «پنجرهٔ متن» چه نقشی دارند.
- مراحل ساختن یک مدل مولد (پیش‌آموزش، تنظیم با دستورالعمل، هم‌راستاسازی) را به انگلیسی شرح دهید.
- تفاوت روش‌های نمونه‌برداری (حریصانه، پرتویی، هسته‌ای) و اثر آن‌ها بر خروجی را تحلیل کنید.
- کاربردهای بازیابی‌محور، ارزیابی خروجی تولیدی و ابزارهای سنجش آن را با واژگان دقیق بیان کنید.
- دربارهٔ خطرهای امنیتی و اخلاقی هوش مصنوعی مولد (تزریق دستور، جعل، توهم مدل، سرقت ادبی) موضع محتاطانه بنویسید.
- با شرطی نوع سوم دربارهٔ تصمیم‌های گذشته و پیامدهای فرضی آن‌ها بنویسید.

---

### 2. Key Vocabulary / واژگان کلیدی

> تلفظ‌ها بر پایهٔ انگلیسی آمریکایی و در قالب IPA نوشته شده‌اند.

**جدول ۱ — مدل‌های زبانی و معماری (Language Models and Architecture)**

| فارسی | تلفظ | Definition (EN) | Example (EN) | English |
|---|---|---|---|---|
| مدل زبانی بزرگ | /lɑːrdʒ ˈlæŋɡwɪdʒ ˈmɑːdəl/<br>لارج لَنگویج مادِل | A very large model trained to predict text. | A large language model can write a full report. | large language model |
| مدل زبانی بزرگ (سرواژه) | /ˌel el ˈem/<br>اِل‌اِل‌اِم | The short name for a large language model. | The LLM answered in three seconds. | LLM |
| ترنسفورمر | /trænsˈfɔːrmər/<br>ترَنسفورمِر | The network design behind modern language models. | The transformer reads the whole sentence at once. | transformer |
| خودرگرسیو | /ˌɔːtoʊrɪˈɡresɪv/<br>آتورِگرِسیو | Producing one new piece at a time, using what came before. | An autoregressive model writes word by word. | autoregressive |
| خودتوجهی | /ˌself əˈtenʃn/<br>سِلف اَتِنشِن | Weighing the parts of the input against each other. | Self-attention links a pronoun to its subject. | self-attention |
| سر توجه | /əˈtenʃn hed/<br>اَتِنشِن هِد | One parallel attention unit inside a layer. | Each attention head learned a different relation. | attention head |
| پیش‌خور | /ˈfiːd fɔːrwərd/<br>فید فوروِرد | The part of a layer that processes each position alone. | The feed-forward part holds most of the weights. | feed-forward |
| نرمال‌سازی لایه | /ˈleɪər ˌnɔːrmələˈzeɪʃn/<br>لِیِر نُرمَلِیزِیشِن | Keeping the numbers of each layer in a stable range. | Layer normalization made training steady. | layer normalization |
| پنجرهٔ متن | /ˈkɑːntekst ˈwɪndoʊ/<br>کانتِکست ویندو | How much text the model can read at one time. | A longer context window helps with long documents. | context window |
| سقف توکن | /ˈtoʊkən lɪmɪt/<br>توکِن لیمیت | The maximum number of units the model accepts. | The report hit the token limit and was cut. | token limit |
| زیرواژه | /ˈsʌbwɜːrd/<br>ساب‌وِرد | A part of a word that the model treats as one unit. | "Running" is split into two subwords. | subword |
| واژگان | /vəˈkæbjəleri/<br>وُکَبْیولِری | The fixed list of units that a model knows. | Unknown names are broken into subwords from the vocabulary. | vocabulary |
| توکن‌بندی | /ˌtoʊkənaɪˈzeɪʃn/<br>توکِنِیزِیشِن | The step that cuts text into small units. | Tokenization decides how numbers are counted. | tokenization |
| لاجیت | /ˈloʊdʒɪt/<br>لاجیت | A raw score for one possible next unit. | The highest logit won the next position. | logit |
| نمونه‌برداری | /ˈsæmplɪŋ/<br>سَمپلینگ | Choosing the next unit from the scores. | Sampling gives different answers to one question. | sampling |
| حریصانه | /ˈɡriːdi/<br>گریدی | Always choosing the highest-scoring unit. | A greedy model repeats the same sentence every time. | greedy |
| پرتویی (جست‌وجو) | /biːm/<br>بیم | Following several good paths at the same time. | Beam search is common in translation. | beam |
| هسته‌ای (نمونه‌برداری) | /ˈnuːkliəs/<br>نوکلیِس | Sampling only from the most likely small set. | Nucleus sampling avoids very strange words. | nucleus |
| تاپ-کی | /ˌtɑːp ˈkeɪ/<br>تاپ کِی | Keeping only the k best choices at each step. | With top-k, the text stayed on topic. | top-k |
| سرگشتگی | /pərˈpleksəti/<br>پِرپلِکسِتی | A number that shows how surprised a model is by text. | Low perplexity means the text looked familiar. | perplexity |
| انسجام | /koʊˈhɪrəns/<br>کوهیرِنس | The quality of fitting together as one whole. | A long answer needs coherence, not only fluency. | coherence |
| روانی | /ˈfluːənsi/<br>فلوئِنسی | The quality of sounding natural and smooth. | Fluency is easy to see and hard to measure. | fluency |
| دستورالعمل | /ɪnˈstrʌkʃn/<br>این‌اس‌تراکشِن | An order that tells the model what to do. | The instruction asked for five short bullets. | instruction |
| تنظیم با دستورالعمل | /ɪnˈstrʌkʃn ˈtuːnɪŋ/<br>این‌اس‌تراکشِن تونینگ | Extra training that teaches a model to follow orders. | Instruction tuning made the model usable by the public. | instruction tuning |
| بدون نمونه | /ˈzɪroʊ ʃɑːt/<br>زیرو شات | Asking for a task with no examples at all. | In zero-shot mode the model only sees the question. | zero-shot |
| با چند نمونه | /ˌfjuː ˈʃɑːt/<br>فیو شات | Giving two or three examples inside the prompt. | Few-shot examples fixed the answer format. | few-shot |
| زنجیرهٔ تفکر | /ˌtʃeɪn əv ˈθɔːt/<br>چِین آو ثات | Asking the model to write the steps before the answer. | A chain-of-thought prompt helped with arithmetic. | chain-of-thought |
| مدل پایه | /faʊnˈdeɪʃn ˈmɑːdəl/<br>فاون‌دِیشِن مادِل | A general model that other systems are built on. | A foundation model is adapted to many tasks. | foundation model |
| قانون مقیاس | /ˈskeɪlɪŋ lɔː/<br>اسکِیلینگ لا | A rule that links size, data, and quality. | Scaling law predicts what a bigger model will do. | scaling law |
| تریلیون | /ˈtrɪljən/<br>ترِیلیون | A thousand billion. | One model reports more than a trillion parameters. | trillion |
| فلاپس | /flɑːps/<br>فلاپس | A unit for counting floating-point operations. | Training used a very large number of FLOPS. | FLOPS |

**جدول ۲ — تولید و کاربردها (Generation and Applications)**

| فارسی | تلفظ | Definition (EN) | Example (EN) | English |
|---|---|---|---|---|
| متن‌به‌تصویر | /ˌtekst tə ˈɪmɪdʒ/<br>تِکست تو ایمِیج | Making a picture from a written description. | Text-to-image tools are used for posters. | text-to-image |
| شرح تصویر | /ˈkæpʃn/<br>کَپشِن | A short text that explains a picture. | The model wrote a caption for every photo. | caption |
| زیرنویس | /ˈsʌbtaɪtl/<br>ساب‌تایْتِل | Text shown at the bottom of a video. | Subtitles are generated in minutes now. | subtitle |
| دوبله | /ˈdʌbɪŋ/<br>دابینگ | Replacing the voices of a video with another language. | Dubbing kept the timing of the original speaker. | dubbing |
| شبیه‌سازی صدا | /vɔɪs ˈkloʊnɪŋ/<br>وُیس کلونینگ | Building a copy of a person's voice. | Voice cloning needs the owner's permission. | voice cloning |
| آواتار | /ˈævətɑːr/<br>اَوَتار | A digital figure that stands for a person. | His avatar speaks in three languages. | avatar |
| پویانمایی | /ˌænɪˈmeɪʃn/<br>اَنیمِیشِن | Moving pictures made from drawings or models. | The studio used AI in the animation stage. | animation |
| استوری‌بورد | /ˈstɔːribɔːrd/<br>استوری‌بورد | A set of simple drawings that plans a video. | They checked the storyboard before the shoot. | storyboard |
| رندر کردن | /ˈrendər/<br>رِندِر | To build the final image or video from a model. | Rendering took forty minutes on one machine. | render |
| واقع‌نمای عکاسی | /ˌfoʊtoʊriˈælɪstɪk/<br>فوتوری‌اَلِستیک | Looking like a real photograph. | A photorealistic image fooled the readers. | photorealistic |
| بزرگ‌نمایی (کیفیت) | /ˈʌpskeɪl/<br>آپ‌اسکِیل | To make an image larger and cleaner. | The tool upscaled the old photo. | upscale |
| ملودی | /ˈmelədi/<br>مِلَدی | A tune that a listener can remember. | The system wrote a simple melody. | melody |
| حق امتیاز | /ˈrɔɪəlti/<br>رُویَلتی | Money paid to a creator for each use of a work. | Artists asked for a royalty on generated music. | royalty |
| نقض حق | /ɪnˈfrɪndʒmənt/<br>این‌فرینجمِنت | Using a protected work without permission. | The court looked for copyright infringement. | infringement |
| حقوق (مالکیت فکری) | /raɪts/<br>رایتس | The legal powers of the owner of a work. | The contract explained who held the rights. | rights |
| انصراف | /ˈɑːpt aʊt/<br>آپت اوت | Choosing not to take part in something. | Artists can opt out of the training set. | opt-out |
| بازنویسی | /ˈpærəfreɪz/<br>پَرَفرِیز | Saying the same idea in different words. | Paraphrase the paragraph and keep the meaning. | paraphrase |
| ایده‌پردازی | /ˈbreɪnstɔːrmɪŋ/<br>برِین‌استورمینگ | Producing many ideas quickly before judging them. | We used brainstorming to list ten titles. | brainstorming |
| آموزش (خصوصی) | /ˈtuːtərɪŋ/<br>توتورینگ | Teaching one student or a small group. | Online tutoring is cheap and always available. | tutoring |
| همراه (دیجیتال) | /kəmˈpænjən/<br>کُمپَنیون | A program that talks with a person like a friend. | A companion app talks with lonely users. | companion |
| گفت‌وگو | /ˈdaɪəlɔːɡ/<br>دایَلوگ | A conversation between two sides. | The dialogue looked polite but was empty. | dialogue |
| گفته | /ˈʌtərəns/<br>آتِرَنس | One short piece of speech or text. | Each utterance was saved with a time stamp. | utterance |
| شخصیت (گفت‌وگو) | /pərˈsoʊnə/<br>پِرسونا | The role that an assistant plays in a chat. | The persona was a patient teacher. | persona |
| ایفای نقش | /ˈroʊl pleɪ/<br>رول پلِی | Acting a situation in order to practise it. | Role-play is used to train new nurses. | role-play |
| لحن | /toʊn/<br>تون | The feeling that the words carry. | The tone was too formal for a chat message. | tone |
| اصطلاح | /ˈɪdiəm/<br>ایدیُم | A fixed phrase whose meaning is not literal. | Idioms are the hardest part to translate. | idiom |
| ظرافت معنایی | /ˈnuːɑːns/<br>نوآنس | A small difference in meaning or feeling. | The translation lost a nuance of the original. | nuance |
| ابهام | /ˌæmbɪˈɡjuːəti/<br>اَمبی‌گیویتی | A situation with more than one possible meaning. | The ambiguity came from one missing word. | ambiguity |
| احساس (تحلیل) | /ˈsentɪmənt/<br>سِنتیمِنت | The feeling behind a text, positive or negative. | Sentiment analysis flags angry reviews. | sentiment |
| استلزام | /ɪnˈteɪlmənt/<br>این‌تِیلمِنت | A conclusion that must follow from two sentences. | The entailment check rejected the wrong answer. | entailment |
| نویسندگی | /ˈɔːθərʃɪp/<br>اُثِرشیپ | The state of being the writer of a text. | Authorship of the final paper stays with the student. | authorship |

**جدول ۳ — بازیابی، ارزیابی و عملیات (Retrieval, Evaluation, and Operations)**

| فارسی | تلفظ | Definition (EN) | Example (EN) | English |
|---|---|---|---|---|
| بازیابی | /rɪˈtriːvl/<br>ریتریوِل | Finding the right document before you answer. | Retrieval from the manual gave the exact paragraph. | retrieval |
| بازیابی‌محور | /rɪˈtriːvl ˈɔːɡmentɪd/<br>ریتریوِل آگمِنتِد | Generation that uses documents found beside the model. | The retrieval-augmented assistant answered from policy files. | retrieval-augmented |
| مبناگیری | /ˈɡraʊndɪŋ/<br>گراونْدینگ | Tying each answer to a real source. | Grounding lets a reviewer check every number. | grounding |
| بریده (متن) | /ˈsnɪpɪt/<br>اسنیپِت | A small part of a page shown as evidence. | The answer listed three snippets with page numbers. | snippet |
| تکه | /tʃʌŋk/<br>چانک | A short piece of a long document. | Each chunk holds about two paragraphs. | chunk |
| تکه‌تکه کردن | /ˈtʃʌŋkɪŋ/<br>چانکینگ | Cutting documents into small pieces for search. | Chunking decides what the model may read. | chunking |
| هم‌پوشانی | /ˈoʊvərlæp/<br>اووِرلَپ | Sharing part of the text between two pieces. | Overlap stops a sentence from being cut in half. | overlap |
| شباهت | /ˌsɪməˈlærəti/<br>سیمِ‌لَرِتی | How close two pieces of meaning are. | Similarity is measured between two vectors. | similarity |
| نزدیک‌ترین | /ˈnɪrɪst/<br>نیِرِست | The least far away in distance. | The nearest chunks are sent to the model. | nearest |
| رتبه‌بندی دوباره | /ˌriːˈræŋk/<br>ری‌رَنک | Sorting the found items a second time, more carefully. | A rerank step moved the best page to the top. | rerank |
| مجموعهٔ کنارگذاشته | /ˈhoʊldaʊt/<br>هولداوت | Data kept apart and never used for training. | The holdout set was opened only once. | holdout |
| جدول رده‌بندی | /ˈliːdərbɔːrd/<br>لیدِر‌بورد | A public table that compares many systems. | The leaderboard changed every week. | leaderboard |
| دوبه‌دو | /ˈperwaɪz/<br>پِیر‌وایز | Comparing two items directly, one against the other. | Pairwise tests ask which answer is better. | pairwise |
| ترجیح | /ˈprefrəns/<br>پرِفرِنس | What a person likes more, when forced to choose. | Human preference decides which answer wins. | preference |
| آلودگی (داده) | /kənˌtæməˈneɪʃn/<br>کُنتَمِنِیشِن | Test data that has already been seen in training. | Contamination makes a good score meaningless. | contamination |
| بلو | /bluː/<br>بلو | A score that compares generated text with a reference. | BLEU is popular in machine translation. | BLEU |
| روژ | /ruːʒ/<br>روژ | A score that checks how much of a reference was covered. | ROUGE is common for summaries. | ROUGE |
| میدان (ارزیابی) | /əˈriːnə/<br>اَرینا | A public place where models are compared blind. | In the arena, users judge without seeing the names. | arena |
| داور | /dʒʌdʒ/<br>جاج | A person, or a model, that gives a score. | A judge model copied the human ranking well. | judge |
| شیوه‌نامهٔ ارزشیابی | /ˈruːbrɪk/<br>روب‌ریک | A written list of what a good answer must contain. | The rubric had five levels for accuracy. | rubric |
| نقد | /krɪˈtiːk/<br>کریتیک | A careful comment on what is wrong and why. | The critique found two unsupported claims. | critique |
| چرخهٔ بازبینی | /rɪˈvɪʒn luːp/<br>ریویژِن لوپ | Writing, checking, and rewriting until it is good. | The revision loop ran for three rounds. | revision loop |
| پیش‌نویس‌کننده | /ˈdræftər/<br>درَفتِر | The part that writes the first version. | The drafter produced a rough answer in seconds. | drafter |
| بازبین (راستی‌آزما) | /ˈverɪfaɪər/<br>وِرِیفایِر | The part that checks the work of another part. | The verifier rejected one number and asked again. | verifier |
| امتیاز اطمینان | /ˈkɑːnfɪdəns skɔːr/<br>کانفیدِنس اسکور | A number that shows how sure the system is. | The confidence score was low, so a human was asked. | confidence score |
| توهم (مدل) | /həˌluːsɪˈneɪʃn/<br>هَلوسینِیشِن | A fluent answer that is simply not true. | Hallucination is the most common complaint. | hallucination |
| پیشرو (مرزی) | /ˈfrʌntɪr/<br>فرانتیِر | The most advanced systems that exist now. | Frontier models change every few months. | frontier |
| ثبت رویداد | /ˈlɔːɡɪŋ/<br>لاگینگ | Writing down what the system did and when. | Logging saved the team a week of work. | logging |
| برش (متن) | /trʌŋˈkeɪʃn/<br>ترونکِیشِن | Cutting off text that is too long to send. | Truncation removed the end of the history. | truncation |
| پر کردن | /ˈpædɪŋ/<br>پَدینگ | Adding empty units to reach a fixed length. | Padding wastes space in a short prompt. | padding |

**جدول ۴ — امنیت، اخلاق و سیاست (Security, Ethics, and Policy)**

| فارسی | تلفظ | Definition (EN) | Example (EN) | English |
|---|---|---|---|---|
| تزریق دستور | /prɑːmpt ɪnˈdʒekʃn/<br>پرامپت این‌جِکشِن | A hidden instruction inside the text that the model reads. | A prompt injection inside a web page changed the answer. | prompt injection |
| دور زدن محدودیت | /ˈdʒeɪlbreɪk/<br>جِیل‌برِیک | Tricking a model into ignoring its rules. | The jailbreak asked the model to role-play a rule-free system. | jailbreak |
| حفاظ | /ˈɡɑːrdreɪl/<br>گارد‌رِیل | A control that stops a system from doing harm. | A guardrail blocked the request for private data. | guardrail |
| نظارت محتوایی | /ˌmɑːdəˈreɪʃn/<br>مادِرِیشِن | Checking user content and removing what breaks the rules. | Moderation is done by filters and by people. | moderation |
| سمّیت زبانی | /tɑːkˈsɪsəti/<br>تاکسیسِتی | Harmful and hateful language. | The team measured toxicity in both languages. | toxicity |
| گفتار نفرت‌آمیز | /heɪt spiːtʃ/<br>هِیت اسپیچ | Speech that attacks a group of people. | Hate speech is banned in the platform rules. | hate speech |
| کلاهبرداری | /frɔːd/<br>فراد | Getting money or data by telling lies. | Fraud is the most expensive misuse of generated voice. | fraud |
| جعل هویت | /ɪmˌpɜːrsəˈneɪʃn/<br>ایمپِرسِنِیشِن | Pretending to be another person. | Impersonation is easy when a voice can be copied. | impersonation |
| بیرون‌کشی داده | /ˌeksfɪlˈtreɪʃn/<br>اِکسفیلترِیشِن | Moving data out of a system without permission. | The attack tried data exfiltration through a long prompt. | exfiltration |
| فهرست مجاز | /əˈlaʊlɪst/<br>اَلاو‌لیست | A list of the only things that are allowed. | An allowlist of domains stopped the leak. | allowlist |
| هم‌راستاسازی | /əˈlaɪnmənt/<br>اَلاینمِنت | Making a system act according to human values. | Alignment work decides what the model refuses. | alignment |
| یادگیری تقویتی از بازخورد انسان | /ˌɑːr el eɪtʃ ˈef/<br>آر‌اِل‌اِچ‌اِف | Training with human comparisons as a reward signal. | RLHF was used to make answers shorter and kinder. | RLHF |
| تیم سرخ | /red tiːm/<br>رِد تیم | A group whose job is to attack the system first. | The red team found four new attacks in one week. | red team |
| هدایت‌پذیری | /ˌstɪrəˈbɪləti/<br>استیرَبِلیتی | How well a model can be guided in one direction. | Steerability is what product teams ask for. | steerability |
| استفادهٔ نادرست | /ˌmɪsˈjuːs/<br>میس‌یوس | Using a tool in a way that hurts people. | The policy lists the main forms of misuse. | misuse |
| تقلب | /ˈtʃiːtɪŋ/<br>چیتینگ | Breaking the rules of study or of a game. | Cheating with a chat assistant is easy to hide. | cheating |
| قانون هوش مصنوعی اروپا | /ˌiː juː ˈeɪ aɪ ækt/<br>ای‌یو اِی‌آی اَکت | A European law that sets duties for AI systems. | The AI Act asks for documents and risk reports. | AI Act |
| صافی محتوا | /ˈkɑːntent ˈfɪltər/<br>کانتِنت فیلتِر | A program that blocks some kinds of text. | The content filter was too strict at first. | content filter |
| اعتماد و ایمنی | /trʌst ənd ˈseɪfti/<br>تراست اَند سِیفتی | The team and the rules that keep users safe. | Trust and safety is a full department now. | trust and safety |
| بازبینی انسانی | /ˈhjuːmən rɪˈvjuː/<br>هیومن ریویو | A person checking a machine decision. | Every refusal goes through human review. | human review |
| شکایت | /ˈɡriːvəns/<br>گریوِنس | A formal complaint by a person who was harmed. | A grievance can be opened from the app. | grievance |
| اعتراض (درخواست بازبینی) | /əˈpiːl/<br>اَپیل | Asking for a decision to be looked at again. | The appeal was answered in two days. | appeal |
| محدودیت نرخ | /reɪt ˈlɪmɪt/<br>رِیت لیمیت | Limiting how often a user may call a system. | A rate limit protected the service from abuse. | rate limit |
| نظارت (بر سامانه) | /ˈoʊvərsaɪt/<br>اووِرسایت | Watching that a system is used correctly. | Independent oversight was added after the incident. | oversight |
| اخلاق (حرفه‌ای) | /ˈeθɪks/<br>اِثیکس | Rules of right behaviour in a profession. | Ethics is a required course in this programme. | ethics |
| توضیح‌پذیری | /ɪkˌspleɪnəˈbɪləti/<br>اِکسپلِینَبِلیتی | Being able to say why a system gave that answer. | Explainability is harder for a large model. | explainability |

---

### 3. Reading / متن اصلی

**عنوان متن: Machine That Writes (ماشینی که می‌نویسد)**

**[1]** Generative AI means software that produces something new: a paragraph, a picture, a voice, or a short piece of music. Parsa, an undergraduate student, met this idea in the second week of his project, when his supervisor asked him to use a large language model (LLM) for a literature review. Hoda, an engineer in a hospital, met the same idea from the other side: she had to build one for the nursing staff. Both of them learned the same first lesson — an LLM does not look up an answer; it continues a text.

**[2]** Before a model can continue anything, the text must be cut into small units. Tokenization breaks a sentence into subwords, and the fixed list of all units that the model knows is its vocabulary. A rare family name may need three subwords, while a common word needs one. This detail is not academic: the cost of a request, the token limit of the model, and the length of the bill all follow from how the text was cut.

**[3]** The engine inside modern text models is the transformer. Unlike an older design that read a sequence one step at a time, a transformer reads the whole passage together, and self-attention decides which earlier parts matter for the part being written now. One attention head may follow the subject of a sentence while another follows a date. The feed-forward part of each block holds most of the learned weights, and layer normalization keeps the numbers in a range where training stays stable.

**[4]** Generation is autoregressive: the model produces one unit, adds it to the text, and then produces the next unit in the same way. For each position it gives a logit, a raw score, to every unit in its vocabulary, and those scores become a probability. Choosing from that probability is sampling. A greedy choice always takes the highest score and often repeats itself; beam search follows a few good paths at once; nucleus sampling keeps a small set of likely units and draws from it; top-k does the same with a fixed count. The temperature setting decides how adventurous those draws are.

**[5]** All of this happens inside a context window. If the conversation is longer than that window, some older text must go, which is called truncation, and a short input is sometimes filled out with padding so that several requests can be processed together. Parsa learned this the hard way: a long literature review lost the first page of instructions, and the model simply forgot the rules that he had written at the beginning.

**[6]** Size is the second thing a beginner must understand. Today's models report parameter counts in the billions, and some reports mention systems with more than a trillion parameters, trained with an enormous number of FLOPS. A scaling law links size, data, and quality, and above a certain size some new abilities appear suddenly, a phenomenon called emergence. A general model of this kind is a foundation model, and a team that needs the very best system of the moment pays for a frontier model that may be replaced in a few months.

**[7]** How does a machine that only continues text become a helper? It is trained in stages. First comes pretraining on a very large corpus of ordinary text, which teaches the shape of the language. Then instruction tuning adds pairs of an instruction and a good answer, so the model learns to follow orders instead of continuing an essay. Only after that does it feel like a product.

**[8]** The last stage uses people directly. In RLHF, human raters look at two answers and say which is better; these pairwise preference decisions become a reward signal, and the model is trained to earn it. The goal of the whole process is alignment, which means acting according to human values and not only producing fluent text. A red team is paid to break the system before users do, and steerability — the ability to guide the model in one direction — is what product teams ask for next.

**[9]** The user's own tool is the prompt. In zero-shot mode the model sees only the question and must guess the expected form. In few-shot mode the prompt contains two or three examples, which fixes the format and the tone. A chain-of-thought prompt asks the model to write the intermediate steps before the final answer, and on arithmetic this single change often improves the result. None of these tricks changes the model; they change the text that the model reads.

**[10]** They also cannot remove the central weakness. A hallucination is an answer that is perfectly fluent and completely wrong: a book that does not exist, a law that was never passed, a number taken from nowhere. Some systems attach a confidence score to each sentence so that a human being can see where the doubt is, and researchers use perplexity to measure how surprised a model is by a text, but a low perplexity does not prove that a claim is true.

**[11]** Hoda's answer to that weakness was retrieval. Her assistant first finds real pages in the hospital's own documents, and only then lets the model write an answer: this pattern is called retrieval-augmented generation. The documents are cut by chunking, each chunk is stored with a small overlap so that no sentence is cut in half, and a similarity search returns the nearest chunks, which a rerank step then sorts more carefully. Every answer ends with a snippet and a page number, and this grounding is what made the nurses trust it.

**[12]** Hoda split the work between two roles. A drafter model wrote the first version in one second, and a verifier checked every number against the retrieved text. If the verifier had found a wrong dose, the whole answer would have been rejected. A short critique from the second model sent the first one back for another attempt, and this revision loop ran at most three times. If she had let the drafter answer alone, the department would have lost the project in a month.

**[13]** Parsa used his model for different work, and he had to learn the difference between help and harm. He used it for brainstorming when ten titles were needed by the morning; he used it to paraphrase a heavy paragraph and to check the tone of an email to a professor. Idioms and nuance were the two places where it failed: a Persian idiom became a strange English sentence, and a small nuance in a legal text disappeared. Ambiguity was worse, because a prompt with two possible meanings produced a confident answer to the wrong question.

**[14]** Measuring generated text is a field of its own. A team keeps a holdout set that was never used in training, and it reports a score that compares the output with a human-written reference: BLEU for translation and ROUGE for summaries are the classic choices. Both numbers are blind to meaning, so a rubric written by the department is added, and either a human judge or a model judge scores each answer against that rubric. A better number is not the same thing as a better answer.

**[15]** Comparisons also happen in public. In an arena, two unknown answers are shown side by side and a user says which is better; the votes build a leaderboard that everyone reads on Monday morning. Hoda's team found one trap: contamination, where examples from a public test set had already appeared in the training data of one model, which made its score look perfect for no good reason. A pairwise preference test on their own hospital questions told them more than any leaderboard did.

**[16]** Then the semester gave Parsa his own incident. He submitted an essay that read well and that he had not really written. The teaching assistant asked a simple question about the second paragraph, and he could not answer it. If he had kept his notes and his drafts, he would have been able to defend every sentence. The rule he received afterwards was clear and reasonable: authorship belongs to the student, and a chat assistant is a tool, like a calculator — useful for thinking, useless as a substitute for thinking. Cheating with a fluent text is easy to do and easy to detect in a five-minute conversation.

**[17]** Used honestly, the same tools teach well. A tutoring assistant can explain one definition in five different ways, wait for the student's answer, and try the next explanation. A dialogue system keeps the last few utterances in view, so a follow-up question can be understood without repeating the first one. When the persona is a patient examiner, role-play becomes a cheap way to practise a defence, and the student can repeat the scene ten times without boring a human teacher.

**[18]** Images and video are a second family of products. A text-to-image system turns a written description into a picture, and a related model writes a caption for a photo that already exists. In video work the same technology adds subtitles, produces dubbing in another language, and builds an avatar that speaks for a person who is not present. A studio may start from a storyboard, generate the animation, and render the final scene; the result can look photorealistic, and an old photograph can be upscaled until the faces look sharp.

**[19]** Music, voice, and rights close this circle. A model can propose a melody in a requested style, and voice cloning can rebuild a real person's voice from a short sample. That is exactly where the law becomes part of the engineering. Who receives a royalty when a generated song earns money? Does the output count as an infringement of a protected work? A platform that trains on public material must therefore explain the rights it holds and offer a clear opt-out to creators who refuse.

**[20]** Language work continues to bring money. Sentiment analysis classifies reviews as positive or negative, and it is already used by every large shop. Entailment checking asks a harder question: does this conclusion really follow from these two sentences? Both tasks were once separate projects with their own datasets. A generative model now does them after a single instruction, and this is why the boundary between "an AI product" and "a big model plus a prompt" has become so thin.

**[21]** The most personal use case is the companion. A chat assistant with memory can talk with a lonely user every evening, remember the name of a pet, and ask about it a week later. The benefit is real, and so is the risk: a commercial companion may be tuned to keep the conversation long, because a long conversation is a long session. Misuse starts exactly there. A product that is paid by the minute has a reason to be interesting, and very little reason to be honest about its own limits.

**[22]** Security is the sharpest edge. A prompt injection hides an instruction inside a document or a web page that the model is asked to read, and the model may follow it as if it came from the owner. A jailbreak persuades the model to ignore its own rules, usually by wrapping the request in a story. If the assistant can call other tools, data exfiltration becomes possible: a careful attacker can move private text out of the system in small pieces. The defences are boring and effective — an allowlist of the tools and domains that may be used, a guardrail on the output, and no access at all to data that the user does not own.

**[23]** Fraud is the human version of the same problem. A copied voice on the telephone can ask a worried parent for money, and impersonation of a manager is enough to move a payment. If Hoda's team had not published the voice of their own assistant, someone else would have cloned it. If the hospital had not taught the staff about fake calls, at least one of them would have believed a familiar voice. Trust in a voice is old, and it is no longer proof of identity.

**[24]** Platforms answer with moderation. A content filter removes the most obvious harm before a human sees it, and a toxicity score flags text for people who review it. Hate speech is the clearest category to ban, because a rule about it can be written down in one paragraph. The hard part is the border: a report on hate speech must be allowed to quote it, while an invitation to hate it must not. Every hospital, school, and forum that deploys an assistant meets this problem in the first week.

**[25]** Rules have also become law. The European AI Act sets duties according to risk, and a system that touches health or education must document its data, its tests, and its limits. Within a company, oversight means a group that is independent of the team that built the model, and ethics is not a poster on the wall but a set of questions asked before the launch. Explainability is harder for a large model than for a decision tree, but a clear report of what the system can and cannot do is always possible. Human review of refusals is the minimum standard, and trust and safety is now a department, not a hobby.

**[26]** Operations decide whether any of this survives contact with users. A rate limit stops one account from using the whole capacity of the service, and logging records what was asked and what was answered, so that a strange case can be studied later. It also settles arguments: a disagreement about what the assistant did in March is easy to close when the record exists.

**[27]** Finally come the processes for people who were harmed. A user who is refused unfairly can open a grievance, and an appeal asks for a second look by another person. In Hoda's hospital, every blocked answer goes to human review within one working day; if the nurses had waited a week for an explanation, they would have stopped using the system entirely.

**[28]** Hoda's own incident had nothing to do with an attacker. A new edition of a drug guide changed one dosage table, and the assistant kept quoting the older number from a chunk that had been cached. If the team had re-indexed the documents after the update, the wrong number would never have appeared. If they had read the logs more carefully, they would have found the pattern three days earlier. The retrieval system had worked exactly as designed; the design had simply not included a step for old text.

**[29]** Both of them ended the term with a similar list. If Parsa had begun from the hospital's own questions instead of a public leaderboard, he would have written a more useful report. If Hoda had stored the source of every chunk from day one, her incident would have been a five-minute fix. Neither of them would now say that a bigger model is the answer: a bigger model with a broken pipeline is a faster way to make the same mistake.

**[30]** What cannot be expected of a generative system is truth. Fluency and coherence are exactly what such models are trained to produce, and neither of them is a check on facts. A paragraph can be smooth, well connected, polite, and false in three details. This is why the honest sentence in every report is the short one that lists the limits: the assistant is good at rewriting and at finding paragraphs, and it is unreliable on numbers, on dates, and on names.

**[31]** So what should a student do with these tools during a degree? Learn the subject first, because a prompt cannot check an answer that nobody in the room understands. Quote the source, keep the drafts, and write down which parts came from the model. Ask for the retrieval, not only for the answer: a page number is worth more than a confident sentence. Finally, treat every number as a claim to be verified, in the same way that a programmer treats every line of borrowed code as a line that must be understood.

**[32]** Teams that ship these products work in a fixed pattern. One model drafts, another one checks, and a human being owns the result. A small open-weight model is chosen when the task is narrow, the data is private, or the answer must be cheap; a frontier model is used when the task is new and the budget allows. If the team had measured only the average quality, they would have missed the expensive cases. If they had measured the worst case, they would have found the real requirement.

**[33]** Parsa now has a rule of his own: he asks the model to write the reasoning and then he checks the sources himself. Hoda has a similar rule for her department: the system may answer, but the nurse decides. If their projects had followed the fashion of the year, both of them would have bought the biggest model available and learned nothing. Because they measured the work instead of the hype, they finished with tools that their colleagues still use. A machine that writes is useful in the same way a library is useful: not because it is clever, but because somebody taught it where the books are.

*(۲۸۷۷ واژه — ۳۳ پاراگراف)*

---

### 4. Persian Translation / ترجمه فارسی

**الف) واژه‌های دشوار و معادل آن‌ها**

| واژه / عبارت | معادل پیشنهادی | نکتهٔ ترجمه |
|---|---|---|
| large language model | مدل زبانی بزرگ | صفت *large* به **اندازهٔ پارامترها** اشاره دارد، نه به طول متن تولیدشده؛ «مدل زبانی طولانی» غلط است. |
| token | توکن (واحد پردازش) | در این حوزه «توکن» واحد متن است، نه نشانهٔ رمزنگاری؛ همان واژه را در کل متن ثابت نگه دارید. |
| autoregressive | خودرگرسیو | معادل «خودبازگشتی» هم دیده می‌شود؛ در متن دانشگاهی یکی را انتخاب کنید و در پرانتز شکل انگلیسی را بیاورید. |
| self-attention | خودتوجهی | نه «خودجذبی» و نه «توجه به خود»؛ اصطلاح جاافتادهٔ فارسی «خودتوجهی» است. |
| perplexity | سرگشتگی | «گیجی مدل» ترجمهٔ محاوره‌ای است؛ در گزارش فنی «سرگشتگی» یا شکل اصلی انگلیسی به کار می‌رود. |
| nucleus sampling | نمونه‌برداری هسته‌ای | «هسته» توده‌ای احتمال است، نه هستهٔ اتم یا هستهٔ پردازنده. |
| context window | پنجرهٔ متن | «پنجره» ظرفیت است، نه پنجرهٔ نرم‌افزار؛ «بازهٔ متن» هم پذیرفته است. |
| truncation | برش (متن) | با «قطع کردن» اشتباه نشود؛ منظور کوتاه‌کردن متن بیش از ظرفیت پنجره است. |
| retrieval-augmented | بازیابی‌محور | «افزوده‌شده با بازیابی» تحت‌اللفظی است؛ شکل رایج «تولید بازیابی‌محور» است. |
| grounding | مبناگیری | «زمین‌گیری» غلط رایج است؛ منظور بستن هر جمله به منبع واقعی است. |
| rerank | رتبه‌بندی دوباره | فعل است، نه اسم دستگاه؛ «دوباره رتبه‌بندی کردن» روان‌تر است. |
| holdout | مجموعهٔ کنارگذاشته | با «آزمون» برابر نیست: کنارگذاشته از ابتدا جدا می‌ماند و در آموزش دیده نمی‌شود. |
| contamination | آلودگی داده | «آلودگی» اینجا یعنی نشت دادهٔ آزمون به آموزش، نه آلودگی فایل یا ویروس. |
| hallucination | توهم مدل | «هذیان» بار پزشکی دارد؛ در نوشتار فنی «توهم مدل» یا شکل انگلیسی به کار می‌رود. |
| prompt injection | تزریق دستور | «تزریق» دستور در متن است؛ «نفوذ دستور» ابهام ایجاد می‌کند. |
| exfiltration | بیرون‌کشی داده | «خارج‌سازی» هم رایج است؛ هر دو به معنای انتقال غیرمجاز داده از سامانه است. |
| steerability | هدایت‌پذیری | با «کنترل‌پذیری» یکی نیست: هدایت‌پذیری یعنی جهت‌دادن به سبک و رفتار مدل. |
| oversight | نظارت مستقل | در متن حقوقی و حاکمیتی «نظارت» ترجمه می‌شود، نه «بی‌توجهی»؛ ریشهٔ واژه گمراه‌کننده است. |
| trust and safety | اعتماد و ایمنی | نام یک واحد سازمانی است؛ در پرانتز شکل انگلیسی را نگه دارید تا با «اطمینان» اشتباه نشود. |

**ب) نکات ترجمه**

۱. **«تولید» در برابر «مولد»:** *generative model* را «مدل مولد» و *generation* را «تولید» ترجمه کنید؛ نوشتن «مدل تولیدی» معنا را عوض می‌کند.
۲. **ساخت مجهول انگلیسی را با «شده است» ترجمه کنید:** *the report was written by an assistant* ← «گزارش را یک دستیار نوشته است» یا «گزارش با دستیار نوشته شده است»؛ آوردن «توسط» جمله را ثقیل می‌کند.
۳. **جملهٔ شرطی نوع سوم در فارسی زمان مخصوص می‌خواهد:** *If they had logged the requests, they would have found the attack* ← «اگر درخواست‌ها را ثبت کرده بودند، حمله را پیدا می‌کردند». آوردن «پیدا خواهند کرد» بی‌ترجمهٔ غلط رایجی است که معنای فرضی را نابود می‌کند.
۴. **اصطلاح‌های چندواژه‌ای را نشکنید:** *retrieval-augmented generation* و *content filter* در فارسی به‌صورت ترکیب جاافتاده می‌آیند؛ ترجمهٔ واژه‌به‌واژهٔ آن‌ها معنا را مبهم می‌کند.
۵. **«ترجیح» در برابر «امتیاز»:** *preference* ترجیح انسانی است و *score* امتیاز عددی؛ در یک پاراگراف هر دو را با یک واژه ترجمه نکنید.
۶. **فعل‌های فنی را با فعل فارسی دقیق بیاورید:** *to serve a model* ← «مدل را در اختیار کاربران گذاشتن»، *to deploy* ← «به‌کارگیری/استقرار»، *to log* ← «ثبت کردن».
۷. **به افعال وجهی گذشته توجه کنید:** *should have checked* یعنی «باید بررسی می‌کرد» (نقد گذشته) و *might have worked* یعنی «شاید کار می‌کرد»؛ ترجمهٔ آن‌ها با زمان حال، معنا را جابه‌جا می‌کند.
۸. **از این ترجمه‌های تحت‌اللفظی بپرهیزید:** *red team* ← «تیم سرخ» (نه «تیم قرمز کاغذی»)، *jailbreak* ← «دور زدن محدودیت‌ها» (نه «فرار از زندان»)، *rate limit* ← «محدودیت نرخ» (نه «حد آهنگ»).

---

### 5. Comprehension Check / درک مطلب

**الف) چهارگزینه‌ای — ده سؤال**

1. What does a large language model do instead of looking up an answer?
   a) it searches a database of checked facts
   b) it asks a human expert for the answer
   c) it continues a text that it has been given

2. What is tokenization?
   a) cutting text into the small units that the model knows
   b) counting the total number of words in a document
   c) translating a text into the model's first language

3. What does self-attention decide inside a transformer?
   a) how long the final answer is allowed to be
   b) which earlier parts matter for the part being written now
   c) which language the model should answer in

4. Why did Parsa lose the first page of his instructions?
   a) because the model was too small for the task
   b) because he wrote the instructions in Persian
   c) because the text was longer than the context window, so it was truncated

5. What is a prompt injection?
   a) an instruction hidden inside a document that the model is asked to read
   b) a very long prompt that costs too much to process
   c) a second training stage with human comparisons

6. In RLHF, what do the human raters do?
   a) they correct the spelling of the corpus
   b) they compare two answers and say which is better
   c) they write the prompt on behalf of the user

7. What is a hallucination?
   a) an answer that arrives too slowly
   b) an answer written in the wrong language
   c) a fluent answer that is simply not true

8. What is a jailbreak?
   a) a hidden instruction inside a web page
   b) a request that persuades a model to ignore its own rules
   c) a public table that compares many models

9. What does contamination mean in an evaluation?
   a) examples from a test set had already appeared in the training data
   b) a new edition of a document was not indexed
   c) the content filter removed a correct answer

10. What did Hoda's incident show?
   a) that an attacker had changed the dosage table
   b) that the model was too small for the nursing staff
   c) that the retrieval system worked as designed, but the design had no step for old text

**ب) صحیح یا غلط — ده سؤال**

1. An autoregressive model produces one unit at a time. (..........)
2. A greedy choice produces more varied text than sampling does. (..........)
3. Layer normalization keeps the numbers in each layer in a stable range. (..........)
4. Instruction tuning is the first stage of training, before pretraining. (..........)
5. In few-shot mode the prompt contains two or three examples. (..........)
6. A low perplexity proves that a claim in the text is true. (..........)
7. In Hoda's assistant, every answer ended with a snippet and a page number. (..........)
8. BLEU and ROUGE measure meaning directly. (..........)
9. An allowlist tells the system which tools and domains it may use. (..........)
10. In the EU AI Act, the duties of a system depend on its risk. (..........)

**پ) پاسخ کوتاه — شش سؤال**

1. Why is tokenization important for the cost and the limit of a request?
2. What is the difference between a greedy choice, beam search, and nucleus sampling?
3. What is the difference between instruction tuning and RLHF, in the words of the text?
4. Why did the nurses trust the retrieval-augmented assistant?
5. How did the drafter and the verifier divide the work in Hoda's system?
6. Why does a rate limit and a log make a service easier to defend?

**ت) ایدهٔ اصلی — دو سؤال**

۱. ایدهٔ اصلی کل متن کدام جمله است؟

a) A generative model is fluent by design, so its output is useful only when retrieval, checking, logging, and a human decision are built around it.
b) A transformer reads the whole passage at once and uses self-attention to weigh the earlier parts.
c) Parsa lost the first page of his instructions because of the context window.

۲. پاراگراف [25] بیشتر دربارهٔ چه چیزی است؟

a) How a red team attacks a chat assistant before its launch.
b) How law and internal control put duties on the people who deploy a generative system.
c) How a content filter and a toxicity score remove harmful text.

**ث) تطبیق — دو جدول**

**جدول ۱:** هر واژه (۱ تا ۵) را به معنی درست آن (الف تا ه) وصل کنید.

| # | Word | | Meaning |
|---|---|---|---|
| 1 | truncation | الف | a raw score for one possible next unit |
| 2 | logit | ب | cutting off text that is too long to send |
| 3 | rerank | پ | a paragraph that is smooth, well connected, and false |
| 4 | hallucination | ت | a fixed phrase whose meaning is not literal |
| 5 | idiom | ث | sorting the found items a second time, more carefully |

**جدول ۲:** هر واژه (۱ تا ۵) را به معنی درست آن (الف تا ه) وصل کنید.

| # | Word | | Meaning |
|---|---|---|---|
| 1 | exfiltration | الف | moving data out of a system without permission |
| 2 | opt-out | ب | a formal complaint by a person who was harmed |
| 3 | steerability | پ | choosing not to take part in a training set |
| 4 | grievance | ت | how well a model can be guided in one direction |
| 5 | fluency | ث | the quality of sounding natural and smooth |

---

### 6. Vocabulary Practice / تمرین واژگان

**الف) جای خالی — بیست سؤال**

از واژه‌های داخل کادر استفاده کنید. هر واژه یک بار.

> **واژه‌ها:** tokenization · vocabulary · context window · logit · sampling · perplexity · instruction · few-shot · hallucination · retrieval · grounding · chunk · overlap · snippet · holdout · leaderboard · contamination · prompt injection · guardrail · moderation

1. Cutting a sentence into the small units that the model knows is called .......... .
2. The fixed list of all the units that a model knows is its .......... .
3. How much text the model can read at one time is the .......... .
4. For each position the model gives a .......... to every unit in its vocabulary.
5. Choosing the next unit from those scores is called .......... .
6. A .......... score shows how surprised a model is by a text.
7. An .......... tells the model what to do.
8. In .......... mode the prompt contains two or three examples.
9. A fluent answer that is simply not true is a .......... .
10. Finding real documents before answering is called .......... .
11. Tying every answer to a real source is called .......... .
12. Each .......... holds about two paragraphs of a long document.
13. A small .......... between two pieces stops a sentence from being cut in half.
14. The answer listed three .......... with page numbers.
15. A .......... set is never used for training.
16. A public table that compares many systems is a .......... .
17. .......... makes a good score meaningless, because the test data had already been seen.
18. A .......... hides an instruction inside a document that the model is asked to read.
19. A .......... stops a system from doing something harmful.
20. .......... is done by content filters and by people.

**ب) وصل کردن — ده سؤال**

هر واژه را به معنی درست آن وصل کنید.

| # | Word | | Meaning |
|---|---|---|---|
| 1 | drafter | الف | the part that checks the work of another part |
| 2 | verifier | ب | the part that writes the first version |
| 3 | judge | پ | a written list of what a good answer must contain |
| 4 | rubric | ت | a public place where models are compared blind |
| 5 | arena | ث | a person, or a model, that gives a score |
| 6 | red team | ج | a group whose job is to attack the system first |
| 7 | jailbreak | چ | tricking a model into ignoring its own rules |
| 8 | toxicity | ح | harmful and hateful language |
| 9 | impersonation | خ | pretending to be another person |
| 10 | oversight | د | watching that a system is used correctly |

**پ) جمله‌سازی — ده سؤال**

با هر مورد یک جمله بنویسید. موضوع همهٔ جمله‌ها هوش مصنوعی مولد است.

1. autoregressive / sampling
2. beam / top-k (هر دو در یک جمله، با مقایسه)
3. foundation model (با **شرطی نوع سوم**)
4. contamination / leaderboard (جمله‌ای که هشدار بدهد)
5. grounding (جمله‌ای که دلیل اعتماد کاربر را بگوید)
6. prompt injection (با **شرطی نوع سوم**)
7. impersonation / fraud
8. opt-out / royalty
9. دو جمله بنویسید: در یکی *should have* و در دیگری *might have* بیاید. موضوع: ارزیابی خروجی مدل
10. دو جمله بنویسید: یکی با *must* و یکی با *might*. موضوع: content filter

**ت) واژه‌سازی: پیشوند و پسوند — یک تمرین**

پیشوند در **ابتدای** واژه و پسوند در **پایان** واژه می‌آید و معنای آن را تغییر می‌دهد:

| پیشوند / پسوند | معنی | نمونه |
|---|---|---|
| self- | خود | attention ← self-attention |
| meta- | فرا، دربارهٔ خود | data ← metadata |
| out- | بیش از، بهتر از | perform ← outperform |
| under- | کم، ناکافی | fitted ← underfitted |
| -ify | فعل ساختن از صفت یا اسم | simple ← simplify |
| para- | در کنار، فراتر | phrase ← paraphrase |

با افزودن پیشوند یا پسوند درست، واژهٔ مناسب بسازید.

1. attention ← .......... (خودتوجهی)
2. phrase ← .......... (بازنویسی)
3. data ← .......... (فراداده)
4. perform ← .......... (بهتر عمل کردن؛ عملکرد بهتری داشتن)
5. simple ← .......... (ساده‌سازی کردن)
6. fitted ← .......... (کم‌آموز؛ دچار کم‌برازش)

---

### 7. Grammar Focus / نکتهٔ گرامری

**موضوع: شرطی نوع سوم (third conditional)**

**توضیح فارسی:**

شرطی نوع سوم دربارهٔ **گذشتهٔ خیالی** حرف می‌زند: کاری که انجام نشد و نتیجه‌ای که در آن صورت رخ می‌داد. این ساختار در گزارش‌های فنی برای **پشیمانی** و **تحلیل تصمیم‌های گذشته** زیاد به کار می‌آید.

ساختار ثابت است: در بند شرط **if + had + قسمت سوم فعل** (past participle) و در بند نتیجه **would have + قسمت سوم فعل**. مثال: *If the team had logged the requests, they would have found the attack.*

سه نکتهٔ ساختاری: ① شکل کوتاه‌شدهٔ *had* همان *'d* است: *If she'd checked ...*؛ ② **منفی** با *had not / hadn't* در بند شرط و *would not have / wouldn't have* در بند نتیجه ساخته می‌شود؛ ③ برای **سؤال**، *would* به ابتدای جمله می‌آید: *Would you have trusted that answer?*

با فعل‌های وجهی دیگر می‌توان معنا را دقیق‌تر کرد: *could have* «می‌توانست (اما نکرد)»، *might have* «شاید رخ می‌داد»، و *should have* «باید انجام می‌داد (اما نداد)» که لحن نقد دارد.

فرق با **نوع دوم** را ببینید. نوع دوم دربارهٔ حال و آیندهٔ خیالی است: *If the context window were longer, the model would keep the instructions.* نوع سوم دربارهٔ گذشتهٔ خیالی است: *If the context window had been longer, the model would have kept the instructions.* پس برای گذشته نوع سوم و برای حال و آینده نوع دوم را به کار ببرید.

دو خطای رایج فارسی‌زبانان: ① آوردن *would have* در بند شرط ✗ *If they would have logged the requests, they would have found the attack.* ← درست: *If they had logged the requests, ...*؛ ② برگرداندن نوع سوم به زبان حال در فارسی ✗ «اگر ثبت می‌کنند، پیدا می‌کنند» ← درست: «اگر ثبت کرده بودند، پیدا می‌کردند».

**جدول ۱ — فرمول شرطی نوع سوم:**

| بخش جمله | شکل | نمونه |
|---|---|---|
| بند شرط | if + had + past participle | If Hoda had re-indexed the documents, ... |
| بند نتیجه | would have + past participle | ... the wrong number would never have appeared. |
| منفی | if ... had not / ... would not have | If the logs had not been kept, we would not have found the change. |
| سؤالی | Would + فاعل + have + past participle ...? | Would you have trusted that answer? |

**جدول ۲ — وجهی‌ها در بند نتیجه:**

| مورد | شکل | معنی و لحن |
|---|---|---|
| امکان ازدست‌رفته | could have + past participle | می‌توانست (اما انجام نشد) |
| احتمال در گذشته | might have + past participle | شاید رخ می‌داد |
| نقد و پشیمانی | should have + past participle | باید انجام می‌داد (اما نداد) |

**جدول ۳ — مقایسهٔ نوع دوم و سوم:**

| نوع | زمان | ساختار | نمونه |
|---|---|---|---|
| دوم | حال یا آیندهٔ خیالی | if + گذشتهٔ ساده، would + فعل ساده | If the model were smaller, it would answer faster. |
| سوم | گذشتهٔ خیالی | if + had + p.p.، would have + p.p. | If the model had been smaller, it would have answered faster. |
| خطای رایج | آمیختن دو نوع | ✗ If they had logged the requests, they would find the attack. | شکل درست: ... they would have found the attack. |

**پنج مثال از دنیای کامپیوتر:**

1. If the team had re-indexed the documents, the wrong number would never have appeared.
2. If we had logged every request, we would have found the injection in one day.
3. If the prompt had contained two examples, the model would have returned the right format.
4. What would you have done if the verifier had rejected every answer?
5. If I had known the difference between retrieval and a hallucination, I would have written a better report.

**تمرین‌ها — چهل سؤال**

**الف) با شکل درست فعل کامل کنید (۱ تا ۱۴).**

1. If Hoda .......... (re-index) the documents, the old number would not have appeared.
2. If the red team .......... (not find) the attack, the users would have found it.
3. The answer would have been shorter if the instruction .......... (ask) for bullets.
4. If Parsa .......... (keep) his drafts, he could have defended every sentence.
5. If the corpus .......... (contain) more Persian text, the translations would have been better.
6. She would have used a smaller model if the data .......... (not be) private.
7. If they .......... (measure) the worst case, they would have changed the requirement.
8. If the content filter .......... (be) too strict, users would have complained in the first week.
9. We would not have lost the page if the text .......... (fit) in the context window.
10. If the raters .......... (compare) the two answers carefully, the reward signal would have been cleaner.
11. Would the model have refused if the prompt .......... (contain) a hidden instruction?
12. If the team .......... (design) the allowlist first, the exfiltration would not have worked.
13. If she had known about the appeal process, she .......... (open) a grievance.
14. The leaderboard would have made sense if the test set .......... (not be) contaminated.

**ب) جمله را به شکل منفی یا سؤالی بنویسید (۱۵ تا ۲۰).**

15. *(منفی)* The verifier would have caught the wrong number.
16. *(سؤالی)* You would have used a smaller model for this task.
17. *(منفی)* The team would have finished the work in one week.
18. *(سؤالی)* They would have bought the frontier model.
19. *(منفی)* She would have trusted the copied voice.
20. *(سؤالی)* The assistant would have answered in Persian.

**پ) شکل درست را انتخاب و جمله را کامل کنید (۲۱ تا ۲۶).**

21. If the team had logged every request, they .......... (would find / would have found) the attack.
22. If the corpus .......... (contained / had contained) more Persian text, the translation would have been better.
23. She would have noticed the nuance if she .......... (read / had read) the legal text in full.
24. If the model .......... (were / had been) smaller, it would not have answered so fluently.
25. They .......... (would not have deployed / would not deploy) the assistant if the rubric had been stricter.
26. If the red team had been hired earlier, the jailbreak .......... (was found / would have been found) before the launch.

**ت) خطای هر جمله را اصلاح کنید (۲۷ تا ۳۲).**

27. If Hoda would have re-indexed the documents, the number would have been right.
28. If Parsa had kept his drafts, he could defend every sentence.
29. If the team had logged the requests, they would found the attack.
30. If she would known the rule, she would not have submitted the essay.
31. If the test set had not been contaminated, the leaderboard will have made sense.
32. If they had measured the worst case, they had changed the requirement.

**ث) تبدیل و جمله‌سازی (۳۳ تا ۳۶).**

33. این جمله را از شرطی نوع دوم به نوع سوم تبدیل کنید: *If the context window were longer, the model would keep the instructions.*
34. این واقعیت را به گذشتهٔ خیالی تغییر دهید: *The team lost the page, so the answer was wrong.*
35. با *should have* یک جملهٔ انتقادی دربارهٔ یک تصمیم گذشته بسازید.
36. با *might have* یک حدس دربارهٔ گذشته بسازید.

**ج) تمرین آزاد (۳۷ تا ۴۰).**

37. یک جملهٔ شرطی نوع سوم دربارهٔ یک تصمیم اشتباه در یک پروژهٔ واقعی (کار آزمایشگاه، کارگاه یا محل کار خودتان) بنویسید.
38. یک جملهٔ شرطی نوع سوم بنویسید که در آن *could have* آمده باشد.
39. یک جملهٔ شرطی نوع سوم بنویسید که در آن شکل منفی آمده باشد.
40. یک جملهٔ شرطی نوع سوم بنویسید که با این معنا شروع شود: «اگر همه‌چیز را از روز اول ثبت کرده بودیم، ...».

---

### 8. Key Sentences Translation / ترجمهٔ جمله‌های کلیدی

**انگلیسی ← فارسی (۱۰ جمله)**

1. If the team had re-indexed the documents, the wrong number would never have appeared.
2. A hallucination is an answer that is perfectly fluent and completely wrong.
3. Instruction tuning adds pairs of an instruction and a good answer, so the model learns to follow orders.
4. In RLHF, human raters compare two answers and their preference becomes a reward signal.
5. A prompt injection hides an instruction inside a document that the model is asked to read.
6. Every answer ended with a snippet and a page number, and this grounding made the nurses trust it.
7. If the red team had been hired earlier, the jailbreak would have been found before the launch.
8. The content filter removes the most obvious harm before a human being sees it.
9. A vote in an arena builds a leaderboard, but contamination can make a score look perfect for no good reason.
10. If Parsa had kept his drafts, he could have defended every sentence of his essay.

**فارسی ← انگلیسی (۱۰ جمله)**

1. اگر تیم گزارش‌ها را ثبت کرده بود، تزریق دستور را در یک روز پیدا می‌کردند.
2. اگر پنجرهٔ متن بزرگ‌تر بود، مدل دستورالعمل‌ها را فراموش نمی‌کرد.
3. توهم مدل یعنی پاسخی روان که درست نیست.
4. اگر صدای او را شبیه‌سازی کرده بودند، خانواده هم می‌توانست فریب بخورد.
5. اگر متن قانونی را کامل خوانده بود، آن ظرافت معنایی را می‌دید.
6. هر پاسخ با یک بریده و شمارهٔ صفحه تمام می‌شد.
7. اگر مهلت تحویل را از روز اول نوشته بودیم، کار دو هفته زودتر تمام می‌شد.
8. برای مهار خروجی، یک حفاظ روی پاسخ‌ها گذاشتیم.
9. اگر دادهٔ آزمون آلوده نبود، امتیاز آن مدل این‌قدر چشمگیر نمی‌شد.
10. یک داور انسانی هر پاسخ رد‌شده را بازبینی می‌کند.

---

### 9. Writing Task / تمرین نگارش

**موضوع: A Tool I Would Have Used Differently — ابزاری که اگر از نو شروع می‌کردم، طور دیگری استفاده می‌کردم**

یکی از ابزارهای مولد را انتخاب کنید که **خودتان** در تکلیف، پروژه یا کارتان به کار برده‌اید (دستیار چت، ترجمهٔ ماشینی، تولید تصویر، زیرنویس، ابزار پیشنهاد کد) و دربارهٔ آن بنویسید:

- آن ابزار چه کاری را برای شما کوتاه کرد و در چه موقعیتی بود؟
- اگر آن تجربه را از نو شروع می‌کردید، چه کاری را متفاوت انجام می‌دادید؟
- یک اشتباه مشخص را با جزئیات بگویید: نبود منبع، اعتماد به یک عدد، نبود ثبت رویداد، یا نبود بازبینی.
- کدام بخش را این بار به انسان واگذار می‌کردید و چرا؟
- یک جملهٔ محتاطانه بنویسید که محدودیت کار شما را بپذیرد.

**شرایط نگارش:**

- نوشته بین **۲۰۰ تا ۳۰۰ واژه** باشد.
- دست‌کم **۵ جملهٔ شرطی نوع سوم** بنویسید (if + had + p.p.، would have + p.p.).
- دست‌کم **۲ جمله** با *could have* یا *should have* داشته باشد.
- دست‌کم **۲ اصطلاح ربطی** از این فهرست به‌کار ببرید: *however*, *therefore*, *even so*, *as a result*.
- دست‌کم **۸ واژه** از جدول‌های واژگان بخش ۲ استفاده شود.

---

### 10. Mini Project / پروژهٔ کوچک

**انشا (نیمه‌تحقیقی): دستیاری که برای کار خودم می‌سازم**

دستیاری طراحی کنید که **به کار واقعی خودتان** می‌خورد (پاسخ به دانشجوها، جست‌وجو در جزوه‌ها و آیین‌نامه‌های یک دانشکده، پاسخ به مشتریان یک کسب‌وکار کوچک، راهنمای فنی یک کارگاه) و گزارش آن را بنویسید:

- **کاربر و کار:** چه کسی از آن استفاده می‌کند و کدام کار طولانی او را کوتاه می‌کند؟
- **منبع:** پاسخ‌ها باید از کجا بازیابی شوند و چرا بازیابی‌محور بهتر از حافظهٔ خود مدل است؟
- **پاک‌سازی منبع:** سندها را چگونه تکه‌تکه می‌کنید، چه هم‌پوشانی‌ای می‌گذارید و چرا؟
- **شکل دستی:** مسیر کار را روی کاغذ بکشید: پرسش ← بازیابی ← پیش‌نویس‌کننده ← بازبین ← تصمیم انسان. روی هر پیکان یک گام و یک ابزار بنویسید.
- **جدول دستی مقایسه:** جدولی با چهار سطر بکشید و دو گزینه را مقایسه کنید: یک مدل کوچک با وزن‌های باز در برابر یک مدل پیشرو — در چهار مورد: هزینه، حریم خصوصی، کیفیت پاسخ، سرعت.
- **خطرها:** یک تزریق دستور ممکن، یک راه جعل هویت، و یک مورد توهم مدل را نام ببرید و برای هر کدام یک حفاظ بنویسید.
- **جمله‌های گرامری:** پنج جملهٔ شرطی نوع سوم دربارهٔ تصمیم‌های همین طراحی بنویسید.

**شرایط نگارش:**

- گزارش را **دست‌نویس روی کاغذ** بنویسید و در **جلسهٔ بعد** به مدرس تحویل دهید.
- دست‌کم **۲۵۰ واژه** باشد.
- دست‌کم **۵ جملهٔ شرطی نوع سوم** و **۲ جمله** با *could have* یا *might have* داشته باشد.
- طرح دستی و جدول دستی مقایسه در گزارش باشد.
- دست‌کم **۱۲ واژه** از جدول‌های واژگان بخش ۲ در گزارش به‌کار رفته باشد.

**واژه‌های یاری‌دهنده:** retrieval · chunking · grounding · snippet · context window · instruction · hallucination · confidence score · drafter · verifier · prompt injection · guardrail · oversight · human review

---

### 11. Did You Know? / آیا می‌دانستید؟

1. **The transformer was introduced in a 2017 paper whose title was "Attention Is All You Need", and the same design is still the base of modern language models.**
   ترنسفورمر در مقاله‌ای در سال ۲۰۱۷ با عنوان «تنها چیزی که لازم دارید توجه است» معرفی شد و همان طراحی هنوز پایهٔ مدل‌های زبانی امروزی است.

2. **Counting text in tokens is not the same as counting words: in English, one token is roughly four characters, and a dense page is about five hundred tokens.**
   شمردن متن با توکن با شمردن واژه‌ها یکی نیست: در انگلیسی یک توکن تقریباً چهار نویسه است و یک صفحهٔ پرمتن حدود پانصد توکن می‌شود.

3. **Industry reports in 2023 and 2024 describe language models with hundreds of billions of parameters, while the first well-known model of 2018 reported about a hundred million.**
   گزارش‌های صنعت در ۲۰۲۳ و ۲۰۲۴ از مدل‌های زبانی با صدها میلیارد پارامتر سخن می‌گویند، در حالی که نخستین مدل شناخته‌شده در سال ۲۰۱۸ حدود صد میلیون پارامتر گزارش کرده بود.

4. **Training with human comparisons became popular after a 2017 paper on learning from human preferences, and this method is now part of the standard pipeline.**
   آموزش با مقایسه‌های انسانی پس از مقاله‌ای در سال ۲۰۱۷ دربارهٔ یادگیری از ترجیح‌های انسان رایج شد و امروز بخشی از مسیر استاندارد تولید مدل است.

5. **Retrieval-augmented generation was described in 2020, and industry surveys in 2023 reported that many teams had adopted it as their first defence against invented answers.**
   تولید بازیابی‌محور در سال ۲۰۲۰ معرفی شد و بررسی‌های صنعتی در ۲۰۲۳ گزارش کردند که بسیاری از تیم‌ها آن را نخستین دفاع خود در برابر پاسخ‌های ساختگی کرده‌اند.

6. **Prompt injection was described in 2022 as a new kind of attack, and it is still listed among the top risks of systems that read documents on the user's behalf.**
   تزریق دستور در سال ۲۰۲۲ به‌عنوان گونه‌ای تازه از حمله معرفی شد و هنوز در فهرست بزرگ‌ترین خطرهای سامانه‌هایی است که به‌جای کاربر سند می‌خوانند.

7. **In 2023, the United States Copyright Office stated that material produced only by a machine cannot be protected by copyright, which left the human contribution as the deciding factor.**
   در سال ۲۰۲۳، ادارهٔ حق تکثیر ایالات متحده اعلام کرد اثری که تنها یک ماشین تولید کرده باشد نمی‌تواند مشمول حق تکثیر شود؛ پس سهم انسانی عامل تعیین‌کننده ماند.

8. **The European Union agreed its AI Act in 2024, and the duties it places on a system depend on the level of risk, not on the size of the model.**
   اتحادیهٔ اروپا قانون هوش مصنوعی خود را در ۲۰۲۴ تصویب کرد و وظایفی که این قانون بر یک سامانه می‌گذارد به سطح خطر آن بستگی دارد، نه به اندازهٔ مدل.
