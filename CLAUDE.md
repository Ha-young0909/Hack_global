# CLAUDE.md - Hack_global 프로젝트 지침 및 AI 협업 규칙

## 1. 프로젝트 문서 구성
- `README.md`: 프로젝트 개요 및 기본 사용 안내
- `CLAUDE.md`: 코딩 AI 에이전트 개발 규칙 및 프로젝트 컨벤션

## 2. Git 브랜치 전략 및 협업 수칙
- **Main 브랜치 보호**: 직접 Push 절대 금지, PR(Pull Request) 병합만 허용
- **1 브랜치 1 담당자 원칙**: 충돌 및 AI 컨텍스트 혼선 방지
- **브랜치 네이밍 규칙**:
  - `feat/기능명`: 새로운 기능 개발
  - `fix/버그명`: 오류 및 버그 수정
  - `docs/문서명`: 문서 작성 및 수정
  - `refactor/개선명`: 코드 구조 및 성능 개선 (동작 변경 없음)

## 3. 작업 흐름 (Workflow)
1. `main` 최신화 (`git pull origin main`) 후 작업 브랜치 생성
2. **Small & Frequent Commits**: 기능 단위로 작게 자주 커밋
3. **Squash and Merge**: PR 머지 시 깔끔한 이력 관리

## 4. 테스트 자동화 & CI/CD
- 기능 구현 시 테스트 코드 동시 작성
- GitHub Actions 자동 검증 (테스트 통과 시에만 PR 승인 및 머지)

## 5. 환경 변수 및 보안 규칙
- API Key, DB 비밀번호 등 비밀 키는 절대 커밋 금지
- 로컬 환경변수는 `.env.local` 사용 및 `.gitignore` 등록 필수
- 변수명만 표기한 `.env.example` 작성하여 동료와 공유

## 6. AI 에이전트 활용 팁
- **기능 단위 새 세션**: 대화가 길어지면 컨텍스트 낭비 및 정밀도 저하 발생 -> 기능 완료 시 새 채팅 시작
- **교차 검증 (Cross Check)**: 생성된 코드는 타 AI 모델이나 팀원 코드 리뷰 거치기
