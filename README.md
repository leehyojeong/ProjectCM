## Project CM

### 프로젝트 설명
- 건국대학교 4학년 1학기 협동분산시스템 팀 프로젝트
- 멀티 서버의 상황에서 분산 투명성을 제공하기 위해 기존 CM Project를 수정하였다.

- __기존 프로젝트에서 변경할 부분__
  - client 접속 시 default server의 additional server의 리스트와 client가 가진 additional server 리스트가 동기화되지 않는다.
  - client가 접속한 후에 default server(SERVER)에 additional server를 추가하는 경우에는 client가 모든 additional server에 정상적으로 접근이 가능하다.
  - clinet가 접속하기 전에 additional server를 추가한 경우에는 이후 접속한 client가 additional server에 접근이 불가능하다.
  - additional server로 접속할 때 사용자가 접속하고 싶은 additional server의 이름을 알아야 한다.
  
![image](https://user-images.githubusercontent.com/39904216/90328761-eae51380-dfd9-11ea-9228-d2fd70d2b183.png)

- __변경 후 프로젝트__
  - additional server 리스트의 동기화 기능을 추가하였다. 
  - 사용자가 어느 서버로 연결할지 선택하는 것이 아니라 서버들 간 connection 수가 적은 서버에게 자동으로 연결되도록 변경하였다.
  
![image](https://user-images.githubusercontent.com/39904216/90328771-fc2e2000-dfd9-11ea-9064-a07156a86642.png)

### 참고 자료
- https://github.com/ccslab/CM.git
- https://sites.google.com/site/kuccslab/research/cm
