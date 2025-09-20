# WarehouseWreckage
UE5 블루프린트를 활용한 미니 게임



<img width="500" alt="image" src="https://github.com/user-attachments/assets/673ae123-ef13-491e-adc6-61804e065cd1" />
<br><br>

- 목표: UE5 블루프린트로 물리 상호작용, 스폰, 입력, 함수화까지 경험하며 작은 슈터 플레이 루프 구성
- 결과: 탄약 소모 규칙과 분기, 발사체 스폰, 5초 후 레벨 재시작 루프 구현 완료

### Concept

- 에디터 실무: Content Drawer 단축키, StarterContent 추가, Level Blueprint 열기
- 블루프린트 기초: Event Graph, 노드와 핀의 의미, 실행 핀과 데이터 핀 구분
- 오브젝트 모델: Object, Actor, Component, Reference의 역할과 메모리 관점
- 물리와 힘: Simulate Physics, Gravity, Mass, Impulse vs Force, Vel Change 옵션
- 벡터와 회전: Vector 연산 기본, Control Rotation으로 조준과 발사 정렬
- 데이터 타입: Vector, Rotator, Transform 같은 구조체 활용과 타입 안정성
- 에셋·레벨링: 에셋 임포트, BSP로 공간 구성, 시작 맵 지정, 머티리얼과 조명 필터링
- 컴포넌트: 루트 정적 컴포넌트, 자식 컴포넌트 트리 구성 원리
- 충돌: Wireframe, Player Collision 보기, Static Mesh Editor에서 Collision 생성/제거
- 스폰: Spawning, Transform, Return pin 이해
- 상태와 로직: 변수 선언과 Getter/Setter, Bool과 Branch로 탄약 소진 처리
- 함수화: Collapse to Function, 입출력 지정, 순수 함수 vs 일반 함수, 멤버 함수와 Self
- 레벨 제어: Delay와 Open Level로 Retry Loop 구성
<br>
- -> 전부 블루프린트를 이용해 구현
<br><br>

### Practice

- 발사체 BP 생성, 발사 시 오브젝트 이름 출력 로그
- 탄약 변수 관리, 0 이하 방지 Branch와 "Out of Ammo" 메시지
- 탄약 소진 시 5초 Delay 후 레벨 재시작
<br><br>

### Tip and Best practice
- BP_ 접두어로 블루프린트 클래스 네이밍하고, 클래스 편집으로 인스턴스 일괄 반영
- 사이드 이펙트 없는 계산은 순수 함수로 만들어 그래프를 간결하게 유지
- 충돌 문제는 Collision 뷰와 Static Mesh Editor에서 원인 파악 후 간소화 Collision 적용


-----
Based on [the lecture](https://www.udemy.com/course/unrealcourse-korean/?couponCode=KEEPLEARNING) on Udemy
