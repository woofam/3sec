# 3SEC Company Website

[`woofam`](https://github.com/woofam) 조직에서 운영하는 3SEC 회사 소개용 정적 사이트입니다. 별도의 빌드 도구 없이 GitHub Pages에서 바로 동작하도록 구성했습니다.

- 대상 저장소: [`woofam/3sec`](https://github.com/woofam/3sec)
- 공개 홈페이지: [https://woofam.github.io/3sec/](https://woofam.github.io/3sec/)
- 3초 메뉴: [서비스 소개 및 실행 페이지 열기](https://woofam.github.io/3sec/#product)
- 브랜드·웹 스타일 기준: [`BRAND_STYLE_GUIDE.md`](BRAND_STYLE_GUIDE.md)

## 준비된 페이지 경로

향후 제품 출시와 앱 내 도움말 연결을 위해 다음 경로를 미리 구성했습니다.

- 3초 키친: [`kitchen/`](kitchen/)
- 3초 키친 사용 가이드: [`kitchen/guide/`](kitchen/guide/)
- 3초 가성비 준비 페이지: [`value/`](value/)
- 3초 가성비 사용 가이드 골격: [`value/guide/`](value/guide/)
- 개인정보 처리방침 골격: [`privacy/`](privacy/)
- 이용약관 골격: [`terms/`](terms/)
- 고객지원 허브 골격: [`support/`](support/)

`준비 중` 또는 `초안`으로 표시된 페이지는 검색 노출을 막는 `noindex`가 설정되어 있습니다. 실제 서비스 정보와 법률 검토가 완료된 뒤 각 파일 상단의 `TODO[...]` 주석을 확인하고 문구·시행일·링크를 교체합니다.

## 브랜드 스타일 관리

브랜드 홈과 향후 추가할 3초 키친·3초 가성비·가이드·정책 페이지는 [`BRAND_STYLE_GUIDE.md`](BRAND_STYLE_GUIDE.md)를 기준으로 제작합니다. 전역 색상과 글꼴, 공통 레이아웃은 [`assets/css/site.css`](assets/css/site.css)의 토큰과 공통 클래스를 사용합니다.

- 화면을 수정하기 전에 브랜드 가이드의 새 페이지 체크리스트를 확인합니다.
- 방문자용 CTA에는 GitHub 저장소 대신 실제 서비스·가이드·정책 주소를 사용합니다.
- 전역 디자인 변경은 CSS 토큰과 브랜드 가이드를 함께 갱신합니다.

## 페이지 구성

- Hero: 3SEC 브랜드 메시지
- About: 회사가 해결하려는 문제
- Product: 첫 번째 제품 `3초 메뉴`
- Principles: 빠름, 실용성, 로컬 우선 설계
- Contact: 토스 앱에서 제품 바로 열기

## 로컬 미리보기

```bash
python3 -m http.server 4173 --directory company-site
```

브라우저에서 [http://localhost:4173](http://localhost:4173)을 엽니다.

## 새 GitHub 저장소로 이전

이 디렉터리의 **내용 전체**를 새 저장소의 루트에 놓습니다. [`.github/workflows/deploy-pages.yml`](.github/workflows/deploy-pages.yml)이 `main` 브랜치의 정적 파일을 GitHub Pages로 자동 배포합니다.

저장소를 만든 뒤 [`woofam/3sec` Pages 설정](https://github.com/woofam/3sec/settings/pages)의 **Build and deployment → Source**를 `GitHub Actions`로 설정합니다. `main` 브랜치에 푸시하면 공식 Pages Actions가 루트의 [`index.html`](index.html)을 배포합니다.

## 파일 구조

```text
company-site/
├── .github/workflows/deploy-pages.yml
├── BRAND_STYLE_GUIDE.md
├── assets/
│   ├── css/site.css
│   ├── images/brand-mark.svg
│   ├── images/product-preview.svg
│   └── js/site.js
├── kitchen/
│   ├── index.html
│   └── guide/index.html
├── value/
│   ├── index.html
│   └── guide/index.html
├── privacy/index.html
├── terms/index.html
├── support/index.html
├── .nojekyll
├── 404.html
├── index.html
├── robots.txt
└── site.webmanifest
```
