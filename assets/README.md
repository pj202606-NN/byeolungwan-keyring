# 이미지 교체 안내

사이트별 배경 2개, 별자리 카드 JPG 28개와 성도 SVG 28개가 연결되어 있습니다. 디자인 참고 이미지는 서비스에 사용하지 않습니다.

| 종류 | 경로 | 권장 형태 |
| --- | --- | --- |
| NFC 고정 배경 | backgrounds/keyring-bg.webp | 전체 화면 cover, 중앙 기준 |
| 결과 고정 배경 | backgrounds/result-bg.png | 전체 화면 cover, 중앙 기준 |
| 공통 로고 | logos/byeolungwan-logo.svg | SVG 원본 비율 유지, 상단 중앙 |
| 성도 | constellations/{starId}.svg | SVG 원본 비율 유지, contain |
| 카드 | cards/{starId}.jpg | 원본 1748×3591, 가로 폭에 맞춰 높이 자동 |
| 장식 | decorations/ | 향후 장식 자산 보관 |

파일을 해당 이름으로 넣고 다시 빌드하면 연결됩니다. 별자리마다 경로를 변경하려면 src/data/constellations/index.ts의 assets를 수정하세요.
이미지 로딩 실패 시 명시적인 임시 영역을 표시합니다. 배경이 없으면 CSS 남색 그라데이션이 표시됩니다.
상단 공통 로고는 아이보리색(#eeeadd)의 실제 SVG를 사용하며, SVG 내부 투명 여백을 고려해 기존 로고 영역에 배치합니다. 로고 로딩 실패 시에만 텍스트 별운관을 사용합니다. 배경 이미지 레이어에만 블러를 적용하고 패널은 어두운 반투명 색상으로 겹칩니다. 장식 이미지는 현재 사용하지 않습니다.

