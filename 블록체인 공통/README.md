# 블록체인 공통
### `블록체인`:
- 누구나 볼 수 있는 공공 거래장부
- 투명성이 극대화 되어 있다
- 모든 노드가 아는 만큼 투명성을 위한 기회비용을 투자한 것
- 지갑에는 얼마가 들어가 있고 어떠한 거래로 돈이 이동했는지 모두 투명하게 공개되어 있다
- 지갑 주소만 알 수 있다면 많은 정보를 알 수 있다.

### `토론`, `투표` 시스템:
- 합의를 위한 시스템으로 합의 알고리즘과 연계된다
- 토론 후 결정을 함에 있어서 중앙의 의견을 따라 가는 것이 아닌 voting을 통해 결정하는 탈중앙화 시스템

### 구조
- 블록에 모든 정보가 적혀있음(크기가 허락하는 한): 거래내용, 거래량 등
- 이러한 블록이 유실되면 없는 거래가 된다
- 이는 시스템을 무너트리는 일이다
- 이러한 점을 해결하기 위해 블록을 유저 수 만큼 카피를 해서 여러게 만든다
- 블록에는 적을 공간이 적기에 이를 이어서 문제를 해결하는데 이 것을 `체인`이라 부른다.
- 체인에 무엇을 연결하는지를 기록해야한다
- 따라서 블록은 헤더, 바디로 구분한다.
- 헤더는 다른 체인과 연결하는 역할, 바디는 거래장부를 적어 놓는다.
- 헤더를 다른 체인에 연결하면 블록 체인이 되는 것이다.
- 헤더를 체인을 통해 다른 블록과 연결하는 것이 Linked List 개념과 유사하다.
- 이러한 블록체인이 유저 수 만큼 여러개 카피되어 존재하고 여러 유저가 이러한 정보를 유지하고 있기에
- 한 블록이 거짓을 적어도 다른 블록에서 알 수가 있다.
- 해킹을 하기 위해서는 전 세계의 블록체인 시스템의 50프로 이상을 동시에 수정하여 데이터를 바꿔야 반영이 된다.
- 이렇게 데이터를 바꾸기 위한 합의론이 합의 알고리즘이다.

### `채굴`
- 블록을 추가로 이어서 장부를 늘리고 싶다(블록이 3개까지 있었는데 4개를 추가로 늘려 네트워크에 기여를 하고 싶다)
- 이렇게 기여를 하게 되면 보상을 요구할 수 있다.
- 이게 바로 코인
- 따라서 많은 사람들이 블록을 늘리기 위해 노력하고 채택되어 이에 따라 코인을 보상 받고 싶을 것
- POW
- 네트워크를 각자의 노력을 통해 유지 시킬 때 보상을 주는 것, 이것이 채굴이고 채굴로서 코인을 받기도 하는 거지

### `합의 알고리즘`
- POW: Proof-of-Work
  - `무언가에 대한 일을 하고 그 일이 제대로 성공했는지에 대한 증명을 하는 것`
  - 일을 많이하면 보상을 주겠다. 내가 많이 일을 한 것을 증명해라
  - 보상을 받아 채굴을 하게 되면 다른 컴퓨터들은 똑같이 복사하는 역할만 수행한다.
  - 최초의 문제를 해결한 사람만 보상을 받는 시스템이기에
  - 유저가 100명이면 100명이 동시에 문제를 풀기위해 작업을 하다 한명만 보상을 받고
  - 남은 99명은 낭비하게 되는 것이다. 유저가 커질수록 이 낭비는 심해질 것이다.
- PoS: Proof-of-Stake(PoW의 낭비를 개선하기 위한 합의 알고리즘)
  - `자신의 지분, 즉 Staking 한 자산을 통해 블록을 생성함`
  - 내가 많이 들고 있음을 증명해라 -> 돈을 많이 가지고 있으면 블록을 찾을 확률이 높다
  - 돈이 많을수록 네트워크가 많으면 피해를 입기에, 판단을 잘해서 네트워크를 뭉게지 않을 것이기에 이득을 주는 것
### `공개키와 비밀키`
- 우편물을 가져가지 못하게 만든 키라 생각하자
- 공개키(public key): 누구나 상대방 지갑 주소를 알면 입금을 할 수 있다. 
- 비밀키(private key): 하지만 출금 하는건 키 가지고 있는 사람만
- 프라이빗 키를 이용해서 퍼블릭 키에 있는 자산을 가져갈 수 있다.
### `Hash Function의 이해`
- Hash: 블록체인은 위변조가 어렵다, 왜 어려운데?
  - 조금만 수정해도 전체가 변한다.
  - 그래서 바뀐걸 알기 쉽다
  - 전체 장부를 비교할 필요가 없는 것
### 클레이튼
- TPS: 1초당 처리할 수 있는 트랜잭션의 규모
  - 1초에 얼마나 많은 거래가 처리되어 블록에 저장 되는지
- IBFT 합의 알고리즘 사용
- 탈중앙화랑은 거리가 있네 그냥 결정하는 사람들이 많은 건데, 오히려 그 많은 사람들을 신뢰할 수 있을까
- BApp
- 오히려 DApp과 Web3.0에 대해서 알아봐야 할듯
