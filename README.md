# 멘토K 프롬프트랩

실전 업무·기획·콘텐츠 제작을 위한 한국어 병행 프롬프트 라이브러리의 원본 저장소입니다.

- 공개 서비스: https://aiwith.kr/prompt/
- 관리자: https://aiwith.kr/prompt/admin.html
- 서비스 저장소: https://github.com/mentor-k/chatgpt-sites-projectbook
- 원본 저장소: https://github.com/mentor-k/promptlab

## 배포 구조

기존 AI 홈페이지의 루트 도메인을 보존하기 위해 공개 서비스는 기존 저장소의 `prompt/` 폴더에서 제공합니다. 이 저장소에는 Prompt Lab 원본과 서버 인증 API 설계가 보관됩니다.

GitHub Pages 사용자 지정 도메인 `aiwith.kr`은 기존 홈페이지 저장소에만 연결해야 합니다. 이 저장소에는 CNAME을 두지 않습니다.

## 관리자 보안

관리자 PIN은 소스에 저장하지 않습니다. `/prompt/admin.js`는 서버 API의 HttpOnly 세션 쿠키를 사용하고, 엑셀은 인증 API에서만 스트리밍합니다. API 구현과 배포 조건은 `server/README.md`를 참고하세요.
