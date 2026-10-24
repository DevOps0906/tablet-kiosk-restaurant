# DESIGN — 식당 키오스크

> 공통 디자인 시스템은 core `DESIGN.md`. 이 문서는 식당 테마와 화면 목록입니다.

## 1. 식당 테마 토큰

| 토큰 | 값 |
|---|---|
| `primary` | `#007A64` |
| `primary-strong` | `#00473A` |
| `primary-tint` | `#E3F7F2` |
| `accent` | `#00C9A7` |
| `ink` | `#12201D` |
| `ink-muted` | `#4A5B57` |
| `background` | `#F4F8F7` |
| `line` | `#D5E2DE` |
| `discount` | `#C81E3F` |

공통 토큰(더치페이 파랑 `#2563EB`, 안내 노랑 `#FEF3D7` 등)은 core `DESIGN.md` 2장.

## 2. 식당 문구

| 항목 | 값 |
|---|---|
| 번호 이름 | 호출번호 (예: `A-017`) |
| 번호 규칙 | `A-001`부터 매일 다시 시작 (접두어 설정 가능) |
| 완료 후 처음 화면 | 30초 뒤 |

## 3. 화면 목록

### 손님 — 스탠드형 (세로 800×1280)

| 화면 | 원본 | 미리보기 |
|---|---|---|
| HW 00 시작 화면 (매장/포장) | [`00-start`](design/00-start.dc.html) | [PNG](screenshots/00-start.png) |
| HW 01 메뉴 선택 (갈비) | [`Main`](design/Main.dc.html) | [PNG](screenshots/Main.png) |
| HW 01-2 주류 · 음료 | [`01b-drinks`](design/01b-drinks.dc.html) | [PNG](screenshots/01b-drinks.png) |
| HW 02 주문 확인 | [`02-cart`](design/02-cart.dc.html) | [PNG](screenshots/02-cart.png) |
| HW 03 결제 방법 선택 · 쿠폰 | [`03-pay-method`](design/03-pay-method.dc.html) | [PNG](screenshots/03-pay-method.png) |
| HW 04 더치페이 (메뉴별 · 인분) | [`04-dutch`](design/04-dutch.dc.html) | [PNG](screenshots/04-dutch.png) |
| HW 05 주문 완료 · 주방 주문서 | [`05-done`](design/05-done.dc.html) | [PNG](screenshots/05-done.png) |

### 손님 — 갤럭시탭형 (가로 1280×800)

| 화면 | 원본 | 미리보기 |
|---|---|---|
| SW 00 시작 화면 (매장/포장) | [`sw-00-start`](design/sw-00-start.dc.html) | [PNG](screenshots/sw-00-start.png) |
| SW 01 메뉴 선택 (갈비) | [`sw-01-menu`](design/sw-01-menu.dc.html) | [PNG](screenshots/sw-01-menu.png) |
| SW 01-2 주류 · 음료 | [`sw-01b-drinks`](design/sw-01b-drinks.dc.html) | [PNG](screenshots/sw-01b-drinks.png) |
| SW 02 주문 확인 | [`sw-02-cart`](design/sw-02-cart.dc.html) | [PNG](screenshots/sw-02-cart.png) |
| SW 03 결제 방법 선택 · 쿠폰 | [`sw-03-pay`](design/sw-03-pay.dc.html) | [PNG](screenshots/sw-03-pay.png) |
| SW 04 더치페이 (인분 · 메뉴별) | [`sw-04-dutch`](design/sw-04-dutch.dc.html) | [PNG](screenshots/sw-04-dutch.png) |
| SW 05 주문 완료 · 주방 주문서 | [`sw-05-done`](design/sw-05-done.dc.html) | [PNG](screenshots/sw-05-done.png) |

### 사장님 세팅 — 갤럭시탭형

| 화면 | 원본 | 미리보기 |
|---|---|---|
| SW 세팅 1 사장님 시작 | [`set-01-start`](design/set-01-start.dc.html) | [PNG](screenshots/set-01-start.png) |
| SW 세팅 2 매장 정보 | [`set-02-store`](design/set-02-store.dc.html) | [PNG](screenshots/set-02-store.png) |
| SW 세팅 3 메뉴 등록 | [`set-03-menu`](design/set-03-menu.dc.html) | [PNG](screenshots/set-03-menu.png) |
| SW 세팅 4 결제 단말 · 프린터 연결 | [`set-04-devices`](design/set-04-devices.dc.html) | [PNG](screenshots/set-04-devices.png) |
| SW 세팅 5 키오스크 모드 | [`set-05-kiosk`](design/set-05-kiosk.dc.html) | [PNG](screenshots/set-05-kiosk.png) |

### 쿠폰

| 화면 | 원본 | 미리보기 |
|---|---|---|
| 쿠폰 1 사장님 쿠폰 관리 대시보드 (반응형) | [`coupon-dashboard`](design/coupon-dashboard.dc.html) | [PNG](screenshots/coupon-dashboard.png) |
| 쿠폰 2 사장님 쿠폰 발행 (반응형) | [`coupon-create`](design/coupon-create.dc.html) | [PNG](screenshots/coupon-create.png) |
| 쿠폰 3 손님 · 스탠드형 시리얼 입력 | [`hw-coupon-serial`](design/hw-coupon-serial.dc.html) | [PNG](screenshots/hw-coupon-serial.png) |
| 쿠폰 4 손님 · 스탠드형 바코드 스캔 | [`hw-coupon-scan`](design/hw-coupon-scan.dc.html) | [PNG](screenshots/hw-coupon-scan.png) |
| 쿠폰 5 손님 · 갤럭시탭 시리얼 입력 | [`sw-coupon-serial`](design/sw-coupon-serial.dc.html) | [PNG](screenshots/sw-coupon-serial.png) |
| 쿠폰 6 손님 · 갤럭시탭 바코드 스캔 | [`sw-coupon-scan`](design/sw-coupon-scan.dc.html) | [PNG](screenshots/sw-coupon-scan.png) |

### 기획 문서 (참고용)

| 화면 | 원본 | 미리보기 |
|---|---|---|
| 07 결제 단계 플로우차트 | [`07-flow`](design/07-flow.dc.html) | [PNG](screenshots/07-flow.png) |
| 08 시스템 구조도 | [`08-structure`](design/08-structure.dc.html) | [PNG](screenshots/08-structure.png) |
| 06 반응형 구간 · 폰트 기준 | [`06-responsive`](design/06-responsive.dc.html) | [PNG](screenshots/06-responsive.png) |
| 설치 방식 비교 (HW vs SW) | [`install-compare`](design/install-compare.dc.html) | [PNG](screenshots/install-compare.png) |

## 4. 식당 전용 컴포넌트

| 컴포넌트 | 설명 | 디자인 |
|---|---|---|
| `AlcoholBanner` | 주류 · 음료 분류 상단 19세 안내 | `01b-drinks` |
| `AdultBadge` | 메뉴 카드 `19` 배지 | `01b-drinks` |
| `PortionStepper` | 인분 − + (최소 인분 표시) | `Main`, `02-cart` |
| `PortionSplitList` | 더치페이 메뉴별 인분 배정 목록 | `04-dutch` |

공통 컴포넌트는 core `DESIGN.md` 6장.

## 5. 디자인과 명세 차이

| 화면 | 디자인 원본 | 구현 기준 |
|---|---|---|
| `set-03-menu` 메뉴 등록 | 분류 칩 `찌개·탕` | `찌개 · 탕` 표기 통일 |
| 시작 화면 | `한국어 · English`, `큰 글씨 · 낮은 화면` 버튼 | MVP에서는 숨김 (core D8, task-026) |
