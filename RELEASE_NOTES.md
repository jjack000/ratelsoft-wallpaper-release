# 릴리즈 노트

## v2026.0105.10 (2026-01-05)
- IO: Trigger 입력 후 설정된 지연 시간에 OK/NG 출력(지연 시점까지 Judge 미완료면 완료 즉시 출력)
- IO: OK/NG 출력은 설정된 펄스 폭(ms)만큼 ON 후 OFF
- 설정: `JudgeOutputDelayMs`, `JudgePulseWidthMs` 추가 및 설정 UI에 반영
- UI: 숫자 입력 전용 컨트롤 `NumericTextBox` 추가(설정값 입력 품질 개선)
- 릴리즈: `release.py` 실행 시 작업 트리에 미커밋 변경이 있으면 경고 후 종료(안전장치)
- 개발/테스트: `CameraTestApp`에 `OpenCvSharp4.WpfExtensions` 패키지 참조 추가

## v2026.0105.9 (2026-01-05)
- Align/Origin 좌표 계산/표시 보정 로직 수정
- 릴리즈: 스크립트 출력에 public release repo 링크 안내 추가

## v2026.0105.8 (2026-01-05)
- CI: GitHub Actions publish에서 prerelease 버전(예: `2025.1231.7-alpha.0.12`) 사용 시 WPF AssemblyVersion 오류가 나지 않도록 `AssemblyVersion`/`FileVersion`을 숫자 4파트로 보정
  - `Version`/`InformationalVersion`은 원본 prerelease 문자열 유지

## v2026.0105.7 (2026-01-05)
- 레시피 이미지 로드 조건 수정: 파일이 존재할 때만 Coord 이미지를 로드하도록 처리

## v2026.0105.6 (2026-01-05)
- 레시피 이미지 저장 안정화: Empty 이미지 저장 방지
- 레시피 저장 시 이미지 파일 저장 로직 호출 추가
- 레시피 저장 다이얼로그 경로 체크 동작 조정(폴더 선택 UX 개선)
- IP 창 초기 표시 개선: Coord 이미지가 없으면 원본 이미지로 대체 표시

## v2026.0105.5 (2026-01-05)
- IO 연결 처리 안정화: IO 디바이스 null 체크로 예외 상황 대응
- IP 창 관리 안정화: IP 윈도우 딕셔너리 초기화/생성 로직 보강
- 이미지 표시 안정화: 선택 이미지가 null/empty일 때 표시 루틴을 중단하도록 가드 추가
- 레시피 이미지 로드 로직 개선(파일 미존재 케이스 처리)

## v2026.0105.4 (2026-01-05)
- IP 창 UI: 로그 패널 높이를 고정(Height=150)하여 레이아웃 안정화
