# MMP M&A Deal Archive — Dashboard

화장품·F&B 섹터 국내 M&A 딜 아카이브 대시보드 (정적 사이트).

## 구성
- `index.html` — 대시보드 (Chart.js·SheetJS는 CDN 로드)
- `dashboard_data.json` — 딜 데이터 (대시보드가 상대경로로 fetch)
- `.nojekyll` — GitHub Pages의 Jekyll 처리 비활성화

## 로컬 실행
```
python -m http.server 8080
# http://localhost:8080 접속
```
(`file://`로 열면 fetch가 막히므로 반드시 로컬 서버로 열 것.)

## 배포 (GitHub Pages)
이 repo를 GitHub에 push 후, **Settings → Pages → Source: `main` 브랜치 / `/ (root)`** 선택.
몇 분 뒤 `https://<사용자명>.github.io/<repo명>/` 에서 공개.

## 데이터 갱신
파이프라인(비공개)에서 `dashboard_data.json`을 새로 생성해 이 파일을 교체하고 다시 push하면 사이트가 갱신됨.
