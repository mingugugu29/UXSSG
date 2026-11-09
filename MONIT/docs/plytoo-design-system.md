# plytoo Design System

> Wanted Design System 기반 · 브랜드 컬러 교체 사양 · v1.0 · 2026-10-23

## 1. 기준과 적용 범위

plytoo는 첨부된 `Wanted Design System.fig`의 디자인 시스템을 기반으로 한다. **브랜드 표현에 쓰이는 색상만 Violet, Lime, Pink로 교체하고, 나머지 디자인 규칙은 원본을 상속한다.**

- Primary: Violet — 핵심 액션과 브랜드 인지.
- Secondary: Lime — 보조 강조와 브랜드 포인트.
- Tertiary: Pink — 세 번째 강조와 보조 콘텐츠 구분.
- 브랜드 배색의 기준은 마지막 첨부 이미지의 PLYTOO 보드다. 큰 바이올렛 면과 화이트 로고, 작은 라임·핑크 면, 짙은 바이올렛 면으로 구성한다.
- 팔레트 수치는 첨부한 세 팔레트 이미지의 **RGB 표기**를 기준으로 하며 HEX는 이를 변환한 값이다. 이미지의 렌더링 색상과 숫자가 다르면 숫자를 우선한다.

이 문서는 원본 전체 컴포넌트를 재직렬화한 덤프가 아니라, **원본을 상속하는 plytoo 디자인 시스템의 브랜드 오버라이드 명세**다. 원본 바이너리에서 토큰 이름과 설명 문자열을 확인했으며, 모든 노드의 수치·변수 연결을 완전히 디코딩한 것은 아니다. 변경하지 않는 속성의 정확한 값은 첨부 `.fig`를 기준으로 한다. 아래 새 팔레트와 매핑은 plytoo용 정의이며 원티드의 기존 값으로 해석하지 않는다.

## 2. 유지하는 원본 규칙

| 영역 | plytoo 적용 |
| --- | --- |
| Typography | 원본의 폰트, 크기, 굵기, 행간, 자간, 텍스트 스타일 유지 |
| Layout | 그리드, 간격, 패딩, 정렬, 반응형·플랫폼별 규칙 유지 |
| Shape | 모서리 반경, 테두리 두께, 컴포넌트 크기 유지 |
| Effect | 그림자, 블러, 불투명도, 상호작용 효과 유지 |
| Components | 구조, variant, 상태, 아이콘, 동작 유지. 브랜드 색상 참조만 변경 |
| Neutral | Common, Neutral, Cool Neutral 계열 원본 유지 |
| Semantic | Label, Background, Line, Fill, Interaction, Status, Static 등 비브랜드 의미 유지 |
| Theme | 원본 Light/Dark 모드 구분과 비브랜드 값 유지 |

원본에서 확인한 `Display`, `Title`, `Heading`, `Headline`, `Body`, `Label`, `Caption` 계열을 새로운 타이포그래피 체계로 대체하지 않는다. 기존 텍스트 스타일에 연결된 폰트를 임의로 교체하지 않는다.

### 반드시 구분할 것

- 브랜드 Primary와 버튼의 Primary variant는 관련되지만, Secondary 브랜드 컬러가 모든 보조 버튼에 자동 적용되는 것은 아니다. 원본에서 중립색인 보조 버튼은 그대로 유지한다.
- Lime은 브랜드 보조색이다. `Status/Positive`를 Lime으로 치환하지 않는다.
- Pink는 브랜드 세 번째 색이다. `Status/Negative`를 Pink로 치환하지 않는다.
- Violet 900은 브랜드 그래픽의 짙은 면이다. 앱의 기본 배경이나 모든 본문 색상을 Violet 900으로 바꾸지 않는다.
- 원본 Blue를 HEX 검색으로 일괄 교체하지 않는다. 브랜드 Primary 참조인지 먼저 구분한다.

## 3. 브랜드 대표색

| 역할 | 팔레트 토큰 | HEX | 적용 |
| --- | --- | --- | --- |
| Primary | Violet/500 | #6155F5 | 대표 브랜드 면, 주요 액션 |
| Secondary | Lime/300 | #B9F36B | 라임 포인트 면, 보조 브랜드 강조 |
| Tertiary | Pink/400 | #F56F98 | 핑크 포인트 면, 세 번째 브랜드 강조 |
| Deep primary | Violet/700 | #3C319F | 깊이감 있는 브랜드 보조 면 |
| Dark primary | Violet/900 | #1F1A51 | 가장 짙은 브랜드 면 |

Lime과 Pink의 대표색은 일괄적으로 500을 쓰지 않는다. 마지막 배색 이미지의 밝은 라임과 핑크에 맞춰 각각 300과 400을 선택했다. 화면 전체의 사용 비율을 새 규칙으로 강제하지 않는다.

## 4. Primitive palette

원본의 Atomic 팔레트와 숫자 체계가 충돌하지 않도록 새 팔레트는 `Plytoo/Palette/{Family}/{Step}` 이름으로 구분한다. 50–900은 첨부 이미지의 명명법이며 원본 0–100 계열과 번호를 직접 대응시키지 않는다. 이 30개 값은 Light/Dark에서 동일한 원시 색상이다.

### Violet

| 토큰 | HEX | RGB |
| --- | --- | --- |
| `Plytoo/Palette/Violet/50` | `#F6F5FF` | 246, 245, 255 |
| `Plytoo/Palette/Violet/100` | `#EDEAFF` | 237, 234, 255 |
| `Plytoo/Palette/Violet/200` | `#D8D3FF` | 216, 211, 255 |
| `Plytoo/Palette/Violet/300` | `#B6ADFF` | 182, 173, 255 |
| `Plytoo/Palette/Violet/400` | `#8F82FF` | 143, 130, 255 |
| `Plytoo/Palette/Violet/500` | `#6155F5` | 97, 85, 245 |
| `Plytoo/Palette/Violet/600` | `#4D40C7` | 77, 64, 199 |
| `Plytoo/Palette/Violet/700` | `#3C319F` | 60, 49, 159 |
| `Plytoo/Palette/Violet/800` | `#2D2578` | 45, 37, 120 |
| `Plytoo/Palette/Violet/900` | `#1F1A51` | 31, 26, 81 |

### Lime

| 토큰 | HEX | RGB |
| --- | --- | --- |
| `Plytoo/Palette/Lime/50` | `#F8FDEB` | 248, 253, 235 |
| `Plytoo/Palette/Lime/100` | `#EFFBD4` | 239, 251, 212 |
| `Plytoo/Palette/Lime/200` | `#DDF7A5` | 221, 247, 165 |
| `Plytoo/Palette/Lime/300` | `#B9F36B` | 185, 243, 107 |
| `Plytoo/Palette/Lime/400` | `#9ADB48` | 154, 219, 72 |
| `Plytoo/Palette/Lime/500` | `#79B62B` | 121, 182, 43 |
| `Plytoo/Palette/Lime/600` | `#5A8A20` | 90, 138, 32 |
| `Plytoo/Palette/Lime/700` | `#41641C` | 65, 100, 28 |
| `Plytoo/Palette/Lime/800` | `#2F4918` | 47, 73, 24 |
| `Plytoo/Palette/Lime/900` | `#203414` | 32, 52, 20 |

### Pink

| 토큰 | HEX | RGB |
| --- | --- | --- |
| `Plytoo/Palette/Pink/50` | `#FFF3F7` | 255, 243, 247 |
| `Plytoo/Palette/Pink/100` | `#FFE4ED` | 255, 228, 237 |
| `Plytoo/Palette/Pink/200` | `#FFC9D9` | 255, 201, 217 |
| `Plytoo/Palette/Pink/300` | `#FF8DAD` | 255, 141, 173 |
| `Plytoo/Palette/Pink/400` | `#F56F98` | 245, 111, 152 |
| `Plytoo/Palette/Pink/500` | `#DC4B7B` | 220, 75, 123 |
| `Plytoo/Palette/Pink/600` | `#B72F61` | 183, 47, 97 |
| `Plytoo/Palette/Pink/700` | `#90234C` | 144, 35, 76 |
| `Plytoo/Palette/Pink/800` | `#6D1D3C` | 109, 29, 60 |
| `Plytoo/Palette/Pink/900` | `#49172B` | 73, 23, 43 |

## 5. Semantic 매핑

### 5.1 기존 Primary 토큰 교체

원본에서 `Primary/Normal`의 `Blue/50` 참조와 `Primary/Strong`, `Primary/Heavy`, `Inverse/Primary` 및 `Semantic/…` 명칭을 확인했다. 기존 토큰 이름을 유지하고 참조 대상만 변경한다. 다음 모드별 값은 **plytoo 신규 매핑**이다. Strong/Heavy는 색상 강도 토큰이며 hover/pressed와 자동으로 같은 의미로 취급하지 않는다.

| 기존 토큰 | Light의 새 참조 | Dark의 새 참조 |
| --- | --- | --- |
| `Primary/Normal` | Violet/500 · #6155F5 | Violet/300 · #B6ADFF |
| `Primary/Strong` | Violet/600 · #4D40C7 | Violet/200 · #D8D3FF |
| `Primary/Heavy` | Violet/700 · #3C319F | Violet/100 · #EDEAFF |
| `Inverse/Primary` | Violet/300 · #B6ADFF | Violet/500 · #6155F5 |

`Semantic/Primary/Normal` 등 동일 역할의 스타일·변수도 같은 참조로 일치시킨다. Inverse는 반대 테마의 Primary/Normal을 참조한다. Dark의 밝은 Primary 위에서 사용하는 텍스트·아이콘은 어두운 전경을 사용해야 한다. 원본 전경이 흰색으로 고정되어 있다면 아래 `OnPrimary` 브랜드 전경 토큰을 적용한다.

### 5.2 새 브랜드 역할

Secondary와 Tertiary는 이 문서에서 추가하는 plytoo 역할이다. 원본에 같은 이름이 있다고 가정하지 않는다. 브랜드 대표색은 양쪽 모드에서 동일하게 유지하고, 텍스트용 강조 색상은 별도로 구분한다.

| 새 토큰 | Light | Dark | 용도 |
| --- | --- | --- | --- |
| `Plytoo/Brand/Primary` | Violet/500 | Violet/500 | 고정 브랜드 그래픽·로고 배경 |
| `Plytoo/Brand/Secondary` | Lime/300 | Lime/300 | 브랜드 포인트 면 |
| `Plytoo/Brand/Tertiary` | Pink/400 | Pink/400 | 브랜드 포인트 면 |
| `Plytoo/Brand/Deep` | Violet/700 | Violet/700 | 짙은 브랜드 면 |
| `Plytoo/Brand/Dark` | Violet/900 | Violet/900 | 가장 짙은 브랜드 면 |
| `Plytoo/Content/Secondary` | Lime/700 | Lime/300 | 배경 위에 표시하는 라임 계열 텍스트 |
| `Plytoo/Content/Tertiary` | Pink/600 | Pink/300 | 배경 위에 표시하는 핑크 계열 텍스트 |
| `Plytoo/OnPrimary` | Static/White | Violet/900 | 테마별 Primary/Normal 위 전경 |
| `Plytoo/OnSecondary` | Violet/900 | Violet/900 | Lime/300 위 전경 |
| `Plytoo/OnTertiary` | Violet/900 | Violet/900 | Pink/400 위 전경 |

고정 `Plytoo/Brand/Primary` 면 위의 로고는 테마와 무관하게 `Static/White`를 사용한다. 위 OnPrimary는 모드에 따라 바뀌는 `Primary/Normal`용이다. 콘텐츠용 색상은 실제 배경과의 대비를 확인한 뒤 적용한다.

### 5.3 기존 Accent 처리

- 브랜드 용도로 쓰는 `Accent/Lime`, `Accent/Violet`, `Accent/Pink`가 있으면 각각 Lime/300, Violet/500, Pink/400으로 연결한다.
- 원본에서 확인한 `Accent/Background/Lime`, `Accent/Background/Violet`, `Accent/Background/Pink`를 브랜드 배경으로 쓰는 경우에도 위 대표색으로 연결한다. 그 위 전경은 해당 On 토큰을 함께 적용한다.
- Cyan, Light Blue 등 나머지 Accent를 새 plytoo 브랜드 요소에 사용하지 않는다. 기존 비브랜드 기능·데이터 구분에서 쓰이는 색상은 이번 변경에서 보존한다.
- 팔레트에 존재한다는 이유만으로 원본 Atomic 색상을 삭제하거나 모든 참조를 바꾸지 않는다.

## 6. 컴포넌트 적용

| 대상 | 적용 규칙 |
| --- | --- |
| 주요 CTA | 원본 Primary 참조를 새 Violet 계열로 교체. 크기·형태·상태 효과 유지 |
| 링크·선택된 탭 | 기존에 Primary를 쓰던 텍스트, 밑줄, 아이콘만 새 Primary로 교체 |
| Checkbox·Radio·Switch | 활성 상태의 기존 Primary 참조만 교체. 비활성·disabled는 원본 유지 |
| Input·Select | 브랜드 focus에 쓰이는 Primary만 교체. 오류·경고 테두리와 기본 테두리는 원본 유지 |
| 브랜드 배지·칩 | 보조 강조가 필요한 경우 Lime/300 또는 Pink/400과 해당 On 토큰 사용 |
| 보조 버튼 | 원본의 중립색·outline·text 역할 유지. Secondary 역할명만 보고 라임으로 변경하지 않음 |
| 알림·검증 메시지 | Positive/Cautionary/Negative 원본 유지 |
| 카드·모달·내비게이션 | 원본 표면·그림자·간격 유지. 브랜드 강조 요소만 변경 |
| Hover·Pressed·Disabled | 원본의 상태 레이어, opacity, 전환 규칙 유지. 새 효과를 추가하지 않음 |

기존 컴포넌트가 Primary 색상을 직접 입력한 경우에만 의미를 확인해 semantic 참조로 연결한다. 원본에서 정의하지 않은 새로운 크기, 패딩, radius, 애니메이션은 이 변경에 포함하지 않는다.

## 7. 브랜드 보드 적용

마지막 첨부 이미지의 의도를 다음 다섯 면으로 재현한다.

1. 주된 큰 면: Violet/500.
2. 큰 면 안의 PLYTOO 로고: Static/White.
3. 보조 영역 상단: Lime/300.
4. 그 아래: Pink/400.
5. 나머지 보조 면: Violet/700, Violet/900.

이 구성은 브랜드 그래픽의 예시다. 모든 제품 화면에 같은 분할 레이아웃이나 배색 비율을 적용하지 않는다. 첨부 이미지의 선택 테두리·핸들은 디자인 요소에 포함하지 않는다.

## 8. 전경과 배경 조합 검증

아래 수치는 RGB에서 계산한 sRGB 상대 명도 대비비다. 반투명도·그라데이션 없이 단색끼리 비교한 값이며 실제 컴포넌트 전체의 접근성 검증을 뜻하지 않는다.

| 전경 | 배경 | 대비비 |
| --- | --- | ---: |
| White | Violet/500 | 5.09:1 |
| Violet/900 | Lime/300 | 12.15:1 |
| Violet/900 | Pink/400 | 5.74:1 |
| Violet/900 | Violet/300 | 7.86:1 |
| White | Lime/300 | 1.30:1 |
| White | Pink/400 | 2.76:1 |

라임·핑크 대표색 위에는 밝은 글자보다 Violet/900 전경을 사용한다. 흰 배경 위의 작은 텍스트를 Lime/300이나 Pink/400으로 직접 표시하지 않는다. 일반 본문은 원본 Label 토큰을 유지한다. 원본의 상태 레이어나 불투명도가 적용된 최종 렌더링에서는 대비를 다시 확인한다.

## 9. 보존할 주요 토큰 목록

아래 토큰은 원본에서 이름을 확인한 비브랜드 역할이다. Light/Dark 값, 투명도와 참조를 그대로 상속한다.

- `Label/{Normal, Strong, Neutral, Alternative, Assistive, Disable}`
- `Background/Normal/{Normal, Alternative}`
- `Background/Elevated/{Normal, Alternative}`
- `Background/Transparent/{Normal, Alternative}`
- `Interaction/{Inactive, Disable}`
- `Line/Normal/{Normal, Neutral, Alternative, _Strong}`
- `Line/Solid/{Normal, Neutral, Alternative}`
- `Fill/{Normal, Strong, Alternative}`
- `Status/{Positive, Cautionary, Negative}`
- `Static/{White, Black}`
- `Inverse/{Background, Label}`
- `Material/Dimmer`
- `Semantic/Shadow/{Normal, Strong, Heavy}`

원본 Opacity 단계 `0, 5, 8, 12, 16, 22, 28, 35, 43, 52, 61, 74, 88, 97, 100`도 유지한다. 특정 토큰 설명에 따로 정의된 투명도 역시 그대로 둔다.

## 10. 적용 완료 기준

- [ ] 새 팔레트 30개의 RGB와 HEX가 이 문서와 일치한다.
- [ ] Primary 참조가 Light/Dark 모두 새 Violet 계열에 연결되어 있다.
- [ ] 브랜드 대표색은 Violet/500, Lime/300, Pink/400이다.
- [ ] 브랜드 용도의 이전 Blue 참조만 교체되었다.
- [ ] 상태색, 중립색, 기본 배경, 본문, 구분선, disabled는 원본과 동일하다.
- [ ] 타이포그래피, 간격, 형태, 그림자, 컴포넌트 구조에 변경이 없다.
- [ ] 라임·핑크 면의 전경과 Dark 모드의 밝은 Primary 전경이 함께 적용되었다.
- [ ] 실제 화면에서 기본·선택·hover·pressed·disabled 상태를 확인했다.

이 체크리스트는 후속 Figma/제품 적용용이다. 이번 산출물은 Markdown 명세이며 첨부 `.fig` 파일 자체는 수정하지 않았다.
