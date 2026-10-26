# YBM DS 사이트

YBM 디자인 시스템 공식 문서 사이트를 준비하는 저장소다.

## 현재 상태
- **구상 단계, 코드 없음.** 사용자가 "만들어줘"라고 하기 전까지 사이트 코드를 만들지 않는다.
- 먼저 읽을 문서
  - [PLAN.md](PLAN.md): 구상 전체 (구조, 데이터 흐름, 화면 설계, 단계, 정해야 할 것)
  - [REFERENCE-ANALYSIS.md](REFERENCE-ANALYSIS.md): Astryx·SEED 분석

## 사용자가 확정한 것
- IA는 **Docs · Foundations · Components · Templates** 네 가지 (Themes·Playground 메뉴 없음). Foundations는 2026-10-26에 Docs 하위에서 상단 메뉴로 분리했다.
- 화면 구성은 Astryx(<https://astryx.atmeta.com/>)를 아주 가깝게 따르고, 컴포넌트 문서 깊이는 SEED(<https://seed-design.io/>)를 따른다.
- Getting Started는 **Quick Start with AI**(AI 도구에 붙여넣는 프롬프트 + 복사 버튼)로 시작한다.
- 만드는 방식은 정적 HTML + GitHub Pages. 빌드 스크립트가 ybm-ds의 `components.json`과 토큰을 읽어 페이지를 생성한다.

## 데이터 원본
- DS 저장소: <https://github.com/luvms012-rgb/ybm-ds>
- 집 Mac: `~/Works/ybm-ds`
- 회사 윈도우: `C:\Users\luvms\Desktop\works\ds`
- 이 사이트 저장소 위치 — 회사 윈도우: `C:\Users\luvms\Desktop\works\ybm-ds-site`

## Figma
- **공식 DS 파일** (기준 원본, 파일명 "디자인 시스템"): <https://www.figma.com/design/1VCEsFU3xMWuXIntIrZz9i/?node-id=2274-1143>
  - 노드 `2274:1143` = Foundations 페이지. 섹션: Color `2288:63` · Typography `2288:64` · Spacing `2288:67` · Radius `2288:66` · Elevation `2288:65`. 사이트 Foundations 메뉴의 원본이다.
- **레퍼런스 파일** (Astryx Library, Community): <https://www.figma.com/design/36Bw0nKoNyurCJvr4RIsaO/?node-id=266-35168>
  - ybm-ds Figma 구성을 이 화면 기준으로 바꿀 예정. **보류 중** — 사용자가 요청할 때만 시작한다.

## 진행 기록
- 2026-10-26 (회사): ybm-ds `main`을 GitHub(`d4f83b6`)에 맞췄다. 회사 PC에만 있던 커밋 전 작업(10-23 폴더 구조 정리, figma-sync `cssOnly` 수정, `components/index.html` 컴포넌트 메인 시안, 작업 메모)은 **회사 PC 로컬 브랜치 `backup/2026-10-26-local`** 에만 있다(GitHub에 없음). 필요하면 회사 PC에서 꺼낸다.

## 작업 방식
- 집(Mac)과 회사(윈도우)를 오가며 작업한다. 시작할 때 `git pull`, 끝낼 때 commit + push.
- 사용자에게는 한국어로, 쉬운 말로 설명한다.
