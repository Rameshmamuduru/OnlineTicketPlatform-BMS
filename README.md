```
app/
 ├── Jenkinsfile
 ├── Dockerfile
 ├── ansible/
 │     ├── deploy-dev.yml
 │     └── deploy-prod.yml
 └── k8s/
       ├── dev/
       │    ├── deployment.yaml
       │    └── service.yaml
       └── prod/
            ├── deployment.yaml
            └── service.yaml
```
```
| Tool        | Typical Use             |
| ----------- | ----------------------- |
| kubeadm     | Standard manual install |
| kops        | AWS self-managed        |
| Rancher RKE | On-prem / VM clusters   |
| MicroK8s    | Local / edge            |
| Talos       | Secure production       |

```
