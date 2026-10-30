# CLAUDE.md - Hack_global 프로젝트 지침

## 1. 프로젝트 개요
- **프로젝트명**: Hack_global
- **핵심 구조**: `src/` (소스코드), `docs/` (문서), `.github/` (설정)

## 2. Git 협업 규칙
- `main` 브랜치 직접 Push 금지 (항상 `feature/기능명` 브랜치 사용)
- 코드 반영 시 PR(Pull Request) 작성 및 팀원 Review/Approve 필수
- 커밋 메시지 규칙:
  - `feat:` 새로운 기능 구현
  - `fix:` 버그 및 에러 수정
  - `docs:` 문서 작성 및 수정
  - `chore:` 폴더 구조, 패키지 설정 등 단순 작업

## 3. 개발 및 보안 지침
- API 키, DB 비밀번호 등은 절대 커밋하지 않고 `.env.local`로만 관리
- 소스 코드는 `src/` 디렉터리 내에 역할별로 분리하여 작성
