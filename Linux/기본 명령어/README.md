### 리눅스 기본 명령어

<table>
  <tr>
    <th>명령어</th>
    <th>사용법</th>
  </tr>
  <tr>
    <td>ls</td>
    <td>파일 리스트 보기(dir)<br>a : 현재 디렉터리의 목록 (숨김파일 포함)<br>l  : 현재 디렉터리의 목록을 자세히 보여줌<br>t : 최종 수정된 시간별로 정렬<br>r : 파일을 역순, 즉 내림차순으로 배열<br>R : 하위 디렉터리의 파일도 모두 보여줌<br><br>[사용 예]<br># ls -al,<br># ls -aC<br># ls -R</td>
  </tr>
  <tr>
    <td>cd</td>
    <td>디렉터리를 변경<br><br>[사용 예]<br>#cd               -    현재 사용자의 홈 디렉터리로 이동<br>#cd ~사용자   -   사용자의 홈 디렉터리로 이동<br>#cd..             -   바로 상위의 디렉터리로 이동 <br>#cd /etc/systemd     -     /etc/systemd 디렉터리로 이동(절대 경로)<br>#cd ../etc/systemd   -   상대 경로로 이동. 현재 디렉터리의 상위로 이동한 후에 다시 /etc/systemd로 이동 </td>
  </tr>
  <tr>
    <td>pwd</td>
    <td>현재 디렉터리의 전체 경로를 화면에 보여준다<br><br>[사용 예]<br>#pwd</td>
  </tr>
  <tr>
    <td>rm</td>
    <td>파일이나 디렉터리를 삭제한다.<br><br>rm [options] file(s)<br><br>i : 삭제 시 정말 삭제 할 지 확인하는 메시지가 나옴<br>f : 삭제 시 확인하지 않고 바로 삭제<br>r : 디렉터리와 그 아래에 있는 하위 디렉터리를 강제로 전부 삭제함.<br><br>[사용 예]<br>#rm abc.txt<br>#rm -i abc.txt<br>#rm -f abc.txt<br>#rm -r abc      &gt; 편리하지만 주의해서 사용해야 함<br><br>* 리눅스에서는 삭제한 파일이나 폴더를 복구하기가 상당히 어렵기 때문에 삭제하기 전 주의해야 한다.</td>
  </tr>
  <tr>
    <td>rmdir</td>
    <td>remove directory 디렉터리를 지운다. 만약 디렉터리가 비어있지 않으면 지울 수 없다.</td>
  </tr>
  <tr>
    <td>cp</td>
    <td>Copy의 약자로 파일이나 디렉터리를 복사한다. 새로 복사한 파일은 사용자의 소유가 된다.<br>그러므로 명령을 실행하는 사용자는 해당 파일의 읽기 권한이 필요하다.<br><br>[사용 예]<br>#cp abc.txt cba.txt   -  abc.txt를 cba.txt라는 이름으로 바꿔서 복사<br># cp -r abc cba        -  디렉터리 복사. abc 디렉터리를 cba 디렉터리로 복사</td>
  </tr>
  <tr>
    <td>touch</td>
    <td>크기가 0인 새 파일을 생성하거나, 이미 파일이 존재한다면 파일의 최종 수정 시간을 변경한다. <br><br>[사용 예]<br>#touch abc.txt  - 파일이 없을 경우엔 abc.txt라는 빈 파일을 생성하고<br>                          파일이 존재 할 경우에는 파일의 최종 수정 시간을 현재 시각으로 변경</td>
  </tr>
  <tr>
    <td>mv</td>
    <td>Move의 약자로 파일이나 디렉터리의 이름을 변경하거나, 다른 디렉터리로 옮길 때 사용한다.<br><br>[사용 예]<br>#mv abc.txt ~/Desktop  -    abc.txt를 Desktop 디렉터리로 이동<br>#aaa bbb ccc ddd         -    aaa, bbb, ccc 파일을 /ddd 디렉터리로 이동<br>#abc.txt www.txt           -    abc.txt의 이름을 www.txt로 변경해서 이동</td>
  </tr>
  <tr>
    <td>mkdir</td>
    <td>Make Directory의 약자로 새로운 디렉터리를 생성한다.<br><br>[사용 예]<br>#mkdir abc : 현재 디렉터리 아래에 abc라는 디렉터리 생성<br>#mkdir -p /def/fgh : /def/fgh 디렉터리를 생성하는데, 만약 '/fgh'의 부모 디렉터리인 '/def' 디렉터리가 없으면 자동 생성</td>
  </tr>
  <tr>
    <td>cat</td>
    <td>파일의 내용을 화면에 보여준다. 여러 개의 파일을 나열하면 파일을 연결해서 보여준다.<br><br>[사용 예]<br>#cat a.txt b.txt  -   a.txt와 b.txt를 연결해서 파일의 내용을 화면에 보여줌</td>
  </tr>
  <tr>
    <td>head,<br>tail</td>
    <td>텍스트 형식으로 작성된 파일의 내용을 화면에 출력한다.<br><br>[사용 예]<br>#head -n filename  -   n줄 만큼 위에서부터 보여준다.<br>#tail -n filename      -  n줄 만큼 아래에서부터 보여준다.<br><br>#head -5 filename   -  앞 5행만 출력<br>#tail -5 filename      -  마지막 5행만 출력</td>
  </tr>
  <tr>
    <td>more</td>
    <td>텍스트 형식으로 작성된 파일을 페이지 단위로 화면에 출력한다.<br>space를 누르면 다음 페이지<br>b를 누르면 앞 페이지로 이동<br>q를 누르면 종료<br><br>[사용 예]<br>#more filename</td>
  </tr>
  <tr>
    <td>less</td>
    <td>more 명령어와 용도가 비슷하지만 기능이 더 확장되어 있다.<br><br>[사용 예]<br>#less filename</td>
  </tr>
  <tr>
    <td>file</td>
    <td>해당 파일이 어떤 종류의 파일인지를 표시해준다.<br><br>[사용 예]<br>#file filename</td>
  </tr>
  <tr>
    <td>clear</td>
    <td>현재 사용중인 터미널 화면을 깨끗하게 지워준다.<br><br>[사용 예]<br>#clear</td>
  </tr>
</table>
