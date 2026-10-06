# 시노펙스 직무체계 분석 및 설계도구 (Job-Spec-Analysis)

시노펙스(SYNOPEX)의 사업 영역(IT, 필터·멤브레인, 바이오·의료)에 맞춘 **NCS 기반 직무분류체계, KSA(지식·기술·태도) 매핑, HRD 교육체계 수립 및 직무 아키텍트 웹앱** 프로젝트입니다.

---

## 📌 프로젝트 개요

- **핵심 목표**: "사업에 필요한 직무 → 요구역량(KSA) → 교육(L&D) → 평가/자격 → 실무 수행 → 역량 개선"의 전 주기를 설계하고 추적 가능한 시스템 구축
- **적용 대상**: 시노펙스 주요 사업부문 (FPCB/IT부품, 멤브레인·필터 수처리, 혈액투석기·바이오/의료기기) 및 공통 경영지원 조직
- **제공 형태**: 단일 실행형 웹 애플리케이션(`synopex-job-architect.html`) 및 체계적 분석/가이드 문서

---

## 🗂 디렉터리 및 주요 파일 구성

```text
Job-Spec-Analysis/
├── synopex-job-architect.html          # 시노펙스 직무체계 설계도구 웹애플리케이션 (SPA)
├── ncs_ksa.js / ncs_ksa2.js            # NCS 및 직무별 KSA(지식·기술·태도) 데이터셋
├── synopex-logo.png / synopex-logo-sm.png # 시노펙스 로고 에셋
│
├── 📖 분석 및 가이드 문서
│   ├── 직무분석 시스템.md                # 전체 추진 가이드 및 조사·설계·개발 프로세스
│   ├── NCS_매핑_조사결과.md              # 시노펙스 사업군별 NCS 표준 직무 매핑 결과
│   ├── 직무구분.정의.기술.md             # 직무구분 체계, 직무정의서 및 직무기술서
│   ├── JD-KSA-L&D.md                   # 직무기술서 기반 KSA 및 교육훈련 매핑
│   ├── HRD-L&D.md                      # 사내 HRD/L&D 교육체계 및 이수 체계도
│   ├── NCS_Learning_Program_Design_Guide.md # NCS 학습모듈 기반 교육과정 개발 가이드
│   └── DESIGN.md                       # 웹앱 디자인 시스템 규격 (컬러, 타이포, 컴포넌트)
│
└── .gitignore                          # 임시/백업 파일 제외 설정
```

---

## 🚀 빠른 시작 (웹앱 실행)

별도의 백엔드 설치나 의존성 빌드 없이 브라우저에서 직접 실행할 수 있습니다.

### 1. 로컬 브라우저에서 직접 열기
- 파일 탐색기에서 `synopex-job-architect.html` 파일을 더블클릭하거나 웹 브라우저(Chrome, Safari, Edge 등)로 드래그하여 실행합니다.

### 2. 로컬 정적 서버로 실행 (선택)
```bash
# Python 내장 서버 활용
python3 -m http.server 8000

# 브라우저에서 http://localhost:8000/synopex-job-architect.html 접속
```

---

## 💡 주요 기능

1. **직무 체계 매핑 뷰어**: 시노펙스 사업별 직무분류와 국가직무능력표준(NCS) 능력단위 매핑 탐색
2. **KSA 역량 프로파일**: 직무별 필요 지식(Knowledge), 기술(Skill), 태도(Attitude) 상세 분석
3. **L&D 교육과정 연계**: 직무/직급별 필수 법정교육, OJT, 직무역량 교육 트랙 확인
4. **반응형 인터페이스 & 다크모드**: Desktop-first 설계, 다크/라이트 테마 자동 전환 지원

---

## 🛠 기술 스택 & 디자인

- **Frontend**: HTML5, Vanilla JavaScript, Vanilla CSS (CSS Custom Properties)
- **Typography**: Plus Jakarta Sans, Noto Sans KR, JetBrains Mono
- **Design Tokens**: [DESIGN.md](file:///Users/greeme/Downloads/Workspace/Job-Spec-Analysis/DESIGN.md) 기반의 세부 토큰 및 Glassmorphism UI
- **데이터 구조**: 사내 독립형 로컬 데이터 구조 (`.js` 데이터셋 바인딩)
