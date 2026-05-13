# Financial-Sentiment-Analysis
Financial Sentiment Analysis Dataset from kaggle
-Link Dataset https://www.kaggle.com/datasets/ankurzing/sentiment-analysis-for-financial-news\
## 📖 Description
This project focuses on analyzing the sentiment of financial texts or tweets. It classifies the text into three distinct categories:
* **Positive**: Mapped to label `0`
* **Negative**: Mapped to label `1`
* **Neutral**: Mapped to label `2`

## ✨ Key Features
* **Data Preprocessing**: Cleans text data using Regular Expressions (removing special characters and numbers), converts text to lowercase, and removes stop words using the NLTK library.
* **Feature Extraction**: Converts text into numerical vectors using TF-IDF (`TfidfVectorizer`), limited to a maximum of 5,000 features to reduce noise.
* **Handling Class Imbalance**: Addresses the imbalanced dataset issue by applying SMOTE (Synthetic Minority Over-sampling Technique).
* **Machine Learning Models**: Trains and compares the performance of three different models: 
  * Multinomial Naive Bayes
  * Logistic Regression (Hyperparameter tuning via `GridSearchCV` to find the best `C` value)
  * Random Forest Classifier
* **Evaluation & Error Analysis**: Evaluates models using Accuracy, Precision, Recall, F1-score, and Confusion Matrix. It also includes an error analysis section that extracts the top 5 misclassified texts to identify the model's weaknesses.
* **Data Visualization**: Visualizes label distribution using a Pie Chart, displays the Logistic Regression's Confusion Matrix via a Heatmap, and highlights the most frequent words in each class using a Word Cloud.

## 🛠️ Technologies & Tools
* **Language**: Python 3
* **Data Manipulation**: Pandas, NumPy
* **Machine Learning & NLP**: Scikit-learn, Imbalanced-learn (SMOTE), NLTK
* **Data Visualization**: Matplotlib, Seaborn, WordCloud


# Financial Sentiment Analysis

## 📖 รายละเอียดโปรเจกต์ (Description)
โปรเจกต์นี้ใช้สำหรับการวิเคราะห์ความรู้สึก (Sentiment Analysis) จากข้อความหรือทวีตที่เกี่ยวข้องกับการเงิน โดยทำการจำแนกความรู้สึกออกเป็น 3 ระดับ ได้แก่:
* **Positive (เชิงบวก)**: แปลงฉลากข้อมูลเป็น 0
* **Negative (เชิงลบ)**: แปลงฉลากข้อมูลเป็น 1
* **Neutral (เป็นกลาง)**: แปลงฉลากข้อมูลเป็น 2

## ✨ ฟีเจอร์หลัก (Key Features)
* **Data Preprocessing**: การทำความสะอาดข้อมูลข้อความด้วย Regular Expressions (เพื่อลบอักขระพิเศษและตัวเลข), การแปลงเป็นตัวพิมพ์เล็ก และลบคำหยุด (Stop words) ด้วยไลบรารี NLTK
* **Feature Extraction**: แปลงข้อความเป็นตัวเลขเพื่อใช้ในการเทรนโมเดลด้วยวิธี TF-IDF (TfidfVectorizer) โดยจำกัดคำศัพท์สูงสุดไว้ที่ 5,000 คำเพื่อลด Noise
* **Handling Class Imbalance**: จัดการปัญหาข้อมูลแต่ละคลาสไม่สมดุล (Class Imbalance) ด้วยเทคนิค SMOTE (Oversampling)
* **Machine Learning Models**: ทดลองและเปรียบเทียบประสิทธิภาพการทำนายด้วยโมเดล 3 รูปแบบ ได้แก่ Multinomial Naive Bayes, Logistic Regression (หาพารามิเตอร์ C ที่ดีที่สุดด้วย GridSearchCV) และ Random Forest
* **Evaluation & Error Analysis**: ประเมินผลโมเดลด้วย Confusion Matrix, Accuracy, Precision, Recall, F1-score รวมถึงมีการดึงตัวอย่างข้อความที่ทำนายผิด (Misclassifications) 5 ลำดับแรกมาวิเคราะห์จุดอ่อนของโมเดล
* **Data Visualization**: สรุปข้อมูลด้วยกราฟแสดงการกระจายตัวของฉลากข้อมูล (Pie Chart), เมทริกซ์ความสับสน (Confusion Matrix Heatmap) ของโมเดล Logistic Regression และแสดงคำที่พบบ่อยในแต่ละคลาสด้วย Word Cloud

## 🛠️ เครื่องมือและไลบรารีที่ใช้ (Technologies & Tools)
* **ภาษา**: Python 3
* **การจัดการและวิเคราะห์ข้อมูล**: Pandas, NumPy
* **Machine Learning & NLP**: Scikit-learn, Imbalanced-learn (SMOTE), NLTK
* **Data Visualization**: Matplotlib, Seaborn, WordCloud

## 🚀 การติดตั้งและการทดลองใช้งาน (Getting Started)
1. โปรเจกต์นี้ถูกเขียนและรันบน Google Colab
2. การนำเข้าข้อมูลมีการเรียกใช้งานจาก Google Drive (`/content/drive/My Drive/data.csv`) คุณจำเป็นต้องเมานท์ (Mount) Google Drive และเปลี่ยนที่อยู่ไฟล์ให้ตรงกับชุดข้อมูลของคุณ
3. เซลล์ในช่วงแรกจะมีการดาวน์โหลดแพ็กเกจ `stopwords` จากไลบรารี NLTK กรุณารันเพื่อเตรียมความพร้อมสำหรับการทำความสะอาดข้อความ
4. รันโค้ดตามลำดับเซลล์เพื่อดำเนินการตั้งแต่ Data Import, Data Preprocessing, Modeling ไปจนถึง Evaluation
