# LY(라인야후) 최신 이슈 트래커

## 프로젝트 개요
라인야후(LY)의 최신 이슈를 추적하는 정적 웹 대시보드.
단일 HTML 파일(`public/index.html`)로 구성된 SPA 스타일 페이지.

## 저장소
- **GitHub**: https://github.com/Ptaesung/LY-issue-tracker
- **배포 URL**: https://ptaesung.github.io/LY-issue-tracker/
- **브랜치**: `master`

## 맥북에서 이어서 작업하기

```bash
# 1. 클론
git clone https://github.com/Ptaesung/LY-issue-tracker.git
cd LY-issue-tracker

# 2. 로컬 확인 (아무 로컬 서버로 열면 됨)
open public/index.html
# 또는
npx serve public

# 3. 수정 후 푸시하면 자동 배포
git add -A
git commit -m "변경 내용"
git push
```

## 프로젝트 구조

```
LY/
├── public/
│   └── index.html          # 메인 페이지 (HTML + CSS + JS 올인원)
├── .github/
│   └── workflows/
│       └── deploy.yml      # GitHub Pages 자동 배포 워크플로우
├── firebase.json           # Firebase Hosting 설정 (기존)
├── .firebaserc             # Firebase 프로젝트 설정 (ly-tracker)
└── CLAUDE.md               # 이 파일
```

## 기술 스택
- **프론트엔드**: 순수 HTML/CSS/JS (프레임워크 없음)
- **폰트**: Noto Sans KR (Google Fonts)
- **디자인**: 다크 테마, 와이어프레임 그리드 배경
- **배포**: GitHub Pages (push 시 자동 배포)
- **대체 배포**: Firebase Hosting (`ly-tracker` 프로젝트)

## 현재 완료된 작업
- [x] 메인 대시보드 페이지 구현
- [x] 모바일 반응형 (768px, 400px 브레이크포인트)
- [x] GitHub 저장소 생성 및 푸시
- [x] GitHub Pages 자동 배포 설정

## 모바일 반응형 브레이크포인트
- `768px 이하`: 태블릿/모바일 — 1열 레이아웃, 폰트 축소
- `400px 이하`: 소형 모바일 — 추가 축소, 세로 배치

## 배포 방법
- **GitHub Pages**: `master` 브랜치에 푸시하면 `.github/workflows/deploy.yml`이 자동 실행
- **Firebase**: `firebase deploy` (별도 로그인 필요)
