# DevOps Engineering Laboratory Workspace

Welcome to my DevOps laboratory repository. This workspace contains comprehensive implementations, deployment manifests, automated pipelines, monitoring dashboards, and verification records for key DevOps competencies.

---

## Portfolio Architecture & Directory Structure

All modular laboratory exercises are organized in dedicated directories under [`Exercises/`](./Exercises):

```text
Exercises/
├── 1-Kubernetes-Getting-Started/                                # K8s Pod initialization, NodePort exposure & cluster verification
├── 2-Minikube-Kubectl-Flask/                                    # Containerized Flask microservice deployment via declarative YAML
├── 3-Minikube-Scaling-Flask-App-with-Replicasets/               # Workload horizontal scaling & self-healing ReplicaSets
├── 4-Docker-Networking/                                         # Isolated bridge networks & multi-container service discovery
├── 5-Docker-Security-AppArmor/                                  # Linux security kernel enforcement & Docker AppArmor profiling
├── 6-Grafana-Realtime-Monitoring-of-Quick-Commerce-App/         # Prometheus metrics scraping & real-time Grafana observability
├── 7-Jenkins-CI-Automation/                                     # Automated continuous integration builds and Git webhook triggers
├── 8-Jenkins-Hello-World-Job/                                   # Declarative freestyle jobs and artifact archiving
├── 9-Jenkins-Multi-Stage-Pipeline/                              # Multi-stage CI pipeline with unit testing and deployment gates
└── 10-Minikube-Multi-Node-Multi-App-Minikube-Deployment/        # Multi-node microservices architecture (Catalog & Cart services)
```

---

## Lab Execution Track & Progress

| Module # | Exercise Name | Core Technical Focus | Implementation Status |
| :---: | :--- | :--- | :---: |
| **01** | [Kubernetes Getting Started](./Exercises/1-Kubernetes-Getting-Started) | Cluster initialization, Pod deployment, and NodePort routing | `COMPLETED` |
| **02** | [Minikube, kubectl & Flask](./Exercises/2-Minikube-Kubectl-Flask) | Declarative deployments, container runtime, and microservices | `COMPLETED` |
| **03** | [Flask Scaling via ReplicaSets](./Exercises/3-Minikube-Scaling-Flask-App-with-Replicasets) | High availability, Pod replication, and fault recovery | `COMPLETED` |
| **04** | [Docker Network Topologies](./Exercises/4-Docker-Networking) | User-defined bridge drivers, DNS resolution, and isolation | `COMPLETED` |
| **05** | [Container Hardening via AppArmor](./Exercises/5-Docker-Security-AppArmor) | Least privilege enforcement, security profiles, Python SDK | `COMPLETED` |
| **06** | [Real-Time Monitoring with Grafana](./Exercises/6-Grafana-Realtime-Monitoring-of-Quick-Commerce-App) | Prometheus time-series scraping, alert thresholds, dashboards | `COMPLETED` |
| **07** | [Automated CI Pipelines with Jenkins](./Exercises/7-Jenkins-CI-Automation) | Containerized Jenkins master, polling, build webhooks | `COMPLETED` |
| **08** | [Jenkins Freestyle Workflows](./Exercises/8-Jenkins-Hello-World-Job) | Build tasks, shell triggers, build history & artifacts | `COMPLETED` |
| **09** | [Multi-Stage Enterprise CI Pipelines](./Exercises/9-Jenkins-Multi-Stage-Pipeline) | Declarative Jenkinsfile, automated testing with pytest, staging | `COMPLETED` |
| **10** | [Multi-Node Microservices Topology](./Exercises/10-Minikube-Multi-Node-Multi-App-Minikube-Deployment) | Cluster topologies, inter-service communication, ingress routing | `COMPLETED` |

---

## Technology Ecosystem

- **Orchestration & Virtualization**: Kubernetes, Minikube, Docker Engine, Docker Desktop
- **Microservices & Programming**: Python 3 (Flask, Docker SDK, Pytest)
- **CI/CD & Automation**: Jenkins (Freestyle jobs, Declarative Pipelines, Webhooks)
- **Observability & Metrics**: Prometheus Time-Series DB, Grafana Visualization Engine
- **Kernel Security**: Linux AppArmor Profiles, Capabilities filtering (`--cap-drop`)
- **Version Control**: Git, GitHub Actions

---

## Documentation Standards

Each exercise directory contains:
- A technical **`README.md`** detailing theoretical architecture, CLI instructions, and output analyses.
- Source manifests (`Dockerfile`, `*.yaml`, `Jenkinsfile`, Python sources).
- An evidence catalog in `screenshots/` validating end-to-end operational execution.
