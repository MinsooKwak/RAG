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

- 선택 사항
  - Model : GPT-3.5 turbo / GPT-4 (streamlit)
  - Chain : RetrievalQA chain / ConversationalRetrieval Chain

- 추후 진행 사항
  - postprocessing 과정으로 RAG 고도화 : reranking 추가 hybrid retrieval test (24.09)
  - 개인 계정의 GPT 토큰 활용해 서비스 사용 가능하도록 추가 예정 (진행중)
  - 이미지 및 표 활용해 RAG 진행 고도화

  ---
- 예시
  
    ![image](https://github.com/user-attachments/assets/346f2809-f883-4933-bb27-0c2542b6779f)


  - 질문 및 답변 (답변 및 참조 문서)
    - User : 이 논문을 요약해줘
    ![image](https://github.com/user-attachments/assets/beada228-4b2d-4434-94c3-4c761b2dbd69)

    - User : LLM as a judge가 뭐야?
    ![image](https://github.com/user-attachments/assets/dcd84e5a-8cae-4672-9de7-d4983e737b69)

    - User : LLM as a judge가 동작하는 방식을 설명해줘.
    ![image](https://github.com/user-attachments/assets/d654eb81-e793-49af-a501-cd064db2ae8a)

