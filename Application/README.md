## Application Infra
### - GKE Flow
![image](https://user-images.githubusercontent.com/117608997/215800467-3bc59726-7cb6-4450-9547-c4a77c7501e2.png)
```
GKE 서비스 내 NEG를 활용한 부하분산 관리
기존 kubernetes 네트워킹의 한계인 doubile-hop-dilemma를 극복
- double-hop dilemma : LoadBalancer가 트래픽을 목적지 Pod가 존재하지 않는 Node로 보낸 경우에는
Pod가 존재하는 Node로 한 번 더 트래픽을 보내는 것
```

</br>

### - Yaml 관계도
![image](https://user-images.githubusercontent.com/117608997/215800791-e37f87b3-8a36-4b9e-a89c-83ab0d06a8f1.png)
```
Ingress 파일 생성 - 외부 HTTP(S) LB
Service 파일 생성 - 내부 클라이언트가 안정적인 내부 IP 주소로 요청을 전송
Deployment 파일 생성 - Replication 및 Deployment 구성
BackendConfig 파일 생성 - Healthcheck 구성
HPA 생성 - 수평형 Pod 자동 확장 구성
```

</br>

## Applciation CICD
### - CI/CD
![image](https://user-images.githubusercontent.com/117608997/215807611-cf107c2c-cfec-48a8-9eb5-761d6e179356.png)
```
Git Hub
- Application 소스 저장, Kubernetes Yaml 파일 저장
Cloud Build
- Google Cloud에서 제공하는 CI 서비스
- Docker 이미지 빌드
Google Artifact Registry
- Docker 이미지 저장소
ArgoCD
- 통합 환경의 지속적인 배포 가능
- Prod 클러스터에 컨테이너로 동작
Helm
- 차트 패키지
Slack
- 트리거 발생 시 Alert
```


