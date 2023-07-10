---
layout: post
title: 🎞 브라우저 렌더링
date: 2023-06-19
categories:
  ["SamBeak", "BrowesrRandering", "Randering", "CRP", "브라우저랜더링"]
---

# 브라우저의 기본 구조

<br>
브라우저 렌더링을 살펴보기 앞서, 브라우저의 구성 요소는 다음과 같다. <br>

- 사용자 인터페이스 : 주소 표시줄, 북마크 메뉴 등 페이지를 보여주는 창을 제외한 모든 부분으로 사용자와 상호작용하는 부분이다. <br>
- 브라우저 엔진 : 사용자 인터페이스와 렌더링 엔진 사이의 동작을 제어하는 엔진으로 페이지 로드와 렌더링 엔진 전달 같은 역할을 한다.<br>
- 렌더링 엔진 : 요청한 컨텐츠를 표시하는 엔진, 화면 출력 <br>
- 네트워크 요청 : HTTP 요청을 보내고 서버로부터 리소스를 받아온다. 각 플랫폼 하부에서 실행되고 독립적 인터페이스이다. <br>
- UI 백엔드 : 콤보 박스, 창 등 기본적 장치를 그려내고, 플랫폼에 명시하지 않은 일반적 인터페이스 <br>
- 자바스크립트 해석기 : 자바스크립트 코드를 해석하며 실행하는 역할 <br>
- 자료 저장소 : 쿠키, 로컬 스토리지 등 클라이언트 측 데이터를 저장하고 웹 데이터 베이스가 정의돼 있는 장소이다. <br>
- 브라우저 확장 기능 : 추가 기능 혹은 사용자 지정 기능을 제공하는 확장 프로그램을 실행하고 관리한다. <br>

# 브라우저의 렌더링 원리

<br>
브라우저는 웹킷(webkit)이나 게코(Gecko) 등 렌더링 엔진을 사용해 화면의 요소를 렌더링한다. <br>
렌더링 엔진은 HTML, CSS, JS로 렌더링을 하는 경우, CRP(Cirtical Reandering Path) 프로세스를 사용해 진행된다. <br><br>

CRP 프로세스는 페이지의 초기 로딩 속도와 사용자 경험에 중요한 영향을 미친다. <br>
리소스의 아북이나 캐싱, 지연 최소화 등을 사용한 최적화를 통해 빠른 로딩과 부드러운 렌더링을 구현할 수 있다. <br><br>

> CRP 프로세스

- 1. HTML 파싱 : DOM(Document Object Model) TREE 구축
- 2. CSS 파싱 : CSSOM(CSS Object Model) TREE 구축
- 3. JS 실행 // HTML 내부 스크립트 존재시 HTML 파싱은 중단된다.
- 4. 렌터 트리(Render Tree) 구축 : DOM과 CSSOM을 결합하여 형셩되고, 레이아웃 정보와 스타일 정보가 포함된다. <br>
     // 화면에 없고, 공간도 차지 않는 요소는 구축X
- 5. Layout/Reflow 단계 : 뷰포트 기반 렌터 트리의 각 노드가 갖는 위치와 크기를 계산한다.
- 6. Paint 단계 : 렌더 트리를 기반으로 화면에 픽셀로 그리는 작업을 수행한다. 실제로 화면에 내용이 표시된다.

파싱은 문서를 해석하고 이해하는 과정을 의미한다. <br>

<br>