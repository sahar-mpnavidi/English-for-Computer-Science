# Lesson 17: Machine Learning and Deep Learning

## Level: B2–C1
## Time: 90–120 minutes

> **درس ۱۷ — یادگیری ماشین و یادگیری عمیق**
> **نکتهٔ گرامری:** شرطی نوع دوم (second conditional) · if + گذشتهٔ ساده، would + فعل ساده · برای موقعیت‌های خیالی
> **متن درس:** ۳۱۰۷ واژه (۳۳ پاراگراف) | **واژگان کلیدی:** ۱۱۹ واژه | **باند سطح:** B2–C1 (پیشرفته)

---

### 1. Lesson Objectives / اهداف درس

- تفاوت سامانهٔ قاعده‌محور با سامانهٔ یادگیرنده را به انگلیسی توضیح دهید و سه خانوادهٔ اصلی یادگیری را نام ببرید.
- مراحل آماده‌سازی داده (مقدار گمشده، دادهٔ پرت، ناترازی، مهندسی ویژگی) را با واژگان دقیق بیان کنید.
- دربارهٔ آموزش یک مدل، نرخ یادگیری، ابرپارامترها و توقف زودهنگام گفت‌وگو کنید.
- تفاوت همگرایی و وگرایی، فلات و بهینهٔ محلی را تشخیص دهید و دربارهٔ آن‌ها تحلیل بنویسید.
- با شرطی نوع دوم دربارهٔ موقعیت‌های خیالی و پیشنهادهای فرضی در پروژه‌های هوش مصنوعی بنویسید.
- دربارهٔ مسئولیت حرفه‌ای، تفسیرپذیری مدل و رد حسابرسی موضع خود را با لحن محتاطانه بیان کنید.

---

### 2. Key Vocabulary / واژگان کلیدی

> تلفظ‌ها بر پایهٔ انگلیسی آمریکایی و در قالب IPA نوشته شده‌اند.

**جدول ۱ — داده و مفاهیم پایه (Data and Core Ideas)**

| فارسی | تلفظ | Definition (EN) | Example (EN) | English |
|---|---|---|---|---|
| نیمه‌بانظارت | /ˌsemi səˈpɜːrvaɪzd/<br>سِمی سِروایزد | Using a few labelled examples and many unlabelled ones. | A semi-supervised model labelled the rest of the images. | semi-supervised |
| خودبانظارت | /ˌself səˈpɜːrvaɪzd/<br>سِلف سِروایزد | Learning from the data's own structure, with no human labels. | Self-supervised models learn from raw text. | self-supervised |
| واقعیت مبنا | /ˈɡraʊnd truːθ/<br>گراونْد تروث | The true, checked answer used for comparison. | The ground truth came from two senior doctors. | ground truth |
| برچسب کلاس | /klæs ˈleɪbl/<br>کلَس لِیبُل | The name of the group that an example belongs to. | The class label was either "urgent" or "routine". | class label |
| برچسب‌گذاری | /ˈleɪbəlɪŋ/<br>لِیبِلینگ | The work of adding the correct answer to each example. | Labelling took three weeks of careful work. | labeling |
| جمع‌سپاری | /ˈkraʊdsɔːrsɪŋ/<br>کراودسورسینگ | Asking a large group of people to do a small task. | They used crowdsourcing for the easy labels. | crowdsourcing |
| جدولی | /ˈtæbjələr/<br>تَبْیولار | Arranged in rows and columns. | Clinic records are mostly tabular data. | tabular |
| متنی | /ˈtekstʃuəl/<br>تِکستشوال | Made of words, not numbers. | Textual data needs different cleaning. | textual |
| سری زمانی | /ˈtaɪm sɪriːz/<br>تایم سیریز | Numbers recorded in a fixed time order. | A time series of heart rates is hard to model. | time series |
| چندوجهی | /ˌmʌltiˈmoʊdəl/<br>مالتی‌مودال | Using more than one kind of data together. | A multimodal model reads images and notes. | multimodal |
| دادهٔ ساختگی | /sɪnˈθetɪk ˈdeɪtə/<br>سین‌ثِتیک دِیتا | Data that a program creates, not real records. | We added synthetic data for the rare cases. | synthetic data |
| دادهٔ شبیه‌سازی‌شده | /ˈsɪmjəleɪtɪd ˈdeɪtə/<br>سیمیولِیتِد دِیتا | Data produced by a model of the real world. | Simulated data tested the pipeline before the launch. | simulated data |
| مقدار گمشده | /ˈmɪsɪŋ ˈvæljuː/<br>میسینگ وَلْیو | A cell in the table with no value in it. | Every table had missing values in two columns. | missing value |
| جانشینی مقدار | /ˌɪmpjuˈteɪʃn/<br>ایمپیوتِیشِن | Replacing a missing value with a reasonable one. | Imputation with the median kept the column usable. | imputation |
| دادهٔ پرت | /ˈaʊtlaɪər/<br>آوتلایِر | A value that is very far from the others. | One outlier was a typing mistake, not a patient. | outlier |
| ناترازی | /ɪmˈbæləns/<br>ایمبَلَنس | A situation where one group is much smaller. | The imbalance between the two classes was severe. | imbalance |
| بازنمونه‌گیری | /ˌriːˈsæmplɪŋ/<br>ری‌سَمپلینگ | Taking the samples again in a different way. | Resampling gave every class the same weight. | resampling |
| حذف تکراری‌ها | /ˌdiːˈdjuːplɪkeɪt/<br>دی‌دیوپلیکِیت | To remove records that appear more than once. | Deduplicate the records before you split them. | deduplicate |
| تنُک | /spɑːrs/<br>اسپارس | Containing very few useful values. | One-hot columns are sparse and very wide. | sparse |
| چگال | /dens/<br>دِنس | Containing values everywhere, with few zeros. | A dense matrix needs much more memory. | dense |
| بُعد (تعداد ویژگی) | /dɪˌmenʃəˈnæləti/<br>دایمِنشِنَلِتی | The number of features in a dataset. | High dimensionality makes distance meaningless. | dimensionality |
| مهندسی ویژگی | /ˈfiːtʃər ˌendʒɪˈnɪrɪŋ/<br>فیچِر اِنجینیرینگ | Designing better inputs for the model by hand. | Feature engineering took longer than training. | feature engineering |
| یک‌داغ | /ˈwʌn hɑːt/<br>وان هات | Coding one category as one position that is on. | City names became one-hot columns. | one-hot |
| توزیع | /ˌdɪstrɪˈbjuːʃn/<br>دیستریبوشِن | The way values spread over their range. | The distribution of age was not symmetric. | distribution |
| واریانس | /ˈveriəns/<br>وِرِیَنس | A number that shows how far values spread. | A large variance means unstable readings. | variance |
| انحراف معیار | /ˈstændərd ˌdiːviˈeɪʃn/<br>استَندِرد دیویِیشِن | The usual distance of a value from the average. | One standard deviation covered most patients. | standard deviation |
| میانه | /ˈmiːdiən/<br>میدِیَن | The middle value when the values are ordered. | The median is safer than the mean here. | median |
| همبستگی | /ˌkɔːrəˈleɪʃn/<br>کورِلِیشِن | A measured link between two sets of numbers. | The correlation between the two tests was weak. | correlation |
| علیت | /kɔːˈzeɪʃn/<br>کازِیشِن | One thing truly causing another. | Correlation is not causation, as every course repeats. | causation |
| کاذب | /ˈspjʊriəs/<br>اسپیوریَس | A link that looks real but has no meaning. | A spurious link appeared between two random columns. | spurious |

**جدول ۲ — آموزش مدل (Training a Model)**

| فارسی | تلفظ | Definition (EN) | Example (EN) | English |
|---|---|---|---|---|
| دور آموزش | /ˈepək/<br>اِپاک | One complete pass over the whole training set. | The model stopped improving after forty epochs. | epoch |
| گرادیان | /ˈɡreɪdiənt/<br>گرِیدیِنت | The direction and size of the steepest change. | The gradient was tiny, so the step was small. | gradient |
| گرادیان کاهشی | /ˈɡreɪdiənt dɪˈsent/<br>گرِیدیِنت دیسِنت | A method that steps downhill to reduce the error. | Gradient descent needs a careful learning rate. | gradient descent |
| انتشار رو به عقب | /ˌbækprɑːpəˈɡeɪʃn/<br>بَک‌پرُپِگِیشِن | Sending the error backwards to update every weight. | Backpropagation is the engine of deep learning. | backpropagation |
| تابع فعال‌سازی | /ˌæktɪˈveɪʃn/<br>اَکتیوِیشِن | A function that decides what a unit passes on. | Without an activation function the model stays linear. | activation |
| نرخ یادگیری | /ˈlɜːrnɪŋ reɪt/<br>لِرنینگ رِیت | How large each training step is. | A high learning rate made the loss jump around. | learning rate |
| ابرپارامتر | /ˌhaɪpərpəˈræmɪtər/<br>هایپِرپَرَمیتِر | A setting that the developer chooses, not the model. | The learning rate is a hyperparameter we choose. | hyperparameter |
| اندازهٔ دسته | /bætʃ saɪz/<br>بَچ سایز | How many examples are used in one step. | A batch size of 64 fitted into the memory. | batch size |
| دستهٔ کوچک | /ˈmɪni bætʃ/<br>مینی بَچ | A small group of examples used in one step. | Mini-batches made training much faster. | mini-batch |
| درهم‌آمیزی | /ˈʃʌfl/<br>شَفل | To mix the order of the examples. | Shuffle the rows before every epoch. | shuffle |
| همگرا شدن | /kənˈvɜːrdʒ/<br>کُنوِرج | To move closer and closer to a stable answer. | The model converged after two hours. | converge |
| همگرایی | /kənˈvɜːrdʒəns/<br>کُنوِرجِنس | The state of having reached a stable answer. | Slow convergence often means a bad scale. | convergence |
| وگرا شدن | /daɪˈvɜːrdʒ/<br>دایوِرج | To move further away and become unstable. | The loss diverged when the rate was too high. | diverge |
| فلات | /plæˈtoʊ/<br>پلاتو | A long period with no improvement. | The metric hit a plateau for ten epochs. | plateau |
| بهینه | /ˈɑːptɪməm/<br>آپتیمُم | The best value that a method can reach. | A local optimum is not always the best answer. | optimum |
| تابع هدف | /əbˈdʒektɪv/<br>آبجِکتیو | The quantity that training tries to reduce. | The objective mixed accuracy with cost. | objective |
| جریمه | /ˈpenəlti/<br>پِنَلتی | An extra cost added to punish complexity. | A small penalty kept the weights modest. | penalty |
| تنظیم‌سازی | /ˌreɡjələrəˈzeɪʃn/<br>رِگولَرِیزِیشِن | A method that stops a model from memorising noise. | Regularization gave a worse training score. | regularization |
| حذف تصادفی | /ˈdrɑːpaʊt/<br>دراپ‌اوت | Randomly ignoring units during training. | Dropout made the network more dependable. | dropout |
| توقف زودهنگام | /ˈɜːrli ˈstɑːpɪŋ/<br>اِرلی استاپینگ | Stopping training when validation stops improving. | Early stopping saved four hours of computing. | early stopping |
| ایستگاه ذخیره | /ˈtʃekpɔɪnt/<br>چِک‌پوینت | A saved copy of the model during training. | The checkpoint from epoch 30 gave the best score. | checkpoint |
| وارسی سریع | /ˈsænəti tʃek/<br>سَنیتی چِک | A quick, simple test of an obvious case. | A sanity check on ten rows caught a bug at once. | sanity check |
| پیش‌آموزش‌دیده | /ˌpriːˈtreɪnd/<br>پری‌ترِیند | Already trained on a large amount of data. | A pretrained model learned our small dataset quickly. | pretrained |
| یادگیری انتقالی | /ˈtrænsfɜːr ˈlɜːrnɪŋ/<br>ترَنسفِر لِرنینگ | Using knowledge from one task in another task. | Transfer learning saved us a month of work. | transfer learning |
| میزان‌سازی | /ˈtuːnɪŋ/<br>تونینگ | Trying different settings to find better results. | Tuning gave a small but real improvement. | tuning |
| فضای جست‌وجو | /sɜːrtʃ speɪs/<br>سِرچ اسپِیس | All the settings that a search may try. | The search space was too large for one week. | search space |
| جست‌وجوی تصادفی | /ˈrændəm sɜːrtʃ/<br>رَندُم سِرچ | Trying settings at random instead of in order. | Random search found a good rate in an hour. | random search |
| مقدار دانه | /siːd ˈvæljuː/<br>سید وَلْیو | The starting number that makes random results repeat. | The same seed value produced the same score. | seed value |
| بازتولید کردن | /ˌriːprəˈduːs/<br>ری‌پرُدیوس | To get the same result again. | We could not reproduce the published numbers. | reproduce |
| بازتولیدپذیری | /ˌriːprəˌduːsəˈbɪləti/<br>ری‌پرُدیوسَبِلیتی | The ability to get the same result again. | Reproducibility is a quality of good research. | reproducibility |
| کاست‌آزمایی | /æbˈleɪʃn/<br>اَب‌لِیشِن | Removing one part to see what it contributes. | An ablation showed that two features did nothing. | ablation |

**جدول ۳ — معماری‌ها و روش‌ها (Architectures and Methods)**

| فارسی | تلفظ | Definition (EN) | Example (EN) | English |
|---|---|---|---|---|
| پرسپترون | /pərˈseptrɑːn/<br>پِرسِپترون | A very simple unit that learns a line. | The first perceptron could not solve every problem. | perceptron |
| کانولوشنی | /ˌkɑːnvəˈluːʃənl/<br>کانوِلوشِنال | Using filters that slide over an image. | A convolutional layer found the edges first. | convolutional |
| کانولوشن | /ˌkɑːnvəˈluːʃn/<br>کانوِلوشِن | The operation of checking a small filter across a grid. | Convolution repeats one small filter everywhere. | convolution |
| تجمیع | /ˈpuːlɪŋ/<br>پولینگ | Reducing a region of a feature map to one value. | Pooling halved the size of the map. | pooling |
| هسته | /ˈkɜːrnl/<br>کِرنِل | The small filter that detects one kind of pattern. | One kernel looked for horizontal edges. | kernel |
| گام | /straɪd/<br>اس‌تراید | How far the filter moves at each step. | A stride of two skipped every other pixel. | stride |
| بازگشتی | /rɪˈkɜːrənt/<br>ریکِرِنت | Reusing an output as an input for the next step. | A recurrent network reads a sequence in order. | recurrent |
| توجه | /əˈtenʃn/<br>اَتِنشِن | A method that lets a model weigh important parts. | Attention helped the model to follow long sentences. | attention |
| درخت تصمیم | /dɪˈsɪʒn triː/<br>دیسیژِن تری | A model that asks a series of simple questions. | The decision tree was easy to explain to the manager. | decision tree |
| شکاف | /splɪt/<br>اسپلیت | A question inside a tree that divides the data. | The first split used the age of the patient. | split |
| برگ | /liːf/<br>لیف | The final node of a tree, which gives the answer. | Each leaf held a small group of examples. | leaf |
| ناخالصی | /ɪmˈpjʊrəti/<br>ایمپیورِتی | How mixed the groups inside a node are. | Low impurity means that the node is almost pure. | impurity |
| آنتروپی | /ˈentrəpi/<br>اِنتِروپی | A measure of disorder inside a group. | Entropy decided which question to ask first. | entropy |
| بهرهٔ اطلاعاتی | /ˌɪnfərˈmeɪʃn ɡeɪn/<br>اینفورمِیشِن گِین | How much a question reduces the disorder. | The lift column showed the information gain. | information gain |
| جنگل تصادفی | /ˈrændəm ˈfɔːrɪst/<br>رَندُم فورِست | Many trees trained on different parts of the data. | A random forest beat the single tree easily. | random forest |
| ترکیبی | /ɑːnˈsɑːmbl/<br>آن‌سامبُل | A model made of several models working together. | The ensemble was stronger than every member. | ensemble |
| تقویت‌سازی | /ˈbuːstɪŋ/<br>بوس‌تینگ | Training new models to correct earlier mistakes. | Boosting pushed the accuracy above ninety percent. | boosting |
| ماتریس درهم‌ریختگی | /kənˈfjuːʒn ˈmeɪtrɪks/<br>کُنفیوژِن مِیتریکس | A table of correct and wrong answers by group. | The confusion matrix showed where the model failed. | confusion matrix |
| مثبت کاذب | /fɔːls ˈpɑːzətɪv/<br>فُلس پازِتیو | A warning that turns out to be wrong. | Every false positive meant one worried patient. | false positive |
| منفی کاذب | /fɔːls ˈneɡətɪv/<br>فُلس نِگَتیو | A real case that the model missed. | A false negative is the most expensive error here. | false negative |
| نرخ خطا | /ˈerər reɪt/<br>اِرِر رِیت | The share of examples that were labelled wrongly. | The error rate dropped to four percent. | error rate |
| لایه‌بندی‌شده | /ˈstrætɪfaɪd/<br>اس‌ترَتیفایْد | Divided so that every group keeps its share. | A stratified split kept both classes in each part. | stratified |
| باقیمانده | /rɪˈzɪdʒuəl/<br>رِزیجوال | What is left after the model's answer is removed. | The residuals grew in very old patients. | residual |
| ابتکاری | /hjuˈrɪstɪk/<br>هیوریستیک | A practical rule that usually works. | We used a heuristic before the model was ready. | heuristic |
| قاعده‌محور | /ˈruːl bæst/<br>رول بِیست | Built from written rules, without learning. | The old rule-based system needed weekly edits. | rule-based |
| نمادین | /sɪmˈbɑːlɪk/<br>سیمبَالیک | Working with symbols and logic, not numbers. | Symbolic systems are still used in some proofs. | symbolic |
| احتمالاتی | /ˌprɑːbəbəˈlɪstɪk/<br>پرابَبِلِستیک | Based on probabilities, not certain answers. | A probabilistic model gives a range of answers. | probabilistic |
| غیرخطی | /ˌnɑːnˈlɪniər/<br>نان‌لینیَر | Not a straight-line relationship. | A nonlinear boundary separated the two groups. | nonlinear |

**جدول ۴ — ارزیابی، استقرار و مسئولیت (Evaluation, Deployment, and Responsibility)**

| فارسی | تلفظ | Definition (EN) | Example (EN) | English |
|---|---|---|---|---|
| رانش (داده) | /drɪft/<br>دریفت | A slow change that moves data away from training. | Drift appeared two months after the launch. | drift |
| تغییر توزیع | /ˌdɪstrɪˈbjuːʃn ʃɪft/<br>دیستریبوشِن شیفت | When the input distribution changes over time. | A distribution shift broke a working model. | distribution shift |
| تغییر دامنه | /doʊˈmeɪn ʃɪft/<br>دومِین شیفت | When the model is used in a different setting. | Domain shift happens when a model moves to a new hospital. | domain shift |
| بازآموزی کردن | /ˌriːˈtreɪn/<br>ری‌ترِین | To train the model again on newer data. | They retrain the model every three months. | retrain |
| بازآموزی | /ˌriːˈtreɪnɪŋ/<br>ری‌ترِینینگ | The process of training a model again. | Retraining is a routine task, not an emergency. | retraining |
| خط لوله | /ˈpaɪplaɪn/<br>پایپ‌لاین | A chain of steps from raw data to a result. | The pipeline cleans, trains, and tests in order. | pipeline |
| مصنوع | /ˈɑːrtɪfækt/<br>آرتِفَکت | Any file that a training run produces. | Every artifact is stored with its own version. | artifact |
| دفتر ثبت | /ˈredʒɪstri/<br>رِجیستری | A place where models and their versions are listed. | The registry held six versions of one model. | registry |
| منشأ | /ˈprɑːvənəns/<br>پراوِنَنس | The history of where data and models came from. | Provenance told us which clinic sent each file. | provenance |
| تبار داده | /ˈlɪniɪdʒ/<br>لینیِج | The full line of steps that produced a value. | Data lineage answered the auditor's question. | lineage |
| سرو کردن مدل | /ˈsɜːrvɪŋ/<br>سِرْوینگ | Running a model so that users can call it. | Serving one model cost less than the training. | serving |
| سایه‌ای | /ˈʃædoʊ/<br>شَدو | Copying live traffic to a new model with no effect. | A shadow model collected data for six weeks. | shadow |
| قناری | /kəˈneri/<br>کَنِری | Giving the new version to a very small group first. | A canary release caught the bug on day one. | canary |
| شتاب‌دهنده | /əkˈseləreɪtər/<br>اَکسِلِرِیتِر | Special hardware that makes training much faster. | One accelerator cut the training time to a day. | accelerator |
| واحد پردازش گرافیکی | /ˌdʒiː piː ˈjuː/<br>جی‌پی‌یو | A chip built for many small calculations at once. | Training on a GPU is the normal choice today. | GPU |
| واحد پردازش تنسور | /ˌtiː piː ˈjuː/<br>تی‌پی‌یو | A chip designed inside a company for machine learning. | A TPU is built for one kind of calculation. | TPU |
| کوانتیزه‌سازی | /ˌkwɑːntəˈzeɪʃn/<br>کوانتِیزِیشِن | Storing numbers with fewer bits to save memory. | Quantization made the model small enough for a phone. | quantization |
| هرس | /ˈpruːnɪŋ/<br>پروینینگ | Removing parts of a network that add little. | Pruning removed half of the units safely. | pruning |
| تقطیر دانش | /dɪˈstɪleɪʃn/<br>دیس‌تیلِیشِن | Training a small model to copy a large one. | Distillation kept the accuracy with a smaller model. | distillation |
| تفسیرپذیری | /ɪnˌtɜːrprətəˈbɪləti/<br>این‌تِرپرِتِبِلیتی | How well a person can understand a model's reasons. | Interpretability mattered more than one extra point. | interpretability |
| رد حسابرسی | /ˈɔːdɪt treɪl/<br>اُدیت ترِیل | A written record of who did what and when. | The audit trail showed who changed the threshold. | audit trail |
| انسان در چرخه | /ˈhjuːmən ɪn ðə luːp/<br>هیومن این دِ لوپ | Keeping a person in the decision process. | A human in the loop reviewed every urgent case. | human in the loop |
| ارزیابی اثر | /ˈɪmpækt əˈsesmənt/<br>ایمپَکت اَسِسمِنت | A study of what a system may change for people. | The impact assessment took two months. | impact assessment |
| کارت مدل | /ˈmɑːdəl kɑːrd/<br>مادِل کارد | A short document that describes a model's limits. | The model card lists the data and the known risks. | model card |
| تخاصمی | /ˌædvərˈseriəl/<br>اَدوِرسِریال | Designed to fool a model on purpose. | An adversarial image fooled the classifier. | adversarial |
| حریف | /ˈædvərseri/<br>اَدوِرسِری | A person or program that attacks the model. | The adversary only needed to change a few pixels. | adversary |
| آشفتگی کوچک | /ˌpɜːrtərˈbeɪʃn/<br>پِرتُربِیشِن | A tiny change that is invisible to a person. | A small perturbation changed the whole answer. | perturbation |
| آلوده‌سازی داده | /ˈpɔɪzənɪŋ/<br>پویزِنینگ | Putting bad examples into the training data. | Data poisoning is hard to see in a huge dataset. | data poisoning |
| عضویت | /ˈmembərʃɪp/<br>مِمبِرشیپ | Whether one person's record was in the training set. | A membership test can leak private information. | membership |
| واترمارک | /ˈwɔːtərmɑːrk/<br>واتِرمارک | A hidden mark that shows where data came from. | A watermark helps a company to prove ownership. | watermark |

---

### 3. Reading / متن اصلی

**عنوان متن: Learning from Examples (یادگیری از نمونه‌ها)**

**[1]** Most software follows instructions that a person has written in advance. A machine-learning system works differently: it receives a large number of examples and works out the rules by itself. This difference sounds small, but it changes how we build, test, and trust software. A rule-based program can be read line by line and corrected; a learned model cannot be read in the same way. Sahar, a master's student, noticed this on the first day of her project, when her supervisor asked her a simple question: why does your model say "urgent" for this patient?

**[2]** The first family of methods is supervised learning, and it needs answers. Every example carries a class label, and the label is the answer that the model must learn to predict. In a clinic, that label may be "urgent", "routine", or "needs a second test". The checked answer, the ground truth, comes from people who know the subject, and the quality of the whole project depends on the quality of that answer.

**[3]** The second family is unsupervised learning, which receives data with no labels at all. Here the model looks for structure: it may group similar records together, or it may reduce a wide table to a few useful numbers. Nobody tells the model what the groups mean; a human being reads the result and decides whether it is interesting.

**[4]** The third family is reinforcement learning. An agent takes an action inside an environment and receives a reward, and it slowly learns which actions bring more reward. One full attempt is called an episode. The hard part is the balance between exploration, which means trying something new, and exploitation, which means using what already works.

**[5]** Between these families there are hybrids. A semi-supervised project uses a small set of labeled examples and a very large set of unlabeled ones, which is the normal situation in a hospital or a factory. A self-supervised model creates its own tasks from the raw data: it hides a word in a sentence and learns to restore it. These ideas reduced the cost of labeling enormously, and they are now used in almost every large system.

**[6]** The shape of the data decides the method. Tabular data lives in rows and columns, like an accounting sheet or a clinic record. Textual data is made of words and needs its own cleaning. A time series records the same measurement again and again in a fixed order, such as the heart rate of one patient every hour. Multimodal systems read more than one kind of data at the same time: an image, a note, and a number together. When real records are rare or private, teams sometimes add synthetic data that a program creates, or simulated data that comes from a model of the real world.

**[7]** Sahar's dataset came from a clinic in her city, and it had forty columns and about nine thousand rows. The first problem was that many cells were empty. A missing value is not a zero, and treating it as a zero would have changed the meaning of the column. She used imputation: she replaced each missing number with the median of that column, because the median is less sensitive to extreme numbers than the mean is. For two text columns she used a clear value such as "unknown", so that the absence of information stayed visible. Two visits from the same patient had also been entered twice, and she had to deduplicate the rows before she counted anything.

**[8]** The second problem was an outlier. One row described a patient of two hundred and ten years, which is a typing mistake and not a medical miracle. She found it by looking at the distribution, and she corrected it with the clinic. An outlier that stays in the data teaches the model something false, and a model that has learned something false will repeat it for years. The easy labels could be collected from a large group of people, a method called crowdsourcing, but a medical label must come from someone who treats patients.

**[9]** The third problem was imbalance. Of nine thousand records, only three hundred carried the class label "urgent", so the two groups were very different in size. If a lazy model called every patient routine, it would reach ninety-seven percent accuracy and still be useless in the clinic. She used resampling: she took the urgent cases again and again, and she also gave the two classes different weights. She kept the original class proportions while she was testing by using a stratified split, so that every part of the data held the same small share of urgent cases.

**[10]** Before training, she had to organize the columns, and this work is called feature engineering. A city name is textual, and a model needs numbers, so she turned each city into a one-hot column. One-hot columns are sparse, because almost every row holds a zero, while a full table of numbers is dense and needs more memory. She also combined two columns into one ratio, and this one decision improved her result more than any change of model. Dimensionality, the number of features, grew quickly: with three hundred columns, the distance between two records becomes almost meaningless, because in a wide space every pair of points is far apart.

**[11]** She also spent two days on statistics. She plotted the distribution of every number and wrote down its median, its variance, and its standard deviation. She standardized the columns that had very different ranges, so that one column measured in thousands would not dominate another measured in tenths. She noticed a strong correlation between two test results and had to remind herself that correlation is not causation. A spurious correlation is more dangerous still, because it looks convincing and a model will use it happily.

**[12]** Then came the training itself. The idea of gradient descent is simple: the objective measures how wrong the model is, the gradient shows the direction of the steepest increase, and the algorithm takes a small step in the opposite direction. The size of that step is the learning rate, and it is the first hyperparameter that every beginner should understand. One complete pass over the training set is an epoch, and the number of examples in one step is the batch size. When the table is large, the work is done in mini-batches, and the rows are mixed by a shuffle before every epoch, so that the model does not learn the order of the file instead of the pattern in the data.

**[13]** A deep network adds one more idea: backpropagation. After the model produces an answer, the error travels backwards through the network and updates every weight a little. Between the layers there is an activation function: if there were no such function, a deep network would be no stronger than a single straight line, because a chain of linear steps is still linear.

**[14]** Training can end in three different ways. If the objective falls steadily, the model converges, and we call that movement convergence. If the learning rate is too high, the numbers grow without limit and the model diverges. If the curve is flat, the model has reached a plateau, and more training will not help. Reaching an optimum does not mean that the problem is solved: a local optimum is only the best answer in its own small region, and a penalty term on complexity changes which optimum the model prefers.

**[15]** Regularization is the general name for the methods that stop a model from memorising noise. Dropout ignores a random part of the network during training, so that no single unit becomes too important. Early stopping watches the validation score, and if that score stopped improving, the run would end there. A checkpoint saves the model as it grows, so that the best version is never lost.

**[16]** Overfitting is the failure that every one of these methods is fighting. A model that has memorised its training set looks perfect during training and fails on a new patient. Cross-validation is the standard defence: the data is cut into several parts, each part becomes the test in turn, and the average score is reported. Sahar's first model had memorised the record number, which was a column with no medical value at all, and her cross-validation score collapsed when she removed it. She then plotted the residuals, which grew in the oldest patients and pointed to one narrow age group. A single sanity check on ten familiar rows would have shown the first problem in five minutes.

**[17]** Deep learning is not always necessary. On a table with nine thousand rows and forty columns, a decision tree is often strong enough, and it is much easier to explain. A tree asks a series of questions; each question is a split, each end point is a leaf, and the tree chooses its questions by looking at impurity. Two common measures of disorder are entropy and information gain, which says how much a question reduces that disorder. Many trees together form a random forest, which is an ensemble, and boosting builds new trees that correct the mistakes of the older ones. A simple random forest was Sahar's baseline, and it took her an afternoon; the deep model that later beat it took three weeks.

**[18]** The idea of learning from data is old. A perceptron, built in the middle of the twentieth century, was one simple unit that learned a straight line, and the first neural networks were chains of these units. Before those networks, most systems were symbolic: they worked with logic and symbols instead of numbers, and a simple heuristic, a hand-written rule that usually worked, was often enough in practice. The field moved slowly for decades, then computing power and data caught up with the theory.

**[19]** Convolutional networks changed image work. A convolution repeats one small filter across the whole image, so the same pattern is found everywhere, and this single idea saves a huge number of parameters. The filter itself is called a kernel, and the distance it moves at each step is the stride. A pooling step then reduces each small region to one value.

**[20]** Recurrent networks were designed for sequences. A recurrent unit reads an input, keeps a summary of what it has seen, and passes that summary to the next step, which makes it a natural choice for a time series or for a sentence. Attention later improved this idea by letting the model weigh the important parts of a long input instead of squeezing everything into one summary. An autoencoder, which is trained to rebuild its own input, is a useful tool for finding unusual records: a row that the network cannot rebuild is worth a second look.

**[21]** Measuring the result is a separate skill. A confusion matrix shows the four possible outcomes, and from it we can read the false positives, which are false alarms, and the false negatives, which are the real cases that were missed. The error rate is only one number, and it can hide a disaster: in a screening test, a false negative is far more expensive than a false positive, so a team that optimises only the error rate can produce a model that nobody dares to use.

**[22]** Choosing a number to improve is a decision, not a detail. A probabilistic model can help here, because it gives a range of answers instead of one confident label, and a well-chosen cutoff turns a probability into a decision. The cutoff, not the model, is often what changes a project from a danger into a tool. Even so, a learned boundary between two groups is not proof of anything: it is a nonlinear or linear approximation of the evidence that the team happened to collect.

**[23]** Sahar's classmate, Ali, worked on the operational side of the same clinic, and his problems were different. His job was to turn a research notebook into a pipeline: a chain of steps that cleans the data, trains the model, tests it, and saves the result. Every file that a run produces is an artifact, and each version of each model is listed in a registry, so that the team can find the exact model that made a decision last March. Provenance and data lineage answer a harder question: where did this row come from, and which clinic sent it? Ali also demanded reproducibility, which means that a colleague with the same data and the same seed value must get the same score. He learned that determinism is impossible in a large system, because parallel code and different hardware change the order of the additions, so he wrote a note about the tolerance instead of promising an exact result.

**[24]** Ali could not reproduce one result from a paper, and the reason was simple: a random seed was never reported. Even a pseudo-random sequence needs a starting point, so he fixed the seed value in the configuration file, wrote it in the documentation, and asked everyone to reproduce the run before believing it. When a result could not be reproduced, he ran an ablation: he removed one part of the model and measured what changed.

**[25]** The hyperparameters of a project are chosen, not learned. The learning rate, the batch size, and the number of layers are typical examples, and the set of possible settings is the search space. Nobody can search that space by hand, so teams use random search, which is often better than a careful grid, and they spend a fixed budget on tuning instead of an unlimited one. Sometimes the better answer is not to start from zero: a pretrained model has already learned general patterns from a large dataset, and transfer learning adapts those patterns to a new task with a small dataset. When researchers describe how they did this, they report a full methodology, step by step, so that readers can check the claim.

**[26]** A model that works in a notebook must still be served to users, and serving changes the requirements. The team cares about how fast a request is answered and how much one answer costs. A shadow deployment copies live traffic to the new model without letting it decide anything, and a canary release gives the new version to a very small group first. Both ideas exist for one reason: a model that is wrong for a thousand users is a serious problem, and a model that is wrong for five users is a normal Monday.

**[27]** Hardware is part of the answer. A GPU was designed for graphics, but its talent for doing thousands of small multiplications at once makes it the standard choice for training, and an accelerator or a TPU is built for the same purpose. When a model must run on a phone, two techniques help: quantization stores each number with fewer bits, and pruning removes the units that add little. Distillation goes further and trains a small model to copy the behaviour of a large one. Energy is the reason all three exist: training a big network has a real cost in electricity, and a smaller model that answers well is a better engineering decision, not only a cheaper one.

**[28]** The world does not stay still, and neither does the data. Drift is any slow change that moves the records away from the training set. A distribution shift can follow a new machine, a new form, or a new season, and a domain shift appears when the model is used somewhere new, such as a second hospital with different habits. Ali's first warning came from a simple dashboard: the share of "urgent" answers fell to zero in one week. The cure was not a new model but retraining: the team retrained the model on the last six months of data and added a monitor that repeats the check every morning.

**[29]** Security and privacy close the circle. An adversary does not need to steal the model to harm it. An adversarial example is an input with a small perturbation that a person cannot see, and it can move an answer to the other side. Data poisoning attacks the other end: a few wrong examples in the training set can teach a rule that only the attacker likes. Membership tests try to work out whether one person's record was in the training data, and a watermark can prove which dataset was used.

**[30]** People who build these systems have decisions to explain, and interpretability is the ability to give an honest reason. Sahar kept a decision tree beside her neural network, because the tree could show the first three questions and the manager could follow them. An audit trail recorded who changed the cutoff and when. An impact assessment is a study of who may be helped or hurt by the system, and a model card is a short document that lists the data, the score, and the known limits. The strongest design that Ali saw in ten years was also the simplest: a human in the loop for every urgent case.

**[31]** By the end of the term, Sahar's model was not the most advanced one in the class, but it was the one that a doctor could question. If she chose a bigger network, she would gain one point and lose the conversation. If she spent two more weeks on tuning, the improvement would be real but small. If the clinic asked her for a perfect score, she would answer that no honest project promises one.

**[32]** Ali's hardest week was different. If the second clinic used the same equipment, the model would work without a change. Because the equipment was new, the readings were slightly different, and a model that had been right for a year started to answer "routine" for urgent cases. If the team did not keep an audit trail, they would search for the reason for a month. Instead they found it in two hours, retrained, and wrote the story into the runbook.

**[33]** So what should a student take from all of this? Learn the data before you learn the model. Keep a simple baseline, because it will tell you whether your clever idea is worth anything. Write down the seed value, the version, and the exact split that you used. Measure the cost of each kind of mistake, not only the average. If you are asked for a perfect system, explain the two places where your system is weak, and sleep well. If a model is going to decide something about a person, keep a human in the loop: a good system does not show how clever it is; it shows how honestly it fails.

*(۳۱۰۷ واژه — ۳۳ پاراگراف)*

---

### 4. Persian Translation / ترجمه فارسی

**الف) واژه‌های دشوار و معادل آن‌ها**

| واژه / عبارت | معادل پیشنهادی | نکتهٔ ترجمه |
|---|---|---|
| ground truth | واقعیت مبنا | ترجمهٔ تحت‌اللفظی «حقیقت زمینی» نادرست است؛ منظور پاسخی است که مرجع انسانی تأیید کرده است. |
| class label | برچسب کلاس | «کلاس» را به «دسته» هم می‌توان ترجمه کرد؛ در متن‌های یادگیری ماشین «برچسب کلاس» رایج‌تر است. |
| feature | ویژگی | در آمار «متغیر» هم پذیرفته است؛ «فیچر» نوشته نمی‌شود. |
| label vs. level | برچسب در برابر سطح | این دو را در ترجمه اشتباه نگیرید: label برچسب پاسخ است و level سطح یک متغیر. |
| imputation | جانشینی مقدار | نه «جایگزینی» به‌تنهایی؛ مفهوم دقیق، پر کردن آگاهانهٔ سلول خالی با مقدار برآوردی است. |
| outlier | دادهٔ پرت | «دادهٔ خارج از محدوده» طولانی است؛ در گزارش فنی «دادهٔ پرت» یا «مقدار پرت» بنویسید. |
| spurious correlation | همبستگی کاذب | «کاذب» الزامی است؛ «همبستگی دروغین» در متن دانشگاهی به کار نمی‌رود. |
| imbalance | ناترازی | در آمار «عدم توازن طبقات» هم درست است؛ «بی‌تعادلی» غیررسمی است. |
| plateau | فلات | «سکون» هم پذیرفته است؛ منظور دوره‌ای است که معیار بهتر نمی‌شود. |
| divergence | واگرایی | مقابل convergence «همگرایی»؛ فعل آن «وگرا شدن» است. |
| regularization | تنظیم‌سازی | در برخی متن‌ها «منظم‌سازی»؛ در این درس یک واژه را به‌کار ببرید و ثابت بمانید. |
| dropout | حذف تصادفی | نام این روش در متن‌های فارسی غالباً «دراپ‌اوت» نوشته می‌شود؛ توضیح فارسی آن «حذف تصادفی واحدها» است. |
| ablation | کاست‌آزمایی | معادل دقیق‌تری برای «برداشتن یک بخش برای سنجش اثر آن» وجود ندارد؛ «حذف‌آزمایی» هم رایج شده است. |
| provenance | منشأ داده | با lineage «تبار داده» فرق دارد: منشأ می‌گوید داده از کجا آمده و تبار می‌گوید از چه مسیری گذشته است. |
| canary release | انتشار قناری | اگر مخاطب با اصطلاح آشنا نیست، در پرانتز توضیح بدهید: «انتشار آزمایشی برای گروهی کوچک». |
| shadow deployment | استقرار سایه‌ای | «سایه» ترجمهٔ استعاری است، نه بخشی از دستگاه؛ همین شکل در صنعت رایج است. |
| interpretability | تفسیرپذیری | با explainability «توضیح‌پذیری» یکی نیست: تفسیرپذیری دربارهٔ سازوکار درونی مدل است. |
| quantization | کوانتیزه‌سازی | «چندسطحی‌کردن» پیشنهاد شده است، اما در نوشتار فنی «کوانتیزه‌سازی» شناخته‌شده‌تر است. |
| sanity check | وارسی سریع | ترجمهٔ «بررسی سلامت» فقط برای دستگاه به‌کار می‌رود؛ اینجا آزمون سادهٔ یک حالت روشن است. |

**ب) نکات ترجمه**

۱. **«آموزش» در برابر «تمرین»:** فعل *train* را برای مدل «آموزش دادن» ترجمه کنید و *practice* را «تمرین کردن». نوشتن «تمرین مدل» در متن تخصصی ابهام ایجاد می‌کند.
۲. **گروه‌های اسمی بلند را بشکنید:** عبارت‌هایی مانند *class-imbalance resampling strategy* را نباید پشت‌سرهم ترجمه کرد؛ در فارسی بنویسید: «راهبرد بازنمونه‌گیری برای ناترازی طبقات».
۳. **مجهول انگلیسی، فاعل‌نمای فارسی:** جملهٔ *the model was trained on nine thousand records* بهتر است «مدل با ۹٬۰۰۰ رکورد آموزش داده شده است» ترجمه شود؛ حذف فاعل و آوردن «توسط» جمله را ثقیل می‌کند.
۴. **ترتیب صفت و اسم:** در انگلیسی صفت پیش از اسم می‌آید (*deep learning*، *pretrained model*)؛ در فارسی معادل‌های ترکیبی جاافتاده‌اند و نباید واژه‌به‌واژه ساخته شوند («یادگیری عمیق»، «مدل پیش‌آموزش‌دیده»).
۵. **افعال مصطلح را حفظ کنید:** *run an ablation* یعنی «کاست‌آزمایی انجام دادن»، نه «دویدن»؛ *serve a model* یعنی «مدل را در دسترس کاربران گذاشتن»، نه «خدمت کردن».
۶. **معیار در برابر متریک:** *metric* را «معیار» ترجمه کنید و *measure* را «سنجه» یا «اندازه»؛ به‌کار بردن یک واژه برای هر دو، مقایسه را نامفهوم می‌کند.
۷. **حرف اضافه‌ها را جابه‌جا نکنید:** *trained on data* یعنی «آموزش‌دیده با داده» و *trained for a task* یعنی «آموزش‌دیده برای یک وظیفه»؛ «آموزش روی وظیفه» غلط رایجی است.
۸. **از ترجمهٔ تحت‌اللفظی این ترکیب‌ها بپرهیزید:** *local optimum* ← «بهینهٔ محلی» (نه «مطلوب محلی»)، *error rate* ← «نرخ خطا» (نه «آهنگ خطا»)، *human in the loop* ← «انسان درون چرخهٔ تصمیم» (نه «انسان در حلقه»).

---

### 5. Comprehension Check / درک مطلب

**الف) چهارگزینه‌ای — ده سؤال**

1. What does a machine-learning system do that a rule-based program does not?
   a) it reads every line of code by hand
   b) it works out the rules from the examples that it receives
   c) it never needs any data at all

2. What does a semi-supervised project use?
   a) only examples that carry a checked answer
   b) only unlabeled data and no labels at all
   c) a small set of labeled examples and a very large set of unlabeled ones

3. Why did Sahar use the median for imputation?
   a) because it is less sensitive to extreme values than the mean
   b) because it is faster to type into a spreadsheet
   c) because it removes the whole column from the table

4. Why can a model reach ninety-seven percent accuracy by calling every patient routine?
   a) because the model is very deep
   b) because the urgent group is much smaller than the other group
   c) because the labels were collected by crowdsourcing

5. What is the learning rate?
   a) the number of examples used in one step
   b) the number of complete passes over the data
   c) the size of each training step

6. What happens if the learning rate is too high?
   a) the numbers grow without limit and the model diverges
   b) the model reaches a plateau after two epochs
   c) the model converges in fewer epochs

7. Why is a false negative the most expensive error in a screening test?
   a) because it worries healthy people for a week
   b) because a real case is missed
   c) because it increases the error rate

8. What did Ali need in order to reproduce a published result?
   a) a larger GPU
   b) a completely new dataset
   c) the random seed that the authors used

9. Why did Sahar keep a decision tree beside her neural network?
   a) because the tree was easier to explain to a manager
   b) because the tree was always more accurate
   c) because the tree needed no training data

10. What did Ali's dashboard show in the week of the incident?
   a) that the clinic had bought new accelerators
   b) that the share of "urgent" answers fell to zero
   c) that the model had never been trained

**ب) صحیح یا غلط — ده سؤال**

1. A learned model can be corrected by reading its lines one by one. (..........)
2. A missing value is the same as a zero. (..........)
3. One-hot columns are usually sparse. (..........)
4. A strong correlation between two columns proves that one causes the other. (..........)
5. Mini-batches are used when the table is large. (..........)
6. A local optimum is the best answer in the whole space of answers. (..........)
7. A checkpoint saves the model while it is being trained. (..........)
8. On a table with forty columns, a decision tree is often easier to explain than a deep network. (..........)
9. Pooling is a step that reduces each small region of an image to one value. (..........)
10. Retraining was the cure for the drift that Ali saw. (..........)

**پ) پاسخ کوتاه — شش سؤال**

1. What three problems did Sahar find in her dataset, and how did she treat each of them?
2. Why is a spurious correlation dangerous for a model?
3. Why is a stratified split necessary when the classes are imbalanced?
4. What is the difference between convergence and divergence, in the words of paragraph [14]?
5. What does regularization try to stop, and which three methods are named in paragraph [15]?
6. Why does Ali write a tolerance in his note instead of promising an exact result?

**ت) ایدهٔ اصلی — دو سؤال**

۱. ایدهٔ اصلی کل متن کدام جمله است؟

a) A machine-learning project succeeds when the data is understood before the model is chosen, and when the team keeps a simple baseline, honest numbers, and a human in the loop.
b) A convolutional network repeats one small filter across the whole image and saves a large number of parameters.
c) Ali fixed a broken pipeline by buying a new accelerator for the clinic.

۲. پاراگراف [29] بیشتر دربارهٔ چه چیزی است؟

a) How a pretrained model is adapted to a new task with transfer learning.
b) How quantization and pruning make a model small enough for a phone.
c) How an adversary can attack a model through its inputs and its training data.

**ث) تطبیق — دو جدول**

**جدول ۱:** هر واژه (۱ تا ۵) را به معنی درست آن (الف تا ه) وصل کنید.

| # | Word | | Meaning |
|---|---|---|---|
| 1 | plateau | الف | a value that is very far from the others |
| 2 | outlier | ب | a long period with no improvement |
| 3 | ablation | پ | a tiny change that a person cannot see |
| 4 | perturbation | ت | a practical rule that usually works |
| 5 | heuristic | ث | removing one part to see what it contributes |

**جدول ۲:** هر واژه (۱ تا ۵) را به معنی درست آن (الف تا ه) وصل کنید.

| # | Word | | Meaning |
|---|---|---|---|
| 1 | drift | الف | the full line of steps that produced a value |
| 2 | lineage | ب | a saved copy of the model during training |
| 3 | checkpoint | پ | a slow change that moves data away from training |
| 4 | watermark | ت | a hidden mark that shows where data came from |
| 5 | leaf | ث | the final node of a tree, which gives the answer |

---

### 6. Vocabulary Practice / تمرین واژگان

**الف) جای خالی — بیست سؤال**

از واژه‌های داخل کادر استفاده کنید. هر واژه یک بار.

> **واژه‌ها:** missing value · imputation · outlier · imbalance · resampling · deduplicate · sparse · dense · dimensionality · feature engineering · distribution · correlation · epoch · gradient · learning rate · hyperparameter · mini-batch · plateau · optimum · dropout

1. A cell in the table with no entry in it is a .......... .
2. Replacing an empty cell with the median of its column is called .......... .
3. One row described a patient of two hundred and ten years; it was clearly an .......... .
4. Because only three hundred records were urgent, the dataset suffered from .......... .
5. She used .......... to give the small class more weight in training.
6. You must .......... the rows first, because some visits had been entered twice.
7. A one-hot column is almost all zeros, so it is .......... .
8. A full table of numbers is .......... and needs much more memory.
9. With three hundred features, high .......... makes the distance between rows meaningless.
10. Turning a city name into a number is a small act of .......... .
11. The .......... of age was not symmetric, so the median was safer than the mean.
12. A strong .......... between two tests does not prove that one causes the other.
13. One complete pass over the training set is called an .......... .
14. The .......... shows the direction of the steepest increase in the objective.
15. A high .......... makes the loss jump around instead of falling.
16. The batch size and the number of layers are .......... that the developer chooses.
17. When the table is large, the work is done in .......... .
18. The metric reached a .......... after ten epochs and never improved again.
19. A local .......... is only the best answer in its own small region.
20. .......... ignores a random part of the network during every training step.

**ب) وصل کردن — ده سؤال**

هر واژه را به معنی درست آن وصل کنید.

| # | Word | | Meaning |
|---|---|---|---|
| 1 | converge | الف | to train the model again on newer data |
| 2 | retrain | ب | to remove records that appear more than once |
| 3 | deduplicate | پ | to move closer and closer to a stable answer |
| 4 | shuffle | ت | to get the same result again |
| 5 | reproduce | ث | to mix the order of the examples |
| 6 | crowdsource | ج | to store each number with fewer bits |
| 7 | prune | چ | to change data so that columns share one range |
| 8 | quantize | ح | to remove the parts of a network that add little |
| 9 | standardize | خ | to ask a large group of people to do a small task |
| 10 | canary | د | a small group that tries a new version first |

**پ) جمله‌سازی — ده سؤال**

با هر مورد یک جملهٔ **شرطی نوع دوم** بنویسید. موضوع همهٔ جمله‌ها داده و مدل است.

1. learning rate / converge
2. imbalance / resampling
3. outlier / distribution
4. checkpoint / reproducibility
5. interpretability / decision tree
6. یک ایده را دو بار بنویسید: یک بار با **شرطی نوع اول** (موقعیت واقعی) و یک بار با **شرطی نوع دوم** (موقعیت خیالی). موضوع: *pretrained model*
7. همان کار را برای *drift* انجام دهید.
8. همان کار را برای *quantization* انجام دهید.
9. دو جمله بنویسید که در یکی *could* و در دیگری *might* به کار رفته باشد. موضوع: *transfer learning*
10. یک توصیهٔ محتاطانه در دو جمله بنویسید؛ در یکی *should* و در دیگری *might* بیاید. موضوع: *human in the loop*

**ت) واژه‌سازی: پیشوند و پسوند — یک تمرین**

پیشوند در **ابتدای** واژه و پسوند در **پایان** واژه می‌آید و معنای آن را تغییر می‌دهد:

| پیشوند / پسوند | معنی | نمونه |
|---|---|---|
| semi- | نیمه، ناقص | supervised ← semi-supervised |
| pseudo- | شبه، ظاهری | random ← pseudo-random |
| auto- | خود | encoder ← autoencoder |
| -ology | دانش و مطالعهٔ یک حوزه | method ← methodology |
| -ize | فعل ساختن از اسم یا صفت | standard ← standardize |
| -ism | نام ساختن از فعل یا صفت | determine ← determinism |

با افزودن پیشوند یا پسوند درست، واژهٔ مناسب بسازید.

1. supervised ← .......... (نیمه‌بانظارت)
2. random ← .......... (شبه‌تصادفی)
3. encoder ← .......... (خودرمزگذار)
4. method ← .......... (روش‌شناسی)
5. standard ← .......... (استانداردسازی کردن)
6. determine ← .......... (جبرگرایی؛ قطعیت کامل نتیجه)

---

### 7. Grammar Focus / نکتهٔ گرامری

**موضوع: شرطی نوع دوم (second conditional)**

**توضیح فارسی:**

شرطی نوع دوم دربارهٔ موقعیتی **خیالی** یا **ناممکن** در زمان حال یا آینده حرف می‌زند. گوینده واقعیت را انکار نمی‌کند؛ فقط فرض می‌کند که وضعیت جور دیگری بود و نتیجهٔ آن فرض را می‌گوید.

ساختار ثابت است: در بند شرط، بعد از *if* از **گذشتهٔ ساده** استفاده می‌کنیم و در بند نتیجه **would + فعل ساده** می‌آوریم. پس *If he asked, he would answer.* درست است، نه *If he would ask*.

سه نکتهٔ ساختاری را جدی بگیرید: ① بعد از *if* هیچ‌وقت *would* نمی‌آید؛ ② در این ساختار برای همهٔ اشخاص، *were* رسمی‌تر و رایج‌تر است (*If I were the manager* ...)؛ ③ به‌جای *would* می‌توان *could* (توانستن) یا *might* (شاید) گذاشت تا معنا دقیق‌تر شود.

برای **سؤال**، *would* به ابتدای جمله می‌آید: *Would you trust this model if nobody explained it?* برای **منفی**، *would not* یا *wouldn't* به کار می‌رود: *If she did not standardize the columns, the result would not be stable.*

شرطی نوع دوم با **نوع اول** فرق دارد. نوع اول به شرطی می‌پردازد که واقعاً ممکن است (*If the data is dirty, the model will fail.*) اما نوع دوم وضعیتی است که در واقعیت وجود ندارد (*If the data were clean, the model would converge faster.*). پس اگر از واقعیت حرف می‌زنید نوع اول و اگر در حال فرض‌سازی هستید نوع دوم را انتخاب کنید.

دو خطای رایج فارسی‌زبانان: ① آوردن *would* در بند شرط ✗ *If I would have more data, I would train a better model.* ← درست: *If I had more data, I would train a better model.*؛ ② آمیختن نوع اول و دوم ✗ *If the filter were smaller, it will be faster.* ← درست: *If the filter were smaller, it would be faster.*

**جدول ۱ — فرمول شرطی نوع دوم:**

| بخش جمله | شکل | نمونه |
|---|---|---|
| بند شرط | if + گذشتهٔ ساده | If the dataset had fewer columns, ... |
| بند نتیجه | would + فعل ساده | ... the model would train faster. |
| منفی | if ... did not / ... would not (wouldn't) | If she did not shuffle the rows, the score would not be stable. |
| سؤالی | Would + فاعل + فعل ساده ...? | Would you use the model if nobody explained it? |

**جدول ۲ — were و افعال وجهی در بند نتیجه:**

| مورد | شکل | نمونه |
|---|---|---|
| بودند فرضی | if + were (همهٔ اشخاص) | If I were the manager, I would ask for a cost report. |
| امکان | could + فعل ساده | If we had accelerators, we could search a larger space. |
| احتمال کمتر | might + فعل ساده | If the labels were noisy, the model might learn a spurious link. |

**جدول ۳ — مقایسهٔ شرطی نوع اول و دوم:**

| نوع | شرط | ساختار | معنی |
|---|---|---|---|
| اول | ممکن و واقعی | if + حال ساده، will + فعل ساده | If the data is dirty, the model will fail. |
| دوم | خیالی و ناممکن | if + گذشتهٔ ساده، would + فعل ساده | If the data were clean, the model would converge faster. |
| خطای رایج | آمیختن دو نوع | ✗ If the data were clean, the model will converge. | شکل درست: ... the model would converge. |

**پنج مثال از دنیای کامپیوتر:**

1. If the two classes were balanced, the error rate would be a useful number.
2. If I had more accelerators, I could try a much larger search space.
3. If the seed value were written in the report, another team would reproduce our score.
4. What would you do if the objective diverged after three epochs?
5. If Sahar removed the record number, her model would stop memorising it.

**تمرین‌ها — چهل سؤال**

**الف) با شکل درست فعل کامل کنید (۱ تا ۱۴).**

1. If the learning rate .......... (be) lower, the loss would not jump around.
2. If she .......... (have) more labeled examples, she would try a semi-supervised model.
3. The model would be easier to explain if we .......... (keep) a decision tree beside it.
4. If the column .......... (not contain) an outlier, the mean and the median would be close.
5. They would retrain the model every month if the data .......... (drift) quickly.
6. If I .......... (be) the manager, I would ask for the cost of every false negative.
7. We could serve the model on a phone if we .......... (quantize) the weights.
8. If the pipeline .......... (save) every artifact, the audit trail would be complete.
9. She would not use crowdsourcing if the labels .......... (need) medical knowledge.
10. If Ali .......... (write) the seed value in the report, other teams would reproduce the result.
11. Would the model converge faster if we .......... (shuffle) the rows before every epoch?
12. If the dataset .......... (not be) so imbalanced, accuracy would be a fair metric.
13. If the team .......... (watch) the drift, they would see the change in one week.
14. I would explain the cutoff to the doctor if he .......... (ask) me.

**ب) با شکل منفی یا سؤالی بنویسید (۱۵ تا ۲۰).**

15. *(منفی)* If the data were clean, the model would learn the pattern.
16. *(سؤالی)* You would trust a model with a high error rate.
17. *(منفی)* She would retrain the model every week.
18. *(سؤالی)* They would call a human expert for every urgent case.
19. *(منفی)* We would use a deep network for this small table.
20. *(سؤالی)* The model would still work if the domain shifted.

**پ) شکل درست را انتخاب و جمله را کامل کنید (۲۱ تا ۲۶).**

21. If the table .......... (is / were) wider, the distance between rows would become meaningless.
22. She would be happy if the error rate .......... (drops / dropped) below five percent.
23. If I .......... (was / were) you, I would check the imbalance first.
24. We .......... (will / would) retrain the model if the readings changed.
25. If the kernel .......... (had / has) more parameters, the network would be slower.
26. Would you use the model if nobody .......... (can / could) explain it?

**ت) خطای هر جمله را اصلاح کنید (۲۷ تا ۳۲).**

27. If I would have more time, I would train a deeper model.
28. If the model has more data, it would converge faster.
29. If she was the manager, she would ask for a cost report.
30. If they would fix the seed value, we would reproduce the result.
31. If the dataset did not balanced, we would use resampling.
32. I would tell you if I will know the answer.

**ث) تبدیل و جمله‌سازی (۳۳ تا ۳۶).**

33. این جمله را از شرطی نوع اول به نوع دوم تبدیل کنید: *If the sensor fails, the alarm will ring.*
34. این جمله را از واقعیت به فرض خیالی تغییر دهید: *The dataset is small, so the model overfits.*
35. با واژه‌های *drift* و *retrain* یک جملهٔ شرطی نوع دوم بسازید.
36. با عبارت *human in the loop* یک سؤال شرطی نوع دوم بسازید.

**ج) تمرین آزاد (۳۷ تا ۴۰).**

37. یک جمله بنویسید که با «اگر من مدیر این پروژه بودم» شروع شود و *would* داشته باشد.
38. یک جملهٔ شرطی نوع دوم بنویسید که در آن *could* آمده باشد.
39. یک جملهٔ شرطی نوع دوم بنویسید که در آن *might* آمده باشد.
40. یک توصیهٔ فرضی در دو جمله بنویسید: در جملهٔ اول فرض کنید یک تصمیم پروژه را تغییر داده‌اید و در جملهٔ دوم نتیجهٔ آن را بگویید.

---

### 8. Key Sentences Translation / ترجمهٔ جمله‌های کلیدی

**انگلیسی ← فارسی (۱۰ جمله)**

1. If the two classes were balanced, the error rate would be a useful number.
2. A model that has memorised its training set looks perfect during training and fails on a new patient.
3. If the seed value were written in the report, another team would reproduce our score.
4. The cutoff, not the model, is often what changes a project from a danger into a tool.
5. Nobody tells the model what the groups mean; a human being reads the result and decides whether it is interesting.
6. If a lazy model called every patient routine, it would reach ninety-seven percent accuracy and still be useless.
7. Provenance and data lineage answer a harder question: where did this row come from, and which clinic sent it?
8. Interpretability is the ability to give an honest reason for a decision.
9. She then plotted the residuals, which grew in the oldest patients and pointed to one narrow age group.
10. If the team did not keep an audit trail, they would search for the reason for a month.

**فارسی ← انگلیسی (۱۰ جمله)**

1. اگر داده‌ها پاک بودند، مدل سریع‌تر همگرا می‌شد.
2. اگر من جای تو بودم، اول ناترازی طبقات را بررسی می‌کردم.
3. اگر مقدار دانه ثبت شده بود، نتیجه بازتولید می‌شد.
4. مدلی که دادهٔ آموزشی را حفظ کرده باشد، روی بیمار جدید شکست می‌خورد.
5. اگر نرخ یادگیری کمتر بود، خطا این‌قدر بالا و پایین نمی‌رفت.
6. هیچ‌کس به مدل نمی‌گوید که گروه‌ها چه معنایی دارند.
7. برای اجرای مدل روی گوشی، وزن‌ها را کوانتیزه کردیم.
8. اگر رانش داده را پایش می‌کردند، تغییر را در یک هفته می‌دیدند.
9. تفسیرپذیری از یک امتیاز بیشتر مهم‌تر بود.
10. اگر تیم رد حسابرسی را نگه نمی‌داشت، یک ماه دنبال علت می‌گشت.

---

### 9. Writing Task / تمرین نگارش

**موضوع: A Model That Would Help My City — مدلی که به شهر من کمک می‌کند**

یک کاربرد یادگیری ماشین را انتخاب کنید که **به شهر یا محلهٔ خودتان** کمک می‌کند (پیش‌بینی مصرف برق، تشخیص ترافیک، مدیریت پسماند، تشخیص زودهنگام بیماری در یک مرکز درمانی محلی، پیش‌بینی خرابی تجهیزات یک کارگاه). دربارهٔ آن بنویسید و این موارد را بگنجانید:

- این مدل چه تصمیمی می‌گیرد و **چه کسی** از آن سود می‌برد یا آسیب می‌بیند؟
- داده از کجا می‌آید، و دو مشکل واقعی آن داده چیست؟ (مقدار گمشده، دادهٔ پرت، ناترازی، حریم خصوصی)
- چرا فرض می‌کنید یک روش ساده (درخت تصمیم یا جنگل تصادفی) خط پایهٔ خوبی است؟
- اگر بودجه و زمان کافی داشتید، چه چیز دیگری را امتحان می‌کردید و چه چیزی را عوض نمی‌کردید؟
- یک جملهٔ محتاطانه بنویسید که محدودیت کار را بپذیرد.

**شرایط نگارش:**

- نوشته بین **۲۰۰ تا ۳۰۰ واژه** باشد.
- دست‌کم **۵ جملهٔ شرطی نوع دوم** بنویسید (if + گذشتهٔ ساده، would + فعل ساده).
- دست‌کم **۲ جمله** با *could* یا *might* داشته باشد (لحن محتاطانه).
- دست‌کم **۲ اصطلاح ربطی** از این فهرست به‌کار ببرید: *however*, *therefore*, *even so*, *as a result*.
- دست‌کم **۸ واژه** از جدول‌های واژگان بخش ۲ استفاده شود.

---

### 10. Mini Project / پروژهٔ کوچک

**انشا (نیمه‌تحقیقی): پروژهٔ یادگیری ماشینی که در ذهن دارم**

پروژه‌ای را انتخاب کنید که **خودتان** می‌توانید آن را شروع کنید یا در محل کار یا تحصیل خود با آن روبه‌رو شده‌اید، و گزارش آن را بنویسید:

- **مسئله و معیار:** مدل چه چیزی را پیش‌بینی می‌کند و شما چه عددی را «موفقیت» می‌دانید؟ هزینهٔ مثبت کاذب و منفی کاذب را جداگانه بنویسید.
- **داده:** داده از کجا می‌آید، چند سطر و چند ستون دارد و چه کسی برچسب‌ها را تأیید می‌کند؟
- **پاک‌سازی:** مقداری گمشده، یک دادهٔ پرت و ناترازی طبقات را نام ببرید و بگویید با هر کدام چه می‌کنید.
- **دو روش:** یک روش ساده و یک روش پیچیده‌تر را نام ببرید و بگویید چرا ابتدا روش ساده را می‌آزمایید.
- **شکل دستی:** مسیر کار را از دادهٔ خام تا رسیدن مدل به کاربر روی کاغذ بکشید و روی هر پیکان، یک گام بنویسید.
- **جدول دستی مقایسه:** جدولی با چهار سطر بکشید و دو روش خود را در این چهار مورد مقایسه کنید: دادهٔ لازم، سرعت آموزش، تفسیرپذیری، هزینهٔ اجرا.
- **ریسک:** اگر داده رانش پیدا کند، چه نشانه‌ای اول از همه دیده می‌شود و چه کسی باید آن را ببیند؟ کجای سامانه انسان در چرخهٔ تصمیم می‌ماند؟
- **جمله‌های گرامری:** پنج جملهٔ شرطی نوع دوم بنویسید که هر کدام یک تصمیم پروژه را در حالت فرضی نشان دهد.

**شرایط نگارش:**

- گزارش را **دست‌نویس روی کاغذ** بنویسید و در **جلسهٔ بعد** به مدرس تحویل دهید.
- دست‌کم **۲۵۰ واژه** باشد.
- دست‌کم **۵ جملهٔ شرطی نوع دوم** و **۲ جمله** با *could* یا *might* داشته باشد.
- طرح دستی و جدول دستی مقایسه در گزارش باشد.
- دست‌کم **۱۲ واژه** از جدول‌های واژگان بخش ۲ در گزارش به‌کار رفته باشد.

**واژه‌های یاری‌دهنده:** class label · ground truth · imbalance · imputation · outlier · feature engineering · baseline · learning rate · overfitting · drift · retraining · interpretability · audit trail · human in the loop

---

### 11. Did You Know? / آیا می‌دانستید؟

1. **The term "machine learning" was used in 1959 by Arthur Samuel, who wrote a program that learned to play the game of checkers.**
   اصطلاح «یادگیری ماشین» در سال ۱۹۵۹ توسط آرتور ساموئل به کار رفت؛ او برنامه‌ای نوشت که بازی تخته‌نرد انگلیسی را یاد می‌گرفت.

2. **The first perceptron was built in 1958 in the United States, and it could learn to tell two simple kinds of pictures apart.**
   نخستین پرسپترون در سال ۱۹۵۸ در آمریکا ساخته شد و می‌توانست یاد بگیرد دو نوع تصویر ساده را از هم تشخیص دهد.

3. **Backpropagation became popular in 1986, and the largest networks of today are still trained with the same basic idea.**
   روش انتشار رو به عقب در سال ۱۹۸۶ رایج شد و بزرگ‌ترین شبکه‌های امروز هم با همان ایدهٔ پایه آموزش می‌بینند.

4. **The ImageNet dataset, published in 2009, held more than fourteen million labelled images, and most of them were labelled by hand.**
   مجموعه دادهٔ ImageNet که در سال ۲۰۰۹ منتشر شد بیش از ۱۴ میلیون تصویر برچسب‌خورده داشت و بیشتر آن‌ها با دست برچسب‌گذاری شده بودند.

5. **In the Netflix Prize competition, which ran from 2006 to 2009, teams worked for three years to improve recommendations by about ten percent.**
   در مسابقهٔ جایزهٔ نتفلیکس که از ۲۰۰۶ تا ۲۰۰۹ برگزار شد، تیم‌ها سه سال کار کردند تا پیشنهادها را حدود ۱۰ درصد بهتر کنند.

6. **Graphics chips, designed for games, turned out to be excellent for training machine-learning models, because they do thousands of small multiplications at once.**
   تراشه‌های گرافیکی که برای بازی طراحی شده بودند، برای آموزش مدل‌های یادگیری ماشین بسیار مناسب از آب درآمدند، چون هزاران ضرب کوچک را هم‌زمان انجام می‌دهند.

7. **Gradient descent is older than computing: a similar method for finding a minimum was published in 1847.**
   گرادیان کاهشی از خودِ رایانش قدیمی‌تر است: روشی مشابه برای یافتن کمینه در سال ۱۸۴۷ منتشر شد.

8. **In 2016, a program learned to play the game of Go and beat a top professional player — a game that many experts had expected to stay difficult for machines for another ten years.**
   در سال ۲۰۱۶ برنامه‌ای بازی «گو» را یاد گرفت و یک بازیکن حرفه‌ای سطح بالا را شکست داد؛ بازی‌ای که بسیاری از متخصصان انتظار داشتند تا ده سال دیگر برای ماشین‌ها دشوار بماند.
