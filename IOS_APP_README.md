# iPhone App Wrapper

현재 웹앱은 GitHub Pages로 배포되고 있고, 이 폴더에는 `Capacitor` 기반 iPhone 앱 래퍼를 바로 이어서 만들 수 있는 설정 파일을 추가해 두었습니다.

## 현재 상태

- `package.json`: Capacitor 실행 스크립트
- `capacitor.config.json`: iPhone 앱 래퍼 설정
- 웹 자산은 루트의 `index.html`, `manifest.json`, `sw.js`를 그대로 사용

## Mac에서 이어서 할 작업

Xcode가 있는 Mac에서 이 저장소를 연 뒤 아래 순서로 진행하면 됩니다.

1. `npm install`
2. `npx cap add ios`
3. `npx cap sync ios`
4. `npx cap open ios`

그다음 Xcode에서:

1. 시뮬레이터 또는 실제 iPhone 선택
2. 앱 이름, 아이콘, 서명 설정
3. 실행 후 UI 확인

## 배포 방향

- 현재 구조는 웹앱을 그대로 내장하는 방식이라 유지보수가 쉽습니다.
- 웹앱 수정 후에는 `npx cap sync ios`만 다시 실행하면 iPhone 앱에 반영할 수 있습니다.

## 참고

이 Windows 환경에서는 `npm`이 잡히지 않아 `ios/` 네이티브 프로젝트 생성까지는 완료하지 못했습니다.
대신 Mac에서 바로 이어서 만들 수 있도록 필요한 설정 파일은 모두 준비해 두었습니다.
