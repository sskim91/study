## Debian 계열 리눅스 우분투 apt 명령어

#### apt-get의 기본 사용법

- 기본 패키지 설치 방법
  - apt-get -y install 패키지 이름
- 패키지 목록의 업데이트
  - apt-get update
- 삭제
  - apt-get remove 패키지 이름
    - 기존 설치된 패키지를 제거한다.
  - apt-get purge 패키지 이름
    - 기존 설치된 패키지를 설정파일을 포함해서 완전히 제거한다.
  - apt-get autoremove
    - 사용하지 않는 패키지를 모두 지운다.
- 내려받은 파일 제거
  - apt-get clean 또는 apt-get autoclean
    - 설치할 때 내려받기한 파일 및 과거의 파일을 제거한다.

#### apt-cache

apt-cache 패키지를 설치하기 전에 패키지에 대한 정보나 의존성 문제를 미리 확인해 볼 수 있다.

- 패키지 정보 보기
  - apt-cache show 패키지이름
    - 패키지의 정보를 화면에 출력한다.
- 패키지 의존성 확인
  - apt-cache depends 패키지이름
    - 패키지에 대한 의존성 정보를 출력한다.
- 패키지 역의존성 확인
  - apt-cache rdepends 패키지이름
    - 이 패키지에 의존하는 다른 패키지의 목록을 보여준다.
