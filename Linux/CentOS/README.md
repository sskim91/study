#### yum의 기본 사용법

- 기본 패키지 설치 방법
  - yum -y install 패키지 이름

- rpm 파일 설치 방법
  -  yum localinstall rpm파일이름.rpm
  - rpm파일이 있다면 'rpm -Uvh' 대신 'yum localinstall'을 실행해 패키지를 설치 할 수있다.
    - 장점 은 현재 디렉터리의 rpm 파일에 의존성 문제가 있을 때 문제를 해결할 수 있는 파일을 인터넷에서 다운로드 해서 설치해 준다는 점이다.

- 업데이트 가능한 목록 보기
  - yum check-update
    - 시스템에 설치된 패키지 중에서 업데이트가 가능한 패키지의 목록을 출력한다.

- 업데이트
  - yum update 패키지이름

- 삭제
  - yum remove 패키지이름
    - 기존 설치된 패키지를 제거한다.

- 정보 확인
  - yum info 패키지이름
    - 패키지 요약 정보를 보여준다.
