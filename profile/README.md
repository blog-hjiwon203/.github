# now-log

누구나 가입해 자기 블로그(`/@주소`)를 열고, 에디터로 글을 쓰고, 다른 블로그 글을 읽고 댓글·공감·구독하는 티스토리형 멀티 블로그 서비스입니다.

**운영** → https://now-log.java21.net

## 저장소

| 저장소 | 내용 |
| --- | --- |
| [now-log](https://github.com/blog-hjiwon203/now-log) | 구현 코드(백엔드 + 프론트), GitHub Actions 배포 |
| [blog-docs](https://github.com/blog-hjiwon203/blog-docs) | 명세·계획·작업 목록·API·ERD·화면 시안, 스텝별 학습 자료 |

## 주요 기능

- 회원가입·로그인(이메일 인증, 카카오·구글), 블로그 개설과 꾸미기
- Tiptap 에디터로 글 작성(이미지, 임시 저장, 공개 범위), 카테고리·태그
- 댓글·답글, 공감, 북마크, 구독과 피드, 알림, 인기 글 순위
- 검색과 bge-m3 임베딩 기반 의미 검색·비슷한 글 추천
- 블로그 관리 화면과 서비스 관리자(신고·정지)

## 기술

- **백엔드** Java 21, Spring Boot 4.1(Web MVC, Security, Data JPA, Flyway), Maven
- **프론트** React, TypeScript, Vite, Tiptap
- **데이터** PostgreSQL 17 + pgvector, Redis, Ollama(bge-m3)
- **테스트** JUnit 5, MockMvc, Testcontainers, ArchUnit, Vitest
- **배포** Docker, GitHub Actions

## 진행 방식

명세 → 계획 → 작업 목록 순서의 Spec Kit 흐름으로 설계하고, 작업 목록의 스텝 단위로 구현했습니다. 스텝마다 그 스텝에서 처음 쓴 개념을 처음부터 정리한 학습 문서를 남겼습니다([learning](https://github.com/blog-hjiwon203/blog-docs/tree/main/specs/001-tistory-blog/learning)).

처음 개발은 과제 제출용 저장소 [AIP-1/blog-basic-AIGJ_01_017-blog](https://github.com/AIP-1/blog-basic-AIGJ_01_017-blog)에서 했고, 2026-10-14에 커밋 기록째 now-log로 옮겼습니다.
