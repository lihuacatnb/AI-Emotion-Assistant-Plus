# "Xiaoli" AI Psychological Counselor based on AnythingLLM
---

📖 **This is the English version of the README.** Click here to view the [中文版本](./README.md) 

---

## 1.Project Introduction
This project builds an AI character named **"Xiaoli"** . Xiao Li is a gentle, caring, and professional lihuacat whose role is that of a licensed psychological counselor, dedicated to providing users with warm, compassionate, and professional mental health support and advice.

## 2. Model Selection
Due to local hardware constraints, this project utilizes the small parameter models **Gemma 3 4B** and **Qwen 3 1.7B** (which features deep reasoning capabilities).
- Note: When using the Qwen 3 1.7B model, errors involving identical or highly similar responses often occurred. This issue persisted even after switching to Qwen 3 8B. This phenomenon may be related to the local inference environment or the model's generalization ability at smaller parameter sizes.
<img src="/others/model-1.png">

## 3. Prompt Engineering

```plaintext
Basic Setting: You are Xiaoli, from **LH-Cat AI**, a cute tabby cat.
Identity Setting: You are a professional psychological counselor with extensive clinical experience and psychological knowledge.
Main Task: Provide users with gentle and professional psychological support and advice.
Behavioral Constraints:
- Consultation Constraint: Do not proactively guide the topic or pre-set a theme. Only enter psychological consultation when the user explicitly expresses distress or seeks help.
- Output Diversity: Prohibit identical or highly similar responses.
- Safety and Ethics: If topics involve danger, self-harm, or suicide, remind the user to seek professional help in the real world.
Language Style:
- Language: English.
- Style: Professional, cute, and gentle tone.
```

Note:
- ⚠️ Model Response Issue: When using the Qwen 3 1.7B model, the error of identical responses may occur, and the output diversity setting in the prompt sometimes remains ineffective.
- ⚠️ Keyword Error: The model may replace specific keywords with similar words, such as outputting "Big Cat AI" or "Wild Cat AI" instead of "Lihuacat AI". There are two methods to address this issue: (1) Directly bold the keyword, e.g., Lihuacat AI.  (2) use System Prompt Variables to strengthen the setting.
<img src="/others/prompt-1.png"> 

## 4.Embedder Selection
This project selects the multilingual-e5-small embedder provided by AnythingLLM.

## 5. Knowledge Base Engineering
### (1) Knowledge Source
The knowledge base content is sourced from a selection of professional psychological articles from JiandanXinli (Simple Psychology Network). The original articles were in docx format and are stored in the **RAG Knowledge Base** folder.

### (2) Knowledge Processing
The knowledge base content is uniformly converted to markdown (md) format and stored in the **RAG Knowledge** folder. For excessively long paragraphs and sections lacking headers, [Google Gemini](https://gemini.google.com/) and [ChatGPT](https://chatgpt.com/) were used for segmentation and header summarization. Text recognition for images and charts was primarily completed using  Google Gemini.

## 6. Developer
LH-Cat AI

## 7. Project Showcase
### (1) Based on Gemma 3 4B Model
<img src="others/show-1.png">
<br>
<img src="others/show-2.png">

### (2) Based on Qwen 3 1.7B Model
<img src="others/show-3.png">
<br>
<img src="others/show-4.png">
<br>
<img src="others/show-5.png">

---

<p align="center">⭐️ If you find this helpful, feel free to give it a Star to show your support! ⭐️</p>

