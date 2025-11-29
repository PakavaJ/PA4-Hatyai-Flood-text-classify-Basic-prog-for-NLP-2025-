<img width="1823" height="852" alt="image" src="https://github.com/user-attachments/assets/3bd66752-403a-4665-9cc8-444bc362db07" />

# ระบบคัดกรองข้อความขอความช่วยเหลือน้ำท่วมหาดใหญ่ด้วย AI

### Project Overview
ในช่วงวิกฤตอุทกภัย ข้อมูลขอความช่วยเหลือบนโซเชียลมีเดียมักมีลักษณะเป็น **Unstructured Data** ที่กระจัดกระจายและมีปริมาณมหาศาล ทำให้การคัดกรองและจัดลำดับความสำคัญ เป็นไปได้ยาก ประกอบกับเป็นโอกาสดีที่ผมได้มีโอกาสเรียน programming ในรายวิชา basic prog for NLP เลยตัดสินใจที่จะนำองค์ความรู้มาบูรณาการและช่วยเหลือผู้คน
โปรเจกต์นี้จึงนำเทคโนโลยี **Large Language Models (LLMs)** มาประยุกต์ใช้เพื่อพัฒนาระบบ **Automated Information Extraction** ที่สามารถเปลี่ยนข้อความดิบให้กลายเป็นข้อมูลที่มีโครงสร้าง (Structured Data) พร้อมประเมินระดับความวิกฤตและสนับสนุนการตัดสินใจของทีมกู้ภัยได้อย่างแม่นยำและทันท่วงที

### Key Features
* สามารถแยกแยะเคสขอความช่วยเหลือหลายรายการจากข้อความเดียว
* ใช้ AI ประเมินบริบทความเร่งด่วน (1-10) โดยวิเคราะห์จาก Keyword และ Sentiment ของผู้ประสบภัย
* ตรวจจับกลุ่มเปราะบาง (ผู้ป่วยติดเตียง, เด็ก, ผู้สูงอายุ) เพื่อการจัดลำดับความสำคัญสูงสุด

### Tech Stack
* **Core Engine:** Python
* **LLM:** Google Gemini API (Model: gemini-1.5-flash)
* **Web Framework:** Streamlit
* **Data Manipulation:** Pandas
* **Visualization:** Altair

โปรเจกต์นี้ใช้เทคนิค **Prompt Engineering** ในการควบคุม Output ของ LLM ให้ตอบกลับมาในรูปแบบ **JSON Structure** ที่เข้มงวด เพื่อลด Hallucination และทำให้ข้อมูลสามารถนำไปประมวลผลต่อใน Dataframe ได้ทันที โดยมีการทำ Data Cleaning และ Normalization ภาษาไทยเพื่อให้เหมาะสมกับการนำเสนอ

---
เป็นส่วนหนึ่งของการบ้าน PA4 รายวิชา Basic prog for NLP 2025
