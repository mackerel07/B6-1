# Cloud Web Service Infrastructure

## 프로젝트 소개

AWS 환경에서 VPC, Public Subnet, Internet Gateway, Route Table, Security Group을 직접 구성하고 EC2에 Nginx를 설치하여 외부에서 접속 가능한 웹 서비스를 구축하였다.

---

## Architecture

- Region : ap-northeast-2 (Seoul)
- VPC : basic-vpc
- Public Subnet : public-subnet
- Internet Gateway : basic-igw
- Route Table : public-rt
- EC2 : cloud-web-server
- Web Server : Nginx

---

## Security Group

### Inbound

| Type | Port | Source |
|------|------|--------|
| SSH | 22 | My IP |
| HTTP | 80 | 0.0.0.0/0 |

---

## External Access Verification

### 선택한 방식

A. 브라우저 접속

### URL

http://13.125.68.192

### 결과

브라우저에서 "Welcome to nginx!" 페이지가 정상적으로 출력됨.

---

## Local Verification

```
curl http://localhost
```

결과

```
Welcome to nginx!
```
