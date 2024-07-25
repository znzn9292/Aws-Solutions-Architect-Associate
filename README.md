## AWS Instance Types

AWS(Amazon Web Services)는 다양한 용도와 성능 요구사항을 충족하기 위해 여러 종류의 인스턴스를 제공합니다.

### 1. 범용 인스턴스 (General Purpose Instances)
   - **T4g, T3, T3a, T2**: 버스트 가능한 성능을 제공하며, 비용 효율적입니다. 주로 소규모 웹 서버, 개발 환경, 테스트 서버 등에 사용됩니다.
   - **M6g, M6i, M5, M5a, M5n, M5zn, M4**: 균형 잡힌 컴퓨팅, 메모리, 네트워크 리소스를 제공합니다. 데이터베이스, 캐싱, 중간 규모의 데이터 프로세싱 작업 등에 적합합니다.

### 2. 컴퓨팅 최적화 인스턴스 (Compute Optimized Instances)
   - **C7g, C6g, C6gn, C6i, C6a, C5, C5a, C5n, C4**: 고성능 프로세서가 필요한 작업에 적합합니다. 고성능 웹 서버, 고성능 컴퓨팅(HPC), 배치 처리, 게임 서버 등에 사용됩니다.

### 3. 메모리 최적화 인스턴스 (Memory Optimized Instances)
   - **R6g, R6i, R5, R5a, R5n, R4**: 메모리 집약적인 애플리케이션에 적합합니다. 인메모리 데이터베이스, 빅데이터 분석, 고성능 NoSQL 데이터베이스 등에 사용됩니다.
   - **X2gd, X2idn, X1e, X1**: 대규모 메모리 용량을 필요로 하는 작업에 적합합니다. SAP HANA, Microsoft SQL Server, 고성능 컴퓨팅(HPC) 애플리케이션 등에 사용됩니다.
   - **z1d**: 높은 컴퓨팅 성능과 메모리 성능을 제공합니다. 전자 설계 자동화(EDA) 애플리케이션, 고성능 SQL 및 NoSQL 데이터베이스에 적합합니다.

### 4. 스토리지 최적화 인스턴스 (Storage Optimized Instances)
   - **I4i, I3, I3en**: 매우 높은 순차적 읽기/쓰기 성능과 낮은 레이턴시를 제공하며, I/O 집약적인 데이터베이스와 NoSQL 데이터베이스 등에 사용됩니다.
   - **D3, D2**: 대용량 스토리지를 필요로 하는 워크로드에 적합합니다. 하둡, 로그 및 데이터 웨어하우스에 사용됩니다.
   - **H1**: 고성능의 HDD 스토리지를 제공합니다. 데이터 웨어하우스, 로그 처리 및 빅데이터 애플리케이션에 적합합니다.

### 5. 가속화 컴퓨팅 인스턴스 (Accelerated Computing Instances)
   - **P4, P3, P2**: GPU를 활용한 머신 러닝 및 고성능 컴퓨팅에 적합합니다. 인공지능(AI), 딥 러닝, 과학적 계산에 사용됩니다.
   - **Inf1**: 인퍼런스 최적화된 인스턴스로, 머신 러닝 인퍼런스 워크로드에 적합합니다.
   - **G5, G4ad, G4dn, G3**: 그래픽 렌더링, 비디오 트랜스코딩, 게임 스트리밍, 머신 러닝 트레이닝 등에 사용됩니다.
   - **F1**: FPGA(Field Programmable Gate Array)를 사용하여 하드웨어 가속이 필요한 워크로드에 적합합니다. 사용자 지정 하드웨어 가속 애플리케이션에 사용됩니다.

이러한 다양한 인스턴스 유형은 AWS 사용자가 자신의 애플리케이션 요구사항에 맞는 최적의 리소스를 선택할 수 있도록 도와줍니다. 각 인스턴스는 특정한 워크로드와 성능 요구사항을 충족하도록 설계되어 있어, 비용 효율적이고 유연한 클라우드 컴퓨팅 환경을 제공합니다.

## EBS Volume Types

### 1. 범용 SSD (General Purpose SSD, gp2/gp3)
- **gp2**:
  - **특징**: 범용 SSD 볼륨으로 다양한 워크로드에 적합합니다.
  - **성능**: 기본적으로 3 IOPS/GB의 성능을 제공하며, 최대 16,000 IOPS까지 증가합니다.
  - **사용 사례**: 부트 볼륨, 중소 규모 데이터베이스, 개발 및 테스트 환경 등.

- **gp3**:
  - **특징**: gp2의 후속 모델로, 고정된 성능과 더 낮은 비용을 제공합니다.
  - **성능**: 기본 3,000 IOPS와 125MB/s의 처리량을 제공하며, 최대 16,000 IOPS와 1,000MB/s까지 설정할 수 있습니다.
  - **사용 사례**: gp2와 유사하지만 더 나은 비용 효율성을 제공합니다.

### 2. 프로비저닝된 IOPS SSD (Provisioned IOPS SSD, io1/io2)
- **io1**:
  - **특징**: 높은 IOPS가 필요한 워크로드를 위해 설계되었습니다.
  - **성능**: 50 IOPS/GB에서 최대 64,000 IOPS까지 설정할 수 있습니다.
  - **사용 사례**: 대규모 데이터베이스, 중요한 트랜잭션 시스템 등.

- **io2**:
  - **특징**: io1의 향상된 버전으로, 높은 내구성과 성능을 제공합니다.
  - **성능**: 최대 64,000 IOPS까지 설정할 수 있으며, 더 높은 내구성을 보장합니다.
  - **사용 사례**: io1과 유사하지만, 더 높은 내구성을 요구하는 미션 크리티컬 애플리케이션에 적합합니다.

### 3. 스루풋 최적화 HDD (Throughput Optimized HDD, st1)
- **특징**: 대용량 데이터 처리량을 필요로 하는 워크로드에 적합합니다.
- **성능**: 처리량은 500MB/s까지 지원하며, IOPS는 변동적입니다.
- **사용 사례**: 빅데이터, 데이터 웨어하우스, 로그 처리 등.

### 4. 콜드 HDD (Cold HDD, sc1)
- **특징**: 저렴한 비용으로 대용량 데이터를 저장하는 데 적합합니다.
- **성능**: 처리량은 250MB/s까지 지원하며, IOPS는 변동적입니다.
- **사용 사례**: 자주 접근하지 않는 데이터, 아카이빙, 백업 등.

### 5. 마그네틱 (Magnetic, standard) [이전 세대]
- **특징**: 비용 효율적인 마그네틱 스토리지로, 현재는 주로 레거시 워크로드에 사용됩니다.
- **성능**: 비교적 낮은 IOPS와 처리량을 제공합니다.
- **사용 사례**: 아카이빙, 저성능 워크로드 등.

### 선택 시 고려사항

1. **성능 요구 사항**:
   - 고성능이 필요한 경우 io1/io2 또는 gp3를 선택합니다.
   - 중간 성능을 원하는 경우 gp2 또는 gp3를 선택합니다.
   - 높은 처리량이 필요한 경우 st1을 선택합니다.
   - 낮은 비용으로 대용량 데이터를 저장하려면 sc1을 선택합니다.

2. **비용**:
   - 비용을 절감하려면 gp3 또는 sc1을 고려합니다.
   - 고성능이 필요하면 io1/io2를 고려하되, 비용이 높아질 수 있습니다.

3. **내구성 및 가용성**:
   - 미션 크리티컬 애플리케이션의 경우 높은 내구성을 제공하는 io2를 선택합니다.

## EBS 다중 연결

AWS EBS(Elastic Block Store)의 다중 연결 기능(Multi-Attach)은 EBS 볼륨을 여러 EC2 인스턴스에 동시에 연결할 수 있게 해주는 기능입니다. 이 기능을 통해 고가용성 및 고성능을 요구하는 애플리케이션에서 단일 EBS 볼륨을 여러 인스턴스가 동시에 읽고 쓸 수 있도록 합니다.

### 다중 연결 기능의 주요 특징

1. **지원되는 볼륨 타입**:
   - 현재 다중 연결 기능은 프로비저닝된 IOPS SSD(io1 및 io2) 볼륨에서만 지원됩니다.

2. **연결 가능 인스턴스 수**:
   - 하나의 EBS 볼륨을 최대 16개의 Nitro 기반 EC2 인스턴스에 동시에 연결할 수 있습니다.

3. **Nitro 기반 인스턴스 필요**:
   - 다중 연결 기능을 사용하려면 Nitro 시스템을 사용하는 인스턴스가 필요합니다.

4. **파일 시스템 및 데이터베이스 지원**:
   - 다중 연결 기능을 사용할 때는 클러스터형 파일 시스템 또는 클러스터형 데이터베이스와 같은 분산 잠금 및 동시성 제어 메커니즘이 필요한 시스템에서 사용하는 것이 좋습니다. 예를 들어, Amazon EFS(Elastic File System) 또는 클러스터형 데이터베이스를 사용하는 것이 일반적입니다.

### 다중 연결 사용 사례

1. **고가용성 클러스터**:
   - EBS 볼륨을 다중 연결하여 고가용성 클러스터 환경을 구축할 수 있습니다. 여러 인스턴스가 동일한 데이터를 공유하면서 읽고 쓸 수 있어, 한 인스턴스가 장애를 일으켜도 다른 인스턴스가 계속해서 작업을 수행할 수 있습니다.

2. **클러스터형 애플리케이션**:
   - 다중 연결 기능은 Oracle RAC(Real Application Clusters)와 같은 클러스터형 데이터베이스 시스템에서 유용합니다. 이러한 시스템은 여러 인스턴스에서 단일 데이터베이스를 공유하여 고가용성 및 확장성을 제공합니다.

3. **데이터 처리 및 분석**:
   - 데이터 처리 및 분석 작업에서 여러 인스턴스가 동일한 데이터셋에 동시에 접근해야 할 경우, 다중 연결 기능을 통해 성능을 향상시킬 수 있습니다.

### 설정 및 사용 방법

1. **EBS 볼륨 생성**:
   - io1 또는 io2 타입의 EBS 볼륨을 생성합니다.

2. **다중 연결 활성화**:
   - EBS 볼륨을 생성할 때 또는 이미 생성된 볼륨의 설정을 변경하여 다중 연결(Multi-Attach)을 활성화합니다.

   ```bash
   aws ec2 create-volume --volume-type io2 --size 100 --availability-zone us-west-2a --multi-attach-enabled
   ```

3. **EC2 인스턴스에 볼륨 연결**:
   - 생성된 볼륨을 여러 EC2 인스턴스에 동시에 연결합니다.

   ```bash
   aws ec2 attach-volume --volume-id vol-0123456789abcdef0 --instance-id i-0123456789abcdef0 --device /dev/sdf
   aws ec2 attach-volume --volume-id vol-0123456789abcdef0 --instance-id i-abcdef0123456789 --device /dev/sdf
   ```

4. **클러스터형 파일 시스템 구성**:
   - 여러 인스턴스에서 동시에 접근할 수 있는 파일 시스템 또는 데이터베이스를 구성합니다. 예를 들어, Amazon EFS 또는 클러스터형 데이터베이스를 사용하여 동시성 제어와 데이터 일관성을 유지합니다.

### 주의사항

- **동시성 제어**:
  - 여러 인스턴스가 동일한 볼륨에 접근할 때 발생할 수 있는 데이터 손상 또는 일관성 문제를 방지하기 위해, 적절한 동시성 제어 메커니즘을 사용해야 합니다.

- **Nitro 기반 인스턴스**:
  - 다중 연결 기능은 Nitro 기반 인스턴스에서만 지원되므로, 이러한 인스턴스를 사용해야 합니다.

- **비용**:
  - 다중 연결 기능을 사용하는 io1/io2 볼륨은 높은 성능을 제공하는 만큼, 비용도 더 높을 수 있습니다. 사용 사례에 따라 비용과 성능의 균형을 잘 맞추는 것이 중요합니다.

다중 연결 기능을 사용하면 AWS EBS의 유연성과 성능을 최대한 활용하여 고가용성과 고성능이 요구되는 애플리케이션을 구현할 수 있습니다. 적절한 설정과 동시성 제어를 통해 안정적으로 운영할 수 있도록 주의가 필요합니다.

AWS EBS 볼륨은 다양한 요구 사항을 충족할 수 있도록 여러 타입을 제공합니다. 각 볼륨 타입은 성능, 용량, 비용 측면에서 차별화되어 있으며, 애플리케이션의 특성과 요구 사항에 맞춰 적절한 볼륨 타입을 선택하는 것이 중요합니다.

## AWS EFS
AWS EFS(Amazon Elastic File System)는 AWS에서 제공하는 완전 관리형 파일 스토리지 서비스로, Amazon EC2 인스턴스와 온프레미스 리소스에서 사용할 수 있습니다. EFS는 표준 파일 시스템 인터페이스와 파일 시스템 액세스 시멘틱스를 제공하여, 사용자가 기존 애플리케이션을 수정하지 않고도 쉽게 통합할 수 있게 합니다.

### 주요 특징

1. **완전 관리형**:
   - AWS EFS는 서버, 스토리지 장치, 백업 등의 관리 작업을 자동으로 처리하여 사용자는 파일 시스템을 설정하고 사용하는 데 집중할 수 있습니다.

2. **확장성**:
   - 파일 시스템 용량이 자동으로 확장 및 축소됩니다. 필요한 경우 페타바이트 단위로 확장되며, 사용량에 따라 자동으로 조정됩니다.

3. **고가용성 및 내구성**:
   - EFS는 여러 가용 영역(AZ)에 걸쳐 데이터를 자동으로 복제하여 높은 가용성과 내구성을 제공합니다.

4. **고성능**:
   - EFS는 높은 처리량과 저지연 성능을 제공하며, 병렬 처리 및 대용량 데이터 처리가 요구되는 워크로드에 적합합니다.

5. **POSIX 호환**:
   - 표준 POSIX 파일 시스템 인터페이스를 제공하여, 기존 애플리케이션과 쉽게 통합할 수 있습니다.

6. **NFS 지원**:
   - NFS(Network File System) 프로토콜을 통해 파일 시스템에 접근할 수 있습니다.

### 사용 사례

1. **웹 서버 파일 스토리지**:
   - 여러 웹 서버 인스턴스에서 공유해야 하는 웹 콘텐츠, 미디어 파일, 애플리케이션 데이터를 저장합니다.

2. **빅데이터 및 분석**:
   - 대규모 데이터 세트에 대해 병렬로 작업하는 분석 및 빅데이터 처리 작업에 사용됩니다.

3. **백업 및 아카이빙**:
   - 중요한 데이터의 백업 및 장기 아카이빙을 위한 안정적인 스토리지로 사용됩니다.

4. **개발 및 테스트 환경**:
   - 여러 개발자가 동시에 접근하고 작업할 수 있는 공유 파일 시스템을 제공합니다.

5. **컨테이너 스토리지**:
   - 컨테이너 오케스트레이션 플랫폼(Kubernetes, ECS 등)에서 사용할 수 있는 공유 파일 스토리지로 사용됩니다.

### EFS 성능 모드

1. **범용 모드(General Purpose)**:
   - 대부분의 워크로드에 적합한 성능을 제공합니다. 저지연 액세스와 높은 처리량을 필요로 하는 애플리케이션에 이상적입니다.

2. **최대 I/O 모드(Max I/O)**:
   - 대규모 데이터 처리 및 병렬 작업을 위한 높은 처리량과 확장성을 제공합니다. 수천 개의 EC2 인스턴스가 동시에 액세스하는 경우에 적합합니다.

### EFS 스토리지 클래스

1. **표준 스토리지 클래스(Standard)**:
   - 자주 접근하는 데이터에 적합한 기본 스토리지 클래스입니다.

2. **인프리퀀트 액세스 스토리지 클래스(Infrequent Access, IA)**:
   - 자주 접근하지 않는 데이터에 적합한 저렴한 스토리지 클래스입니다. 데이터를 이동하여 비용을 절감할 수 있습니다.

### EFS 설정 방법

1. **파일 시스템 생성**:
   - AWS 관리 콘솔에서 "Create file system"을 클릭하여 파일 시스템을 생성합니다. 필요한 설정을 지정하고 생성합니다.

2. **보안 그룹 및 네트워크 설정**:
   - 파일 시스템에 접근할 수 있는 보안 그룹 및 네트워크 설정을 구성합니다.

3. **마운트 대상 생성**:
   - 파일 시스템을 사용할 각 가용 영역(AZ)에서 마운트 대상을 생성합니다. 마운트 대상은 NFS를 통해 EC2 인스턴스가 파일 시스템에 연결할 수 있게 합니다.

4. **EC2 인스턴스에 파일 시스템 마운트**:
   - EC2 인스턴스에서 NFS 클라이언트를 사용하여 파일 시스템을 마운트합니다.

   ```bash
   sudo mount -t nfs4 -o nfsvers=4.1 fs-12345678.efs.us-west-2.amazonaws.com:/ efs-mount-point
   ```

### 요약

AWS EFS는 완전 관리형, 확장성, 고가용성, 고성능을 제공하는 파일 스토리지 서비스로, 다양한 워크로드에서 쉽게 사용할 수 있습니다. POSIX 호환 인터페이스와 NFS 지원을 통해 기존 애플리케이션과 통합할 수 있으며, 다양한 성능 모드와 스토리지 클래스를 통해 비용 효율적인 스토리지 솔루션을 제공합니다.

AWS Certified Solutions Architect - Associate (SAA-C03) 시험에 나올 만한 Elastic Load Balancer (ELB) 및 Auto Scaling Group (ASG) 관련 주요 내용을 정리하면 다음과 같습니다.

## Elastic Load Balancing (ELB)

### 종류
1. **Application Load Balancer (ALB)**
   - **레벨**: 7계층 (애플리케이션 레벨)
   - **특징**: HTTP/HTTPS 트래픽을 처리하며, URL 기반 라우팅, 호스트 기반 라우팅, 경로 기반 라우팅을 지원.
   - **사용 사례**: 웹 애플리케이션, 마이크로서비스, HTTP/2 및 WebSocket 지원이 필요한 경우.

2. **Network Load Balancer (NLB)**
   - **레벨**: 4계층 (전송 레벨)
   - **특징**: TCP 및 UDP 트래픽을 처리하며, 초저지연과 고성능이 필요할 때 사용.
   - **사용 사례**: 고성능, 저지연이 필요한 애플리케이션, TCP/UDP 기반 서비스.

3. **Classic Load Balancer (CLB)**
   - **레벨**: 4계층 및 7계층 모두 지원
   - **특징**: 이전 세대의 로드 밸런서로, 기존 애플리케이션과의 호환성을 위해 사용.
   - **사용 사례**: 이미 사용 중인 CLB가 있는 경우, 새로 시작하는 프로젝트에는 권장되지 않음.

### 주요 기능
- **헬스 체크**: 인스턴스의 상태를 주기적으로 확인하여, 비정상 인스턴스를 자동으로 트래픽에서 제외.
- **세션 지속성 (Sticky Sessions)**: 동일한 클라이언트 요청을 동일한 백엔드 인스턴스로 라우팅.
- **SSL/TLS 종료**: 로드 밸런서에서 SSL/TLS 암호화를 종료하여 백엔드 인스턴스의 부담을 줄임.
- **보안 그룹 및 네트워크 ACL**: 로드 밸런서와 인스턴스 간의 트래픽 제어.
- **Auto Scaling 연동**: ELB는 Auto Scaling과 연동되어 인스턴스 수의 동적 조정 지원.

AWS Certified Solutions Architect - Associate (SAA-C03) 시험에 나올 만한 Sticky Sessions에 대한 중요한 내용을 정리하면 다음과 같습니다:

## Sticky Sessions
Sticky Sessions (세션 지속성)은 클라이언트의 요청이 처음 연결된 동일한 백엔드 서버로 지속적으로 라우팅되도록 하는 로드 밸런싱 기능입니다. 이를 통해 상태 정보가 서버에 저장되는 상태 저장 애플리케이션에서 일관된 사용자 경험을 제공할 수 있습니다.

### 작동 방식
Sticky Sessions은 로드 밸런서가 클라이언트의 세션 식별자를 기반으로 트래픽을 특정 백엔드 서버에 지속적으로 라우팅하는 방식으로 작동합니다. AWS Elastic Load Balancing (ELB)에서는 이를 세션 지속성 또는 세션 어피니티라고도 합니다.

### AWS ELB에서의 Sticky Sessions

#### Application Load Balancer (ALB)
- **세션 지속성 쿠키**: ALB는 클라이언트와 서버 간의 세션을 지속하기 위해 `AWSALB`라는 이름의 쿠키를 사용합니다.
- **쿠키 설정**: ALB에서는 세션 지속성을 설정할 때 세션 지속성 쿠키의 유효 기간을 설정할 수 있습니다.
- **동작**: 클라이언트가 ALB에 연결될 때, ALB는 백엔드 서버에 연결하고 쿠키를 클라이언트에게 전송합니다. 이후 클라이언트의 모든 요청은 동일한 백엔드 서버로 라우팅됩니다.

#### Classic Load Balancer (CLB)
- **생성된 쿠키**: CLB는 `AWSELB`라는 이름의 쿠키를 생성하여 세션 지속성을 관리합니다.
- **내부 및 외부 쿠키**: CLB는 자체적으로 쿠키를 생성하거나 애플리케이션이 설정한 쿠키를 사용할 수 있습니다.
- **동작**: 클라이언트의 첫 요청에 대해 CLB는 쿠키를 생성하고 클라이언트에게 전송합니다. 이후 클라이언트의 모든 요청은 동일한 백엔드 인스턴스로 라우팅됩니다.

### 사용 사례
- **상태 저장 애플리케이션**: 로그인 세션, 장바구니 정보 등 사용자 세션 데이터를 서버에 저장하는 애플리케이션에 적합합니다.
- **세션 데이터 일관성**: 특정 사용자의 모든 요청이 동일한 서버로 라우팅됨으로써 세션 데이터의 일관성을 유지합니다.

### 설정 방법

#### Application Load Balancer (ALB)
1. **로드 밸런서 설정에서 대상 그룹 선택**.
2. **세션 지속성 활성화**: 대상 그룹 속성에서 `Enable session stickiness` 옵션을 선택합니다.
3. **쿠키 설정**: 세션 지속성 쿠키의 유효 기간을 설정합니다 (예: 60초).

#### Classic Load Balancer (CLB)
1. **로드 밸런서 설정에서 로드 밸런서 선택**.
2. **세션 지속성 구성**: `Policies` 탭에서 `Enable load balancer generated cookie stickiness`를 선택합니다.
3. **쿠키 만료 시간 설정**: 필요에 따라 쿠키의 만료 시간을 설정합니다.

### 시험 대비 주요 포인트

- **세션 지속성의 정의와 필요성**: 클라이언트 요청을 동일한 백엔드 서버로 라우팅하여 상태 저장 애플리케이션에서 일관된 사용자 경험을 제공하는 이유를 이해.
- **ALB와 CLB의 세션 지속성 차이점**: 두 로드 밸런서 유형에서 세션 지속성을 설정하고 관리하는 방법의 차이점.
- **설정 및 구성 방법**: AWS 콘솔에서 ALB와 CLB의 세션 지속성을 활성화하고 설정하는 방법.
- **사용 사례**: 세션 지속성이 필요한 시나리오 및 이를 활용하여 애플리케이션의 일관성을 유지하는 방법.

## Auto Scaling Group (ASG)

### 주요 개념
- **Auto Scaling Group**: 특정 수의 인스턴스를 자동으로 관리하고 유지하는 그룹. 인스턴스 수를 조정하여 애플리케이션의 가용성과 확장성을 보장.
- **Launch Configuration / Launch Template**: ASG가 새 인스턴스를 시작할 때 사용할 설정을 정의. 인스턴스 유형, AMI, 키 페어, 보안 그룹 등을 포함.
- **Desired Capacity**: ASG가 유지하려고 하는 인스턴스의 목표 수.
- **Minimum / Maximum Capacity**: ASG가 유지할 수 있는 인스턴스의 최소 및 최대 수.
- **Scaling Policies**: 특정 조건에서 ASG가 인스턴스를 추가하거나 제거하도록 지시하는 규칙.

### 주요 기능
- **헬스 체크 통합**: ELB 및 EC2 상태 체크를 기반으로 인스턴스 상태를 확인하고 비정상 인스턴스를 교체.
- **다양한 조정 옵션**:
  - **동적 조정**: CloudWatch 알람을 기반으로 인스턴스 수를 동적으로 조정.
  - **예측 조정**: 과거 데이터와 예측 알고리즘을 사용하여 인스턴스 수를 자동으로 조정.
  - **스케줄 기반 조정**: 특정 시간에 인스턴스 수를 조정하도록 스케줄 설정.
- **EC2 스팟 인스턴스 지원**: 비용 최적화를 위해 스팟 인스턴스를 사용하여 ASG 구성 가능.
- **다중 가용 영역 지원**: 가용성을 높이기 위해 여러 가용 영역에 인스턴스를 분산 배치.

### 사용 사례
- **웹 애플리케이션**: 트래픽 패턴에 따라 인스턴스 수를 자동으로 조정하여 가용성과 비용 효율성을 최적화.
- **빅 데이터 처리**: 데이터 처리 작업이 증가하거나 감소할 때 자동으로 인스턴스 수를 조정.
- **백엔드 서비스**: 트래픽 변화에 따라 서버 수를 자동으로 조정하여 백엔드 서비스의 성능 보장.

### 시험 대비 주요 포인트

- **ELB 유형 및 사용 사례**: ALB, NLB, CLB의 차이점과 각각의 사용 사례 이해.
- **헬스 체크 설정**: ELB와 ASG의 헬스 체크 설정 및 관리 방법.
- **Auto Scaling Policies**: 동적 조정, 예측 조정, 스케줄 기반 조정의 차이점과 사용 방법.
- **Launch Configuration / Launch Template**: 차이점과 설정 방법.
- **다중 가용 영역 배포**: ASG와 ELB를 사용하여 고가용성 애플리케이션을 배포하는 방법.

## ASG 조정 정책

### 1. 동적 조정 (Dynamic Scaling)

동적 조정 정책은 실시간 모니터링된 지표에 따라 자동으로 인스턴스 수를 조정합니다. 이 조정은 크게 두 가지 방식으로 이루어집니다.

#### 대상 추적 조정 (Target Tracking Scaling)
- **개념**: 목표 지표 (예: CPU 사용률)를 설정하고 ASG가 이를 유지하도록 인스턴스 수를 자동으로 조정합니다.
- **예시**: 목표 CPU 사용률을 50%로 설정하면, ASG는 CPU 사용률이 50%에 가까워지도록 인스턴스를 추가하거나 제거합니다.
- **사용 사례**: 특정 지표를 일정 수준으로 유지하고자 할 때.

#### 단계 조정 (Step Scaling)
- **개념**: 지표가 특정 임계값을 초과할 때 또는 미만일 때 인스턴스를 단계적으로 추가하거나 제거합니다.
- **예시**: CPU 사용률이 70%를 초과하면 인스턴스를 2개 추가하고, 30% 미만으로 떨어지면 1개 제거합니다.
- **사용 사례**: 지표 변동 폭에 따라 점진적으로 조정이 필요할 때.

#### 간단 조정 (Simple Scaling)
- **개념**: 특정 조건이 충족되면 지정된 수의 인스턴스를 추가하거나 제거합니다.
- **예시**: CPU 사용률이 80%를 초과하면 인스턴스를 1개 추가합니다.
- **사용 사례**: 간단한 조정 정책이 필요할 때, 단일 이벤트 기반 조정.

### 2. 예측 조정 (Predictive Scaling)

예측 조정 정책은 과거 트래픽 패턴을 분석하여 미래의 트래픽을 예측하고, 이에 따라 사전에 인스턴스를 추가하거나 제거합니다.
- **개념**: 과거 데이터를 바탕으로 향후 트래픽 변동을 예측하여 미리 준비합니다.
- **예시**: 매일 오전 9시에서 11시 사이 트래픽이 급증한다면, 이 시간에 맞춰 인스턴스를 사전에 추가합니다.
- **사용 사례**: 일정한 트래픽 패턴이 있는 애플리케이션, 예측 가능한 트래픽 증가가 있는 경우.

### 3. 스케줄 기반 조정 (Scheduled Scaling)

스케줄 기반 조정은 특정 시간에 인스턴스 수를 조정하는 방법입니다.
- **개념**: 미리 정의된 시간표에 따라 인스턴스를 조정합니다.
- **예시**: 매일 오후 6시에 인스턴스를 5개로 설정하고, 오전 8시에 다시 3개로 줄입니다.
- **사용 사례**: 정해진 시간에 트래픽이 변동하는 경우, 예: 업무 시간 동안의 트래픽 증가.

### 조정 정책 구성 요소

#### 조정 정책 설정 시 고려할 요소
- **CloudWatch 알람**: 지표를 모니터링하고 조건을 설정하여 트리거 이벤트를 정의합니다.
- **Cool Down Period**: 인스턴스가 추가되거나 제거된 후 일정 기간 동안 추가 조정이 발생하지 않도록 하는 시간.
- **지표 선택**: CPU 사용률, 네트워크 트래픽, 메모리 사용량 등 다양한 지표를 기준으로 설정 가능.

#### 조정 정책 적용
- **ASG 콘솔**: AWS 관리 콘솔에서 조정 정책을 설정하고 관리.
- **CLI 및 SDK**: AWS CLI 또는 SDK를 통해 프로그래밍 방식으로 조정 정책 설정.

### 시험 대비 주요 포인트
- **조정 정책 유형 이해**: 동적 조정, 예측 조정, 스케줄 기반 조정의 차이점과 사용 사례.
- **대상 추적 조정**: 목표 지표 설정과 자동 조정 원리.
- **단계 조정 및 간단 조정**: 임계값 기반 조정과 단계적 조정의 차이점.
- **예측 조정**: 과거 트래픽 패턴 분석 및 예측 조정의 장점.
- **스케줄 기반 조정**: 특정 시간에 인스턴스를 조정하는 방법과 사용 사례.
- **CloudWatch 연동**: 지표 모니터링 및 알람 설정을 통한 자동 조정 트리거.

## Aurora RDS
Aurora는 Amazon의 고성능 관계형 데이터베이스 서비스로, MySQL 및 PostgreSQL 호환성, 고가용성, 자동 복구, 확장성 등 여러 가지 강력한 기능을 제공합니다.

### 1. **Aurora 개요**
- **고성능 및 고가용성**: Aurora는 MySQL 및 PostgreSQL 호환 데이터베이스로, 상용 데이터베이스 성능을 제공하며, 내구성과 가용성을 위해 설계됨.
- **자동 복구**: 데이터는 여러 가용 영역(AZ)에 자동으로 복제되며, 특정 AZ의 장애 시 자동으로 다른 AZ로 장애 조치됨.
- **비용 효율성**: 상용 데이터베이스의 1/10 비용으로 고성능 데이터베이스 제공.

### 2. **아키텍처**
- **분산된 스토리지 시스템**: Aurora는 최대 64TB의 분산된 스토리지를 사용하여 자동으로 확장 가능. 데이터는 6개의 복사본이 3개의 가용 영역에 분산 저장됨.
- **Compute와 Storage의 분리**: 컴퓨팅 인스턴스와 스토리지 레이어가 분리되어 있어, 독립적으로 확장 가능.

### 3. **호환성**
- **MySQL 호환**: Aurora MySQL은 MySQL 5.6, 5.7, 8.0 버전과 호환.
- **PostgreSQL 호환**: Aurora PostgreSQL은 PostgreSQL 9.6, 10, 11, 12, 13 버전과 호환.

### 4. **자동화 및 관리**
- **자동 백업**: Aurora는 지속적인 백업을 Amazon S3에 자동으로 수행.
- **스냅샷**: 수동으로 데이터베이스 스냅샷을 생성 가능.
- **자동 패치**: Aurora는 데이터베이스 인스턴스에 대한 소프트웨어 패치를 자동으로 적용 가능.

### 5. **고가용성 및 복구**
- **리전간 복제**: Aurora Global Database를 사용하면, 여러 AWS 리전에 데이터베이스를 복제하여 지연 시간이 짧고 재해 복구가 가능.
- **Aurora Multi-AZ 배포**: 고가용성 배포를 위해 읽기 전용 복제본을 다른 AZ에 생성 가능.

### 6. **성능**
- **저지연 읽기**: 최대 15개의 읽기 전용 복제본을 추가하여 읽기 성능을 확장 가능.
- **비동기 복제**: Aurora는 비동기 복제를 사용하여 낮은 지연 시간과 높은 쓰기 성능을 제공.

### 7. **보안**
- **암호화**: 저장된 데이터와 전송 중인 데이터를 암호화 가능. AWS KMS(Key Management Service)를 사용하여 암호화 키 관리.
- **네트워크 격리**: Amazon VPC를 사용하여 데이터베이스 인스턴스를 네트워크로 격리 가능.
- **IAM 통합**: AWS Identity and Access Management(IAM)와 통합하여 데이터베이스 접근 권한을 세밀하게 제어 가능.

### 8. **모니터링 및 로깅**
- **Amazon CloudWatch**: 성능 메트릭을 모니터링하고 경고를 설정 가능.
- **Enhanced Monitoring**: 운영 체제 수준에서 메트릭 수집.
- **Performance Insights**: 데이터베이스 성능을 모니터링하고 문제를 분석하는 데 유용한 도구.

### 9. **Aurora Serverless**
- **자동 확장**: 애플리케이션의 수요에 따라 자동으로 데이터베이스 용량을 조정.
- **비용 효율성**: 사용한 만큼만 비용을 지불.

## AWS RDS 백업

### 1. **자동 백업 (Automated Backups)**
- **자동화된 일일 백업**: RDS는 지정된 백업 보존 기간 동안 매일 자동으로 데이터베이스를 백업.
- **백업 보존 기간**: 기본값은 7일이며 최대 35일까지 설정 가능.
- **자동 백업의 저장 위치**: 백업은 S3에 저장되며, 데이터베이스 인스턴스에 영향을 주지 않도록 설계됨.
- **포인트 인 타임 복구 (PITR)**: 백업 보존 기간 동안 특정 시점으로 데이터베이스를 복구할 수 있음.
- **백업 기간**: 백업 기간은 유지보수 창과 별도로 설정할 수 있음.

### 2. **DB 스냅샷 (DB Snapshots)**
- **수동 스냅샷**: 사용자가 원할 때 언제든지 데이터베이스 인스턴스의 스냅샷을 수동으로 생성 가능.
- **백업 보존**: 수동 스냅샷은 자동으로 삭제되지 않으며, 사용자가 명시적으로 삭제해야 함.
- **복원**: 스냅샷을 사용하여 새로운 데이터베이스 인스턴스를 생성할 수 있음.
- **저장 위치**: 스냅샷 역시 S3에 저장됨.
- **크로스 리전 스냅샷**: 스냅샷을 다른 리전으로 복사하여 재해 복구 용도로 사용 가능.

### 3. **백업 전략**
- **백업 주기 및 보존 정책**: 비즈니스 요구사항에 맞게 백업 주기와 보존 기간을 설정.
- **자동 백업 및 수동 스냅샷 병용**: 자동 백업으로 일상적인 데이터 보호를 하면서, 주요 변경 사항 이전에 수동 스냅샷을 생성하여 추가적인 보안을 확보.
- **테스트 복구**: 정기적으로 복구 절차를 테스트하여 백업의 유효성과 복구 시간을 확인.

### 4. **백업 비용**
- **자동 백업**: 백업 스토리지 비용은 데이터베이스 스토리지 용량의 100%까지 무료. 이를 초과하는 부분에 대해서는 추가 비용 발생.
- **수동 스냅샷**: 스냅샷에 저장된 데이터 용량에 따라 비용이 발생.

### 5. **백업 설정**
- **콘솔 설정**: AWS Management Console을 통해 간편하게 백업 보존 기간 및 스냅샷 생성 가능.
- **CLI 및 API**: AWS CLI 또는 API를 사용하여 자동화된 백업 설정 및 스냅샷 관리 가능.

### 백업 복구 주요 포인트

#### 1. **포인트 인 타임 복구 (PITR)**
- **포인트 인 타임 복구**: 백업 보존 기간 내의 특정 시점으로 데이터베이스를 복구 가능.
- **복구 절차**: 새로운 데이터베이스 인스턴스를 생성하면서 해당 시점의 데이터를 복원.

#### 2. **스냅샷 복구**
- **DB 인스턴스 생성**: 기존 스냅샷에서 새로운 DB 인스턴스를 생성하여 복구.
- **크로스 리전 복구**: 다른 리전으로 복사된 스냅샷을 사용하여 재해 복구.

#### 백업 및 복구 시 고려사항
- **데이터베이스 크기**: 대규모 데이터베이스의 경우 백업과 복구 시간이 길어질 수 있음.
- **백업 주기**: 변경이 빈번한 데이터베이스는 짧은 백업 주기를 설정하여 데이터 손실을 최소화.
- **복구 시간 목표 (RTO)**: 복구 시간이 비즈니스 요구사항을 충족하는지 확인.
- **데이터 손실 목표 (RPO)**: 백업 주기가 데이터 손실 허용 범위 내에 있는지 확인.

AWS Certified Solutions Architect - Associate (SAA-C03) 시험을 준비하면서 Amazon S3와 보안 관련 주요 내용을 정리해보겠습니다.

## Amazon S3 (Simple Storage Service)

#### 기본 개념
- **객체 스토리지**: 파일을 객체로 저장하는 스토리지 서비스
- **버킷**: 객체를 저장하는 컨테이너. 버킷 이름은 전 세계에서 유일해야 함
- **객체**: 파일과 메타데이터의 조합. 객체에는 키(파일명), 데이터, 메타데이터가 포함됨
- **S3 URI**: s3://bucket-name/key

#### 스토리지 클래스
- **S3 Standard**: 자주 액세스되는 데이터를 위한 높은 내구성과 가용성을 제공
- **S3 Intelligent-Tiering**: 데이터 액세스 패턴에 따라 자동으로 비용을 최적화
- **S3 Standard-IA**: 적게 액세스되는 데이터를 위한 비용 효율적인 스토리지
- **S3 One Zone-IA**: 한 개의 가용 영역에 저장되는 적게 액세스되는 데이터
- **S3 Glacier**: 아카이빙을 위한 저비용 스토리지
- **S3 Glacier Deep Archive**: 장기 보관용 아카이브 스토리지, 가장 저렴한 옵션

#### 버킷 설정 및 관리
- **버킷 정책**: 버킷 수준에서 액세스를 제어하는 JSON 기반의 정책
- **ACL(Access Control List)**: 객체 수준에서 액세스를 제어
- **버전 관리**: 객체의 이전 버전을 보관하여 데이터 보호
- **수명 주기 정책**: 객체의 수명 주기를 자동으로 관리하여 비용 최적화
- **S3 이벤트 알림**: 특정 이벤트(예: 객체 생성, 삭제) 발생 시 알림을 설정

#### 보안
- **IAM(Identity and Access Management)**: 사용자와 리소스에 대한 액세스 제어
- **S3 버킷 정책**: 버킷과 그 안의 객체에 대한 액세스를 제어
- **S3 암호화**: 데이터를 보호하기 위해 전송 중(TLS/SSL) 및 저장 중(SSE-S3, SSE-KMS, SSE-C) 암호화
  - **SSE-S3**: Amazon S3 관리형 키를 사용하는 서버 측 암호화
  - **SSE-KMS**: AWS Key Management Service (KMS) 관리형 키를 사용하는 서버 측 암호화
  - **SSE-C**: 고객 제공 키를 사용하는 서버 측 암호화
  - **고객 측 암호화**: 데이터를 업로드하기 전에 암호화
- **VPC 엔드포인트**: 프라이빗 네트워크에서 S3에 안전하게 액세스
- **MFA Delete**: 다단계 인증을 통한 삭제 방지
- **S3 Block Public Access**: 퍼블릭 액세스를 차단하는 설정

#### 성능 및 최적화
- **멀티파트 업로드**: 큰 파일을 여러 파트로 나누어 병렬로 업로드
- **Transfer Acceleration**: 전 세계적으로 빠른 업로드를 위한 CloudFront 엣지 로케이션 사용
- **Cross-Region Replication (CRR)**: 객체를 다른 리전으로 복제하여 데이터 내구성 및 접근성 향상
- **S3 Select**: S3 객체에서 필요한 데이터만 필터링하여 검색

### 보안

#### IAM(Identity and Access Management)
- **사용자와 그룹**: IAM 사용자와 그룹을 통해 AWS 리소스에 대한 액세스를 제어
- **역할(Role)**: 다른 AWS 서비스나 사용자가 특정 권한을 가지도록 역할을 부여
- **정책(Policy)**: JSON 문서로 액세스 권한을 정의

#### 네트워크 보안
- **VPC (Virtual Private Cloud)**: 가상 네트워크를 통해 AWS 리소스를 보호
- **보안 그룹**: 인스턴스 수준에서 인바운드/아웃바운드 트래픽 제어
- **네트워크 ACL**: 서브넷 수준에서 트래픽 제어
- **VPN 및 Direct Connect**: 온프레미스 네트워크와 AWS 간의 안전한 연결

#### 데이터 보호
- **암호화**: 데이터의 기밀성을 보장
  - **KMS**: 키를 생성하고 관리
  - **Certificate Manager**: SSL/TLS 인증서를 관리
- **백업 및 복구**: 데이터 손실을 방지하기 위한 백업 전략
- **CloudTrail**: API 호출을 로깅하여 모니터링 및 감사

#### 모니터링 및 로깅
- **CloudWatch**: 로그, 메트릭, 이벤트를 모니터링하여 리소스의 상태를 추적
- **AWS Config**: 리소스 설정을 추적하고 규정 준수 여부를 평가
- **CloudTrail**: API 활동을 로깅하여 보안 분석 및 규정 준수

이러한 내용을 바탕으로 SAA-C03 시험 준비에 필요한 S3와 보안의 주요 내용을 이해하고 정리할 수 있습니다. 추가적인 심화 학습이 필요하면 AWS 공식 문서와 강의를 참고하세요.
