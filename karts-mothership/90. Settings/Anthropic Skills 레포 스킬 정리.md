---
index:
  - "[[🏷️ 공부]]"
links:
type:
  - "[[Tool Study]]"
  - "[[CMDS-System-Files/CLAUDE|Claude Code Guide]]"
  - "[[Claude-Code-skills]]"
tags:
  - AI
  - Claude
  - skills
세션 이름: 클로드 코드 공부
---
# Anthropic Skills 레포 스킬 정리

> 출처: https://github.com/anthropics/skills  
> 조사일: 2026-05-24

**스킬이란?** 클로드한테 "이 폴더에 있는 설명서 읽어서 특수 능력 장착해" 하는 것. 일반 클로드에는 없는 전문 행동을 추가해줌.

총 17개 스킬, 5개 카테고리.

---

## 🎨 크리에이티브 계열

### algorithmic-art
[[수학으로 그림 그리는 기계]].
1. 그림의 철학 선언문(4~6문단) 먼저 작성
2. p5.js로 인터랙티브 HTML 아트 생성 (슬라이더로 실시간 조작)
3. 씨앗값(seed)으로 같은 그림 재현 가능. claude.ai에서 바로 열림

### canvas-design
박물관 걸어도 될 수준의 디자인 1장 만들기.
1. 비주얼 철학 선언 (어떤 미적 운동을 따를 것인가)
2. PDF/PNG로 단 한 장의 아트워크 출력
- 규칙: 텍스트 최소화, 요소 겹침 금지, "수천 시간 공들인 것처럼" 보여야 함

### frontend-design
"AI가 만든 티 나는 디자인" 탈출 키트.
- Inter 폰트, 보라색 그라데이션, 뻔한 레이아웃 명시적으로 금지
- 브루탈리즘·맥시멀리즘·레트로 등 구체적인 미적 방향성 먼저 결정
- 그 방향에 맞는 타이포, 컬러, 애니메이션 체계적으로 구현

### slack-gif-creator
슬랙용 GIF 이모지/메시지 애니메이션 제작.
- 슬랙 이모지 규격(128×128, 10~30fps) 자동 준수
- PIL로 바운싱·펄싱·페이드인 등 애니메이션 직접 드로잉
- 이미지 변환 or 처음부터 새로 제작

---

## 💻 개발 계열

### claude-api
클로드 API로 앱 만들 때 전문가 모드.
- Python/TypeScript/Go 등 언어 감지 → 맞는 공식 SDK 코드 생성
- 프롬프트 캐싱, 스트리밍, 툴 유즈, 배치 등 고급 기능 구현 안내
- 모델 버전 마이그레이션 지원 (4.5 → 4.6 → 4.7)
- 규칙: OpenAI SDK 절대 안 섞음

### mcp-builder
클로드가 외부 서비스를 쓸 수 있게 해주는 플러그인 서버 제작.

> MCP = Model Context Protocol. 클로드한테 "이 API도 써도 돼" 하는 연결 규격

1. 대상 API 분석 + 툴 설계
2. TypeScript(기본) 또는 Python(FastMCP)으로 서버 구현
3. MCP Inspector로 테스트
4. LLM이 잘 쓸 수 있는지 평가 문항 10개 생성

### webapp-testing
웹 앱을 로봇처럼 자동으로 클릭하고 테스트.
- Python + Playwright 조합
1. 정적 HTML이냐 동적이냐 판단
2. 서버 자동 켜기 (`with_server.py`)
3. 스크린샷 찍어 셀렉터 확인 → 클릭/입력 자동화
- 핵심: `networkidle` 대기로 JS 완전 실행 후 검사

### web-artifacts-builder
React+TypeScript로 공유 가능한 단일 HTML 파일 제작.
- React 18 + Vite + Tailwind + shadcn/ui 셋업 자동화
- 개발 후 Parcel로 번들링 → 파일 하나로 압축
- 상태관리/컴포넌트 라이브러리가 필요한 복잡한 결과물용

---

## 📄 문서 계열

### docx / pdf / pptx / xlsx
Word, PDF, PowerPoint, Excel 파일 생성·편집.
- 소스 공개(교육·데모용), 오픈소스는 아님
- `pptx`는 `/pptx-maker` 스킬의 원조

### doc-coauthoring
사람 + 클로드 함께 쓰는 문서 협업 3단계 워크플로우.
1. 클로드가 질문 → 배경·제약·독자 파악
2. 섹션별 브레인스토밍 → 구조 잡기 → 반복 수정
3. 새 클로드 인스턴스가 "독자 입장"으로 문서 읽고 허점 발견

---

## 🏢 비즈니스/브랜드 계열

### brand-guidelines
Anthropic 공식 브랜드 스타일 적용기.
- 색상: 다크 `#141413`, 라이트 `#faf9f5`, 오렌지/블루/그린 포인트
- 폰트: 제목 Poppins, 본문 Lora (폴백: Arial/Georgia)

### internal-comms
회사 내부 커뮤니케이션 글쓰기 도우미.
- 팀 업데이트, 뉴스레터, FAQ, 상황 보고서, 인시던트 리포트 포맷 제공

### theme-factory
프레젠테이션/문서용 디자인 테마 10종 + 커스텀 테마 생성.
- "Ocean Depths", "Midnight Galaxy" 등 사전 제작 세트
- 슬라이드, 문서, 랜딩페이지에 일관된 스타일 적용

---

## ⚙️ 메타 스킬

### skill-creator
스킬 자체를 만드는 스킬 (재귀적).
1. 어떤 스킬을 만들지 의도 파악
2. SKILL.md 초안 작성
3. 테스트 프롬프트 2~3개 실행
4. 스킬 있을 때 vs 없을 때 결과 비교
5. 수치 평가 → 반복 개선
- 규칙: SKILL.md 500줄 이하, description은 "충분히 강하게" 써야 잘 트리거됨

---

## 한눈에 정리

| 분야 | 스킬들 |
|------|--------|
| 아트/디자인 | algorithmic-art, canvas-design, frontend-design, slack-gif-creator |
| 개발 도구 | claude-api, mcp-builder, webapp-testing, web-artifacts-builder |
| 문서 | docx, pdf, pptx, xlsx, doc-coauthoring |
| 브랜드/비즈니스 | brand-guidelines, internal-comms, theme-factory |
| 메타 | skill-creator |

---

## 🛠️ 설치 방법 (Claude Code 기준)

공식 마켓플레이스 등록 후 번들 단위로 설치. 개별 스킬 선택 설치 불가.

**Step 1 — 마켓플레이스 등록**
```
/plugin marketplace add anthropics/skills
```

**Step 2 — 번들 설치**
```
/plugin install example-skills@anthropic-agent-skills   ← 크리에이티브·개발 스킬 묶음
/plugin install document-skills@anthropic-agent-skills  ← docx·pdf·pptx·xlsx 묶음
```

> `example-skills`: algorithmic-art, canvas-design, claude-api, doc-coauthoring, internal-comms, skill-creator 등  
> `document-skills`: docx, pdf, pptx, xlsx

설치 후에는 그냥 말로 쓰면 됨.  
예: `"PDF 스킬 써서 이 파일에서 폼 필드 추출해줘"`

---

## 🎯 짭응이 맞춤 응용 제안

> 직업: 3D 애니메이션 프로듀서 / 배경 컨셉 디자이너  
> 기질: 자극추구 MAX, 몰입 폭발형, 완벽주의 함정 주의

### algorithmic-art
**→ 배경 컨셉 무드보드 / 씬 레퍼런스 생성기**  
"이 씬의 색조는 수학적 노이즈로 표현한다"는 알고리즘 철학을 먼저 세운 뒤, 파라미터 조작으로 무한 변주 가능한 인터랙티브 무드보드 생성. 레퍼런스 수집 시간을 "직접 생성"으로 대체.  
*예시 프롬프트: "황폐한 도시 배경의 해질녘 무드, 파티클 시스템으로 먼지와 빛 산란 표현해줘"*

### canvas-design
**→ 포트폴리오 컨셉 페이지 / 클라이언트 제안서 비주얼**  
텍스트 최소화 원칙이 3D 아트디렉션 감각과 딱 맞음. 클라이언트에게 보내는 프로젝트 제안서를 텍스트 문서 대신 "작품 한 장"으로 대체 가능.  
*예시 프롬프트: "VR 환경 프로젝트 제안, 공간감·몰입감 컨셉으로 단 한 장짜리 비주얼 제안서"*

### claude-api
**→ 반복 작업 자동화 파이프라인 구축**  
애니메이션 프로덕션의 반복 행정(파일명 규칙 체크, 납품 체크리스트 생성, 클라이언트 피드백 분류)을 API 앱으로 자동화. 바이브코딩 프로젝트와 연결하기에도 최적.  
*예시: 납품 폴더 스캔 → 누락 파일 감지 → 클라이언트 보고서 자동 생성*

### docx / pdf / pptx / xlsx
**→ 제안서·견적서·포트폴리오 PDF 원클릭 생성**  
`pptx`: 클라이언트 피치덱을 `/pptx-maker`보다 한층 로우레벨로 컨트롤할 때  
`pdf`: 납품 스펙 문서, 계약서 양식 생성  
`xlsx`: 프로젝트별 작업 시간·단가 트래킹 시트 자동화  
`docx`: 외주 계약서 초안, 기획서 포맷 통일

### [[🧰 doc-coauthoring]]
**→ 지원사업 기획서 / 작업 노트 구조화**  
`70. Outputs/Deadline/` 지원사업 폴더의 기획서 작성에 직접 응용. 클로드가 먼저 질문으로 배경을 파악하고, 섹션별로 같이 써내려감. 마지막 단계에서 "심사위원 입장"으로 허점 검토.  
*즉: 지원사업 기획서 = doc-coauthoring 3단계 워크플로우로 처리*


### internal-comms
**→ 팀 공유 회의록 / 클라이언트 업데이트 메일**  
`60. Collections/Meetings/` 회의록을 넣으면 클라이언트용 업데이트 메일, 팀 공유 요약본으로 자동 변환. 회의 후 5분 안에 공유 문서 완성 가능.

### skill-creator
**→ QPH 전용 커스텀 스킬 제작**  
현재 `.claude/skills/`에 있는 `/today`, `/prj-sync` 등을 이 스킬로 직접 개선·최적화 가능. 새로운 반복 작업이 생길 때마다 스킬로 굳히는 루틴 구축.  
*예: "3D 납품 체크리스트 스킬", "_anchor.md 자동 업데이트 스킬" 등*
