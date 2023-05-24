---
title: "📝 AWS CLF 요약정리"
categories:
  - AWS
tags:
  - 자격증
  - aws
author_profile: true
comments: true
search: true
toc: true
toc_label: "AWS CLF 요약정리"
toc_icon: "minus"
toc_sticky: true
---

# AWS CLF

## 📊 출제 구성

{% capture notice-2 %}

1. 클라우드 개념 : 26%
2. 보안 및 규정 준수 : 25%
3. 기술 : 33%
4. 결제 및 요금제 : 16%
   {% endcapture %}

<div class="notice">{{ notice-2 | markdownify }}</div>

## 🗂 출제 범위

<img src="{{site.url}}{{site.baseurl}}/assets/images/awsService.jpeg" alt="awsService">

## 📝 요약정리

### 🔸 클라우드

#### 클라우드의 이점

##### 민첩성

- 광범위한 기술에 쉽게 액세스할 수 있으므로 더 빠르게 혁신하고 상상할 수 있는 거의 모든 것을 구축할 수 있다.
- 필요에 따라 리소스를 빠르게 구동할 수 있다.
- 단 몇 분 만에 기술 서비스를 배포할 수 있다.

##### 탄력성

- 비즈니스 요구가 변화함에 따라 이러한 리소스를 확장하거나 축소하여 용량을 즉시 늘리거나 줄일 수 있다.
- 오버 프로비저닝할 필요없이 실제로 필요한 만큼 리소스를 프로비저닝하면 된다.

##### 고 가용성

- 가용영역(AZ) 중 하나에 장애가 발생하더라도 애플리케이션이 계속 실행되어야 한다.
- 장애가 발생하더라도 바로 복구하여 서비스를 지속할 수 있다.(단, 복구를 위한 약간의 장애시간도 포함된다.)

##### 비용 절감

- 클라우드를 통해 고정 비용(데이터 센터, 물리적 서버 등)을 가변 비용으로 전환하고, 사용한 만큼만 비용을 지불할 수 있다.
- 규모의 경제 덕분에 직접 운영할 때보다 가변 비용이 훨씬 더 저렴하다.

##### 몇 분 만에 전 세계 배포

- 클라우드를 통해 몇 분 만에 새로운 지리적 리전으로 확장하고 전 세계에 배포할 수 있다.
- AWS는 전 세계에 인프라가 있으므로 사용자는 클릭 몇번으로 여러 물리적 위치에 애플리케이션을 배포할 수 있다.
- 애플리케이션을 최종 사용자와 근접하게 배치하면 지연 시간이 단축되고 사용자 경험이 향상된다.

#### 클라우드 컴퓨팅 유형

##### Infrastructure as a Service(IaaS)

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/IaaS.jpeg){: .align-left}

- IaaS에는 클라우드 IT를 위한 기본 빌딩 블록이 포함되어 있다.
- 일반적으로 네트워킹 기능, 컴퓨터(가상 또는 전용 하드웨어) 및 데이터 스토리지 공간에 대한 액세스를 제공합니다.
- IaaS는 IT 리소스에 대한 최고 수준의 유연성과 관리 제어 기능을 제공합니다.
- 많은 IT 부서 및 개발자에게 익숙한 기존 IT 리소스와 가장 유사합니다.

##### Platform as a Service(PaaS)

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/PaaS.jpeg){: .align-left}

- PaaS를 사용하면 기본 인프라(일반적으로 하드웨어와 운영 체제)를 관리할 필요가 없어 애플리케이션 개발과 관리에 집중할 수 있습니다
- 애플리케이션 실행과 관련된 리소스 구매, 용량 계획, 소프트웨어 유지 관리, 패치 작업 또는 다른 모든 획일적인 작업에 대한 부담 없이 더욱 효율적으로 운영할 수 있습니다.

##### Software as a Service(SaaS)

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/SaaS.jpeg){: .align-left}

- SaaS는 서비스 공급자에 의해 실행되고 관리되는 완전한 제품을 제공합니다.
- 대부분의 경우 SaaS라고 하면 웹 기반 이메일과 같은 최종 사용자 애플리케이션을 말합니다.
- SaaS 오퍼링의 경우 서비스를 유지 관리하는 방법이나 기본 인프라를 관리하는 방법에 대해 생각할 필요가 없습니다.
