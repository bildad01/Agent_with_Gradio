# 🤖 AI 면접관 Agent v1.0

## 📌 프로젝트 개요
이 프로젝트는 이력서를 기반으로 면접 질문을 생성하고, 지원자의 답변을 AI가 평가 및 피드백하는 **AI 면접 시뮬레이터**입니다. GPT-4o-mini와 LangGraph를 활용하여 실전 면접처럼 작동하며, 사용자가 인터랙티브하게 경험할 수 있도록 Gradio 인터페이스를 제공합니다.

---

## 🔧 기술 스택

| 분류              | 사용 기술 |
|-------------------|-----------|
| Programming       | Python |
| LLMs              | OpenAI GPT-4o-mini |
| ML Frameworks     | LangChain, OpenAI API |
| Data Handling     | Pandas, Numpy |
| Vector DB         | Chroma, OpenAI Embeddings |
| File I/O          | PyMuPDF (fitz), python-docx |
| Orchestration     | LangGraph |
| Front-End         | Gradio |
| 기타              | OS, AST, Tempfile 등 |

---

## 🧩 주요 기능

### ✅ 1. 이력서 분석
- PDF 및 DOCX 이력서 텍스트 추출
- 핵심 요약 생성 (GPT 기반)
- 이력서 기반 핵심 키워드 10개 도출

### ✅ 2. 질문 전략 및 질문 생성
- 6개 면접 전략에 따라 총 120개 질문 생성
- 질문 카테고리: 경력 및 경험, 동기, 커뮤니케이션, 논리적 사고, 기술 스택, 장단점
- Chroma 벡터 DB에 질문 저장 및 검색 기반 질문 생성

### ✅ 3. 답변 평가 및 피드백
- 답변에 대해 4가지 항목 평가 (질문 연관성, 구체성, 자기이해도, 두괄식)
- 평가 결과에 따라 재평가 여부 판단 및 수행
- 피드백 저장 및 누적 평가 관리

### ✅ 4. 대화형 인터페이스
- Gradio를 활용한 사용자와 AI 면접관 간의 인터뷰 시뮬레이션
- 대화 형태로 인터뷰 진행 및 실시간 피드백 제공

### ✅ 5. 종합 피드백 리포트
- 인터뷰 종료 시 전략별 요약, 강점 및 약점 제공
- 전체 면접에 대한 종합 평가 메시지 출력

---

## 🚀 실행 방법
```bash
pip install -r requirements.txt
python app.py
```

또는 Colab 환경에서 구글 드라이브 연동 및 requirements.txt 설치 후 `app.py` 실행

---

## 💡 느낀 점
> GPT API와 LangChain, LangGraph를 활용하여 구조화된 면접 루프를 설계하는 데 집중했습니다. 단순한 질문-응답이 아닌, 질문 전략 → 답변 평가 → 재질문 및 피드백 → 종료 조건까지 AI 면접관의 역할을 최대한 반영하고자 했습니다.

---

> 본 프로젝트는 AI 기술을 활용한 면접 연습 도구로, 자기 개발 및 취업 준비에 유용하게 활용될 수 있습니다.
