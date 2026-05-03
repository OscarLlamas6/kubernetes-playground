# 09-secrets — Secrets Management

Herramientas para almacenar, distribuir y rotar secretos de forma segura en Kubernetes.

## Herramientas

- [Sealed Secrets](./01-sealed-secrets/README.md) — Operator / CRD-based · Not CNCF · Estable
- [External Secrets Operator](./02-external-secrets-operator/README.md) — Operator / CRD-based · Not CNCF · Estable
- [SOPS (con Flux/Argo)](./03-sops-flux-argo/README.md) — CLI / Encryption · Not CNCF · Estable
- [HashiCorp Vault Agent Injector](./04-vault-agent-injector/README.md) — Operator / Sidecar · Not CNCF · Estable
- [Secrets Store CSI Driver](./05-secrets-store-csi-driver/README.md) — CSI driver / Operator · CNCF Graduated · Estable
- [Infisical Operator](./06-infisical-operator/README.md) — Operator / CRD-based · Not CNCF · Beta
- [Doppler Kubernetes Operator](./07-doppler-k8s-operator/README.md) — Operator · Not CNCF · Estable
