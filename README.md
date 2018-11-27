# Hadoop ecosystem 간략한 소개

1. Hadoop framework
많은 분산 시스템은 master worker architecutre 를 가지고 있다. Hadoop 역시 그렇다.
    
2. Hadoop 은 두개의 major components 가 존재한다. 
    1. HDFS (Hadoop Distrubuited File System)
        - HDFS 는 거대한 storage 로, Data 에 HA(high availabilty) 와 HS(High scalability) 를 제공합니다
        - 무수히 많은 worker machine을 HDFS 에 추가 할 수 있습니다. (HS)
        - namenode : HDFS master daemon
            meta information (file 이 나눠진 정보 및 어느 datanode 에 있는지 ) 을 저장하고 있다. 이 정보는 memory 에 저장된다 .
        - datanode : worker process 
            will have huge amount of storage capacity 
        - datanode 는 3초마다 namenode 에 reporting 을 보낸다. 
        - HDFS 추가되는 파일은 block criteria 또는 block size 로 조각된다. (default .128MB)
        - namenode 에서 파일 정보를 먼저 확인하여 datanode 에서 IO 를 발생시켜 파일을 읽는다.
        - namenode 가 master 이기 때문에 이곳만 관리하면 되어서 HS 하기가 편하다.
    2. YARN (Yet Another Resource Negotiator)
    HDFS 가 HA 를 구성하기 위해서 3개의 복제본을 생성할 수 있고 이것을 Reflication factor 라고 부릅니다. 이것을 증가 / 감소 될 수 있으며 프로세스 수행을 YARN 과 같이 합니다.

3. federation 
    - Namdnode 의 HA 구성 
    - hot backup
    - namenode parallel to each other,

### 용어정리
- Master worker architecutre
지속적인 실행 가능 한 시스템으로 n 개의 worker machine 과 하나의 master machine 으로 이루어져 있다. 각각의 worker machine 정상 동작함을 지속적으로 master machine 에게  heartbeat singal 또는 report 를 보낸다.
- Replication factor
HA 구성을 하는 핵심
