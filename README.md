# k8s-playground

Laboratorio práctico para explorar el ecosistema completo de Kubernetes y cloud-native (~180 herramientas en 32 categorías).

Las herramientas están alineadas con el [CNCF Landscape](https://landscape.cncf.io/) y con los proyectos vigentes a 2026.
Cada subcarpeta incluye un README con contexto, una carpeta `manifests/`, `examples/` y `notes/` para ir construyendo el laboratorio paso a paso.

---

## Índice de categorías

| # | Categoría | Descripción |
|---|-----------|-------------|
| 01 | [01-cluster-creation](./01-cluster-creation/README.md) — **Cluster Creation** | Clusters locales, distros, managed services y herramientas IaC para aprovisionar Kubernetes |
| 02 | [02-package-management](./02-package-management/README.md) — **Package Management** | Gestión de manifiestos y paquetes: Helm, Kustomize y alternativas modernas |
| 03 | [03-gitops](./03-gitops/README.md) — **GitOps** | Operadores GitOps para sincronizar clusters desde repositorios Git |
| 04 | [04-ci-cd](./04-ci-cd/README.md) — **CI/CD** | Pipelines de integración y entrega continua nativos de Kubernetes |
| 05 | [05-service-mesh](./05-service-mesh/README.md) — **Service Mesh** | Mallas de servicios para tráfico mTLS, observabilidad L7 y políticas entre microservicios |
| 06 | [06-networking-cni](./06-networking-cni/README.md) — **Networking / CNI** | Plugins CNI que implementan la red del cluster: Cilium, Calico, Flannel y más |
| 07 | [07-ingress-gateway](./07-ingress-gateway/README.md) — **Ingress / Gateway** | Controladores de Ingress y Gateway API para exponer servicios al exterior |
| 08 | [08-load-balancers](./08-load-balancers/README.md) — **Load Balancers** | Load balancers para clusters on-prem: MetalLB, kube-vip y alternativas |
| 09 | [09-secrets](./09-secrets/README.md) — **Secrets Management** | Gestión segura de secretos: desde Sealed Secrets hasta Vault y External Secrets Operator |
| 10 | [10-policy-security](./10-policy-security/README.md) — **Policy & Security** | Motores de políticas y admission control: OPA Gatekeeper, Kyverno y más |
| 11 | [11-runtime-security](./11-runtime-security/README.md) — **Runtime Security** | Detección de amenazas en tiempo de ejecución: Falco, Tetragon y eBPF |
| 12 | [12-image-security](./12-image-security/README.md) — **Image Security** | Escaneo de vulnerabilidades y firma de imágenes de container |
| 13 | [13-supply-chain](./13-supply-chain/README.md) — **Supply Chain Security** | Seguridad de la cadena de suministro: SBOMs, firmas y attestations |
| 14 | [14-observability-metrics](./14-observability-metrics/README.md) — **Observabilidad — Métricas** | Prometheus y su ecosistema para métricas, alertas y almacenamiento a largo plazo |
| 15 | [15-observability-logs](./15-observability-logs/README.md) — **Observabilidad — Logs** | Recolección, agregación y consulta de logs: Loki, Fluentd, Fluent Bit y más |
| 16 | [16-observability-tracing](./16-observability-tracing/README.md) — **Observabilidad — Tracing** | Distributed tracing con OpenTelemetry, Jaeger, Tempo y Zipkin |
| 17 | [17-event-driven](./17-event-driven/README.md) — **Event-Driven / Messaging** | Arquitecturas event-driven en Kubernetes: KEDA, Knative Eventing, NATS, Kafka y más |
| 18 | [18-serverless-functions](./18-serverless-functions/README.md) — **Serverless / Functions** | FaaS y serverless sobre Kubernetes: Knative Serving, OpenFaaS, Fission y más |
| 19 | [19-storage](./19-storage/README.md) — **Storage** | Almacenamiento persistente en Kubernetes: Rook/Ceph, Longhorn, OpenEBS, Velero y más |
| 20 | [20-databases-on-k8s](./20-databases-on-k8s/README.md) — **Databases on Kubernetes** | Operadores de bases de datos: PostgreSQL, MySQL, TiDB, Vitess y más |
| 21 | [21-autoscaling](./21-autoscaling/README.md) — **Autoscaling** | Escalado automático de pods y nodos: HPA, VPA, Karpenter y KEDA |
| 22 | [22-multi-tenancy](./22-multi-tenancy/README.md) — **Multi-Tenancy** | Aislamiento y multi-tenancy en un mismo cluster: vcluster, Capsule, HNC y más |
| 23 | [23-multi-cluster](./23-multi-cluster/README.md) — **Multi-Cluster** | Federación y gestión de múltiples clusters: Karmada, OCM, Submariner y más |
| 24 | [24-developer-experience](./24-developer-experience/README.md) — **Developer Experience** | Herramientas para desarrollo local en Kubernetes: Tilt, Skaffold, Telepresence y más |
| 25 | [25-management-uis](./25-management-uis/README.md) — **Management UIs** | Interfaces gráficas y TUI para gestionar clusters: Lens, k9s, Headlamp y más |
| 26 | [26-cost-optimization](./26-cost-optimization/README.md) — **Cost Optimization** | Visibilidad y optimización de costos en Kubernetes: OpenCost, Goldilocks y más |
| 27 | [27-chaos-engineering](./27-chaos-engineering/README.md) — **Chaos Engineering** | Ingeniería del caos para probar la resiliencia: Chaos Mesh, LitmusChaos y más |
| 28 | [28-ai-ml-on-k8s](./28-ai-ml-on-k8s/README.md) — **AI/ML on Kubernetes** | Plataformas ML/AI sobre Kubernetes: Kubeflow, KServe, Ray, GPU Operator y más |
| 29 | [29-edge-iot](./29-edge-iot/README.md) — **Edge / IoT** | Kubernetes en el edge y dispositivos IoT: KubeEdge, OpenYurt, Akri y k3s |
| 30 | [30-platform-engineering](./30-platform-engineering/README.md) — **Platform Engineering** | IDP y plataformas internas de desarrollo: Backstage, Crossplane, Port y Kratix |
| 31 | [31-runtime-alternatives](./31-runtime-alternatives/README.md) — **Runtime Alternatives** | Runtimes alternativos: containerd, CRI-O, gVisor, Kata Containers, Wasm y más |
| 32 | [32-api-management](./32-api-management/README.md) — **API Management** | Gestión de APIs sobre Kubernetes: Kong, Tyk, Gravitee y más |

---

## Cómo usar este repo

### Orden de aprendizaje sugerido

1. **La base** — clusters, paquetes y GitOps:
   - `01-cluster-creation` → levantá un cluster local (minikube, kind o k3d)
   - `02-package-management` → aprendé Helm y Kustomize
   - `03-gitops` → Argo CD o Flux CD
   - `14-observability-metrics`, `15-observability-logs`, `16-observability-tracing` → Prometheus + Grafana + Loki + OpenTelemetry

2. **Seguridad** (una vez que tenés la base):
   - `09-secrets` → Sealed Secrets o External Secrets
   - `10-policy-security` → Kyverno u OPA Gatekeeper
   - `11-runtime-security` → Falco
   - `12-image-security` → Trivy + Cosign
   - `13-supply-chain` → Sigstore

3. **Networking** (se puede ir en paralelo con seguridad):
   - `06-networking-cni` → Cilium
   - `07-ingress-gateway` → Gateway API + Cilium o NGINX
   - `05-service-mesh` → Istio o Linkerd
   - `08-load-balancers` → MetalLB (si es on-prem)

4. **El resto según interés**:
   - Storage, databases, autoscaling, multi-cluster, AI/ML, edge, platform engineering, etc.

---

## Tabla comparativa

| Herramienta | Categoría | Tipo | CNCF status | Madurez | Caso de uso típico |
|-------------|-----------|------|-------------|---------|-------------------|
| | | | | | |

---

## Progreso

### 01-cluster-creation — Cluster Creation

- [ ] Minikube
- [ ] kind (Kubernetes in Docker)
- [ ] k3d
- [ ] MicroK8s
- [ ] Docker Desktop Kubernetes
- [ ] Rancher Desktop
- [ ] Colima
- [ ] OrbStack
- [ ] K3s
- [ ] k0s
- [ ] MicroShift
- [ ] kubeadm
- [ ] Talos Linux
- [ ] Sidero Omni
- [ ] Rancher RKE2
- [ ] Cluster API (CAPI)
- [ ] Kubespray
- [ ] Amazon EKS
- [ ] Azure AKS
- [ ] Google GKE
- [ ] Oracle OKE
- [ ] DigitalOcean DOKS
- [ ] Linode LKE
- [ ] Civo Kubernetes
- [ ] Vultr VKE
- [ ] Terraform / OpenTofu
- [ ] Pulumi
- [ ] AWS CloudFormation
- [ ] Azure Bicep
- [ ] Crossplane
- [ ] Kubernetes the Hard Way

### 02-package-management — Package Management

- [ ] Helm
- [ ] Kustomize
- [ ] Carvel (ytt/kapp/kbld)
- [ ] Jsonnet / Tanka
- [ ] cdk8s
- [ ] Timoni
- [ ] Glasskube

### 03-gitops — GitOps

- [ ] Argo CD
- [ ] Flux CD
- [ ] Rancher Fleet
- [ ] werf
- [ ] Kargo

### 04-ci-cd — CI/CD

- [ ] Tekton
- [ ] Argo Workflows
- [ ] Jenkins X
- [ ] Drone
- [ ] Buildkite Agents
- [ ] Dagger

### 05-service-mesh — Service Mesh

- [ ] Istio
- [ ] Linkerd
- [ ] Cilium Service Mesh
- [ ] Consul Connect
- [ ] Kuma
- [ ] Open Service Mesh (deprecated)
- [ ] Traefik Mesh

### 06-networking-cni — Networking / CNI

- [ ] Cilium
- [ ] Calico
- [ ] Flannel
- [ ] Weave Net (legacy)
- [ ] Antrea
- [ ] Kube-router
- [ ] Multus CNI

### 07-ingress-gateway — Ingress / Gateway

- [ ] NGINX Ingress Controller
- [ ] Traefik
- [ ] HAProxy Ingress
- [ ] Contour
- [ ] Kong
- [ ] Emissary-ingress (Ambassador)
- [ ] Kubernetes Gateway API
- [ ] Cilium Gateway API
- [ ] Envoy Gateway

### 08-load-balancers — Load Balancers

- [ ] MetalLB
- [ ] kube-vip
- [ ] PureLB
- [ ] Cloud LB Controllers

### 09-secrets — Secrets Management

- [ ] Sealed Secrets
- [ ] External Secrets Operator
- [ ] SOPS (con Flux/Argo)
- [ ] HashiCorp Vault Agent Injector
- [ ] Secrets Store CSI Driver
- [ ] Infisical Operator
- [ ] Doppler Kubernetes Operator

### 10-policy-security — Policy & Security

- [ ] OPA Gatekeeper
- [ ] Kyverno
- [ ] Kubewarden
- [ ] jsPolicy
- [ ] Validating Admission Policy
- [ ] Pod Security Standards

### 11-runtime-security — Runtime Security

- [ ] Falco
- [ ] Tetragon
- [ ] Tracee
- [ ] KubeArmor
- [ ] AppArmor / SELinux

### 12-image-security — Image Security

- [ ] Trivy
- [ ] Grype / Syft
- [ ] Clair
- [ ] Cosign / Sigstore
- [ ] Notary v2 / Notation
- [ ] Kyverno (verify images)
- [ ] Connaisseur

### 13-supply-chain — Supply Chain Security

- [ ] Sigstore (Cosign / Rekor / Fulcio)
- [ ] in-toto
- [ ] Tekton Chains
- [ ] GUAC
- [ ] SBOM Generators (Syft/Trivy/etc.)

### 14-observability-metrics — Observabilidad — Métricas

- [ ] Prometheus
- [ ] Thanos
- [ ] Cortex / Grafana Mimir
- [ ] VictoriaMetrics
- [ ] Grafana
- [ ] kube-state-metrics
- [ ] Prometheus Node Exporter

### 15-observability-logs — Observabilidad — Logs

- [ ] Grafana Loki / Promtail
- [ ] Fluentd
- [ ] Fluent Bit
- [ ] Vector
- [ ] ELK / EFK Stack
- [ ] OpenSearch

### 16-observability-tracing — Observabilidad — Tracing

- [ ] OpenTelemetry
- [ ] Jaeger
- [ ] Grafana Tempo
- [ ] Zipkin
- [ ] Pixie

### 17-event-driven — Event-Driven / Messaging

- [ ] Knative Eventing
- [ ] Argo Events
- [ ] Dapr
- [ ] KEDA
- [ ] NATS / NATS Operator
- [ ] Strimzi (Kafka on K8s)
- [ ] RabbitMQ Cluster Operator

### 18-serverless-functions — Serverless / Functions

- [ ] Knative Serving
- [ ] OpenFaaS
- [ ] Kubeless (legacy)
- [ ] Fission
- [ ] Fn Project

### 19-storage — Storage

- [ ] Rook / Ceph
- [ ] Longhorn
- [ ] OpenEBS
- [ ] Portworx
- [ ] MinIO Operator
- [ ] Velero
- [ ] Kasten K10
- [ ] Stash

### 20-databases-on-k8s — Databases on Kubernetes

- [ ] CloudNativePG
- [ ] Zalando Postgres Operator
- [ ] Percona Operators
- [ ] Vitess
- [ ] TiDB Operator
- [ ] KubeDB
- [ ] StackGres

### 21-autoscaling — Autoscaling

- [ ] HPA / VPA / Cluster Autoscaler
- [ ] Karpenter
- [ ] KEDA
- [ ] Goldilocks

### 22-multi-tenancy — Multi-Tenancy

- [ ] vcluster
- [ ] Capsule
- [ ] HNC (Hierarchical Namespace Controller)
- [ ] kiosk
- [ ] Loft

### 23-multi-cluster — Multi-Cluster

- [ ] Karmada
- [ ] Open Cluster Management
- [ ] Cluster API (multi-cluster)
- [ ] Submariner
- [ ] Liqo
- [ ] KubeFed (legacy)

### 24-developer-experience — Developer Experience

- [ ] Tilt
- [ ] Skaffold
- [ ] Telepresence
- [ ] Okteto
- [ ] DevSpace
- [ ] Garden
- [ ] mirrord

### 25-management-uis — Management UIs

- [ ] Lens
- [ ] k9s
- [ ] Headlamp
- [ ] Rancher Manager
- [ ] Portainer
- [ ] Octant (archived)
- [ ] Kubernetes Dashboard

### 26-cost-optimization — Cost Optimization

- [ ] OpenCost / Kubecost
- [ ] Karpenter (cost angle)
- [ ] Goldilocks
- [ ] KubeGreen

### 27-chaos-engineering — Chaos Engineering

- [ ] Chaos Mesh
- [ ] LitmusChaos
- [ ] Chaos Toolkit
- [ ] Pumba
- [ ] kube-monkey

### 28-ai-ml-on-k8s — AI/ML on Kubernetes

- [ ] Kubeflow
- [ ] KServe
- [ ] Ray / KubeRay
- [ ] vLLM on Kubernetes
- [ ] NVIDIA GPU Operator
- [ ] Volcano

### 29-edge-iot — Edge / IoT

- [ ] KubeEdge
- [ ] OpenYurt
- [ ] Akri
- [ ] K3s (Edge)

### 30-platform-engineering — Platform Engineering

- [ ] Backstage
- [ ] Crossplane
- [ ] Port
- [ ] Kratix
- [ ] CAPI + Crossplane (combo)

### 31-runtime-alternatives — Runtime Alternatives

- [ ] containerd
- [ ] CRI-O
- [ ] gVisor
- [ ] Kata Containers
- [ ] Firecracker + Kata
- [ ] WasmEdge
- [ ] SpinKube
- [ ] Krustlet (legacy)

### 32-api-management — API Management

- [ ] Kong Gateway
- [ ] Tyk
- [ ] Apigee (Google)
- [ ] Gravitee
- [ ] 3scale (Red Hat)

---

## Contribuir

Cada subcarpeta sigue la misma estructura:
- `README.md` — contexto, cuándo usarlo, ejemplo
- `manifests/` — YAMLs, Helm values, Kustomize overlays
- `examples/` — apps de demostración
- `notes/` — apuntes, links y lecciones aprendidas
