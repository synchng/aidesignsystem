# 🎨 Design System: Glow-up Web Interface

이 디자인 시스템은 미니멀하고 신뢰감 있는 정보 전달을 목적으로 합니다. 넓은 여백(White Space), 정교한 타이포그래피 계층 구조, 그리고 부드러운 인터랙션 요소를 특징으로 합니다.

---

## 1. Color Palette (색상)

### Primary & Neutral Colors
* **Background:** `#FFFFFF` (순수 흰색 - 깔끔하고 투명한 느낌)
* **Text Primary (Main Headings):** `#111111` (깊은 차콜 블랙 - 가독성 확보)
* **Text Secondary (Body/Muted):** `#666666` 또는 `#707070` (부드러운 그레이)
* **Accent (Interactive/Brand):** `#000000` (강조 버튼 및 활성화 탭)
* **Subtle Accent (Links/Badges):** `#1E5128` 또는 `#2E7D32` (딥 그린 - 'More' 링크 및 출처 아이콘용)

### Card & Component Colors
* **Default Card Background:** `#F9F9F9` (매우 밝은 회색으로 미세한 경계 분리)
* **Active/Focused Card:** 테두리 없는 반투명 블러 효과 (`rgba(0, 0, 0, 0.05)` 기반의 그라데이션 및 블러)
* **Border/Divider:** `#EEEEEE` (아주 연한 회색 line)

---

## 2. Typography (타이포그래피)

* **Primary Font Family:** `Inter`, `SF Pro Display`, 또는 `Helvetica Neue` (Clean Sans-serif)

| 역할 (Role) | 크기 (Size) | 두께 (Weight) | 색상 (Color) | 특징 (Notes) |
| :--- | :--- | :--- | :--- | :--- |
| **Super Title** | 12px | Bold (700) | Secondary | 자간 넓게 (Tracking), 모두 대문자 |
| **Main Hero Title** | 48px ~ 56px | Regular (400) / Medium (500) | Primary | 핵심 키워드에만 Accent Color나 두께 변화 적용 |
| **Card Title** | 24px | Semi-Bold (600) | Primary / White | 카드 내부 헤드라인 |
| **Body Text** | 15px ~ 16px | Regular (400) | Secondary | 줄바꿈(Line-height) 1.5~1.6으로 여유 있게 설정 |
| **Caption / Citation**| 12px | Regular (400) | Secondary (Muted) | 학술 출처 및 주석용 |

---

## 3. Components (주요 컴포넌트)

### 3.1. Navigation Bar (네비게이션 바)
* **구조:** Left (로고) | Center (메뉴 링크) | Right (Utility 버튼 - Login, Join Now)
* **Join Now Button:** * Background: `#111111`
    * Text: `#FFFFFF` (14px, Medium)
    * Border-Radius: `8px`
    * Padding: `10px 20px`

### 3.2. Segmented Control / Tabs (카테고리 탭)
* **기본 상태 (Inactive):** 텍스트 컬러 `#707070`, 배경 없음 또는 투명.
* **활성화 상태 (Active):** * Background: `#111111`
    * Text: `#FFFFFF`
    * Border-Radius: `20px` (정원 캡슐 형태)
    * Padding: `8px 16px`

### 3.3. Data/Content Cards (콘텐츠 카드)
기본 상태와 마우스 호버(Hover) 또는 선택(Active) 상태의 대비가 명확해야 합니다.

* **일반 카드 (Default Card):**
    * Background: `#F8F9FA`
    * Border-Radius: `16px`
    * Padding: `32px`
    * Shadow: 없음 (또는 아주 미세한 `blur 4px` 그레이 섀도우)

* **포커스 카드 (Focused/Active Card - 이미지 내 2번째 카드 스타일):**
    * Background: 선명한 배경 대신 **그라데이션이 들어간 불투명 블러(Glassmorphism)** 느낌 적용.
    * **CSS 효과 예시:**
        ```css
        background: linear-gradient(135deg, rgba(110, 110, 110, 0.8), rgba(60, 60, 60, 0.9));
        backdrop-filter: blur(20px);
        color: #FFFFFF;
        box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
        transform: translateY(-4px); /* 미세한 상승 효과 */
        transition: all 0.3s ease;
        ```

---

## 4. Layout & Spacing (레이아웃 및 여백)

* **Grid:** 표준 12컬럼 그리드 사용 (화면 캡처 기준 콘텐츠 영역은 4컬럼씩 4개 카드 배열 구조)
* **Max Width:** `1200px` 또는 `1440px` (중앙 정렬)
* **Section Padding:** * Hero 영역 상하 여백: `120px` 이상 확보하여 시각적 압박감 해소.
    * 카드 간 간격 (Gap): `24px`

---

## 5. Design Principles (디자인 원칙)

1.  **Less is More:** 불필요한 테두리(Border)나 원색의 사용을 제한하고, 여백을 통해 그룹핑을 표현합니다.
2.  **Typography Contrast:** 얇은 서체와 두꺼운 서체, 큰 글씨와 작은 글씨의 대비를 확실하게 주어 시선의 흐름을 유도합니다.
3.  **Soft Shadows & Blurs:** 컴포넌트의 입체감은 강한 선이 아닌, 부드러운 그림자와 배경 블러(Backdrop blur) 처리로 고급스럽게 연출합니다.
