### Cloudera Data Hadoop (CDh) Quick install

```bash
wget http://archive.cloudera.com/cm5/installer/latest/cloudera-manager-installer.bin
chmod 755 cloudera-manager-installer.bin
./cloudera-manager-installer.bin
```

ip_address:7180
default : admin / admin


 Clusterd 구성을 위해 3개의 instance 를 더 띄운다.


### Cloudera Install Phases and Paths
1. Install Jdk
2. Set up Database
3. Install Cloudera Manager Server
4. Install Cloudera Manager Agent
5. Install Cloudera Data Hadoop And Manager Service software
6. Create, Configure and Start Coludera Data Hodoop and Managed Service

#### Coludera Manager Introdcution And Overview
Three-Components
- Management Service
    monitoring / alerting / reporting
- Cloudera Manager Database
- Cloudera Repository and Clients

Agent 는 모든 node 에 설치 됨
 - install trigger 
 - node monitoring 
 - start / stop processes
 - 15 초 마다 heartbeat 전송 (default) 
 - right install / user setup configuration 모두 agent 로 통해 수행된다.


 ### Cloudera Parcels
Coludera Manager 는 두개의 Software 배포 Format 이 있다.
- Parcels
    Cloudera 에 매우 구체적이다.
    Parcles 은 독립적인 install Direcotry 를 가져   다양한 version 을 설치할 수 있다.
    sudo permission 없이 설치 할수 있다.
    automatically downloads / distrubtutions / activate
    os 에 맞게 설치해준다. (찾을 필요가 없다.)
- Packagse