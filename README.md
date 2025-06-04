# 🧐 MBTI 테스트 웹사이트

이 프로젝트는 HTML, Bootstrap, 바닐라 JavaScript를 기반으로 제작된 간단한 MBTI 테스트 웹 애플리케이션입니다. 사용자는 12개의 질문에 대해 예/아니오로 답하며 자신의 MBTI 유형을 확인할 수 있습니다.  

<img width="269" alt="image" src="https://github.com/user-attachments/assets/ab7fdb73-d1b4-4acb-bffd-e0dfa8fa577c" />

🔗 https://dayedev.github.io/chat-gpt-mbti/  

## 기능 설명

1. **랜딩 페이지 (`index.html`)**
   - "MBTI 테스트"라는 타이틀과 "시작하기" 버튼을 중앙에 배치
   - 버튼 클릭 시 `test.html`로 이동

2. **테스트 페이지 (`test.html`)**
   - 총 12개의 질문이 순차적으로 출력
   - 각 질문은 MBTI의 4가지 지표(E/I, S/N, T/F, J/P)를 기반으로 구성됨
   - 사용자는 "예" 또는 "아니오" 버튼으로 응답
   - 응답은 지표 알파벳(E, I, S, N, T, F, J, P) 형태로 `answers` 배열에 저장

3. **질문 전환 및 응답 저장 (`index.js`)**
   - 버튼 클릭 시 다음 질문으로 자동 이동
   - 질문 번호와 텍스트가 함께 갱신됨
   - 마지막 질문 이후, 사용자의 응답을 바탕으로 MBTI 유형 계산
   - 4가지 지표별로 더 많이 선택된 알파벳을 결과로 선택
   - 예: [E, N, F, P] → `ENFP`
   - 결과는 로컬스토리지(`localStorage`)에 `mbti_result` 키로 저장

4. **결과 페이지 (`result.html`)**
   - 로컬스토리지에 저장된 MBTI 값을 불러와 결과 출력
   - 예: `ENFP입니다!`로 화면에 표시
   - 결과가 없을 경우 `"아직 테스트를 진행하지 않았습니다!"` 메시지 출력
   - 버튼 문구가 `"다시하기"` 또는 `"테스트 하러 가기"`로 조건에 따라 변경

5. **스타일링**
   - Bootstrap 5를 이용한 반응형 UI
   - Noonnu에서 제공하는 `S-CoreDream-3Light` 폰트 적용
   - 카드, 버튼, 텍스트 중앙 정렬 등 깔끔한 사용자 경험 제공

## 향후 개선 방향

- 결과에 따른 MBTI 성격 설명 추가
- 소셜 미디어 공유 기능
- 반응형 개선 및 다크모드 지원
- 질문 무작위화 기능
