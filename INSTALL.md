# 설치 가이드 (10분)

## 1. Obsidian 설치

- https://obsidian.md → 본인 OS 용 다운로드
- 무료, Mac / Windows / Linux / iOS / Android 모두 가능

## 2. 스타터킷 압축 풀기

- `karts-starter-kit.zip` 을 받았다면 원하는 위치에 풀기
- 권장 위치: `~/Documents/karts/`, `~/Obsidian/karts/` 등

압축 풀면 다음 구조:
```
karts-starter-kit/
├── README.md
├── ARCHITECTURE.md
├── INSTALL.md  ← 지금 여기
├── karts-mothership/   ← 마더십 볼트
└── karts-satellite/    ← 새틀라이트 볼트
```

## 3. 두 볼트 열기

### 마더십 볼트 열기
1. Obsidian 실행
2. 화면 우하단 *Open another vault* 클릭 (또는 첫 실행이면 환영 화면)
3. *Open folder as vault* 클릭
4. `karts-mothership/` 폴더 선택 → Open
5. *"Trust author and enable plugins"* 묻는 다이얼로그 나오면 **Trust**

### 새틀라이트 볼트 열기 (별도 창)
1. 마더십이 열린 상태에서 메뉴 **File → Open another vault** 또는 좌하단 볼트 스위처
2. *Open folder as vault* → `karts-satellite/` 선택
3. **New window** 옵션 체크 → Open (두 창이 동시에 열림)

## 4. 첫 5분 — 둘러보기

### 마더십 쪽
- 좌측 파일 트리에서 `01. Projects/_sample-project/` 펼치기
- `_Project Overview` 클릭 → 샘플 작품 노트 보기
- 우상단 **Open Graph View** (🕸 아이콘) → 작품 노트들의 연결 확인

### 새틀라이트 쪽
- `10. Wiki/Concepts/_sample 사실주의 미학` 열기
- `00. Raw Sources/_sample 스크랩` 열기 → frontmatter 확인
- `20. Queries/_sample 우울한 분위기 모음` 열기

## 5. 권장 플러그인 설치 (수업 진행과 함께)

> 수업 회차마다 필요한 플러그인을 그때그때 활성화합니다. 미리 다 설치하지 마세요.

### 1회차 (5/14) 까지 — Core 플러그인만
- Obsidian 기본 설치 시 들어있는 것들로 충분
- **Templates** 코어 플러그인은 켜둘 것 (Settings → Core plugins → Templates ON)
- Templates 폴더 지정: `90. Settings/Templates`

### 2회차 (5/21) 전에 — Community 플러그인 4종
Settings → Community plugins → Turn on community plugins → Browse 에서:
1. **Dataview** — 자료 쿼리·집계
2. **Templater** — 고급 템플릿 (선택)
3. **Excalidraw** — 손그림 다이어그램
4. **Image Toolkit** — 이미지 확대 미리보기

### 3회차 (5/28) 전에 — AI 플러그인
1. **Smart Connections** — 유사도 기반 자동 연결·검색
2. **Copilot (by Logan Yang)** — 채팅 인터페이스로 볼트 쿼리 (선택)

## 6. (선택) 동기화 설정

본인 데이터를 백업·여러 기기 동기화하려면:

| 방법 | 비용 | 난이도 |
|------|------|------|
| Obsidian Sync | 월 $4 | ★ (가장 쉬움) |
| iCloud Drive 폴더에 두기 | 무료 | ★★ |
| Git + GitHub Private Repo | 무료 | ★★★ |
| Dropbox/Google Drive | 무료/유료 | ★★ (충돌 가능) |

## 7. (선택) AI 도구 계정

3회차에서 라이브로 쓸 LLM 도구:
- **ChatGPT** (무료 또는 Plus $20/월): https://chatgpt.com
- **Claude** (무료 또는 Pro $20/월): https://claude.ai
- 둘 중 하나만 있어도 충분. 가능하면 Plus/Pro 권장 (긴 컨텍스트).

## 8. 문제 발생 시

- 강의 중에는 손 들고 질문
- 강의 외 시간엔 단톡/메일로 (강의 첫날 안내)
- Obsidian 공식 포럼: https://forum.obsidian.md (영어)
- Obsidian 한국 사용자 모임 (검색)

## 첫 회차 (5/14) 전 체크리스트

- [ ] Obsidian 설치 완료
- [ ] 스타터킷 압축 풀기 완료
- [ ] 마더십 볼트 열기 성공
- [ ] 새틀라이트 볼트 열기 성공
- [ ] 샘플 노트 1개 이상 열어봄
- [ ] 본인 작품 자료 *10개 정도* 폴더에 모아두기 (1회차 시 인박스에 옮겨올 것)

준비 끝. 5/14 19:00 영상원에서 만나요.
