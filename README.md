# AI 챗봇 실행 가이드

이 프로그램은 컴퓨터에서 AI와 대화할 수 있는 웹사이트입니다. 아래 순서대로 따라하시면 누구나 실행할 수 있습니다.

## 준비물
- 인터넷에 연결된 컴퓨터 (Windows, Mac, Linux 모두 가능)
- 이메일 주소 (API 키 발급용)

## 1단계: Python 설치

### Windows 사용자
1. 웹 브라우저에서 https://www.python.org/downloads/ 접속
2. 노란색 "Download Python" 버튼 클릭
3. 다운로드된 파일 실행
4. **중요**: "Add Python to PATH" 체크박스에 체크 표시
5. "Install Now" 클릭하여 설치 완료

### Mac 사용자
1. 웹 브라우저에서 https://www.python.org/downloads/ 접속
2. "Download Python" 버튼 클릭
3. 다운로드된 .pkg 파일 실행하여 설치

## 2단계: 명령 프롬프트(터미널) 열기

### Windows
1. 키보드에서 `Windows키 + R` 누르기
2. "cmd" 입력하고 Enter
3. 검은 화면이 나타나면 성공

### Mac
1. `Command + Space` 누르기
2. "터미널" 또는 "Terminal" 입력하고 Enter
3. 검은 화면이 나타나면 성공

## 3단계: 프로젝트 폴더로 이동
1. 명령 프롬프트에서 다음과 같이 입력 (따옴표 제외):
   ```
   cd "이 폴더의 경로"
   ```
   예시: `cd "C:\Users\사용자명\Desktop\Simple AI ChatBot"`

2. Enter 키 누르기

## 4단계: 필요한 프로그램 설치
명령 프롬프트에서 다음 명령어 입력하고 Enter:
```
pip install flask groq
```
설치가 완료될 때까지 기다리세요 (1-2분 소요).

## 5단계: API 키 발급받기
1. 웹 브라우저에서 https://console.groq.com 접속
2. "Sign Up" 또는 "로그인" 클릭
3. 이메일로 계정 생성
4. 로그인 후 "API Keys" 메뉴 클릭
5. "Create API Key" 버튼 클릭
6. 생성된 긴 문자열(API 키) 복사하기

## 6단계: API 키 설정
1. 이 폴더에서 `app.py` 파일을 메모장으로 열기
   - 파일 우클릭 → "연결 프로그램" → "메모장"
2. 7번째 줄에서 `your_groq_api_key_here` 부분을 찾기
3. 따옴표 사이의 내용을 복사한 API 키로 바꾸기
   - 예시: `client = Groq(api_key="gsk_abc123def456...")`
4. 파일 저장하기 (Ctrl+S)

## 7단계: 챗봇 실행
1. 명령 프롬프트에서 다음 명령어 입력:
   ```
   python app.py
   ```
2. "Running on http://127.0.0.1:5000" 메시지가 나타나면 성공

## 8단계: 웹사이트 접속
1. 웹 브라우저 열기 (크롬, 엣지, 사파리 등)
2. 주소창에 다음 입력:
   ```
   localhost:5000
   ```
3. AI 챗봇 화면이 나타나면 완료!

## 사용 방법
- 텍스트 입력창에 질문 입력
- "전송" 버튼 클릭
- AI의 답변 확인

## 종료 방법
- 명령 프롬프트에서 `Ctrl + C` 키 누르기
- 또는 명령 프롬프트 창 닫기

## 문제가 생겼을 때

### "python을 찾을 수 없습니다" 오류
- Python 설치 시 "Add Python to PATH" 체크했는지 확인
- 컴퓨터 재시작 후 다시 시도

### "pip을 찾을 수 없습니다" 오류
- 명령 프롬프트에서 `python -m pip install flask groq` 입력

### API 키 오류
- app.py 파일에서 API 키가 올바르게 입력되었는지 확인
- API 키 앞뒤에 따옴표가 있는지 확인

### 웹사이트가 열리지 않음
- 명령 프롬프트에서 오류 메시지 확인
- 방화벽이나 백신 프로그램 때문일 수 있음
