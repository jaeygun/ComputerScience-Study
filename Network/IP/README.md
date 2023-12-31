# IP
`IP`란 인터넷 프로토콜(Internet Protocol)의 약자로 인터넷 상에서 데이터를 주고받기 위한 통신규약이다.

통신을 해서 데이터를 주고 받기 위해서 출발지와 도착지가 존재해야 하는데 이를 위해서 생겨난 개념이 IP주소이다.

IP주소는 쉽게 비유하자면 각 장비에 부여되는 고유 주소이다.

<br/>

## IPv4
`IPv4`란 IP version 4의 약자로 제일 첫번째로 사용된 프로토콜이다. IPv4같은 경우 0.0.0.0 ~ 255.255.255.255 까지 4개로 구분된 .의 형태로 나타나지고 각 자리는 0 ~ 255까지 대략적으로 42억개의 IP주소를 생성할 수 있다.

하지만 점점 인터넷이 발달하면서, 이 42억개의 주소가 만약 모두 사용된다는 문제가 발생할 수 있다.

이를 위해서 고안된 새로운 체계가 `IPv6`이다.

<br/>

## IPv6
`IPv6`란 IP version 6의 약자로 128비트의 주소공간은 128 비트로 표현할 수 있는 2^128개인 약 3.4x1038개(340,282,366,920,938,463,463,374,607,431,768,211,456개) 의 주소를 갖고 있어 거의 무한대로 쓸 수 있다.

이렇게 IPv6는 IPv4보다 주소 할당의 갯수 뿐만 아니라 네크워크 속도나 보안적인 부분에서 뛰어나지만 기존의 주소체계를 완전히 변경하기에는 천문학적인 비용이 들기 때문에 제대로 상용화가 되지 않았다.

<br/>

## 그렇다면?
그렇다면 IPv4의 체계로 우리는 계속 사용하고 있는데 사실 이 42억개의 주소는 이미 모두 고갈 되었다. 하지만 우리는 IP가 할당받을 때 혹시 IP가 부족할까 하는 걱정은 전혀 하지 않는다. 그 이유를 설명하기 위해 `사설 IP`에 대해서 알 필요가 있다.

<br/>

![IP](./image/Network(IP).png)

IP는 크게 `공인IP`와 `사설IP`로 구분할 수 있다. 비유를 들어서 설명을 하자면 A학교에서 사용되는 피시들은 그 학교 안에서만 식별 가능한 IP를 할당 받는다. 이 IP들이 `사설IP`이다. 사설 IP의 가장 큰 특징으로는 외부에서 해당 IP를 찾을 수 없다는 것이다. 내가 학교에서 사용 중인 PC의 IP는 192.168.1.10인데 이 IP는 외부에서 조회가 전혀 안된다는 의미이다.<br/>
(ex. 192.168.1.10, 192.168.1.11, 192.168.1.12 ...)

이러한 사설IP들은 외부로 통신을 시도하게 되면 라우터에서 IP가 NAT되어서 외부에서도 식별 가능한 `공인IP`로 변경이 되어서 외부로 통신을 시도하게 된다.

그러면 이렇게 `사설IP`를 사용하는 이유는 무엇일까?
1. IPv4의 부족문제 <br/>
공유기가 없다면 특정 망에 있는 피시 한대한대 모두 공인IP를 따로 할당 받아야하는 문제가 있다. 공유기에 공인IP를 할당받게 되면 망 안에서 사용되는 피시들은 모두 사설 IP로 할당 받아 사용이 가능하다.

2. 보안성<br/>
사설IP가 할당 된 피시 각각은 외부에서 접근이 불가능하기 때문에, 일반적으로 인터넷 공유기가 이러한 일종의 보안의 역활도 하고 있는 것이다.

<br/>

> Q: NAT란?<br/>
> A: NAT란 Network Address Translation의 약자로, 네트워크 주소 변환을 말한다. 쉽게 이해하자면 외부와 통신이 불가능한 망을 사설망이라고 하고 해당 망에서 사용되는 IP들을 사설IP라고 한다면, 이 사설IP들은 외부와 통신을 위해서 외부와 통신이 가능한 공인IP로 라우터에서 변환되어서 통신을 하게 되는데, 이를 NAT라고 한다.

<br/>

> Q: 라우터란?<br/>
> A: 라우터란 패킷을 목적지까지 정확하게 전달하기 위해 다음 네트워크 지점을 연결하는 장비라고 할 수 있다. `라우터의 목적으로는 서로 다른 네트워크를 연결하는 것`이라고 할 수 있다.



<br/>
<br/>
<br/>

## _References_
- https://c0mp.tistory.com/927
- https://inpa.tistory.com/entry/WEB-%F0%9F%8C%90-IP-%EA%B8%B0%EC%B4%88-%EC%82%AC%EC%84%A4IP-%EA%B3%B5%EC%9D%B8IP-NAT-%EA%B0%9C%EB%85%90-%EC%A0%95%EB%A7%90-%EC%89%BD%EA%B2%8C-%EC%A0%95%EB%A6%AC