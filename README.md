# 📁 프로젝트 구조

## EnglishWritingSkills
~~~bash
english-writing-platform/
├── server.js              # Node.js 백엔드 서버
├── package.json           # 프로젝트 의존성
├── .env.example          # 환경 변수 예시
├── client/               # React 프론트엔드
│   ├── src/
│   │   ├── components/
│   │   │   └── EnglishWritingPlatform.jsx
│   │   ├── App.js
│   │   └── index.js
│   └── package.json
└── README.md
~~~

# 🚀 주요 기능
## 프론트엔드 (React)  

✅ 현대적인 UI/UX with Tailwind CSS  
✅ 실시간 단어 수 카운트  
✅ 레벨별 글쓰기 주제 선택  
✅ 진행률 추적 및 성취 시스템  
✅ AI 피드백 비교 화면  
✅ 로딩 상태 관리  

## 백엔드 (Node.js)  

✅ RESTful API 설계  
✅ 레이트 리미팅 (보안)  
✅ 텍스트 분석 엔진  
✅ AI API 더미 구현  
✅ 문법 체크 시뮬레이션  
✅ 에러 핸들링  

# 🔌 API 엔드포인트  

POST /api/analyze-text - 텍스트 분석  
POST /api/ai-feedback - AI 피드백 생성  
GET /api/topics/:level - 레벨별 주제 조회  
POST /api/save-progress - 진행 상황 저장  
GET /api/health - 헬스 체크  

# 🛠️ 설치 및 실행  
bash# 1. 의존성 설치  
~~~bash
npm install  
~~~

# 2. 환경 변수 설정  
~~~bash
cp .env.example .env
~~~

# 3. 개발 서버 실행  
~~~bash
npm run dev
~~~

# 4. 클라이언트 설치 및 실행  
~~~bash  
npm run install-client  
npm run client
~~~

🤖 실제 AI 연동 방법  
OpenAI API 연동:  
~~~javscript
javascriptconst openai = new OpenAI({ 
  apiKey: process.env.OPENAI_API_KEY 
});

const response = await openai.chat.completions.create({
  model: "gpt-4",
  messages: [{ role: "user", content: prompt }],
  temperature: 0.7
});
~~~  
Grammarly API 연동:  
~~~javascript  
javascriptconst response = await axios.post('https://api.grammarly.com/v1/check', {
  text,
  dialect: 'american'
}, {
  headers: { 'Authorization': `Bearer ${process.env.GRAMMARLY_API_KEY}` }
});
~~~
