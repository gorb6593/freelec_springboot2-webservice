1. 인텔리제이로 플젝 시작 - O
2. 테스트 코드 작성 - O
3. JPA 연동 - O
4. 화면 (~23-07-05) O
5. 로그인 기능 (~23-07-07) O 
6. aws (~23-07-09) 하는중
7. (putty에서 aws rds 접속이 안되는데 권한 문제인 것 같은데 권한허용해도 안되서 여기하는중)
ec2 자체의 보안그룹에서 보안 인바운드맞추기...
8. 배포 
9. 자동화 
10. 마무리 

★★★오류가 안나면 이상하다. 맑은 정신으로 멘탈잡기★★★


Amazon RDS 데이터베이스 작업할 때, 
1.수정사항 즉시 적용 해놓고 작업시작 하기 => 진짜 세상이 억까하는 느낌들기전에 이것부터 하기
2.db이름 설정안하면 생성안함 (수정할떄도 수정칸에없음)

만난 오류들
1. gitignore 무시하고 올라가는 현상
git rm - r --cached . 
git add . 
=> 깃 캐시 제거 

2. ec2서버에서 java다운로드 안되는 현상
AWS 인스턴스 생성할 때, 

Amazon Machine Image(AMI) 선택할때 
프리티어 가능한거 중에 
Amazon linux2 AMI(HVM)으로 선택해야 다른 오류가 안남...

3. putty접속 문제
no supported authentication methods available (server sent publickey gssapi-keyex gssapi-with-mic)
인스턴스 생성하면서
보안그룹에 ssh 로 포트 22번 내 ip허용해놨는데
내 컴퓨터 아이피가 번경되서 그 후로 꼬여서 다시 했음
내 아이피 고정하거나 변경되면 보안그룹에서 변경해주면됨

4. DB서버 시간 한국시간아님
권한문제로 안되기 시작함 => 9시간 더함

5. rds생성할 때, 보안그룹 default로 잡혀있는데 해당 ec2로 맞추고 거기에 해당하는 보안그룹 열어주기..