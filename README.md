# RAG

### RAG Paper Assistant chatbot
- RAG를 활용한 논문 QA assistant chatbot [(코드 링크)](demo/chatbot/RAG_paper_assistant_chatbot.ipynb)

![image](https://github.com/user-attachments/assets/7528bca6-204b-4def-8fcd-46601e2ed78b)

- 진행 내용  
  | 항목           | 내용                                                                 |
  |----------------|----------------------------------------------------------------------|
  | **Chunking**   | RecursiveCharacterTextSplitter 사용 <br>(chunksize=750, chunk_overlap=50, separator = ["\n\n"]) |
  | **VectorDB**   | FAISS                                                                |
  | **Chain**      | - type : ConversationalRetrievalChain / RetrievalQA<br>- 대화 저장을 위해 ConversationalRetrievalChain 사용(4개까지 지정) |
  | **비고**       | streamlit 통한 웹 제작                                                |


- 추후 진행 사항
  - 개인 계정의 GPT 토큰 활용해 서비스 사용 가능하도록 추가 예정 (진행중)
  - 이미지 및 표 활용해 RAG 진행 고도화
