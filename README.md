# KARTS AI Animation — 팀 협업 볼트

> ComfyUI를 활용한 AI 애니메이션 제작 팀 프로젝트 (2026)
> 3인 팀 · 하나의 공통 소스 · 각자의 스타일 방향

## 이게 뭔가

하나의 애니메이션 소스를 공유하고, 각자 원하는 방향의 AI 애니메이션을 제작하는 협업 프로젝트.  
이 볼트(`karts-mothership`)는 팀 공유 공간이다. 개인 지식 자산은 각자 로컬에서 관리한다.

## 파이프라인 개요

```
공통 소스 선정
    ↓
Blender → Depth + Outline pass 추출
    ↓
Z-Image Turbo로 레퍼런스 프레임 생성
    ↓
각자 스타일 레퍼런스 준비
    ↓
WAN VACE + SkyReels V3로 각자 방향 렌더링
```

## 폴더 구조

```
beol_zip/
├── README.md           ← 지금 여기
├── ARCHITECTURE.md     ← 볼트 설계 설명
├── INSTALL.md          ← Obsidian 설치 가이드
└── karts-mothership/   ← 팀 공유 볼트
    ├── 00. Inbox/          ← 임시 메모, 아이디어
    ├── 01. Projects/
    │   └── ai-animation-2026/
    │       ├── _Project Overview.md
    │       ├── Synopsis/       ← 공통 소스 애니메이션 설명
    │       ├── Setup/          ← 공통 소스 파일 경로 + 파이프라인 세팅
    │       └── Moods/          ← 멤버별 스타일 방향 + 레퍼런스
    │           ├── Doryong/
    │           ├── Gupgi/
    │           └── Sosa/
    ├── 02. Daily/          ← 작업 일지
    ├── 03. Permanent Notes/ ← 프로젝트 후 남길 노하우
    ├── 04. Meetings/       ← 회의록
    └── 90. Settings/Templates/
```

## 협업 규칙

| 폴더 | 누가 편집하나 |
|------|------|
| `Setup/` | 팀 공통 — 누구나 |
| `Synopsis/` | 팀 공통 — 누구나 |
| `Moods/Doryong/` `Moods/Gupgi/` `Moods/Sosa/` | 본인 폴더만 |
| `02. Daily/` | 각자 본인 날짜 파일만 |

## 빠른 시작

1. **Obsidian 설치**: https://obsidian.md
2. **이 저장소 클론**
3. **Obsidian에서 볼트 열기**: "Open folder as vault" → `karts-mothership` 선택
4. **`01. Projects/ai-animation-2026/_Project Overview` 열기**
5. **본인 `Moods/Doryong/`, `Moods/Gupgi/`, `Moods/Sosa/` 중 해당 폴더에서 작업 시작**

자세한 설치 가이드는 [[INSTALL]].

## 설치 필요 사항

- [Obsidian](https://obsidian.md)
- [ComfyUI](https://github.com/comfyanonymous/ComfyUI)
- [Blender](https://www.blender.org)
- VACE SkyReels V3 모델 (세팅은 `Setup/_Pipeline` 참조)
