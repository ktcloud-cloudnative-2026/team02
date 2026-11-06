# deploy

Kubernetes 매니페스트와 Argo CD 설정. 클러스터 · GitOps 담당이 구조를 정합니다.

`main`에 머지되면 GitHub Actions가 이미지를 만들고, Argo CD가 `overlays/<환경>`을 클러스터에 배포합니다.

```
deploy/
  cluster/            클러스터 구축 기록: kubeadm, Calico, MetalLB, local-path, Envoy Gateway, Argo CD
  platform/           모든 서비스가 같이 쓰는 설정: MetalLB IP 풀, Gateway, HTTPRoute
  base/               서비스별 Deployment · Service (환경 공통)
    menu/  order/  kitchen/  congestion/  auth/  admin/
  overlays/dev/       dev에서만 바꿀 값 (replicas, 이미지 태그, ConfigMap 등)
  overlays/prod/      prod에서만 바꿀 값
  argocd/             Application
```

- 이미지 빌드(CI)는 `.github/workflows/`에 둡니다
- 지금은 `cluster/`부터 채우고, 나머지 폴더는 해당 단계에서 만듭니다

## 2팀 값

| 항목 | dev | prod |
|---|---|---|
| control plane | 10.10.22.11 | 10.10.22.21 |
| 워커 | 10.10.22.12, .13 | 10.10.22.22, .23 |
| MetalLB 대역 | 10.10.22.100-127 | 10.10.22.200-223 |
| 파드 대역 | 10.244.0.0/16 | 10.244.0.0/16 |

## [미정]

- 클러스터 안에 DB를 둘지, 강사 제공 PostgreSQL VM(10.10.22.10)만 쓸지
- 메시지 큐 배포 방식
- prod 배포를 자동으로 할지, 승인 후 할지

## 주의

- admin.conf, `~/.kube/config`, join 토큰, DB 비밀번호는 저장소 · 채팅에 올리지 않습니다
- 비밀 값은 Kubernetes Secret으로 관리하고, 저장소에는 값을 비운 예시만 둡니다
