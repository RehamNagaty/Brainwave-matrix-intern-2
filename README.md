# Tweet Sentiment Extraction Project | مشروع استخراج الشعور من التغريدات

## Objective | الهدف
Extract the portion of a tweet (`selected_text`) that reflects the sentiment (`positive`, `negative`, or `neutral`) using Natural Language Processing (NLP) techniques.

استخراج الجزء من التغريدة (selected_text) الذي يعبّر عن الشعور (إيجابي، سلبي، أو محايد) باستخدام تقنيات معالجة اللغة الطبيعية (NLP).

---

## Dataset | مجموعة البيانات
- Source: Tweet Sentiment Extraction competition dataset
- Files: `train.csv`, `test.csv`, `sample_submission.csv`
- Columns: `text`, `sentiment`, `selected_text`

البيانات مأخوذة من مسابقة "Tweet Sentiment Extraction" وتتضمن أعمدة النص والشعور والجزء المعبر عنه.

---

## Preprocessing | المعالجة المبدئية
- Lowercasing
- Removing URLs, mentions, punctuation, and numbers
- Stopword removal
- Lemmatization

- تحويل كل الأحرف إلى أحرف صغيرة  
- إزالة الروابط والإشارات والعلامات  
- إزالة الكلمات الشائعة غير المهمة  
- استخدام Lemmatization للحصول على الجذور الصحيحة

---

## Baseline Modeling | النموذج الأولي
- If sentiment = neutral → return full tweet text
- If selected_text is found in text → return it
- Otherwise → return the first 3 words (as an approximation)

إذا كان الشعور محايدًا نعيد النص كامل إذا وجد الجزء المعبر في النص نعيده وإلا نأخذ أول 3 كلمات.

---

## Evaluation | التقييم
- Metric: **Jaccard Score**
- Average score: ~0.989
- Good predictions: `'I love this'` → `'love this'`
- Bad predictions: `'this is terrible'` → `'this is'`

تم التقييم باستخدام معامل Jaccard وكانت النتائج الأولية ممتازه.

---

## Future Work | العمل المستقبلي
- Fine-tune BERT or similar models for better extraction
- Add EDA and visualizations
- Deploy as a web app using Streamlit

تحسين النموذج باستخدام BERT أو غيره - إضافة مخططات تحليلية - وإمكانية نشر المشروع كتطبيق.

---

## Author

Reham Nagaty  


[LinkedIn](linkedin.com/in/reham-mohamed-nagaty/)

