# SCC (Security Context Constraints) Annotation in NooBaa Components

## For All NooBaa Deployments

| Component | Type | `openshift.io/required-scc` value |
| :--- | :--- | :--- |
| `noobaa-core` | StatefulSet| `noobaa-core` |
| `noobaa-endpoint` | Deployment| `noobaa-endpoint` |
| `noobaa-agent` | Pod | `noobaa-agent` |
| `noobaa-operator` | Deployment| `restricted-v2` |
| `cnpg-controller-manager` | Deployment | `restricted-v2` |
| `noobaa-db-pg-cluster-<number>` | Cluster | `restricted-v2` |

**Note:** For the DB pods, this is relevant only for new deployments (not upgrade).

## Other

| Component | Type | `openshift.io/required-scc` value |
| :--- | :--- | :--- |
| `noobaa-db-pg-cluster-<number>-init` | Job | `restricted-v2` |
| `prometheus-adapter` | Deployment| `restricted-v2` |
| `noobaa-core-upgrade` | Job | `noobaa-core` |
| `analyze-resource` | Job | `restricted-v2` |
