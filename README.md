# ODWS-S02-Data-Replication
Oracle Data Platform 워크샵에서 OCI-GoldenGate(줄여서 OCI-GG)를 이용한 데이터 복제 파트 입니다.


## 사전 준비 사항
- ODWS-S01-Data-Pipeline 실습을 완료하며 생성된 ADW가 있어야 합니다. (만약, S01 시나리오 없이 진행한다면 OCI 내에서 빈 상태의 ADW DB 하나를 생성해두면 됩니다.)
  

## 실습 아키텍처
- ATP 데이터베이스를 소스로 하며, ADW, MySQL 및 OCI Streaming을 타겟으로 구성하여 다양한 데이터 통합을 실습해 보겠습니다. (OCI-GG에서는 다양한 이기종 데이터 통합을 지원합니다. 지원하는 다양한 데이터 소스/타겟의 최신 정보는 다음 URL: https://docs.oracle.com/en/cloud/paas/goldengate-service/wxntz/index.html 에서 확인 가능합니다.)
  
- OCI-GG 서비스는 같은 타입의 데이터베이스는 1개의 OCI-GG Deployment 내에서 구성할 수 있고, 이기종 데이터 간의 통합을 할 때에는 각각의 OCI-GG Deployment를 구성해야 합니다.
  
- 따라서 이번 실습에서는 아래의 그림과 같이 총 3개의 OCI-GG Deployment를 생성하여 각각의 데이터 통합을 수행해 보도록 하겠습니다.

<p align="center"><img src="https://github.com/oraclekr-data-platform/ODWS-S02-Data-Replication/blob/main/assets/283835612-d116bbf0-269a-4861-b696-59f7da012dbf.png" width="250px" height="250px"></p>



