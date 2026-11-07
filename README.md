# 애피 날리기 — AppieRagdoll

마인크래프트 스킨을 입은 래그돌을 잡고 던지는 물리 장난감. 단일 HTML 파일로 동작한다.

## 실행

인터넷이 필요하다 (three.js / cannon-es CDN 사용).

- `Appie-ragdoll.html`을 브라우저로 직접 열기, 또는
- `python -m http.server 8000` 후 http://localhost:8000/Appie-ragdoll.html 접속

## 조작

| 입력 | 동작 |
|---|---|
| 드래그 | 애피 잡고 던지기 |
| WASD | 카메라 이동 (Shift 가속) |
| 우클릭 드래그 | 시점 회전 |
| 휠 | 앞뒤 이동 |
| TAB / ESC | 메뉴 열기·닫기 |
| R / F / M | 스폰 / 날리기 / 효과음 토글 |
| Ctrl+Z / Ctrl+Y | 오브젝트 되돌리기·다시 실행 |
| Enter (스킨란) | 스킨 적용 |

## 기능

- **스킨**: 마인크래프트 자바 에디션 이름 입력 시 해당 스킨 적용 (PlayerDB → Ashcon → crafthead/minotar 폴백), classic 4px 기준
- **물리**: cannon-es 6파츠 래그돌 + ConeTwist 조인트, 클론끼리 볼링핀처럼 충돌
- **스테이지**: 64×64 베이스 플레이트, 크기 조절 가능
- **오브젝트**: 사진판·투명 블럭·투명 벽 추가, 기즈모 + 수치 편집, undo 40단계
- **녹화**: GIF / MP4 최대 15초
- **설정**: 강도·그림자·효과음·화면 흔들림·토스트, localStorage 저장

## 스택

- three.js 0.160.0 + cannon-es 0.20.0 (CDN, 폴백 포함)
- GolaCSS (`gola/`, 오프라인 동봉)

## 파일

| 파일 | 설명 |
|---|---|
| `Appie-ragdoll.html` | 본체 (전부 이 안에) |
| `Appie_1019-skin.png` | 기본 스킨 64×64 |
| `Appie_1019-3D-model.zip` | 모델 소스 패키지 (obj + mtl + skin) |
| `hurt1-3.mp3`, `ShanShenBu.mp3` | 효과음 |
| `gola/` | GolaCSS + SDF 폰트 에셋 |
