# ET 설치 파일

ET(MongoDB GUI) 설치 파일과 자동 업데이트 정보만 올리는 저장소입니다. 소스 코드는 여기에 없습니다.

**받기: [최신 릴리스](https://github.com/ccn-yun-gibin/et-releases/releases/latest)** 의 Assets 에서

| PC | 파일 |
|---|---|
| 맥 (애플 실리콘 M1·M2·M3·M4) | `ET-<버전>-arm64.dmg` |
| 맥 (인텔) | `ET-<버전>-x64.dmg` |
| 윈도우 (설치) | `ET-<버전>-setup.exe` |
| 윈도우 (설치 없이 실행) | `ET-<버전>-portable.exe` |

맥 종류는 사과 메뉴 → 이 Mac에 관하여 에서 "칩"(Apple → arm64) / "프로세서"(Intel → x64) 로 확인합니다.

## 처음 열 때 (서명 없는 앱)

**맥**
1. dmg 를 열고 ET 를 응용 프로그램(Applications) 폴더로 끌어 넣습니다.
2. 응용 프로그램 폴더에서 ET 를 **우클릭 → 열기 → 열기**.
   막히면 **시스템 설정 → 개인정보 보호 및 보안** 아래 **"그래도 열기"**.
3. "손상되었기 때문에 열 수 없습니다" 가 나오면 터미널에서 한 번:
   ```
   xattr -dr com.apple.quarantine /Applications/ET.app
   ```
4. 새 버전으로 덮어쓴 뒤 처음 켤 때 키체인 'ET Safe Storage' 확인 창이 뜨면 **항상 허용** (저장한 접속 비밀번호를 그대로 쓰기 위해).

**윈도우**
- "Windows의 PC 보호" 창에서 **추가 정보 → 실행**.

## 업데이트

ET 는 이 저장소의 최신 릴리스를 6시간마다 확인해 새 버전이 있으면 알려 줍니다 (Settings → Updates 에서 끄기·바꾸기 가능).
- 윈도우 설치판: 알림에서 받기 → **Restart and Update**
- 맥·윈도우 포터블: 알림에서 받기 → 받은 파일을 열어 덮어쓰기

`et-update.json` 은 앱이 읽는 업데이트 정보입니다(버전·파일 크기·sha512).
