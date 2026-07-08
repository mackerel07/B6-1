# Troubleshooting Report

## 문제

VPC 생성 시 다음 오류 발생

```
You are not authorized to perform ec2:CreateVpc
```

---

## 원인 가설

IAM 사용자에게 VPC 생성 권한이 부여되지 않았다.

---

## 검증

IAM 정책을 확인한 결과 CreateVpc 권한이 존재하지 않았다.

---

## 조치

IAM Group에

- AmazonEC2FullAccess
- AmazonVPCFullAccess

정책을 추가하였다.

---

## 결과

VPC 생성이 정상적으로 완료되었다.

---

## 재발 방지

IAM 사용자 생성 후 필요한 정책이 연결되었는지 먼저 확인한다.

AdministratorAccess는 사용하지 않는다.
