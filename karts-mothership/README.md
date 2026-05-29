# 🛠 Karts Mothership — AI 애니메이션 팀 볼트

> 이 볼트는 팀 공유 공간입니다.
> 개인 지식 자산은 각자 로컬에서 따로 관리하세요.
> 설계 철학은 [[../ARCHITECTURE]] 를 보세요.

## 폴더 구조

```
00. Inbox/                      ← 분류 전 임시 메모, 아이디어
01. Projects/                   ← 프로젝트 폴더
   └── ai-animation-2026/
       ├── _Project Overview.md ← 목표·일정·소스 현황
       ├── Synopsis/            ← 공통 소스 애니메이션 설명
       ├── Setup/               ← 공통 소스 파일 경로 + 파이프라인 세팅
       │   ├── _Source.md
       │   └── _Pipeline.md
       └── Moods/               ← 멤버별 스타일 방향 + 레퍼런스
           ├── Doryong/
           ├── Gupgi/
           └── Sosa/
02. Daily/                      ← 작업 일지 (YYYY-MM-DD-이름.md)
03. Permanent Notes/            ← 프로젝트 후 남길 파이프라인 노하우
04. Meetings/                   ← 회의록 (YYYY-MM-DD-회의명.md)
90. Settings/Templates/         ← 노트 템플릿
```

## 협업 규칙

**팀 공통 편집**
- `01. Projects/ai-animation-2026/Synopsis/`
- `01. Projects/ai-animation-2026/Setup/`
- `01. Projects/ai-animation-2026/_Project Overview.md`

**본인만 편집**
- `01. Projects/ai-animation-2026/Moods/Doryong/` or `Gupgi/` or `Sosa/`
- `02. Daily/YYYY-MM-DD-본인이름.md`

## 그래프 뷰 활용

레퍼런스는 **노트 하나씩** 만든다. `_Style Direction.md`에서 각 노트를 `[[ref-작품명]]`으로 연결하면  
멤버 간 공통 키워드가 그래프에서 자동으로 드러난다.

## 시작하기

1. `01. Projects/ai-animation-2026/_Project Overview` 열기
2. `Moods/Doryong/`, `Moods/Gupgi/`, `Moods/Sosa/` 중 본인 폴더 열기
3. `_Style Direction.md` 작성 시작
4. 작업일마다 `02. Daily/YYYY-MM-DD-이름.md` 생성

## Templates 사용법

1. Settings → Core plugins → **Templates** ON
2. Templates folder: `90. Settings/Templates`
3. 새 노트에서 `Cmd+P` → "Insert template" → 원하는 템플릿 선택
