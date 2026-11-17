# 로컬 웹폰트

두 폰트 모두 공식 GitHub 배포본을 변형하지 않고 저장했습니다. 런타임 외부 폰트 서버를 사용하지 않습니다.
출처의 고정 커밋·다운로드 URL·바이트 수·SHA-256은 `sources.json`에 기록합니다.

| 폰트 | 파일 | 실제 가변 굵기 축 | 버전 | 라이선스 |
| --- | --- | --- | --- | --- |
| Pretendard | PretendardVariable.woff2 | 45–930, 기본 400 | 1.309 (1.3.9) | SIL OFL 1.1 |
| 본명조 / Source Han Serif KR | SourceHanSerifKR-VF.otf.woff2 | 250–900 | 2.003 | SIL OFL 1.1 |

가변 굵기 범위는 다운로드한 폰트의 fvar 테이블을 직접 확인한 값이며 `src/fonts.css`에 동일하게 등록했습니다.
CSS 굵기 400을 기존처럼 유지하며 임의의 합성 굵기를 만들지 않습니다.

- Pretendard 공식 배포처: https://github.com/orioncactus/pretendard
- Pretendard 공식 라이선스: https://github.com/orioncactus/pretendard/blob/main/LICENSE
- 본명조 공식 배포처: https://github.com/adobe-fonts/source-han-serif
- 본명조 WOFF2: https://github.com/adobe-fonts/source-han-serif/tree/release/Variable/WOFF2/OTF/Subset
- 본명조 공식 라이선스: https://github.com/adobe-fonts/source-han-serif/blob/master/LICENSE.txt

원본 라이선스 파일 `Pretendard-LICENSE.txt`, `SourceHanSerifKR-LICENSE.txt`를 함께 보관·배포합니다.
파일을 수정·서브셋화·재명명하지 않았습니다. CSS의 로컬 family 별칭으로 등록했습니다.

두 사이트 모두 운세 보기 버튼(`.accordion-trigger`)과 최하단 문구(`.site-footer`)만 Pretendard를 사용합니다.
그 밖의 본문·제목·별자리 이름·간략총평·카테고리 메뉴·안내·운세 본문은 본명조를 사용합니다.
Pretendard에 없는 한자는 로컬 본명조를 차선 폰트로 사용합니다. 실제 로고는 기존 SVG입니다.
글자 크기·행간·자간·색상·정렬·카드·버튼·여백은 변경하지 않았습니다.

재다운로드가 필요하면 프로젝트 루트에서 `node scripts/download-fonts.mjs`를 실행하세요.
이미 `sources.json`이 있으면 기록된 공식 커밋에서 다운로드하고 SHA-256을 검사합니다.
개발용 다운로드 때만 인터넷이 필요하며, 빌드·사이트 접속 시에는 필요하지 않습니다.
