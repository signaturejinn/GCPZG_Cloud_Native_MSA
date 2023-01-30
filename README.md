# Cloud Native 기반 MSA 웹 서비스 구축
### - MSA 웹 서비스
### - IaC 인프라
### - Container 기반 인프라
### - 실시간 모니터링

</br>

## 🗓️ 진행 기간
- 2022.11.14 ~ 2022.12.14

</br>

## 👥 팀 구성
- Infra 구축 5명

</br>

## ⚙️ 사용 기술
#### CSP
<img src="https://img.shields.io/badge/Google GCP-4285F4?style=for-the-badge&logo=Google Cloud&logoColor=white"> <!--gcp-->

#### OS
<img src="https://img.shields.io/badge/Google Container-Optimzed OS-4285F4?style=for-the-badge&logo=Google Cloud&logoColor=white"> <!--gcp-->

#### DB
<img src="https://img.shields.io/badge/mysql 5.7-4479A1?style=for-the-badge&logo=mysql&logoColor=white">  <!--mysql-->

### Container
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=Docker&logoColor=white">  <!--Docker-->

### Orchestration
<img src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=Kubernetes&logoColor=white">  <!--k8s-->
<img src="https://img.shields.io/badge/GCP GKE-4285F4?style=for-the-badge&logo=Google Cloud&logoColor=white"> <!--gcp gke-->

Google Sheets
<img src="https://img.shields.io/badge/Google Sheets-34A853?style=for-the-badge&logo=Google Sheets&logoColor=white"> <!--gcp-->
<img src="https://img.shields.io/badge/Looker Studio-276DC3?style=for-the-badge&logo=Looker&logoColor=white"> <!--Looker-->

CI/CD
<img src="https://img.shields.io/badge/Jenkins-D24939?style=for-the-badge&logo=Jenkins&logoColor=white">  <!--jenkins-->
<img src="https://img.shields.io/badge/ArgoCD-EF7B4D?style=for-the-badge&logo=Argo&logoColor=white">  <!--argocd-->
<img src="https://img.shields.io/badge/GCP Cloud Build-4285F4?style=for-the-badge&logo=Google Cloud&logoColor=white"> <!--gcp-->
<img src="https://img.shields.io/badge/Terraform Cloud-7B42BC?style=for-the-badge&logo=Terraform&logoColor=white">  <!--terraform cloud-->

### Framework
<img src="https://img.shields.io/badge/Spring-6DB33F?style=for-the-badge&logo=Spring&logoColor=white">  <!--spring-->

#### Team Collabolation Tool
<img src="https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=Notion&logoColor=white"> <!--Notion-->
<img src="https://img.shields.io/badge/Drawio-000000?style=for-the-badge&logo=Drawio&logoColor=white"> <!--Draw.io-->
<img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=Git&logoColor=white"> <!--Git-->
<img src="https://img.shields.io/badge/Github-181717?style=for-the-badge&logo=Github&logoColor=white"> <!--Github-->

</br>

## 🙋🏻‍♂️ 담당 업무
- IaC 테라폼을 활용한 인프라 구축
- Terraform Cloud를 활용한 CI/CD 자동화 구현
- GKE를 활용한 컨테이너 기반 MSA 웹 애플리케이션 구축
- Cloud SQL을 활용한 DB 구축 및 이중화를 통한 고가용성
- Cloud Build와 ArgoCD 애플리케이션 CI/CD 자동화 구현
- Prod/Test 환경 분리를 통한 안정성있는 인프라 운영
- Cloud Monitoring을 활용한 실시간, 지속적 운영 관리
- Cloud Logging을 활용한 실시간 Logging Data 수집
- BigQuery를 활용한 Log Data 필터링 및 테이블로 수집 및 저장
- Cloud Storage를 활용한 Log Data 장기 보관
- Looker Studio를 활용한 필터링 데이터 보고서 형식으로 시각화
- Slack을 활용한 알람으로 실시간 모니터링 구현

</br>

## 📝 상세 내용 
### 📌 요구사항
![image](https://user-images.githubusercontent.com/117608997/215614932-1878e660-6ed9-4a0c-977d-2901db4d69db.png)

</br>

### 📌 Infra Architecture
![image](https://user-images.githubusercontent.com/117608997/215613643-a70f292a-709f-4921-8c56-fd79fa123bcb.png)
```
Test와 Prod 클러스터 분리를 통해 독립적인 Test와 배포 관리
```

</br>

### 📌 Infra: CI/CD Pipeline
![image](https://user-images.githubusercontent.com/117608997/215613710-4a9fc5eb-f6f1-4798-8dcc-1abe2329eb7e.png)
```
Terraform Cloud를 활용한 지속적인 배포 및 관리와 Slack를 활용한 실시간 알람
```

</br>

### 📌 Application Architecture
![image](https://user-images.githubusercontent.com/117608997/215613800-392e892b-6460-41c0-9152-9e98d7ced08d.png)
```
GKE 서비스 내 NEG를 활용한 부하분산 관리
```

</br>

### 📌 Application CI/CD Pipeline
![image](https://user-images.githubusercontent.com/117608997/215613946-cdbd189d-b6bb-4744-b58b-9bd3092d3087.png)
```
Test / Prod 환경 분리를 통한 Test 배포 
Cloud Build를 통한 지속적인 통합 및 이미지 관리
ArgoCD를 활용한 Kubernetes 환경 자동화 배포 관리
Helm Chart를 활용한 패키지 관리
Slack을 활용한 실시간 알람 및 모니터링
```
</br>

### - [Application

### 📌 Monitoring Architecture
![image](https://user-images.githubusercontent.com/117608997/215615830-834c28c6-3a3d-4647-9089-542c1311a417.png)
```
BigQuery와 Looker를 활용한 실시간 Log Data 시각화
Cloud Monitoring을 활용한 대시보드로 지속적인 모니터링
이상 상황 발생 시 Slack을 통해 실시간 알람 및 신속한 장애 처리 가능
```

</br>

### 📌 요구사항 점검
![image](https://user-images.githubusercontent.com/117608997/215615904-ad6cbd7f-4a3e-40d8-9aed-4bd1cf5ee736.png)

</br>

## ⛓️ 구축 과정
### 🔗 Notion Link
#### - [GCP MSA 2-Tier Infra Project](https://glen-party-257.notion.site/GCP-MSA-2-Tier-Project-7e1542b3b8e44bd0b3583f87f86802af)

### 🔗 Notion Link

</br>
