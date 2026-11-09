# MONIT (모닛)

친구들과 놀러간 장소가 지도 위에 **추억 사진 섬네일 마커**로 쌓이는 프라이빗 소셜 라이프로그 서비스.

| 경로 | 내용 |
|---|---|
| `docs/MONIT-prd-v1.0-ko.md` | PRD v1.0 |
| `docs/plytoo-design-system.md` | 디자인 시스템 (Violet / Lime / Pink) |
| `index.html` | 웹앱 (Google Maps JS API, 단일 파일) |
| `design-prototype/` | Claude Design 캔버스 소스 (인터랙티브 프로토타입) |

## 실행
1. `cp config.example.js config.js` 후 Google Maps JavaScript API 키 입력 (`config.js`는 git에 올라가지 않음)
2. 키는 Cloud Console에서 HTTP 리퍼러와 Maps JavaScript API로 제한
3. `python3 -m http.server 8000` → http://localhost:8000

데이터는 브라우저 localStorage에만 저장되는 데모이며, 사진은 picsum 임시 이미지입니다.
