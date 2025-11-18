# AI_Poet_App.md

## 📝 AI 시인 Streamlit 애플리케이션 분석

이 문서는 사용자가 제공한 **`app.py`** (Streamlit 애플리케이션 코드)와 **`requirements.txt`** (필요 패키지 목록) 파일의 내용을 정리하고 분석한 것입니다.

---

### 1. 💻 `app.py` (인공지능 시인 코드)

이 파이썬 스크립트는 **Streamlit**을 프론트엔드로, **LangChain**을 LLM 연동 프레임워크로 사용하여 OpenAI의 `gpt-4o-mini` 모델을 통해 시를 작성하는 웹 애플리케이션을 구현합니다.

### **주요 기능**

- **웹 인터페이스**: `st.title`과 `st.text_input` 등을 사용하여 "인공지능 시인"이라는 제목의 간단한 사용자 환경(UI)을 구성합니다.
- **API 키 입력**: 사이드바 (`st.sidebar`)에서 사용자에게 **OpenAI API Key**를 입력받고, 성공 또는 경고 메시지를 표시합니다.
    - 입력된 키는 `os.environ['OPENAI_API_KEY']`를 통해 환경 변수에 설정됩니다.
- **LangChain 체인**:
    - **모델**: `gpt-4o-mini` 모델을 사용하도록 초기화됩니다.
    - **프롬프트**: 시스템 메시지로는 "You are a helpful assistant that writes beautiful Korean poetry."가 설정되어 한국어 시를 작성하도록 지시합니다.
    - **구성**: `ChatPromptTemplate` → `llm` → `StrOutputParser`의 순서로 체인 (`chain`)이 구성됩니다.
- **시 생성**: 사용자가 입력한 주제를 기반으로 체인을 `invoke`하여 시를 생성하고, 결과를 화면에 출력합니다.
- **예외 처리**: API 키 미입력, 주제 미입력, API 키 오류 등 다양한 실행 오류에 대한 메시지를 사용자에게 보여줍니다.
- **📝 AI 시인 Streamlit 애플리케이션 분석**

이 문서는 사용자가 제공한 **`app.py`** (Streamlit 애플리케이션 코드)와 **`requirements.txt`** (필요 패키지 목록) 파일의 내용을 정리하고 분석한 것입니다.

**1. 💻 `app.py` (인공지능 시인 코드)**

이 파이썬 스크립트는 **Streamlit**을 프론트엔드로, **LangChain**을 LLM 연동 프레임워크로 사용하여 OpenAI의 `gpt-4o-mini` 모델을 통해 시를 작성하는 웹 애플리케이션을 구현합니다.

**주요 기능**

• **웹 인터페이스**: `st.title`과 `st.text_input` 등을 사용하여 "인공지능 시인"이라는 제목의 간단한 사용자 환경(UI)을 구성합니다.
• **API 키 입력**: 사이드바 (`st.sidebar`)에서 사용자에게 **OpenAI API Key**를 입력받고, 성공 또는 경고 메시지를 표시합니다.
    ◦ 입력된 키는 `os.environ['OPENAI_API_KEY']`를 통해 환경 변수에 설정됩니다.
• **LangChain 체인**:
    ◦ **모델**: `gpt-4o-mini` 모델을 사용하도록 초기화됩니다.
    ◦ **프롬프트**: 시스템 메시지로는 "You are a helpful assistant that writes beautiful Korean poetry."가 설정되어 한국어 시를 작성하도록 지시합니다.
    ◦ **구성**: `ChatPromptTemplate` → `llm` → `StrOutputParser`의 순서로 체인 (`chain`)이 구성됩니다.
• **시 생성**: 사용자가 입력한 주제를 기반으로 체인을 `invoke`하여 시를 생성하고, 결과를 화면에 출력합니다.
• **예외 처리**: API 키 미입력, 주제 미입력, API 키 오류 등 다양한 실행 오류에 대한 메시지를 사용자에게 보여줍니다.

**2. 📜 `requirements.txt` (필요 패키지 목록)**

이 파일은 프로젝트 실행에 필요한 **Python 패키지**와 **버전**을 나열합니다.**패키지버전역할 (주요 라이브러리)**`streamlit` (app.py 코드 내 존재)N/A웹 UI 개발`langchain1.0.5`LLM 애플리케이션 프레임워크`langchain-core1.0.4`LangChain의 핵심 구성 요소`langchain-openai1.0.2`OpenAI API 연동`openai2.7.2`OpenAI 공식 라이브러리`langgraph1.0.3`LLM 기반 에이전트 그래프 빌드`pydantic2.12.4`데이터 유효성 검사 및 설정 관리`requests2.32.5`HTTP 요청 처리`httpx0.28.1`비동기 HTTP 클라이언트`tiktoken0.12.0`OpenAI 토큰 인코딩/디코딩

**📝 AI 시인 Streamlit 애플리케이션 분석**

이 문서는 사용자가 제공한 **`app.py`** (Streamlit 애플리케이션 코드)와 **`requirements.txt`** (필요 패키지 목록) 파일의 내용을 정리하고 분석한 것입니다.

**1. 💻 `app.py` (인공지능 시인 코드)**

이 파이썬 스크립트는 **Streamlit**을 프론트엔드로, **LangChain**을 LLM 연동 프레임워크로 사용하여 OpenAI의 `gpt-4o-mini` 모델을 통해 시를 작성하는 웹 애플리케이션을 구현합니다.

**주요 기능**

• **웹 인터페이스**: `st.title`과 `st.text_input` 등을 사용하여 "인공지능 시인"이라는 제목의 간단한 사용자 환경(UI)을 구성합니다.
• **API 키 입력**: 사이드바 (`st.sidebar`)에서 사용자에게 **OpenAI API Key**를 입력받고, 성공 또는 경고 메시지를 표시합니다.
    ◦ 입력된 키는 `os.environ['OPENAI_API_KEY']`를 통해 환경 변수에 설정됩니다.
• **LangChain 체인**:
    ◦ **모델**: `gpt-4o-mini` 모델을 사용하도록 초기화됩니다.
    ◦ **프롬프트**: 시스템 메시지로는 "You are a helpful assistant that writes beautiful Korean poetry."가 설정되어 한국어 시를 작성하도록 지시합니다.
    ◦ **구성**: `ChatPromptTemplate` → `llm` → `StrOutputParser`의 순서로 체인 (`chain`)이 구성됩니다.
• **시 생성**: 사용자가 입력한 주제를 기반으로 체인을 `invoke`하여 시를 생성하고, 결과를 화면에 출력합니다.
• **예외 처리**: API 키 미입력, 주제 미입력, API 키 오류 등 다양한 실행 오류에 대한 메시지를 사용자에게 보여줍니다.

**2. 📜 `requirements.txt` (필요 패키지 목록)**

이 파일은 프로젝트 실행에 필요한 **Python 패키지**와 **버전**을 나열합니다.**패키지버전역할 (주요 라이브러리)**`streamlit` (app.py 코드 내 존재)N/A웹 UI 개발`langchain1.0.5`LLM 애플리케이션 프레임워크`langchain-core1.0.4`LangChain의 핵심 구성 요소`langchain-openai1.0.2`OpenAI API 연동`openai2.7.2`OpenAI 공식 라이브러리`langgraph1.0.3`LLM 기반 에이전트 그래프 빌드`pydantic2.12.4`데이터 유효성 검사 및 설정 관리`requests2.32.5`HTTP 요청 처리`httpx0.28.1`비동기 HTTP 클라이언트`tiktoken0.12.0`OpenAI 토큰 인코딩/디코딩

**3. 💡 핵심 기술 요약**
**요소기술/패키지설명프론트엔드/배포**Streamlit파이썬 코드로 빠르게 웹 애플리케이션 개발.**LLM 연동**LangChain & `langchain-openai`LLM 체인 및 모듈화된 API 접근 제공.**LLM 모델**`gpt-4o-mini`시를 생성하는 데 사용된 경량화된 OpenAI 모델.**주요 작업**Chain (프롬프트-모델-파서)시스템의 역할 정의 및 사용자 입력 처리 흐름 구성.