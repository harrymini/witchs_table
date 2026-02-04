# 🍽️ Food Structure (푸드 스트럭처)

<div align="center">

**가공식품 화학성분 분석 및 인체 영향도 지표 플랫폼**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

</div>

---

## 📋 목차

- [프로젝트 개요](#-프로젝트-개요)
- [시장 분석 및 벤치마킹](#-시장-분석-및-벤치마킹)
- [핵심 가치](#-핵심-가치)
- [주요 기능](#-주요-기능)
- [서비스 아키텍처](#-서비스-아키텍처)
- [시스템 아키텍처](#-시스템-아키텍처)
- [사용자 플로우](#-사용자-플로우)
- [타겟 사용자](#-타겟-사용자)
- [비즈니스 모델](#-비즈니스-모델)
- [기술 스택](#-기술-스택)
- [시작하기](#-시작하기)
- [로드맵](#-로드맵)
- [기여하기](#-기여하기)

---

## 🎯 프로젝트 개요

**Food Structure**는 가공식품의 화학 성분을 과학적으로 분석하여, 인체에 미치는 영향을 객관적인 지표로 제공하는 헬스케어 플랫폼입니다.

### 기획 배경

- **정보의 비대칭성**: 복잡한 화학 용어(산도조절제, 유화제 등)로 인해 일반 소비자가 위험도를 파악하기 어려움
- **기준의 모호성**: 국가별(EU, USA, KR)로 상이한 허용 기준으로 인한 혼란
- **과학적 접근 필요**: 공포 마케팅이 아닌, 글로벌 보건 표준에 근거한 객관적 데이터 제공

### 미션 & 비전

```
🎯 Mission
가공식품의 화학 성분을 해체하여 인체 영향도를 객관적 지표로 환산한다.

🌟 Vision
대한민국에서 가장 신뢰받는 식품 화학 데이터 및 건강 대안 솔루션
```

---

## 📊 시장 분석 및 벤치마킹

성공적인 글로벌/국내 서비스를 분석하여 **푸드 스트럭처만의 고유한 영역**을 정의합니다.

### 글로벌 벤치마크 분석

| 서비스명 | 핵심 강점 | 시사점 |
|---------|----------|--------|
| **Yuka** (유럽) | 직관적인 신호등 컬러 UI<br/>즉각적인 대안 제품 추천 | 복잡한 수치보다 시각적인 '등급' 피드백이 중요함 |
| **EWG Food Scores** (미국) | 학술적 근거에 기반한 1~10점 척도<br/>유해성 구체 명시 | 데이터의 전문성과 투명성이 신뢰의 핵심임 |
| **Open Food Facts** (글로벌) | 80만 개 이상의 방대한<br/>오픈 소스 데이터 | 글로벌 API 연동을 통한 확장 가능성 확인 |

### 국내 시장 현황

**엄선(Umsun)**
- 국내 유통 제품 특화 및 커뮤니티 강점
- 한계: 글로벌 기준 비교나 생리학적 기전 설명 부족

### 푸드 스트럭처만의 차별화 전략 (USP)

```mermaid
graph LR
    A[차별화 포인트] --> B[글로벌 입체 비교]
    A --> C[생리학적 기전 해설]
    A --> D[섭취 빈도 가중치]

    B --> B1[KR vs FDA vs EFSA<br/>기준 동시 제공]
    C --> C1[장 점막 작용 기전<br/>구조적 설명]
    D --> D1[실질적 위험도<br/>랭킹 제공]

    style A fill:#e1f5ff
    style B fill:#fff4e1
    style C fill:#ffe1f5
    style D fill:#f5e1ff
```

1. **글로벌 입체 비교**: KR vs FDA vs EFSA 기준을 동시 제공하여 가장 보수적인 안전 가이드 제시
2. **생리학적 기전 해설**: 단순히 "나쁘다"가 아니라 "이 성분이 장 점막에 어떤 작용을 하는지" 구조적으로 설명
3. **섭취 빈도 가중치**: 독성 수치에 현대인의 평균 섭취 빈도를 결합한 '실질적 위험도' 랭킹 제공

---

## 💡 핵심 가치

- **과학적 근거 기반**: 감정이 아닌 논문과 데이터에 기반한 분석
- **투명한 정보 제공**: 글로벌 안전 기준을 병렬 비교하여 사용자 스스로 판단 가능
- **실질적 위험도 평가**: 단순 독성이 아닌 실생활 섭취 빈도를 고려한 가중치 적용
- **대안 솔루션 제시**: 문제 제기에서 끝나지 않고 더 나은 선택지 제공
- **생리학적 작동 원리 설명**: 화학 성분이 인체에 미치는 영향을 생리학적 관점에서 구체적으로 해설

---

## 🚀 주요 기능

### 1. 스마트 성분 분석 및 가이드

- **바코드 스캔**: 한 번의 스캔으로 제품 내 모든 첨가물 추출
- **목적별 그룹화**: 보존제, 감미료, 착색료 등 화학적 용도에 따라 직관적 분류

### 2. 가중치 기반 인체 영향도 랭킹

실질적 위험도를 산출하기 위한 3가지 가중치 알고리즘:

| 요소 | 가중치 | 설명 |
|------|--------|------|
| **현대인 섭취 빈도** | 40% | 소스, 빵 등 일상 식품에 얼마나 흔하게 사용되는가? |
| **체내 축적 및 지속성** | 30% | 대사되지 않고 체내에 머물며 장기적 영향을 주는가? |
| **생리학적 독성 수준** | 30% | 호르몬 교란, 장내 미생물 파괴 등 학술적 근거 강도 |

### 3. 글로벌 안전 기준 투명 비교

- **다국가 기준 병렬 배치**: FDA(미국), EFSA(유럽), 식약처(한국) 허용치 비교
- **개인별 ADI 계산**: 사용자 체중 데이터 기반으로 1일 최대 섭취 권고량 환산
  - 예: "이 과자는 1.5봉지까지 안전합니다"

### 4. 클린 라벨(Clean Label) 대안 제시

- **스마트 추천**: 위험 성분이 배제된 유사 용도의 대체 제품 추천
- **시각적 비교**: 기존 vs 추천 제품의 Health Score 차트 제공

---

## 🔄 서비스 아키텍처

전체 서비스 플로우는 4단계로 구성됩니다.

```mermaid
graph LR
    A[유입 단계] --> B[분석 단계]
    B --> C[결과 단계]
    C --> D[액션 단계]

    A1[바코드 스캔] --> A
    A2[제품명 검색] --> A
    A3[사진 촬영] --> A

    B1[DB 매핑/추출] --> B
    B2[식약처/해외 API] --> B

    C1[인체 영향 분석] --> C
    C2[국가별 기준 비교] --> C

    D1[클린라벨 추천] --> D
    D2[구매/기록 연동] --> D

    style A fill:#e1f5ff
    style B fill:#fff4e1
    style C fill:#ffe1f5
    style D fill:#f5e1ff
```

### 단계별 상세 프로세스

| 단계 | 기능 | 설명 |
|------|------|------|
| **유입 단계** | 바코드 스캔<br/>제품명 검색<br/>사진 촬영(OCR) | 사용자가 제품 정보를 입력하는 3가지 방법 제공 |
| **분석 단계** | DB 매핑/추출<br/>식약처/해외 API 연동 | 제품 성분 데이터를 추출하고 글로벌 DB와 매칭 |
| **결과 단계** | 인체 영향 분석<br/>국가별 기준 비교 | 가중치 알고리즘 적용 및 FDA/EFSA/MFDS 기준 비교 |
| **액션 단계** | 클린라벨 추천<br/>구매/기록 연동 | 대안 제품 추천 및 이커머스 연계 |

---

## 🏗️ 시스템 아키텍처

```mermaid
graph TB
    subgraph "Client Layer"
        A[Mobile App] --> B[Web App]
        B --> C[Barcode Scanner]
        B --> D[Product Search]
    end

    subgraph "API Gateway"
        E[REST API]
        F[GraphQL API]
    end

    subgraph "Service Layer"
        G[Product Analysis Service]
        H[Impact Ranking Engine]
        I[Safety Standard Service]
        J[Recommendation Engine]
    end

    subgraph "Data Layer"
        K[(Product DB)]
        L[(Chemical DB)]
        M[(User DB)]
        N[(Global Standards DB)]
    end

    subgraph "External Services"
        O[FDA API]
        P[EFSA API]
        Q[MFDS API]
        R[OCR Service]
    end

    A --> E
    B --> E
    C --> E
    D --> F

    E --> G
    F --> G
    E --> H
    F --> I
    E --> J

    G --> K
    G --> L
    H --> L
    H --> M
    I --> N
    J --> K

    I --> O
    I --> P
    I --> Q
    C --> R
```

---

## 👥 사용자 플로우

```mermaid
flowchart TD
    Start([사용자 시작]) --> Scan{제품 입력 방법}

    Scan -->|바코드 스캔| Barcode[바코드 인식]
    Scan -->|수동 검색| Search[제품명 검색]
    Scan -->|사진 촬영| OCR[성분표 OCR]

    Barcode --> Analysis[성분 분석 시작]
    Search --> Analysis
    OCR --> Analysis

    Analysis --> Extract[첨가물 추출 및 분류]
    Extract --> Weight[가중치 계산]

    Weight --> Impact{인체 영향도 평가}
    Impact -->|섭취 빈도 40%| Freq[일상 노출도 분석]
    Impact -->|체내 축적 30%| Accum[축적성 평가]
    Impact -->|독성 수준 30%| Toxic[독성 데이터 조회]

    Freq --> Score[종합 점수 산출]
    Accum --> Score
    Toxic --> Score

    Score --> Compare[글로벌 기준 비교]
    Compare --> FDA[FDA 기준]
    Compare --> EFSA[EFSA 기준]
    Compare --> MFDS[식약처 기준]

    FDA --> ADI[개인별 ADI 계산]
    EFSA --> ADI
    MFDS --> ADI

    ADI --> Result{결과 표시}
    Result --> Detail[상세 분석 리포트]
    Result --> Alert[위험 성분 경고]
    Result --> Alternative[대안 제품 추천]

    Alternative --> Recommend[클린 라벨 제품 목록]
    Recommend --> Compare2[건강 점수 비교]
    Compare2 --> Purchase[구매 링크 제공]

    Detail --> Save[기록 저장]
    Save --> End([완료])
    Purchase --> End
```

---

## 🎯 타겟 사용자

### Core (고관여층)
자가면역질환, 알레르기, 당뇨 전단계 등 성분 관리가 생존과 직결된 사용자

### Active (체크슈머)
영유아 자녀를 둔 부모로, 식품 첨가물이 아이의 성장에 미치는 영향을 철저히 검증하는 층

### Mass (자기관리층)
다이어트, 헬스 등 건강한 식단을 지향하며 효율적인 영양 섭취를 원하는 일반인

---

## 💰 비즈니스 모델

```mermaid
graph LR
    A[수익 모델] --> B[제휴 모델]
    A --> C[인증 비즈니스]
    A --> D[데이터 리포트]

    B --> B1[클린 라벨 제품<br/>구매 수수료]
    C --> C1[푸드 스트럭처<br/>인증 마크 부여]
    D --> D1[월간 섭취 분석<br/>구독 서비스]

    style A fill:#e1f5ff
    style B fill:#fff4e1
    style C fill:#ffe1f5
    style D fill:#f5e1ff
```

### 수익 구조

1. **제휴 모델 (Affiliate)**: 클린 라벨 제품 추천 시 구매 링크를 통한 수수료
2. **인증 비즈니스**: 푸드 스트럭처 기준 통과 제품 인증 마크 부여 및 마케팅 협업
3. **데이터 리포트**: 구독형 모델로 월간 화학물질 섭취 분석 및 디톡스 가이드 제공

### 비즈니스 순환 구조 (Business Loop)

```mermaid
graph TD
    A[신뢰성 있는 정보 제공] --> B[사용자 경험 향상]
    B --> C[클린 라벨 대안 추천]
    C --> D[인증 및 커머스 연계]
    D --> E[수익 창출]
    E --> A

    A1[공공 데이터 +<br/>해외 DB 활용] -.-> A
    B1[분석 리포트<br/>구독 서비스] -.-> B
    C1[제휴 업체<br/>Affiliate] -.-> C
    D1[인증 마크<br/>라이선싱] -.-> D

    style A fill:#e1f5ff
    style B fill:#fff4e1
    style C fill:#ffe1f5
    style D fill:#f5e1ff
    style E fill:#e1ffe1
```

이 순환 구조는 신뢰할 수 있는 데이터를 기반으로 사용자 경험을 개선하고, 이를 통해 수익을 창출하며, 다시 더 나은 데이터와 서비스로 재투자하는 선순환 모델을 구축합니다.

---

## 🛠️ 기술 스택

### Frontend
- React / React Native
- TypeScript
- Tailwind CSS
- Redux Toolkit

### Backend
- Node.js / Express
- GraphQL
- PostgreSQL
- Redis

### AI/ML
- TensorFlow (이미지 인식)
- Python (데이터 분석)
- OpenCV (OCR)

### Infrastructure
- AWS (EC2, S3, RDS)
- Docker
- GitHub Actions (CI/CD)

---

## 🚀 시작하기

### 필요 조건

- Node.js 18.x 이상
- PostgreSQL 14.x 이상
- Docker (선택사항)

### 설치

```bash
# 저장소 클론
git clone https://github.com/yourusername/food-structure.git
cd food-structure

# 의존성 설치
npm install

# 환경 변수 설정
cp .env.example .env

# 데이터베이스 마이그레이션
npm run db:migrate

# 개발 서버 실행
npm run dev
```

### 환경 변수 설정

```env
DATABASE_URL=postgresql://user:password@localhost:5432/foodstructure
FDA_API_KEY=your_fda_api_key
EFSA_API_KEY=your_efsa_api_key
MFDS_API_KEY=your_mfds_api_key
OCR_SERVICE_KEY=your_ocr_key
```

---

## 🗓️ 로드맵

```mermaid
gantt
    title Food Structure 개발 로드맵
    dateFormat YYYY-MM
    section Phase 1: 도입기
    MVP 개발                        :2026-03, 3M
    핵심 제품 DB 구축 (5,000종)     :2026-04, 2M
    베타 테스트                     :2026-06, 1M

    section Phase 2: 확장기
    이미지 인식 고도화              :2026-07, 2M
    사용자 커뮤니티 오픈            :2026-08, 1M
    개인 기록 기능                  :2026-09, 1M

    section Phase 3: 안정기
    반려동물 사료 확장              :2026-10, 2M
    이커머스 연계 강화              :2026-12, 2M
    글로벌 진출 준비                :2027-02, 3M
```

### Phase 1: 도입기 (MVP)
- 핵심 기능 개발 (성분 분석, 영향도 랭킹)
- 필수 가공식품 5,000종 데이터베이스 구축
- 가중치 기반 랭킹 알고리즘 구축
- 바코드 스캔 및 기본 검색 기능

### Phase 2: 확장기
- 이미지 인식(OCR) 기능 고도화
- **개인별 체중 기반 ADI 알림 기능** 추가
- 사용자 커뮤니티 및 리뷰 기능
- 개인별 섭취 기록 및 분석 대시보드

### Phase 3: 안정기
- 반려동물 사료/간식 영역 확장
- **클린 커머스 구독 연동** 강화
- 이커머스 플랫폼 연계 확대
- 해외 시장 진출 (글로벌 DB 확대)

---

## 🎨 마케팅 전략

### 콘텐츠 마케팅

**유튜브 쇼츠**
- 'AI 강아지 인터뷰' 포맷으로 식품 성분을 심문하는 형식
- 호기심 유발형 쇼트폼 콘텐츠

**전문 블로그**
- 생리학, 영양학 논문 기반 성분 분석 칼럼
- 감정 배제, 팩트 중심의 과학적 접근

---

## 📊 데이터 처리 프로세스

```mermaid
sequenceDiagram
    participant U as User
    participant A as App
    participant S as Analysis Service
    participant D as Database
    participant E as External APIs

    U->>A: 제품 스캔/검색
    A->>S: 제품 정보 요청
    S->>D: 제품 데이터 조회
    D-->>S: 기본 정보 반환

    S->>S: 성분 추출 및 분류
    S->>D: 화학물질 데이터 조회
    D-->>S: 성분별 상세 정보

    par 글로벌 기준 조회
        S->>E: FDA 기준 요청
        E-->>S: FDA 데이터
    and
        S->>E: EFSA 기준 요청
        E-->>S: EFSA 데이터
    and
        S->>E: MFDS 기준 요청
        E-->>S: MFDS 데이터
    end

    S->>S: 가중치 계산 (40-30-30)
    S->>S: 종합 점수 산출
    S->>D: 대안 제품 검색
    D-->>S: 클린 라벨 제품 목록

    S-->>A: 종합 분석 결과
    A-->>U: 시각화된 리포트 표시
```

---

## 🤝 기여하기

Food Structure는 오픈소스 프로젝트입니다. 기여를 환영합니다!

### 기여 방법

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### 기여 가이드라인

- 코드 스타일: ESLint + Prettier 설정 준수
- 테스트: 새로운 기능은 반드시 테스트 코드 작성
- 커밋 메시지: [Conventional Commits](https://www.conventionalcommits.org/) 규칙 따르기
- 문서화: 주요 변경사항은 CHANGELOG.md에 기록

---

## 📄 라이선스

이 프로젝트는 MIT 라이선스 하에 배포됩니다. 자세한 내용은 [LICENSE](LICENSE) 파일을 참조하세요.

---

## 📧 연락처

프로젝트 관련 문의사항이 있으시면 아래로 연락 주세요.

- Email: contact@foodstructure.com
- Website: https://foodstructure.com
- Issue Tracker: https://github.com/yourusername/food-structure/issues

---

<div align="center">

**Made with ❤️ for healthier food choices**

[⬆ Back to Top](#-food-structure-푸드-스트럭처)

</div>
