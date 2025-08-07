🛡️ Feature Extraction Based Ensemble Stacking for Combating Cyber Threat in Phishing URLs
🕵️ Project Overview
Phishing-website-detection:
Phishing attacks are the practice of sending fraudulent communications that appear to come from a reputable source. Phishing URLs mainly target individuals and/or organizations through social engineering attacks by exploiting the humans' weaknesses in information security awareness.

Phishing costs Internet users billions of dollars per year. It refers to luring techniques used by identity thieves to fish for personal information in a pond of unsuspecting Internet users. Phishers use spoofed email and phishing software to steal personal information and financial account details such as usernames and passwords.

The experiments were carried out on a dataset that originally contained 1,056,937 labeled URLs (phishing and legitimate). We consider various data mining algorithms for evaluation of the features in order to get a better understanding of the structure of URLs that spread phishing.

📚 Introduction to NLP
Natural Language Processing (NLP) makes it possible for computers to understand the human language. NLP analyzes the grammatical structure of sentences and the individual meaning of words, then uses algorithms to extract meaning and deliver outputs.

With NLP, machines can make sense of written or spoken text and perform tasks like translation, keyword extraction, topic classification, and more.

⚙️ NLP Pipeline
✨ NLP Contains Three Steps:
Preprocessing

Vectorization

Model Selection

🧹 NLP Preprocessing Techniques
Expand Contractions

Lower Case

Remove Punctuations

Remove Words and Digits Containing Digits

Remove Stopwords

Rephrase Text

Stemming and Lemmatization

Remove White Spaces

🔢 NLP Vectorization Techniques
Count Vectorizer

TF-IDF

Word2Vec

GloVe

FastText

📊 Dataset
The train and test datasets were provided individually.

Train Dataset: 100,860 rows with URL information and its property (legitimate or not)

Test Dataset: 25,220 rows without labels

Natural language preprocessing techniques like tokenization were applied to the dataset.

🧼 Dataset Preprocessing
The dataset consists of URLs used to detect whether a given URL is malicious or legitimate.
Certain special characters (e.g., @, *, $, :, |, _, ') appear more frequently in phishing URLs and are used as key distinguishing features. Phish-hinted words may also be present in the base URL or path.

Special characters such as //, /, -, and . were replaced with a space (' ') during preprocessing.

Note: Stemming and Lemmatization were not used for this dataset, as they would change the context and return false results.

📐 Vectorization Techniques
Machines cannot identify text data directly. To train models, the text must be converted into vector form using vectorization techniques.

TF-IDF
TF-IDF (Term Frequency–Inverse Document Frequency) reflects how important a word is in a document. This generates a sparse matrix, which is then used to train models like Naive Bayes.

Count Vectorizer
CountVectorizer breaks down text into words by preprocessing—like converting to lowercase and removing special characters.

🧠 Training Dataset Models
Naive Bayes
This is a generative learning model based on Bayes Theorem and assumes feature independence. It’s simple, scalable, and well-suited for large datasets.

Random Forest
A classification algorithm that builds a group of decision trees at the training level. This ensemble method helps reduce overfitting seen in individual decision trees.

🧪 Testing Dataset
The URLs from the test dataset are predicted using the trained Naive Bayes model through a deployed web interface.

🌐 Model Deployment
Model deployment is done using Flask to host the trained model on a web browser.

📈 Results
The evaluation metric used is Matthews Correlation Coefficient.

Vectorization	Model	Accuracy
CountVectorizer	Naive Bayes	98%
CountVectorizer	Random Forest	86%
TF-IDF	Naive Bayes	98.1%

🧾 Conclusion
After training the dataset with Naive Bayes, Perceptrons, and Random Forest, the highest accuracy was achieved with Naive Bayes.

To provide security for individuals’ sensitive information, everyone must be able to distinguish between legitimate and phishing URLs. This project serves as an effective practice for building that understanding.
