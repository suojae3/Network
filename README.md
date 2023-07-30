# CS_Network

### 강의명: 한양대학교 컴퓨터 네트워크 이석복 교수 + Inflearn CS개념 강의<br/><br/> 

### 목차
###
[1.프로토콜이란 무엇인가요?](#01.-프로토콜이란-무엇인가요?)<br/><br/> 
[2.Network Core란 무엇인가요?](#02.-network-core란-무엇인가요?)
[3.그렇다면 이러한 Network Core 에 의한 전달방식 2가지가 무엇인지 설명해주세요](#03.-그렇다면-이러한-network-core-에-의한-전달방식-2가지가-무엇인지-설명해주세요)
[4. Circuit Switching 의 단점을 간략하게 설명해주세요](#04.-Circuit-Switching-의-단점을-간략하게-설명해주세요)
---

### 01. 프로토콜이란 무엇인가요?<br/><br/> 


<img src="https://github.com/suojae3/CS_Network/assets/126137760/f6c7b469-dc91-4899-87b0-543196d4dc2e" width="400" height="200"/>


- 쉽게 말해 기계와 기계간의 대화함에 있어 일종의 약속입니다
- 네트워크 용어에서 나오는 P는 Protocol의 약자가 대부분이며 대표적인 프로토콜로는 인터넷 프로토콜인 TCP/IP가 있습니다

---

### 02. Network Core란 무엇인가요?<br/><br/> 


<img src="https://github.com/suojae3/CS_Network/assets/126137760/14c7a3ef-f161-41c5-86cf-2ce7b28e4802"  width="400" height="200"/><br/><br/> 


- 프로토콜을 준수함으로서 데이터를 전달하게 되는데 이러한 데이터 전달은 중간중간에 라우터가 받아서 전달하게 됩니다
- 네트워크 코어는 간단하게 말해 이러한 라우터의 집합이라고 볼수 있습니다

---


### 03. 그렇다면 이러한 Network Core 에 의한 전달방식 2가지가 무엇인지 설명해주세요

- 네트워크 전달 방식에는 크게 두가지 **Circuit Switching** 과 **Packet Switching** 이 있습니다.


<img src="https://github.com/suojae3/CS_Network/assets/126137760/d90a86de-8f6c-4ff8-9ce8-4093b5fdfbbc" width="400" height="200"/>


- **Circuit Switching** 은 출발지부터 목적지까지 미리 예약을 하고 특정 사용자만을 위해 만들어놓은 방식입니다. (ex_ 옛날 유선전화망)
- 사진처럼 링크 전부를 주는 것이 아닌 어떤 유저한테는 링크 이부분만 주고 이부분만 주고 이런방식


<img src="https://github.com/suojae3/CS_Network/assets/126137760/444cf207-10ce-4217-9492-a53e74fd12b0" width="400" height="200"/>


- **Packet Switching** 은 인터넷에서 사용하는 방식으로, 유저로부터 패킷을 받아 그때그때 올바른 방향으로 전송(forwarding)해주는 방식입니다.

---


### 04. Circuit Switching 의 단점을 간략하게 설명해주세요


<img src="https://github.com/suojae3/CS_Network/assets/126137760/67d82364-5459-408a-8ac7-88d432eae27f" width="400" height="200"/>


- 일반적인 인터넷 사용패턴은 계속해서 데이터를 주고 받는 것이 아닌 일단 클릭후 뉴스같은 걸 보다가 (데이터 주고받지않는 시간), 또 흥미있는게 생기면 클릭(데이터 통신)하는 패턴입니다.
- 만약 Circuit Switching을 사용하면 사용자가 통신하지 않는 시간에도 그 경로가 주어진 사용자에게 한정되기 때문에 낭비가 됩니다

---


### 05. Packet Switching 을 사용할시 생기는 문제들에 대해 설명해주세요


<img src="https://github.com/suojae3/CS_Network/assets/126137760/5e1184f0-85ca-4295-adc3-95c26dfae433"  width="400" height="200"/>


- Packet Switching 의 첫번째 문제점은 **Queueing Delay** 입니다.
- 먼저 라우터로부터 패킷을 받으면 패킷 검사를 하고 (이때 패킷 검사하는 시간이 **Processing Delay**), 이제 outgoing edge로 뿜어내야하는데 만약 outgoing edge에 큐가 길게 늘여져있을 경우 앞에 애들이 나갈 때까지 기다려야합니다. 이 기다리는 시간이 **Queueing Delay** 입니다


!<img src="https://github.com/suojae3/CS_Network/assets/126137760/54264535-9541-4892-a56c-7e4c3c44d1ec" width="400" height="200"/>


- 두번째 문제는 **Transmission Delay**입니다. **Transmission Delay**는 첫번째 비트가 나가는 그 시간부터 마지막 비트가 뿜어져 나가기까지 걸리는 시간입니다 (패킷은 빛의 집합)
- 따라서 Transmission Delay는 패킷 크기를 링크 band width로 나눈 시간이 됩니다
- 비유하자면 패킷이 물바구니이고 링크가 링크 Band Width가 파이프라면 파이프가 크면 물을 한번에 들이붇으면 끝나는 것처럼 **Transmission Delay** 도 비슷한 원리입니다.

---


### 06. Propagation Delay에 대해 설명해주세요


![image](https://github.com/suojae3/CS_Network/assets/126137760/14a3ab67-dd63-46cc-bd68-96c783082a97)


- 패킷이 라우터에서 라우터로 전달될 때 올라온 비트가 도착지로 이동할 때까지 걸리는 시간입니다
- 간단히 정의하자면 **Propagation Delay**는 빛의 속도로 링크 길이를 나눈 것과 같습니다
- 쉽게 말해 그냥 빛의 속도로 링크를 통과하는데 걸리는 시간입니다

---

### 07. Processing Delay 와Transmission Delay 는 어떻게 줄일 수 있을까요?

![image](https://github.com/suojae3/CS_Network/assets/126137760/70f098c3-705c-4c92-9dd3-a04834bd9139)


- Processing Delay 패킷을 확인하는 시간, 비트 에러를 체크하는 시간입니다.
- 간단한 해결방법은 성능좋은 라우터로 갈아치우는 것입니다. 라우터가 좋으면 CPU 성능도 좋은거고 작업을 빠르게 진행할 수 있습니다
- Transmission Delay를 줄이기 위해서는 링크의 BandWidth를 늘리면 됩니다

---

### 08.  **Queueing Delay** 는 어떻게 줄일까요?

- **Queueing Delay** 는 인터넷 사용자 패턴에 달린 문제이기 때문에 가장 골치아픈 문제라고 할 수 있습니다
- 네트워크 상의 문제는 사실상 거의 **Queueing Delay**에서 발생한다고 볼 수 있습니다.
- 사실상 줄이는 방법은.. 마땅치 않습니다. 사용자가 패킷을 그만던지게 하는 방법말고는..

---

### 09. 패킷 유실(Packet Loss)이란 무엇인가요?

![image](https://github.com/suojae3/CS_Network/assets/126137760/05789765-ee8f-4ebd-99c9-fa96e8cc99cf)


- **Queueing Delay**가 발생할 때 패킷이 계속해서 큐에 밀려들면 큐에 들어가지 못하고 버려지는 현상입니다.
- 다시말해 큐가 넘치는 상황에서 패킷이 들어올 때 나타나는 현상이라고 말할 수 있습니다
- 모든 패킷유실이 **Queueing Delay**에서 발생하는 것은 아니지만 대부분의 경우가 이에 해당됩니다
