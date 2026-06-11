# Mypage_0610

의료기기 SW 개발자를 목표로 하는 개발자의 개인 자기소개 웹페이지입니다.

---

## 프로젝트 개요

- **목적**: 개인 포트폴리오 및 자기소개 페이지
- **기술 스택**: HTML, JavaScript
- **개발자 목표**: 의료기기 SW 개발 (도메인 지식 + 개발 역량 병행 학습)

---

## 개발 환경

| 항목 | 내용 |
|------|------|
| OS | Windows + WSL2 Ubuntu |
| 편집기 | Claude Code Web |
| 저장소 | GitHub (`nebu-25/Mypage_0610`) |
| 브랜치 | `main` |

---

## Git 연결 설정

### 현재 방식: GitHub CLI (`gh`) 인증

```bash
# Remote URL
https://github.com/nebu-25/Mypage_0610.git

# 인증 방식
gh auth login  # 브라우저 인증
gh auth setup-git  # git credential 연결
```

### 설정 이력

| 날짜 | 변경 내용 |
|------|-----------|
| 2026-06-10 | PAT 토큰 URL 방식 → gh CLI 인증 방식으로 전환 |

### 전환 배경

Claude Code Web 환경에서 PAT 토큰이 URL에 하드코딩된 방식(`https://github_pat_...@github.com/...`)으로 연결되어 있어 `git push`가 동작하지 않는 문제가 발생했다. gh CLI 인증 방식으로 전환하여 해결했다.

> 관련 이슈: [#1 Claude Code Web에서 git push 불가](https://github.com/nebu-25/Mypage_0610/issues/1)

### gh CLI 초기 설치 방법 (WSL2 기준)

```bash
# 1. gh 설치
sudo apt install gh -y

# 2. 브라우저 로그인
gh auth login
# GitHub.com → HTTPS → Login with a web browser 선택

# 3. Remote URL 교체 (토큰 제거)
git remote set-url origin https://github.com/nebu-25/Mypage_0610.git

# 4. git credential 연결
gh auth setup-git
```

---

## 파일 구조

```
Mypage_0610/
├── index.html    # 메인 자기소개 페이지
├── prompt.txt    # 페이지 기획 내용
└── README.md     # 프로젝트 문서 (현재 파일)
```
