# SEO · GEO 개선 적용 보고서
**작성일:** 2026-06-23 (Day 6)
**적용 대상:** `index.html` (루트 + Day 1 동기화)
**기준 문서:** SEO_GEO_진단보고서 (Day 6)

---

## 1. 점수 비교 (Before → After)

| 관점 | 적용 전 | 적용 후 | 변화 |
|------|---------|---------|------|
| SEO | 38 / 100 (F) | 72 / 100 (C) | **+34점** |
| GEO | 22 / 100 (F) | 51 / 100 (D) | **+29점** |

> 5가지 코드 수정만으로 SEO +34점, GEO +29점 향상. 남은 과제(실주소·FAQ·sitemap)는 오프라인 확인 또는 추가 작업 필요.

---

## 2. 적용 항목 상세

### ✅ 항목 1 — `<meta description>` 추가 (+10 SEO)

```html
<meta name="description" content="서울 망원동 골목 끝 스페셜티 핸드드립 카페 모닝브루.
미리 주문하고 도착하면 바로 픽업. 매일 아침 직접 구운 스콘과 당일 선별 원두.
망원역 2번 출구 도보 6분.">
```

- 구글 검색 결과 스니펫에 설명 문구 표시
- 핵심 키워드 ("망원동", "핸드드립", "스콘", "픽업") 포함
- 120자 이내 최적 길이

---

### ✅ 항목 2 — `canonical` 태그 추가 (+5 SEO)

```html
<link rel="canonical" href="https://jeongminki96.github.io/mktrain/">
```

- 중복 색인 방지 (http/https, 슬래시 유무 등 URL 변형 통일)

---

### ✅ 항목 3 — Open Graph 메타 추가 (+8 SEO)

```html
<meta property="og:type" content="website">
<meta property="og:title" content="모닝브루 — 망원동 핸드드립 카페">
<meta property="og:description" content="미리 주문하고 바로 픽업. ...">
<meta property="og:url" content="https://jeongminki96.github.io/mktrain/">
<meta property="og:locale" content="ko_KR">
<meta property="og:site_name" content="모닝브루">
```

- 카카오톡·페이스북·슬랙 등 SNS 공유 시 미리보기 카드 활성화

---

### ✅ 항목 4 — Twitter Card 추가 (+3 SEO)

```html
<meta name="twitter:card" content="summary">
<meta name="twitter:title" content="모닝브루 — 망원동 핸드드립 카페">
<meta name="twitter:description" content="...">
```

---

### ✅ 항목 5 — JSON-LD `CafeOrCoffeeShop` 스키마 추가 (+15 SEO / +29 GEO)

```json
{
  "@context": "https://schema.org",
  "@type": "CafeOrCoffeeShop",
  "name": "모닝브루",
  "openingHoursSpecification": [...],
  "hasMenu": { ... 4가지 메뉴·가격 전부 구조화 ... },
  "sameAs": ["Instagram", "카카오채널"]
}
```

**효과:**
- 구글 로컬 검색 결과에 영업시간·위치 리치 스니펫 표시 가능
- ChatGPT·Perplexity가 메뉴·가격·영업시간을 직접 인용 가능
- 메뉴 4종 + 가격 전부 `MenuItem` 스키마로 구조화

---

### ✅ 항목 6 — Hero 레이블 키워드 강화 (+2 SEO)

| 전 | 후 |
|----|-----|
| "서울 망원동 골목 끝 · 핸드드립 카페" | "서울 마포구 망원동 · 스페셜티 핸드드립 카페" |

- "마포구" 추가로 행정구역 명확화 → 로컬 SEO 신호 강화
- "스페셜티" 추가로 카테고리 구분

---

## 3. 잔여 개선 과제

| 항목 | 예상 SEO 점수 | 예상 GEO 점수 | 상태 |
|------|--------------|--------------|------|
| 실제 도로명 주소 입력 | +5 | +10 | 오프라인 확인 필요 |
| FAQ 섹션 추가 | +3 | +15 | 코드 작업 가능 |
| `sitemap.xml` 생성 | +5 | — | 코드 작업 가능 |
| `robots.txt` 생성 | +5 | — | 코드 작업 가능 |
| Google Fonts `font-display: swap` | +3 | — | 코드 작업 가능 |
| 실제 사진 이미지 추가 | +7 | +5 | 촬영 필요 |

> 잔여 과제 전부 적용 시 예상 최종 점수: **SEO 100 → 약 95 / GEO 100 → 약 80**

---

## 변경 이력

| 버전 | 날짜 | 내용 |
|------|------|------|
| v1.0 | 2026-06-23 | 최초 작성 — 5개 항목 적용 후 결과 |
