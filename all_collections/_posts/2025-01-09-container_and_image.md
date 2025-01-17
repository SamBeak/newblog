---
layout: post
title: 📦도커 / 컨테이너와 이미지
date: 2025-01-09
categories: ["SamBeak", "Docker", "devops"]
---

# 컨테이너와 이미지 <br>

> ## Container란 무엇인가?

<br>
Docker를 한번이라도 사용해본 적이 있다면 <br>
'컨테이너'라는 단어를 들었을 때, <br>
정확히 어떤 개념인지는 몰라도 <br>
어떻게 동작하는지 그려질 것이다 <br><br>

23년도에 정리했던 개념보다는 <br>
직접 사용하고 경험해봐야 와 닿는 것이 <br>
훨씬 크게 작용하기 때문이다 <br><br>

# 컨테이너? <br>

그럼에도 컨테이너라는 개념은 Docker에서 상당히 중요하다 <br>
그렇기에 체험보다 정확한 개념을 알고 <br>
접근하는 것이 중요하다 <br><br>

윈도우의 경우로 예를 들어 살펴보면<br>
사용자별로 환경이나 <br>
설치 프로그램이 다르다는 것을 알 수 있다 <br><br>
컨테이너도 마찬가지로 <br>
각 컨테이너별로 다른 환경을 제공 받게 된다 <br>
쉽게 말해, 내 컴퓨터 안의 가상 컴퓨터 같은 것이다 <br><br>

가상 컴퓨터라는 말처럼 <br>
각 컨테이너는 각각의 고유한 포트와 <br>
네트워크 주소를 가지고 있고 <br>
저장 공간 또한 별도로 갖게 된다 <br><br>

> ## Image란 무엇인가?

<br>
필자의 경우 <br>
학창시절 게임은 온라인 게임보다는 <br>
CD 게임이 주를 이뤘다 <br>
이 때, CD를 살펴보면 <br>
각 CD 별로 다른 게임이 실행됐는데 <br>
이미지가 바로 이런 역할을 수행한다 <br><br>

정리하면 Container라는 컴퓨터에서 <br>
Image라는 CD를 넣고 실행하는 것이다 <br><br>
