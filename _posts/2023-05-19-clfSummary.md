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

### 🔸 액세스

#### AWS Management Console

- AWS 클라우드를 액세스하고 관리하는데 필요한 모든 것을 하나의 웹 인터페이스에서 활용할 수 있다.

#### AWS CLI(AWS Command Line Interface)

- AWS 서비스를 관리하는 통합 도구이며, 하나의 도구만 다운로드하여 구성하면 여러 개의 AWS 서비스를 명령줄에서 제어하고 스크립트를 통해 자동화할 수 있다.

#### 소프트웨어 개발 키트(SDK)

- 개발자를 위한 플랫폼별 구축 도구 세트이다.
  ##### SDK 사용이점
  - 애플리케이션에 통합할 수 있는 사전 빌드된 구성 요소와 라이브러리를 제공하여 **개발 효율성을 높인다.**
  - 개발자가 애플리케이션을 빠르게 구축하고 통합할 수 있는 도구를 제공하여 **더 빠르게 배포**할 수 있도록 한다.
  - 개발자가 소프트웨어 애플리케이션을 **빌드, 테스트 및 배포할 수 있도록 사전 빌드된 모듈, 구성요소, 패키지 및 도구를 제공**한다.
  - 애플리케이션 개발에 **필요한 시간과 리소스를 줄여준다.**

### 🔸 분석(Analytics)

#### Amazon Kinesis

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/kinesis.png){: .align-left-clf}

- **실시간으로 스트리밍 데이터**를 손쉽게 수집, 처리 및 분석할 수 있으므로 새로운 정보에 신속하게 대응할 수 있다.
- **완전관리형**으로 스트리밍 애플리케이션을 운영하므로 사용자는 인프라를 관리할 필요가 없다.
- 모든 규모의 스트리밍 데이터를 처리하고 매우 짧은 지연 시간으로 수많은 소스의 데이터를 처리할 수 있다.**(확장성)**
- 모든 데이터가 수집된 후에야 처리를 시작할 수 있는 것이 아니라 데이터가 수신되는 대로 처리 및 분석하여 즉시 대응이 가능하다.

#### Amazon Athena

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/athena.png){: .align-left-clf}

- **페타바이트** 규모 데이터를 상주 위치에서 쉽고 유연하게 분석한다.
- 오픈소스 프레임워크에 구축된 서버리스 **대화형 분석 서비스**로 개방형 테이블과 파일 형식을 지원한다.
- **실행된 쿼리에 대한 요금만 지불**하므로 구성, 소프트웨어 업데이트 또는 인프라 확장에 따른 비용을 절약할 수 있다.

#### Amazon QuickSight

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/quickSight.png){: .align-left-clf}

- 모든 데이터 연결 및 크기 조정 가능하고 사용자 지정 가능한 대시보드 구축 가능하다.
- 모두를 위한 진정한 셀프 서비스 BI 지원하고 네이티브 AWS 서비스 통합 가능하다.
- 관리할 서버가 없으며, 사용량에 따라 요금 지불한다.

### 🔸 개발자 도구(Developer Tools)

#### AWS CodeBuild

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/codeBuild.png){: .align-left-clf}

- 자체 빌드 서버를 설정, 관리, 패칭할 필요가 없다.
- 용량을 **자동으로 확장**할 수 있으므로 빌드가 실행 대기열에 대기하지 않는다.
- **구축하는 데 사용한 시간만큼만 요금을 지불**한다.
- 사전 패키징된 구축 환경 또는 자체 구축 환경을 사용하고 **사용자의 키로 아티팩트를 암호화**할 수 있다.

#### AWS codeCommit

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/codeCommit.png){: .align-left-clf}

- 자체 소스 제어 서버를 호스팅, 유지 관리, 백업, 확장할 필요가 없다.
- 전송 중 자동 암호화된 파일을 사용하여 **리포지토리에 대해 사용자별 액세스**를 지정할 수 있다.
- 확장 가능하고 이중화이며 내구성이 뛰어난 아키텍쳐를 통해 리포지토리의 고가용성과 접근성을 유지할 수 있다.
- AWS 기반의 구축, 스테이징 및 프로덕션 환경에 가깝게 리포지토리를 유지할 수 있다.

#### AWS codeDeploy

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/codeDeploy.png){: .align-left-clf}

- 애플리케이션을 자동화하고, 개발, 테스트, 프로덕션 환경에 **일관되게 배포**할 수 있다.
- 플릿 상태를 모니터링하고 필요에 따라 업데이트를 **자동으로 롤백**할 수 있다.
- AWS Management Console 또는 AWS CLI를 통해 애플리케이션 배포를 시작하고 배포상태를 추적할 수 있다.
- 기존 설정 코드를 재사용하고 기존 소프트웨어 릴리스 프로세스나 지속적인 전송 도구 체인과 통합할 수 있다.

### 🔸 데이터베이스(Database)

#### Amazon Aurora

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/aurora.png){: .align-left-clf}

- MySQL 및 PostgreSQL과 호환되는 완전관리형 관계형 데이터베이스 엔진으로 MySQL보다 최대 5배 많은 처리량과 PostgreSQL보다 3배 **많은 처리량**할 수 있다.
- 선불약정이 없어 **사용한 만큼만 비용을 지불**한다.
- 서버리스와 같은 혁신 기능이 포함된 완전관리형 데이터베이스를 통해 사용자 만족도를 높이는 애플리케이션 구축에 집중하여 생산성을 개선하고 총 소유 비용을 낮출 수 있다.
- 뛰어난 **보안성과 가용성, 내구성**을 가지고 있다.

#### Amazon DynamoDB

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/dynamodb.png){: .align-left-clf}

- 모든 규모에서 고성능 애플리케이션을 실행하도록 설계된 완전관리형의 **서버리스 키-값 NoSQL데이터베이스**이다.
- 자동백업 및 복원 **높은 가용성과 안정성을 바탕**으로 데이터를 보호한다.
- 무제한 처리량과 스토리지와 **자동 다중 리전 복제 기능**을 사용하여 앱을 제공할 수 있다.
- 요구사항에 따라 **자동으로 확장되고 축소**되는 완전관리형 서버리스 데이터베이스이므로 비용을 최적화할 수 있다.

#### Amazon RDS

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/rds.png){: .align-left-clf}

- AWS 클라우드에서 관계형 데이터베이스를 보다 **쉽게 설정, 운영 및 확장**할 수 있게 해주는 웹 서비스이다.
- 업계 표준 관계형 데이터베이스에 **비용 효율적이고 크기 조정이 가능한 용량을 제공**하고 일반적인 데이터베이스 관리 작업을 관리한다.
- 선택한 관계형 데이터베이스 엔진을 클라우드 or 온프레미스에 배포하고 크기를 조정할 수 있다.
- 다중 AZ 배포로 **고가용성**을 가진다.

#### Amazon ElastiCache

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/elasticache.png){: .align-left-clf}

- **신속한 관리형 인 메모리 시스템**에서 정보를 검색할 수 있는 기능을 지원함으로써 웹 애플리케이션의 성능을 향상시킬 수 있다.
- 사용자 작업과 쿼리에 대한 로드 및 **응답 시간이 향상**될 뿐 아니라 웹 애플리케이션 확장에 따른 **비용도 절감**된다.
- 고가용성 및 확장성을 제공한다.

#### Amazon Redshift

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/redshift.png){: .align-left-clf}

- **데이터웨어하우스**이다.
- 운영 데이터베이스 및 데이터 레이크에서 정형 데이터 및 반정형 데이터를 분석하고 AWS가 설계한 하드웨어 및 기계 학습을 사용해 어떤 규모에서든 **최고의 가격 대비 성능**을 지원한다.
- 데이터 웨어하우스 인프라를 관리할 필요 없이 모든 데이터에 대해 몇 초 만에 분석을 실행하고 확장할 수 있다.

### 🔸 저장소(Storage)

#### AWS Storage Gateway

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/storageGateway.png){: .align-left-clf}

- 온프레미스 소프트웨어 어플라이언스를 클라우드 기반 스토리지와 연결하여 조직의 온프레미스 IT 환경과 AWS 스토리지 인프라 간의 원활하고 안전한 통합을 제공하는 서비스이다.
- 비용 효율적인 백업 및 신속한 재해 복구를 위해 데이터를 AWS 클라우드에 안전하게 업로드할 수 있다.

#### Amazon EFS

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/efs.png){: .align-left-clf}

- 스토리지 용량과 성능을 프로비저닝하거나 관리하지 않고도 파일 데이터를 공유할 수 있도록 **완전히 탄력적인 서버리스 파일 스토리지를 제공**한다.
- 애플리케이션 중단 없이 온디맨드 방식으로 페타바이트까지 확장하고 파일을 추가 및 제거함에 따라 **자동으로 확장 및 축소**하도록 구축되었다.
- 간단한 웹 서비스 인터페이스가 있으므로 **파일 시스템을 쉽고 빠르게 생성하고 구성**할 수 있다.
- 모든 파일 스토리지 인프라를 관리하므로 복잡한 파일 시스템 구성을 배포, 패치 및 **유지 관리하는 복잡성**을 피할 수 있다.

#### AWS Snowball

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/snowball.png){: .align-left-clf}

- 페타바이트 규모의 데이터 전송 디바이스이다.
- Amazon S3 간에 데이터를 가져오거나 내보낼 수 있으며 인터넷을 사용하지 않고 하나 이상의 장치로 데이터를 물리적으로 전송할 수 있다.

##### ➕ AWS Snowball Edge

- 온보딩 컴퓨팅으로 100TB 데이터 전송 디바이스이다.

#### AWS Backup

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/backup.png){: .align-left-clf}

- 하이브리드 워크로드 전반에서 데이터 보호를 중앙 집중화하고 자동화하는 **완전관리형 서비스**이다.
- 정책을 기반으로 대규모 데이터 보호를 간편하고 비용 효율적으로 수행할 수 있다.
- 중앙 집중식 콘솔, 자동화된 백업 일정 관리, 백업 보존 관리, 백업 모니터링 및 알림을 제공한다.

#### AWS S3

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/s3.png){: .align-left-clf}

- 언제든지 어디서나 원하는 양의 데이터를 저장하고 검색하는 데 사용할 수 있는 간편한 웹 서비스 인터페이스를 제공한다.
- 클라우드 네이티브 스토리지를 사용하는 애플리케이션을 손쉽게 구축할 수 있다.
- **확장성**이 뛰어나고 **사용한 만큼만 비용을 지불**하므로 작은 규모에서 시작해 성능 또는 안정성 저하 없이 원하는 대로 애플리케이션을 확장할 수 있다.

🔻 아래 비교하여 알아두기!
{: .red-font}

- ##### ➕ AWS S3 Standard

- 일반적으로 **한 달에 한 번 이상 자주 액세스**하는 데이터에 대해 밀리초 단위의 액세스 대기 시간과 높은 처리 성능을 지원하는 내구성 강한 스토리지를 제공한다.
- 일년 동안 여러 가용 영역에 걸쳐 **99.99%의 데이터 가용성과 99.999999999%의 객체 내구성**을 제공한다.
- 저장 AZ은 **최소 3개이상**이여야 한다.
- 검색 요금은 없고 수명 주기 정책을 사용한다.
- ##### ➕ AWS S3 Standard-IA

- 액세스 빈도가 낮지만 필요할 때 빠르게 액세스해야 하는 데이터에 적합하다.
- 일년 동안 여러 가용 영역에 걸쳐 **99.99%의 데이터 가용성과 99.999999999%의 객체 내구성**을 제공한다.
- 저장 AZ은 **최소 3개이상**이여야 한다.
- 30일 이내에 S3 Standard-IA에서 삭제된 데이터는 **30일** 전체에 대한 요금이 부과된다.(GB당 스토리지 요금과 GB당 검색 요금)
- S3 **수명 주기 정책을 사용**하여 스토리지 간에 자동으로 객체를 전환할 수 있다.
- 장기 파일 스토리지, 이전 동기화 및 공유 스토리지, 다른 오래된 데이터에 적합하다.
- ##### ➕ AWS S3 One Zone-IA

- 단일 가용 영역 내에 데이터를 중복으로 저장하여, 지리적으로 분리된 여러 가용 영역 전체에 데이터를 중복 저장하는 지리적으로 중복된 S3 Standard-IA 스토리지보다 20% 저렴하다.
- 일년 동안 여러 가용 영역에 걸쳐 **99.99%의 데이터 가용성과 99.999999999%의 객체 내구성**을 제공한다.
- 저장 AZ은 **오직 1개**여야 한다.
- 스토리지 클래스의 데이터는 가용 영역의 물리적 손실 또는 가용성 손실에 대해 복원력이 유지되지 않는다.
- S3 **수명 주기 정책을 사용**하여 스토리지 간에 자동으로 객체를 전환할 수 있다.
- 백업 복사본, 재해 복구 복사본 또는, 손쉽게 재생성 가능한 기타 데이터 등 자주 액세스하지 않는 스토리지에 적합하다.

#### Amazon EBS

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/ebs.png){: .align-left-clf}

- EC2 인스턴스에 사용할 블록 수준 스토리지 볼륨을 제공한다.
- 포맷되지 않은 원시 블록 장치처럼 작동한다.
- 빠르게 액세스할 수 있어야 하고 장기 지속성이 필요한 데이터에 사용이 적합하다.
- 사용한 만큼 비용을 지불한다.

### 🔸 Cloud Financial Management

#### AWS Budgets

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/budgets.png){: .align-left-clf}

- 예산 비용 또는 사용량을 초과(또는 초과할 것으로 예상)될 때 알려주는 예산을 설정할 수 있다.

<br/>
<br/>
<br/>

#### AWS Cost & Usage Report

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/cost&usageReport.png){: .align-left-clf}

- 결제 보고서를 작성하고 게시하여 클라우드 비용 내역을 분류한다.
- 사용하면 계정에 대한 가장 포괄적인 비용 및 사용량 데이터를 검토하고 항목화하며 정리할 수 있다.

<br/>
<br/>

#### Amazon CloudWatch

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/cloudwatch.png){: .align-left-clf}

- 실시간 로그, 지표 및 이벤트 데이터를 자동화된 대시보드에 수집하고 이를 시각화하여 인프라 및 애플리케이션 유지 관리를 간소화한다.
- 향후 용량 요구 사항을 이해하고 예측하는 데 관측성을 사용하면 예약 및 스팟 요금을 통해 가능한 **비용 절감 효과**를 얻을 수 있다.

#### AWS CloudFormation

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/cloudFormation.png){: .align-left-clf}

- 개발자와 기업이 손쉽게 관련 AWS 및 서드 파티 리소스의 모음을 쉽게 생성하고 순서에 따라 예측 가능한 방식으로 프로비저닝 및 관리할 수 있는 방법을 제공하는 서비스이다.
- 친숙한 프로그래밍 언어를 사용하여 클라우드 애플리케이션 리소스를 모델링한 후 사용자 IDE에서 직접 CloudFormation을 사용하여 인프라를 프로비저닝할 수 있다.
- ex) 사용자가 리소스 프로비저닝 프로세스를 자동화하여 코드형 인프라를 배포할 수 있는 AWS서비스는?
  <br/>= AWS CloundFormation

#### AWS License Manager

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/license.png){: .align-left-clf}

- 소프트웨어 공급업체(ex: Microsoft, SAP, Oracle 및 IBM)의 소프트웨어 라이선스를 AWS 및 온프레미스 환경에서 중앙 집중식으로 쉽게 관리할 수 있게 해주는 서비스이다.
- 라이선스 사용에 대한 제어 및 가시성을 제공하여 라이선스 초과를 제한하고 비준수 및 잘못된 보고의 위험을 줄일 수 있다.

#### AWS Config

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/config.png){: .align-left-clf}

- AWS 계정에 있는 AWS 리소스의 구성을 자세히 보여준다.
- 내부 정책 및 모범 사례를 준수하는지 확인하기 위해 **빈번한 감사**가 필요한 데이터로 작업할 수 있다.
- 리소스가 생성, 변경 또는 삭제될 때 지속적으로 리소스를 평가한다.

<br/>

#### AWS OpsWorks

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/opsworks.png){: .align-left-clf}

- Puppet 또는 Chef를 사용하여 클라우드 엔터프라이즈에서 애플리케이션을 구성하고 운영하는 데 도움이 되는 구성 관리 서비스이다.

<br/>
<br/>

#### AWS CloudTrail

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/cloudTrail.png){: .align-left-clf}

- AWS Management Console,AWS SDK, 명령줄 도구 및 기타AWS 서비스를 통해 이루어진 API 및 비 API **계정 활동에 대한 기록**을 제공한다.
- 관리 활동을 분석하여 사용자의 AWS 계정에서 비정상적인 API 호출률 또는 오류율 활동을 감지하여 관리한다.

#### AWS Systems Manager

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/systemsManager.png){: .align-left-clf}

- 여러 AWS와 멀티클라우드 및 하이브리드 환경의 서비스의 운영 데이터를 중앙집중화하고 AWS 리소스 전체에서 작업을 자동화할 수 있다.
- 리소스 그룹을 선택하여 리소스 그룹의 최근 API 작업, 리소스 구성 변경, 관련 알림, 운영 경보, 소프트웨어 인벤토리, 패치 규정 준수 상태를 볼 수 있다.

#### AWS Trusted Advisor

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/trustedAdvisor.png){: .align-left-clf}

- AWS 모범 사례를 따르는 데 도움이 되는 권장 사항을 제공한다.
- AWS 인프라를 최적화하고 보안 및 성능을 개선하며 비용을 절감하고 서비스 할당량을 모니터링할 방법을 식별하여 사용자 권장 사항에 따라 서비스 및 리소스를 최적화할 수 있다.

<br/>🔻 Trusted Advisor의 검사는 AWS 환경을 분석하고 모범 사례를 따르기 위한 작업을 권장한다.
{:.red-font}

- 비용최적화
- 성능
- 보안
- 내결함성
- 서비스 할당량

#### AWS Secrets Manager

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/secretsManager.png){: .align-left-clf}

- 애플리케이션, 서비스 및 IT 리소스에 대한 액세스를 보호하는 데 도움이 되는 보안 정보 관리 서비스이다.
- 수명 주기 동안 데이터베이스 자격 증명, API 키 및 기타 보안 정보를 손쉽게 교체, 관리 및 검색할 수 있다.
- AWS 클라우드, 타사 서비스 및 온프레미스에 있는 리소스에 액세스하는 데 사용되는 **보안 정보를 보호하고 관리**할 수 있다.

#### Amazon EC2 Auto Scaling

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/autoScaling.png){: .align-left-clf}

- Amazon EC2 인스턴스를 자동으로 시작하거나 종료하여 애플리케이션 로드를 처리하기에 적절한 수의 Amazon EC2 인스턴스를 유지할 수 있도록 설계된 완전관리형 서비스이다.
- 비정상 인스턴스를 탐지하여 교체하는 EC2 인스턴스 플릿 관리를 통해 그리고 사용자가 정의하는 조건에 따라 Amazon EC2 용량을 자동으로 확장 또는 축소함으로써 애플리케이션 **가용성을 유지**할 수 있다.
- 수요가 급증할 경우 Amazon EC2 인스턴스의 수를 자동으로 늘려 성능을 그대로 유지하고, 수요가 적을 경우 자동으로 용량을 줄여 **비용을 절감**할 수 있다.

### 🔸 Compute

#### AWS Lambda

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/lambda.png){: .align-left-clf}

- 서버를 프로비저닝하거나 관리할 필요 없이 코드를 실행할 수 있다.
- 사용한 컴퓨팅 시간만큼만 비용을 지불하고, 코드가 실행되지 않을 때는 요금이 부과되지 않는다.
- 사실상 모든 유형의 애플리케이션이나 백엔드 서비스에 대한 코드를 별도의 관리 없이 실행할 수 있다.
- 코드를 업로드하기만 하면, Lambda에서 높은 가용성으로 코드를 실행 및 확장하는 데 필요한 모든 것을 처리한다.
- 코드를 자동으로 트리거하도록 설정하거나 웹 또는 모바일 앱에서 직접 코드를 호출할 수 있다.

#### AWS Elastic Beanstalk

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/elasticBeanstalk.png){: .align-left-clf}

- 개발자가 손쉽게 AWS 클라우드에서 애플리케이션을 신속하게 배포하고 관리할 수 있다.
- 개발자가 애플리케이션을 업로드하기만 하면 자동으로 용량 프로비저닝, 부하 분산, Auto-Scaling, 애플리케이션 상태 모니터링 등의 배포 세부 정보를 처리한다.

#### Amazon Lightsail

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/lightsail.png){: .align-left-clf}

- 개발자에게 클라우드에서 웹사이트와 웹 애플리케이션을 배포하고 관리할 수 있는 컴퓨팅, 스토리지 및 네트워킹 용량 및 기능을 제공한다.
- 가상 프라이빗 서버(VPS) 공급자로, 클라우드에서의 애플리케이션 구축 및 호스팅 솔루션이 필요한 개발자, 소규모 비즈니스, 학생 및 다른 사용자가 가장 손쉽게 AWS를 시작할 수 있는 방법이다.

  {% capture notice-2 %}

#### ✔ **가상 프라이빗 서버란?**

- ‘인스턴스’라고도 하는 가상 프라이빗 서버는 VPS 호스팅을 통해 고도의 보안과 가용성이 보장되는 환경에서 웹 사이트와 웹 애플리케이션을 경제적으로 실행할 수 있는 서버
  {% endcapture %}

<div class="notice">{{ notice-2 | markdownify }}</div>

- 프로젝트를 빠르게 시작하는 데 필요한 모든 것(가상 머신, 컨테이너, 데이터베이스, CDN, 로드 밸런서, DNS 관리 등)이 포함되어 있으며, 이러한 서비스를 저렴하고 예측 가능한 월간 요금으로 사용할 수 있다.

#### Amazon EC2

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/ec2.png){: .align-left-clf}

- 클라우드에서 컴퓨팅 파워의 규모를 자유자재로 변경할 수 있는 웹 서비스이다.
- 개발자가 보다 **쉽게 웹 규모의 컴퓨팅 작업을 수행**할 수 있도록 설계되었다.
- 클라우드에서 스토리지를 사용할 수 있는 것처럼 **클라우드에서 “컴퓨팅”을 수행**할 수 있다.
- 새로운 서버 인스턴스를 획득하고 부팅하는 데 필요한 시간을 단 몇 분으로 단축하므로 컴퓨팅 요구 사항의 변화에 따라 **신속하게 용량을 확장하거나 축소**할 수 있다.
- **실제 사용한 만큼**만 요금을 지불하면 되므로, 컴퓨팅 비용이 절약된다.

#### AWS Batch

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/batch.png){: .align-left-clf}

- 개발자, 과학자 및 엔지니어가 AWS에서 수많은 배치 컴퓨팅 작업을 효율적으로 손쉽게 실행할 수 있게 해주는 배치 관리 기능 세트이다.
- 제출된 배치 작업의 볼륨 및 특정 리소스 요구 사항에 따라 최적의 수량 및 컴퓨팅 리소스의 유형(ex: CPU 또는 메모리 최적화 컴퓨터 리소스)을 동적으로 프로비저닝한다.
- **추가 비용은 없고** 배치 작업을 저장하고 실행하기 위해 생성한 AWS 리소스(ex: EC2 인스턴스 또는 AWS Fargate)에 대한 비용만 지불하면 된다.
- 작업을 처리하는 시점을 더 큰 용량 또는 더 저렴한 용량을 사용할 수 있는 기간으로 옮길 수 있다.
- **작업의 우선순위를 지정**할 수 있으므로 비즈니스 목표에 맞춰 리소스를 사용할 수 있다.

### 🔸 Containers

#### Amazon ECS

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/ecs.png){: .align-left-clf}

- 컨테이너식 애플리케이션의 배포, 관리 및 크기 조정을 간소화하는 완전관리형 컨테이너 오케스트레이션 서비스이다.
- 유연한 컴퓨팅 옵션 전반에서 애플리케이션을 시작, 모니터링 및 확장하여 애플리케이션에 필요한 다른 지원 AWS 서비스와 자동으로 통합한다.
- 사용자 지정 크기 조정 및 용량 규칙 생성과 같은 시스템 작업을 수행하고 애플리케이션 로그 및 원격 분석의 데이터를 관찰하고 쿼리한다.
- 보안, 규정 준수 및 아키텍처는 규제 표준을 충족하므로 안심하고 구축할 수 있다.
- 컨테이너용 AWS Fargate 서버리스 컴퓨팅과 함께 사용하면 배포 속도를 높여 애플리케이션에 집중할 수 있다.
- Auto Scaling 및 사용량에 따른 요금을 사용할 수 있으므로 비용이 절감된다.

#### Amazon EKS

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/eks.png){: .align-left-clf}

- AWS 클라우드와 온프레미스 데이터 센터에서 Kubernetes를 실행하는 데 사용되는 관리형 Kubernetes 서비스이다.
- 클라우드에서 컨테이너 예약, 애플리케이션 가용성 관리, 클러스터 데이터 저장 및 다른 주요 태스크를 담당하는 Kubernetes 컨트롤 플레인의 가용성과 확장성을 관리한다.
- AWS 네트워킹 및 보안 서비스와의 통합뿐만 아니라 AWS 인프라의 모든 성능, 규모, 신뢰성 및 가용성을 활용할 수 있다.
- 온프레미스에서 완벽하게 지원되는 일관된 Kubernetes 솔루션을 제공한다.
- 통합된 도구를 사용하여 AWS Outposts, 가상 머신 또는 베어 메탈 서버에 간편하게 배포할 수 있다.

#### AWS Fargate

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/fargate.png){: .align-left-clf}

- 컨테이너에 적합한 서버리스 컴퓨팅 엔진으로, ECS 및 EKS와 연동된다.
- 서버를 프로비저닝하고 관리할 필요가 없기 때문에 애플리케이션별로 리소스를 지정하고 관련 비용을 지불할 수 있으며, 계획적으로 애플리케이션을 격리하여 보안을 개선할 수 있다.
- 사용자가 프로비저닝, 패치 적용, 클러스터 용량 관리 또는 인프라 관리가 필요 없다.
- 컨테이너식 애플리케이션에서 사용한 vCPU, 메모리, 스토리지 리소스의 양에 대한 비용만 지불한다.

### 🔸 애플리케이션 통합(Application Integration)

#### Amazon SNS

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/sns.png){: .align-left-clf}

- 클라우드에서 손쉽게 알림을 설정, 운영 및 전송할 수 있도록 하는 웹 서비스이다.
- 개발자에게 애플리케이션의 메시지를 게시하고 이를 구독자나 다른 애플리케이션에 즉시 전송할 수 있는 고도로 확장 가능하며 유연하고 비용 효율적인 기능을 제공한다.

#### Amazon SQS

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/sqs.png){: .align-left-clf}

- 자체 소프트웨어를 구축하여 메시지 대기열을 관리하거나 개발과 구성에 상당한 사전 시간 투자가 필요한 상용 또는 오픈 소스 메시지 대기열 시스템을 사용한다.
- 방대한 규모를 지원하므로 하루에 수십억 건의 메시지를 처리할 수 있다.
- 전송하는 트래픽 양을 확장하거나 축소할 수 있다.

{% capture notice-2 %}

#### ✔ **Amazon SNS는 Amazon SQS와 어떻게 다릅니까?**

- Amazon SNS를 사용하면 애플리케이션에서 정기적으로 업데이트를 확인하거나 '폴링'할 필요 없이 '푸시' 메커니즘을 통해 다수의 구독자에게 시간이 관건인 메시지를 보낼 수 있다.
- Amazon SQS는 분산 애플리케이션에서 폴링 모델을 통해 메시지를 교환하는 데 사용되는 메시지 대기열 서비스로 애플리케이션의 분산 구성 요소가 모든 구성 요소를 동시에 사용하지 않고도 메시지를 보내고 받을 수 있는 유연성을 제공한다.
- 송신 구성 요소와 수신 구성 요소를 분리할 수 있다.
{% endcapture %}
<div class="notice">{{ notice-2 | markdownify }}</div>

### 🔸 Contact Center

#### Amazon Connect

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/connect.png){: .align-left-clf}

- 옴니채널 클라우드 콜센터이다.
- 다른 AWS 서비스와 함께 사용하여 고객에게 혁신적이고 새로운 경험을 제공할 수 있다.

### 🔸 Networking & Content Delivery

#### Amazon Route 53

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/route53.png)
{: .align-left-clf}

- 가용성과 확장성이 우수한 도메인 이름 시스템(DNS), 도메인 이름 등록, 상태 확인 웹 서비스이다.
- 도메인 이름을 구매 및 관리하고 도메인에 대한 DNS 설정을 자동으로 구성할 수도 있다.<br/><br/>
  {% capture notice-2 %}

#### ✔ **DNS란?**

- www.example.com과 같이 사람이 읽을 수 있는 이름을 컴퓨터가 서로 연결하는 데 사용하는 192.0.2.1과 같은 숫자 IP 주소로 변환하는 글로벌 배포 서비스
- 이름과 숫자 간의 매핑을 관리하여 마치 전화번호부와 같은 기능을 한다.
  {% endcapture %}

<div class="notice">{{ notice-2 | markdownify }}</div>

#### Amazon VPC

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/vpc.png){: .align-left-clf}

- AWS 클라우드에서 논리적으로 격리된 공간을 프로비저닝하고, 정의한 가상 네트워크에서 AWS 리소스를 시작할 수 있다.
- 기업 데이터 센터와 VPC 사이에 하드웨어 가상 프라이빗 네트워크(VPN) 연결을 생성하여, 기업 데이터 센터의 확장으로서 AWS 클라우드를 사용할 수 있다.
- 네트워크 구성을 손쉽게 사용자 지정할 수 있다.

  {% capture notice-2 %}

#### ✔ **Amazon VPC의 구성 요소는?**

- Virtual Private Cloud
- 서브넷
- 인터넷 게이트웨이
- NAT 게이트웨이
- 가상 프라이빗 게이트웨이
- 피어링 연결
- VPC 엔드포인트
- 송신 전용 인터넷 게이트웨이
  {% endcapture %}

<div class="notice">{{ notice-2 | markdownify }}</div>

#### Amazon Direct Connect

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/directConnect.png){: .align-left-clf}

- 인터넷이 아닌 다른 방법으로 AWS에 연결할 수 있는 네트워킹 서비스이다.
- 인터넷을 통해 전송해야 했던 데이터를 이제는 고객 시설과 AWS 간의 프라이빗 네트워크 연결을 통해 전달할 수 있다.
- 많은 상황에서 프라이빗 네트워크 연결은 인터넷 기반 연결보다 비용이 적게 들고 대역폭이 늘어나며 좀 더 일관된 네트워크 경험을 제공할 수 있다.

#### Amazon CloudFront

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/cloudFront.png){: .align-left-clf}

- 비즈니스 및 웹 애플리케이션 개발자에게 짧은 지연 시간과 빠른 데이터 전송 속도를 사용하여 콘텐츠를 간편하고 비용 효율적으로 배포할 방법을 제공한다.
- 모든 AWS 인프라 서비스와 마찬가지로 Amazon CloudFront는 장기 약정 또는 최소 요금이 필요 없고 사용량에 따라 지불하는 셀프 서비스이다.
- AWS에서 실행되는 웹 애플리케이션을 DDoS 공격으로부터 보호하는 관리형 서비스 - AWS Shield

#### Amazon API Gateway

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/apiGateway.png){: .align-left-clf}

- 어떤 규모에서든 개발자가 API를 손쉽게 게시, 유지 관리, 모니터링 및 보호할 수 있도록 지원하는 완전관리형 서비스이다.
- 데이터, 비즈니스 로직 또는 기능에 액세스할 수 있도록 "현관문" 역할을 하는 API를 생성할 수 있다.
- 트래픽 관리, 권한 부여 및 액세스 제어, 모니터링, API 버전 관리를 비롯해 최대 수십만 건의 동시 API 호출을 수락 및 처리하는 데 관련된 모든 작업을 처리한다.
- 최소 요금이나 시작 비용이 없으므로 HTTP API와 REST API의 경우 수신한 API 호출과 전송한 데이터 양에 대해서 WebSocket API의 경우 전송하고 수신한 메시지와 사용자/디바이스가 WebSocket API에 연결한 시간에 대해서만 요금을 지불하면 된다.

#### Amazon Inspector

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/inspector.png){: .align-left-clf}

- Amazon Elastic Compute Cloud(EC2), AWS Lambda 함수 및 컨테이너 워크로드에서 소프트웨어 취약성과 의도하지 않은 네트워크 노출을 지속적으로 스캔하는 자동화된 취약성 관리 서비스이다.
- 실행 중인 Amazon EC2 인스턴스, Lambda 함수 및 Amazon ECR 리포지토리를 자동으로 검색하고 즉시 워크로드에서 소프트웨어 취약성과 의도하지 않은 네트워크 노출을 지속적으로 스캔하기 시작한다.

#### Amazon GuardDuty

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/guardDuty.png){: .align-left-clf}

- AWS 계정, Amazon EC2 인스턴스, AWS Lambda 함수, Amazon EKS 클러스터, Amazon Aurora 로그인 활동 및 Amazon S3에 저장된 데이터에서 악의적 활동을 지속적으로 모니터링하는 지능형 위협 탐지 서비스이다.
- 즉시 거의 실시간 및 대규모로 계정과 네트워크 활동의 연속 스트림을 분석하기 시작한다.

#### AWS Shield

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/shield.png){: .align-left-clf}

- AWS에서 실행되는 웹 애플리케이션을 DDoS(Distributed Denial of Service) 공격으로부터 보호하는 관리형 서비스이다.
- AWS Shield Standard는 추가 비용 없이 모든 AWS 고객에게 자동으로 활성화된다.

#### AWS WAF

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/waf.png){: .align-left-clf}

- 고객이 정의한 조건에 따라 웹 요청을 허용, 차단 또는 모니터링(계수)하는 규칙을 구성하여 공격으로부터 웹 애플리케이션을 보호하는 웹 애플리케이션 방화벽이다.
- AWS Shield Standard는 추가 비용 없이 모든 AWS 고객에게 자동으로 활성화된다.

### 🔸 그 외

#### 공동책임모델

![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/shared.png){: .align-left-clf}

- **AWS 책임 '클라우드의 보안'**
  - AWS는 AWS 클라우드에서 제공되는 모든 서비스를 실행하는 인프라를 보호할 책임이 있다.
  - 인프라는 AWS 클라우드 서비스를 실행하는 하드웨어, 소프트웨어, 네트워킹 및 시설로 구성된다.
- **고객 책임 '클라우드에서의 보안'**
  -
