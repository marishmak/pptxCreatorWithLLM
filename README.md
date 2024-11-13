#Presentation Creator with LLM
Created by Mariia Shmakova

##Goal of project:
The goal of this project is to create a Telegram bot that generates presentations based on course materials (or simply PDF files) and topics for all presentations. The bot will utilize a combination of technologies, including Sentence Transformer to embed database items, Retrieval-Augmented Generation (RAG), and Google Generative AI, to extract relevant information from course materials and generate presentations.

##How it works?
1. start bot
2. extract pdf from bot
3. extract topics from pdf page by page and pull it to db using gemini to summarize and preprocess
4. receive list of topic per course from bot
5. iterate over topics: 
- extract text from db using custom embedding function (Snowflake)
- checking the similarity of files and topics using Squared L2 distance(photo here)
- ask gemini to create code for presentation based on this text
- run code and receive PP presentation
6. pull pptx  presentations to bot
