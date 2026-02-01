# 스픽 할인코드 웹사이트 - 사용 설명서

GitHub Pages로 무료 호스팅되는 스픽 할인코드 사이트입니다.

---

## 무엇을 바꾸고 싶으면 어디를 수정하나요?

| 바꾸고 싶은 것 | 수정할 파일 |
|---------------|------------|
| 할인 링크 | `_data/links.yml` |
| 페이지 제목 | `_data/seo.yml` |
| 페이지 설명 | `_data/seo.yml` |
| 검색어 키워드 | `_data/seo.yml` |
| 브랜드 색상 | `content/main-page-content.md` 맨 위 |
| 소개글/히어로 | `content/sections/01-intro.md` |
| 가격표 | `content/sections/02-pricing.md` |
| 3단계 학습 | `content/sections/03-learning-steps.md` |
| 프리미엄 vs 플러스 | `content/sections/04-plan-guide.md` |
| FAQ | `content/sections/05-faq.md` |
| 왜 스픽? | `content/sections/06-why-speak.md` |
| 특별 혜택 | `content/sections/07-special-offer.md` |
| 이미지 교체 | `content/images/` (같은 파일명 덮어쓰기) |
| 영상 교체 | `content/videos/` (같은 파일명 덮어쓰기) |
| CSS 디자인 | `content/colors-and-styles.css` |

---

## 파일 구조

```
_data/                               ← 설정 파일 (링크, SEO)
├── links.yml                        # 할인 링크
└── seo.yml                          # 페이지 제목, 설명, 키워드

content/                             ← 콘텐츠 파일 (글, 이미지, 영상, CSS)
├── main-page-content.md             # 페이지 조립 + 브랜드 색상 설정
├── sections/                        # 섹션별 내용
│   ├── 01-intro.md                  # 히어로 이미지 + 소개글
│   ├── 02-pricing.md                # 가격 비교표
│   ├── 03-learning-steps.md         # 3단계 학습 (동영상+글)
│   ├── 04-plan-guide.md             # 프리미엄 vs 플러스 가이드
│   ├── 05-faq.md                    # FAQ
│   ├── 06-why-speak.md              # 왜 스픽?
│   └── 07-special-offer.md          # 특별 혜택 + 최종 CTA
├── images/                          # 이미지 (같은 이름으로 덮어쓰기)
│   ├── 01-main-hero.jpg
│   ├── 02-plan-comparison.jpg
│   └── 03-pdf-gift-detail.jpg
├── videos/                          # 영상 (같은 이름으로 덮어쓰기)
│   ├── step1-learning-video.mp4
│   ├── step2-practice-video.mp4
│   └── step3-ai-tutor-video.mp4
├── colors-and-styles.css            # CSS 디자인
└── _template.md                     # 새 페이지 만들 때 복사용
```

---

## 1. 할인 링크 수정하기

`_data/links.yml` 파일을 열어서 URL만 바꾸면 됩니다:

```yaml
premium: "https://새로운-프리미엄-링크"
premium_plus: "https://새로운-플러스-링크"
```

사이트의 모든 버튼에 자동 반영됩니다.

---

## 2. SEO (검색 최적화) 수정하기

`_data/seo.yml` 파일을 열어서 수정하면 됩니다:

```yaml
title: "여기에 구글 검색결과 제목"
description: "여기에 구글 검색결과 설명"
keywords: "키워드1, 키워드2, 키워드3"
```

---

## 3. 섹션 내용 수정하기

`content/sections/` 폴더에서 해당 파일만 열어서 수정하면 됩니다.
메모장처럼 수정하면 됩니다. 마크다운 문법을 사용합니다.

---

## 4. 이미지/영상 교체하기

`content/images/` 또는 `content/videos/` 폴더에서 같은 파일 이름으로 덮어쓰기만 하면 됩니다.
코드 수정 불필요!

---

## 5. GitHub Pages 배포

### 내용 수정 후 업데이트
1. GitHub에서 파일 클릭 > 연필 아이콘 > 수정 > Commit
2. 1-2분 후 자동 반영

---

## 건드리지 않아도 되는 파일들

| 파일 | 설명 |
|------|------|
| `_layouts/default.html` | 페이지 구조 (시스템) |
| `_includes/head.html` | SEO 메타태그 (시스템) |
| `_includes/footer.html` | 하단 안내문구 (시스템) |
| `_config.yml` | Jekyll 설정 (시스템) |
| `.gitignore` | Git 설정 |
