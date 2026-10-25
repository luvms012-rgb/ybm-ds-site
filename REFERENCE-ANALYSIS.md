# YBM 디자인 시스템 사이트 — 레퍼런스 분석

- 작성: 2026-10-25
- 레퍼런스: Astryx (<https://astryx.atmeta.com/>), SEED (<https://seed-design.io/>)
- 확정된 방향
  - 최상위 IA는 **Docs · Components · Templates** 세 가지로 한다.
  - Getting Started는 Astryx처럼 **Quick Start with AI**로 시작한다.

---

## 0. 한 줄 결론

**뼈대와 화면 구성은 Astryx, 컴포넌트 문서 내용의 깊이는 SEED**를 따른다.
YBM DS는 이미 SEED와 같은 체계를 쓴다. 예를 들어 Action Button의 variant 이름이 SEED와 똑같다. 그래서 SEED의 문서 항목(Anatomy, Properties, Guidelines, Specification)이 그대로 맞는다.

---

## 1. Astryx 분석 (메인 레퍼런스)

### 1-1. 공통 화면 틀 (셸)

| 영역 | 내용 |
|---|---|
| 상단 바 | 높이 48px, 반투명 흰색(80%)에 블러. 왼쪽 로고, 가운데 메뉴(Docs, Components, Templates, Themes, Playground), 오른쪽 검색·다크모드·Discord·GitHub 아이콘과 검정 `Get started` 버튼 |
| 왼쪽 사이드바 | 너비 260px. 그룹 제목이 있고 그룹은 접힌다. 항목 14px/20, 선택된 항목은 굵게(600)에 둥근 배경(12px) |
| 본문 | 너비 800px |
| 오른쪽 목차 | 너비 232px, 스크롤해도 따라온다(sticky). Docs 페이지에만 있고 컴포넌트 상세에는 없다 |
| 글꼴 | Figtree. H1 42/52 600, H2 29/36 600, 본문 17/28, 리드 문장 17/24 회색(#4E606F) |
| 검색 | 상단 돋보기 → 화면 가운데 커맨드 팔레트. 하단에 단축키 안내(↑↓ 이동, ↵ 선택, Esc 닫기) |
| 기타 | 다크 모드 토글, "본문 바로가기" 링크. 기술 스택은 Next.js, React 19, StyleX |

### 1-2. 홈

1. **히어로**: 큰 로고타입, 한 줄 소개(2줄), CTA 2개(`Get started` 검정, `Browse components` 회색), 기술 스택 문구가 있다. 양옆에 실제 컴포넌트로 만든 예시 카드가 떠 있고, 아래 점 표시로 넘기는 캐러셀이다.
2. **벤토 그리드**: 왼쪽에 "Start anywhere. Change anything. Ship faster." 문구, 그 옆에 카드 4장(테마, 180+ 컴포넌트, 에이전트용 DS, 템플릿)이 있다. 카드마다 연한 배경, 제목, 설명, 실제 컴포넌트 미리보기와 `Explore →` 링크로 구성된다.
3. **수치 + 3열**: "Astryx powers over 13,000 apps" 아래로 3열(Design for speed / Built by the people who use it / Ready for what's next)이 있고, 각 열에 링크가 있다.
4. **소식**: "Stay in the know"에 큰 카드 1장과 작은 카드 2장(블로그·릴리스)을 둔다.
5. **마무리 CTA 배너**: "Discover the full design system"과 버튼 2개.
6. **푸터**: 로고, 한 줄 링크, 소셜 아이콘, 저작권으로 간결하다.

### 1-3. Docs

**사이드바 그룹**
- Documentation: Getting Started, What's New
- Guide(18개): Authoring, Browser support, Layout, Migration, Principles, Styling, Theming, Working with AI 등
- Foundations: All Tokens, Color, Elevation, Icons, Illustrations, Motion, Shape, Spacing, Typography
- Libraries: 패키지별 문서(cli, core, richtext)

**Getting Started 페이지 순서**
1. H1과 리드 문장 한 줄
2. **Quick Start with AI**: "AI 코딩 도구에 이걸 붙여넣으세요" 안내 아래 **라벨이 달린 프롬프트 상자 2개**가 있다(① "Set up the design system", ② "Give it a look"). 각 상자 오른쪽 위에 복사 버튼이 있다.
3. Install: 단계별 설치(한 번 설치, 기본 CSS·테마 추가, 첫 컴포넌트, 커스터마이즈)
4. Example Apps, Explore the CLI
5. 오른쪽 목차에 위 단계가 그대로 나온다.

### 1-4. Components

**개요 페이지 (`/components`)**
- 사이드바 맨 위에 **"Search components" 입력창**이 있다. 그 아래 컴포넌트 목록이 있고, 하위 컴포넌트가 있으면 펼쳐진다(예: Button → Button Group, Icon Button, Toggle Button).
- 본문 위쪽에는 가운데 정렬된 "Browse the library", 설명 한 줄, 버튼 2개(`Install core library`, `View Figma`)가 있다.
- **카테고리별 3열 카드**: Action, Chat, Container, Content, Feedback & Status, Form Controls, Layout, Navigation, Overlay, Table & List, Utility. 카드는 회색 영역 안의 실제 렌더링 미리보기와 아래 이름으로 이뤄진다.

**상세 페이지 (`/components/Button`)**
- H1 아래에 패키지·버전 메타(예: `@astryxdesign/core v0.7.4 · Button`)가 한 줄 있다.
- **탭 3개: Overview / Properties / Accessibility**. URL에 `?tab=properties`가 붙어서 링크로 공유할 수 있다.
- **Overview**: 큰 미리보기 → Usage → Anatomy → **Best practices**(Do/Don't 배지가 붙은 표) → **Examples**
  - 예제 카드는 제목, 미리보기, `Description | Code` 전환, `Open in Playground`로 구성된다.
- **Properties**: 위쪽에 라이브 미리보기가 있고, 아래 **Props 표**는 Required와 Optional로 나뉜다. 열은 이름·타입·설명이고, 오른쪽 컨트롤에서 값을 바꾸면 미리보기가 즉시 바뀐다.
- **Accessibility**: 색 대비 요구사항 표(요구·비율·적용 상태·가이드·WCAG 조항)가 있다.

### 1-5. Templates

- 가운데 정렬 제목 "Templates"와 설명 한 줄이 있다.
- **필터 칩**: All, Dashboard, Table, Form, Settings, Login, Tools, Content, AI Chat, Gallery, Shell
- **3열 카드 51종**: 실제 페이지를 축소한 썸네일과 이름으로 구성된다.
- 카드를 클릭하면 **미리보기 모달**이 열린다(`?preview=dashboard`). 모달에는 제목, 설명, 실제 페이지가 있고, 하단에 CLI 명령 복사 버튼과 `Open in Playground`가 있다.

---

## 2. SEED 분석 (내용 레퍼런스)

### 2-1. 공통 화면 틀

- 상단 바 높이 76px, 고정. 메뉴는 Get Started, Foundations, Components, Patterns, Develop ▾(React, Lynx), AI & Tools, Updates이다. 오른쪽에 다크모드와 검색이 있다.
- 사이드바 240px, 오른쪽 "목차". 글꼴은 **Pretendard Variable**로, YBM DS와 같다.

### 2-2. 홈 — 연출 중심

인트로 영상 → 영상과 이미지로 만든 벤토 → 검은 배경의 "당근의 디자인 시스템 SEED" → 디자인 원칙 스크롤 연출 → 파운데이션 쇼케이스 카드(가로 스크롤) → "SEED가 자라나는 과정" 블로그 카드 → 오렌지 푸터와 대형 로고 순서다.
부드러운 스크롤(Lenis)과 커스텀 커서를 쓰고, 글자 대부분이 이미지·영상 안에 있다. **보기엔 좋지만 만들고 고치는 비용이 커서 홈은 Astryx 방식을 권장한다.**

### 2-3. Components

- **개요**: 큰 H1, 설명, 3열 카드(썸네일과 이름). 사이드바에는 Overview, Progress Board, 알파벳순 컴포넌트, "추천 문서" 점 표시, Deprecated가 있다.
- **상세(디자인 문서)**. 이 구성이 YBM에 가장 쓸모 있다.
  - 상단: 분류(Components), **LLMS.txt** 버튼, H1, 설명, **플랫폼 지원 배지**(Figma · React · Lynx · iOS · Android ✓)
  - Anatomy
  - Properties: Size, Layout, Variant, State, Width
  - Guidelines: 위계 표(강조 수준·Variant·화면 내 개수·용도), Do/Don't 이미지, 조합·배치·라벨 작성법
  - 비교(예: Action Button vs Chip), 더 알아보기
  - **Specification**: variant·size별 토큰 값 표
  - 페이지가 아주 길어서(약 30,000px) 오른쪽 목차가 꼭 필요하다.
- **디자인 문서(`/components/...`)와 개발 문서(`/react/components/...`)를 분리**한다.

### 2-4. 기타 섹션

- Foundations: Design Token, Color, Typography, Iconography, Elevation, Gradient, Inclusive Design, International Design, Layout, Motion, Radius, Spacing, State, Voice and Tone, Writing, Feedback
- Patterns: Loading, Safe Area
- AI & Tools: llms.txt, Skill, Doctor, MCP, Figma MCP, Docs MCP

---

## 3. 현재 YBM DS와 연결되는 점

| 이미 있는 것 | 사이트에서 쓰는 곳 |
|---|---|
| `components.json`: 47종의 이름, CSS 클래스, Figma 노드 ID, props | Components 사이드바, 개요 카드, 상세 페이지 상단을 **자동 생성** |
| `tokens.css`: palette 303, bg 64, fg 27, stroke 22, font-size/line-height 각 51, radius, shape, space, elevation, z-index | Foundations 페이지(All Tokens, Color, Typography 등)의 표와 견본 |
| `index.html`: 48종을 한 페이지에 미리보기, Light/Dark, Shape 전환 | 컴포넌트별 미리보기·예제로 나눠 상세 페이지에 넣음 |
| `data-theme="dark"`, `data-shape` | 상단 바의 다크모드·Shape 토글 |
| `ybm-ds.js`: Dialog, Snackbar, Slider 등 | 예제가 실제로 동작 |
| README: 사용법, Cascade Layers, 커스텀 규칙, 동기화 | Docs > Guide 페이지 원고 |
| ybm-guide의 `cs`(고객센터), `signup`(회원가입) 화면 | Templates 첫 후보 |

YBM DS는 React 패키지가 아니라 **CSS + 작은 JS**이다. 그래서 Astryx의 `Code` 탭과 Props 표는 **HTML 스니펫과 클래스·속성 표**로 바꿔 쓴다.

---

## 4. 제안 IA (Docs · Components · Templates)

### Docs
- **시작하기**: Getting Started(Quick Start with AI → 설치 → 첫 컴포넌트), 새 소식
- **가이드**: 사용법, Cascade Layers, 커스텀 규칙(`--ds-*` 변수), 테마·Shape, JS 기능, Figma 동기화·기여 방법
- **Foundations**: All Tokens, Color, Typography, Spacing, Radius·Shape, Elevation, Icons
- **리소스**: Figma 파일, GitHub, llms.txt

### Components
- 개요: 카테고리별 카드
- 상세: 탭 3개(Astryx). 탭 안의 내용은 SEED 깊이로 채운다.
  - **Overview**: 미리보기, 설명, Anatomy, Variant·Size·State, 가이드라인(Do/Don't), 예제(미리보기 + HTML 복사)
  - **Properties**: 클래스·속성·`--ds-*` 변수 표, 값을 바꿔 보는 라이브 미리보기, Specification(토큰 값)
  - **Accessibility**: 대비·키보드·스크린리더 요구사항
- 상단 배지: Figma ✓ · HTML/CSS ✓ (SEED의 플랫폼 배지 방식)

**47종 카테고리 배정안 (Astryx 카테고리 기준)**

| 카테고리 | 컴포넌트 |
|---|---|
| Action | Action Button, Text Link, Floating Action Button, Toggle Button, Chip |
| Form Controls | Field Label, Text Field Input, Text Field Textarea, Field Button, Prefix Select, Select Trigger, Select Content·Item, Checkbox, Radio Group, Switch, Quantity Picker, Slider, Date Picker |
| Navigation | Tabs, Chip Tabs, Segmented Control, Bottom Navigation, Side Navigation, Pagination, Breadcrumbs, Stepper |
| Content | Badge, Tag Group, Avatar, Card, Divider |
| Feedback & Status | Callout, Snackbar, Banner, Skeleton, Progress, Progress Circle, Empty |
| Overlay | Help Bubble, Tooltip, Menu·Menu Item, Dialog, Alert Dialog, Bottom Sheet |
| Container | Accordion |
| Table & List | Table, List·List Item |

### Templates
- 필터 칩, 3열 카드 썸네일, 미리보기 모달(복사·새 창 열기)
- 초기 후보: 회원가입, 고객센터(ybm-guide에서 가져옴), 로그인, 마이페이지, 결제·신청 폼, 목록·테이블, 빈 화면·오류

Astryx의 Themes와 Playground는 최상위 메뉴에서 뺀다. Playground 기능은 컴포넌트 Properties 탭의 라이브 미리보기와 템플릿 미리보기 모달로 대신한다.

---

## 5. 정해야 할 것

1. **홈 구성**: Astryx식 가벼운 히어로 + 벤토를 권장한다. SEED식 영상 연출은 제작·유지 비용이 크다.
2. **기술 방식**
   - 지금처럼 정적 HTML을 GitHub Pages에 올리고, `components.json`·`tokens.css`를 읽어 빌드 스크립트로 페이지를 생성하는 방식
   - Next.js 등 프레임워크를 쓰는 방식

   DS가 순수 CSS라 앞의 방식으로도 충분하다.
3. **Quick Start with AI 프롬프트 내용**: npm 패키지가 없다. 그래서 "이 CSS·JS 링크를 넣고, `--ds-*` 변수만 바꾸고, 클래스 신설·`!important` 금지" 같은 YBM 규칙을 프롬프트로 만들고 `llms.txt`를 함께 제공한다.
4. **공개 범위·호스팅**: 공식 사이트라면 회사 도메인·승인 여부를 정해야 한다. 지금 저장소는 공개 상태다.
5. **브랜드 에셋**: YBM 로고, 히어로 이미지, 국문/영문 표기.
6. **"아주 유사하게"의 범위**: 레이아웃·구성·인터랙션 패턴은 참고해도 된다. 다만 Astryx·SEED의 로고, 문구, 이미지, 일러스트는 가져오지 않고 YBM 것으로 만든다.
