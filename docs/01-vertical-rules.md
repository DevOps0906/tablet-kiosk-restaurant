# 01 식당 업무 규칙

> 코드 위치: `tablet-kiosk-core/apps/kiosk/lib/verticals/restaurant/`. 확장 지점 정의는 core `docs/08-vertical-module.md`.

## 업무 규칙

### 1. 인분 단위 주문

- 고기 메뉴는 수량 대신 **인분**으로 표시 (`돼지갈비 3인분`)
- 최소 인분(기본 2인분) 미만이면 장바구니에서 안내하고 결제 진행 불가
- 추가 주문(같은 테이블 두 번째 주문)도 1인분부터 가능 — 첫 주문 여부는 MVP에서 구분하지 않음 (결정 필요)

### 2. 주류 · 음료

- 분류 이름 `주류 · 음료`, 분류 상단 배너: **"주류는 만 19세 이상만 주문 가능 · 가져다 드릴 때 직원이 신분증을 확인해요"**
- 주류 메뉴 카드에 `19` 배지
- 주류를 담으면 주문서에 `★주류 · 신분증 확인★` 줄 인쇄
- 키오스크에서 나이 인증은 하지 않음 (직원 확인 방식)

### 3. 식사 메뉴

- 된장찌개는 고기 주문이 있을 때만 담을 수 있음 (`requires_meat`)
- 물냉면 등 식사는 주방 메모 "고기 후 제공" 표시 가능

### 4. 더치페이

- 방식: N등분 · 메뉴별(인분) · 금액
- **메뉴별**: 고기는 1인분 단위로 쪼개 결제자에게 배정 (`돼지갈비 1인분 · 3인분 중 2번째`)
- 식사 · 음료는 1개(그릇 · 병) 단위로 배정

### 5. 주방 주문서

- 고기 · 식사 · 찌개 분류(`kitchen_group`)별로 나눠 출력 가능 (주방 프린터 분류 설정)
- 맨 위 `A-017 매장` (2배 크기), 고기는 인분으로 표기
- 결제 정보 줄: `결제 3건 · 더치페이 접수 14:32`

## 확장 지점 구현

| 확장 지점 | 식당 구현 |
|---|---|
| `theme` | 제이드 그린 테마 |
| `preset` | 고기 · 식사 · 찌개 · 탕 · 주류 · 음료 분류 + 위 예시 메뉴 |
| `labels` | `호출번호`, 완료 문구 "주방으로 주문서가 전송됐어요" |
| `menuCardDecorator` | 주류 `19` 배지, 인분 표기, 인기 배지 |
| `categoryBanner` | 주류 · 음료 분류의 19세 안내 |
| `itemConfigurator` | 고기: 인분 수 선택 (기본 최소 인분) |
| `cartRules` | 최소 인분, `requires_meat` |
| `splitOptions` | 메뉴별 분할에서 인분 단위 쪼개기 |
| `printBlocks.kitchen` | 분류별 분할, 주류 신분증 확인 줄 |
| `doneScreenExtras` | 호출번호 안내 |
| `setupExtras` | 호출번호 시작값, 고기 최소 인분, 주방 프린터 분류 매핑 |

정의하지 않은 확장 지점은 기본 구현(아무것도 안 함)을 씁니다.

## 데이터 키 (`vertical_attrs` · `vertical_data`)

| 위치 | 타입 | 뜻 |
|---|---|---|
| `menu_items.vertical_attrs.portion_unit` | string | 표시용 단위 (`1인분 250g`) |
| `menu_items.vertical_attrs.min_portions` | int | 최소 주문 인분 (기본 2, 세팅 5단계에서 켜고 끔) |
| `menu_items.vertical_attrs.is_alcohol` | bool | 주류 여부 → 19 배지, 안내 |
| `menu_items.vertical_attrs.requires_meat` | bool | 고기 주문 시에만 담기 (된장찌개) |
| `order_items.kitchen_group` | string | 주방 출력 분류 (고기 · 식사 · 찌개) |

새 키를 추가하면 이 표를 먼저 고칩니다. 조회 · 집계가 많아지면 core에서 컬럼으로 승격합니다.
