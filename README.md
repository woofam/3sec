# 3SEC Company Website

[`woofam`](https://github.com/woofam) 조직에서 운영하는 3SEC 회사 소개용 정적 사이트입니다. 별도의 빌드 도구 없이 GitHub Pages에서 바로 동작하도록 구성했습니다.

- 대상 저장소: [`woofam/3sec`](https://github.com/woofam/3sec)
- 공개 홈페이지: [https://woofam.github.io/3sec/](https://woofam.github.io/3sec/)
- 3초 메뉴: [토스 앱에서 열기](intoss://3sec-menu)

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
├── assets/
│   ├── css/site.css
│   ├── images/brand-mark.svg
│   ├── images/product-preview.svg
│   └── js/site.js
├── .nojekyll
├── 404.html
├── index.html
├── robots.txt
└── site.webmanifest
```
