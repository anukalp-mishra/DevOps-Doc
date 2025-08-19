# DevOps Interview Preparation Kit

---

## 1. **Version Control (Git, GitHub, GitLab, Bitbucket)**

**Key Concepts:**
- Branching & Merging
- Conflict Resolution
- Git Workflows (Git Flow, GitHub Flow)
- Pull Requests and Code Reviews

**Sample Interview Q&A:**
- *Q: What is Git?*
  - **A:** Git is a distributed version control system that lets multiple developers work on a project simultaneously, tracking changes and enabling collaboration.

- *Q: How do you resolve a merge conflict in Git?*
  - **A:** Use `git status` to identify conflicting files, manually edit them to fix conflicts, then add and commit the changes.

- *Q: What is a rebase and when would you use it?*
  - **A:** A rebase applies your changes on top of another branch, creating a linear history. Use it to integrate updates before merging or to clean up commit history.

- *Q: How do you squash commits in Git?*
  - **A:** Use `git rebase -i <base-commit>` and mark commits as "squash" to combine them, then save and complete the rebase.

- *Q: What is a fork and how is it different from a branch?*
  - **A:** A fork creates a separate copy of a repository, usually for contributing to open source; a branch is a pointer within the same repo.

---

## 2. **CI/CD (Jenkins, GitHub Actions, GitLab CI, CircleCI, Travis CI)**

**Key Concepts:**
- Pipeline stages: build, test, deploy
- Automation & triggers
- YAML pipeline configuration

**Sample Interview Q&A:**
- *Q: What is CI/CD?*
  - **A:** CI/CD automates code integration, testing, and deployment, ensuring faster and more reliable software delivery.

- *Q: What is a build artifact? How do you manage artifacts?*
  - **A:** Build artifacts are outputs (binaries, packages, etc.) from the build process. Manage them using artifact repositories like JFrog Artifactory or Nexus.

- *Q: What is a deployment pipeline? Describe its stages.*
  - **A:** A deployment pipeline typically includes stages such as code checkout, build, test (unit/integration), artifact packaging, deploy, and post-deploy validation.

- *Q: How do you handle rollback in a CI/CD pipeline?*
  - **A:** You can trigger rollback by redeploying a previous stable artifact or using deployment strategies like blue-green or canary to revert traffic.

- *Q: How do you handle secret management in your pipelines?*
  - **A:** Use secret management tools (Vault, AWS Secrets Manager) and pipeline features to inject secrets securely, avoiding hardcoding.

- *Q: What is blue-green deployment? What is canary deployment?*
  - **A:** Blue-green deployment uses two environments to switch traffic from old to new with minimal downtime. Canary deployment gradually shifts traffic to the new version, monitoring for issues.

- *Q: How do you ensure zero-downtime deployments?*
  - **A:** Use strategies like blue-green, canary, and rolling updates, along with health checks and load balancers.

---

## 3. **Containers (Docker)**

**Key Concepts:**
- Images, Containers, Volumes, Networks
- Dockerfile, Compose
- Key commands (`run`, `build`, `ps`, `rm`, `pull`, `commit`)

**Sample Interview Q&A:**
- *Q: What is Docker?*
  - **A:** Docker is a platform to build, ship, and run applications inside containers, which package the app and its dependencies for consistency across environments.

- *Q: How are containers different from VMs?*
  - **A:** Containers share the host OS kernel and are lightweight, while VMs run separate OS instances and are heavier.

- *Q: How do you monitor and troubleshoot containers in production?*
  - **A:** Use monitoring tools like Prometheus, Grafana, and container logs; inspect with `docker logs`, `docker stats`, and integrate with centralized logging.

- *Q: What is a sidecar container?*
  - **A:** It’s a container that runs alongside the main container in a Pod to provide supporting features like logging, proxying, or monitoring.

- *Q: What is container networking and how is it managed?*
  - **A:** Container networking enables communication between containers and with the outside world, managed via Docker networks or Kubernetes services.

---

## 4. **Orchestration (Kubernetes, Helm)**

**Key Concepts:**
- Pods, Deployments, Services, ConfigMaps, Secrets
- Helm Charts

**Sample Interview Q&A:**
- *Q: What is Kubernetes?*
  - **A:** Kubernetes is a container orchestration platform that automates deployment, scaling, and management of containerized applications.

- *Q: What is a namespace in Kubernetes and how is it used?*
  - **A:** Namespaces provide logical isolation for resources, useful for separating environments or teams.

- *Q: What is the difference between a ReplicaSet and a Deployment?*
  - **A:** A ReplicaSet ensures a specified number of pod replicas; a Deployment manages ReplicaSets and provides rolling updates and rollbacks.

- *Q: How do you scale applications in Kubernetes?*
  - **A:** Update the replica count in a Deployment or use Horizontal Pod Autoscaler.

- *Q: What is pod affinity and anti-affinity?*
  - **A:** These control pod placement based on other pod locations, improving availability or reducing resource contention.

- *Q: How do you manage secrets and configuration in Kubernetes?*
  - **A:** Use ConfigMaps for configuration and Secrets for sensitive data, mounting them as environment variables or volumes.

- *Q: What is RBAC in Kubernetes?*
  - **A:** Role-Based Access Control restricts user actions based on roles and permissions.

- *Q: What is an init container in Kubernetes?*
  - **A:** An init container runs before app containers to perform setup tasks like config or dependency initialization.

---

## 5. **Infrastructure as Code (Terraform, Ansible, CloudFormation)**

**Key Concepts:**
- Declarative resource management
- Providers (AWS, Azure, GCP)
- Playbooks, Roles (Ansible), Modules (Terraform)

**Sample Interview Q&A:**
- *Q: What is Terraform?*
  - **A:** Terraform is an IaC tool that lets you define and manage infrastructure using code, supporting multiple cloud providers.

- *Q: What is the difference between declarative and imperative approach in IaC?*
  - **A:** Declarative defines the desired end state (e.g., Terraform, CloudFormation); imperative provides step-by-step instructions (e.g., Ansible).

- *Q: How do you manage infrastructure state in Terraform?*
  - **A:** Terraform uses state files (local or remote) to track resources. For teams, use remote backends (S3, Azure Blob) and state locking.

- *Q: How do you manage infrastructure for multiple environments?*
  - **A:** Use workspaces, separate state files, variable files, or folder structures for each environment.

---

## 6. **Cloud Platforms (AWS, Azure, GCP)**

**Key Concepts:**
- Compute (EC2, Compute Engine, VM)
- Storage (S3, Blob, Bucket)
- Kubernetes managed services (EKS, AKS, GKE)

**Sample Interview Q&A:**
- *Q: How would you secure an S3 bucket?*
  - **A:** Use bucket policies, enable encryption, restrict public access, and use IAM roles.

- *Q: What is auto-scaling? How do you implement it?*
  - **A:** Auto-scaling automatically adjusts resources based on load, implemented with AWS Auto Scaling Groups, Azure Scale Sets, or Kubernetes HPA.

- *Q: What is a VPC? How do you secure resources within a VPC?*
  - **A:** A VPC is a virtual private cloud for network isolation; secure with subnets, security groups, NACLs, and IAM policies.

- *Q: How do you handle disaster recovery in cloud environments?*
  - **A:** Use backup/restore, multi-region replication, infrastructure as code for reproducibility, and DR drills.

- *Q: How do you optimize costs in the cloud?*
  - **A:** Use resource tagging, rightsizing, reserved instances, auto-scaling, monitoring unused resources, and leveraging cloud-native cost management tools.

---

## 7. **Monitoring & Logging (Prometheus, Grafana, ELK, Datadog, Splunk)**

**Key Concepts:**
- Metrics, Dashboards, Alerts
- Log aggregation and analysis

**Sample Interview Q&A:**
- *Q: How do you monitor application health?*
  - **A:** Use Prometheus for metrics and Grafana for dashboards; set up alerts for anomalies.

- *Q: What is the difference between monitoring and observability?*
  - **A:** Monitoring tracks known metrics/events; observability enables deeper insight into unknown issues using logs, metrics, tracing.

- *Q: How do you set up alerting for critical failures?*
  - **A:** Define alerting rules in monitoring tools, send notifications via email, Slack, PagerDuty, etc.

- *Q: How do you aggregate and visualize logs from multiple services?*
  - **A:** Use ELK stack (Logstash for aggregation, Elasticsearch for search, Kibana for visualization) or cloud-native solutions.

---

## 8. **Configuration Management (Ansible, Puppet, Chef, SaltStack)**

**Key Concepts:**
- Idempotency, Inventory, Playbooks, Roles

**Sample Interview Q&A:**
- *Q: What is a playbook in Ansible?*
  - **A:** A playbook is a YAML file defining tasks to automate configuration and deployment on target servers.

---

## 9. **Networking & Security**

**Key Concepts:**
- Load Balancing, Firewalls, SSL/TLS, IAM

**Sample Interview Q&A:**
- *Q: How do you secure a Docker container?*
  - **A:** Use non-root users, minimize image size, restrict container capabilities, update images regularly, and scan for vulnerabilities.

- *Q: How do you ensure security in your CI/CD pipeline?*
  - **A:** Use secret management, code scanning tools, restrict permissions, and integrate security checks early in the pipeline.

- *Q: What is container image scanning?*
  - **A:** It detects vulnerabilities in images using tools like Trivy, Clair, or built-in registry scanners.

- *Q: How do you handle vulnerabilities in open-source dependencies?*
  - **A:** Use dependency scanning tools (Snyk, Dependabot), timely updates, and monitoring for new CVEs.

- *Q: What tools do you use for security testing?*
  - **A:** Use tools like OWASP ZAP, SonarQube, Snyk, and custom scripts for static/dynamic analysis.

- *Q: How do you ensure compliance in a DevOps pipeline?*
  - **A:** Integrate automated compliance checks, maintain audit logs, and use security policies and scanning tools.

---

## 10. **Linux & Scripting**

**Key Concepts:**
- Shell scripting, process management, permissions, systemd

**Sample Interview Q&A:**
- *Q: How do you find a process using a specific port?*
  - **A:** Use `netstat -tulpn | grep <port>` or `lsof -i :<port>`.

- *Q: How do you schedule a cron job?*
  - **A:** Add an entry to the crontab file using `crontab -e` with the desired schedule and command.

- *Q: How do you troubleshoot high CPU usage on a Linux server?*
  - **A:** Use tools like `top`, `htop`, `ps aux --sort=-%cpu`, and analyze running processes and resource usage.

- *Q: What is the difference between hard and soft links?*
  - **A:** Hard links point directly to file data and persist until all are deleted; soft links (symlinks) are pointers to the file name/path.

---

## 11. **DevOps Culture & Practices**

**Key Concepts:**
- Collaboration, automation, feedback loops, agility

**Sample Interview Q&A:**
- *Q: What is the goal of DevOps?*
  - **A:** To bridge the gap between development and operations, enabling faster, more reliable software delivery through automation and collaboration.

- *Q: What is the difference between Agile and DevOps?*
  - **A:** Agile focuses on iterative development and delivery; DevOps extends Agile principles to deployment, operations, and automation.

- *Q: How do you handle communication and collaboration between development and operations teams?*
  - **A:** Use shared tools, regular meetings, DevOps culture, and automation to improve transparency and cooperation.

- *Q: Describe a challenging incident you handled in production.*
  - **A:** When a deployment failed due to a misconfigured environment variable, I checked logs, rolled back to a stable release, coordinated with the team to fix the config, redeployed, and added checks to prevent recurrence.

- *Q: How do you approach troubleshooting a failed deployment?*
  - **A:** Check logs, roll back if necessary, analyze pipeline output, communicate with teams, and document the incident for future prevention.

- *Q: Give an example of how you automated a manual process.*
  - **A:** Automated server provisioning using Terraform and Ansible, reducing setup time from hours to minutes.

- *Q: How do you stay updated with the latest DevOps trends and tools?*
  - **A:** Follow blogs, attend webinars, participate in communities, and experiment with new tools in lab environments.

---

## 12. **Site Reliability Engineering (SRE) & Service Mesh**

**Key Concepts:**
- SRE principles (SLI, SLO, SLA, error budgets)
- Service mesh (Istio, Linkerd): traffic management, observability, security

**Sample Interview Q&A:**
- *Q: What is SRE and how does it relate to DevOps?*
  - **A:** SRE applies software engineering to operations for reliability and scalability. It complements DevOps by focusing on service reliability and monitoring.

- *Q: What is a service mesh?*
  - **A:** An infrastructure layer for managing service-to-service communication, with features like traffic management, security, and observability.

---

## 13. **Disaster Recovery, High Availability & Cost Optimization**

**Sample Interview Q&A:**
- *Q: How do you design for high availability?*
  - **A:** Use redundant resources, load balancing, failover strategies, and multi-region deployments.

- *Q: How do you ensure disaster recovery for critical services?*
  - **A:** Automated backups, multi-region replication, infrastructure as code, and regular DR drills.

- *Q: How have you optimized cloud costs in your previous projects?*
  - **A:** Resource tagging, regular audits, rightsizing, reserved instances, auto-shutdown, and cost monitoring tools.

---

## 14. **Compliance & Auditing**

**Sample Interview Q&A:**
- *Q: How do you ensure compliance in a DevOps pipeline?*
  - **A:** Automated compliance checks, maintain audit logs, and apply security policies and scanning tools.

---

## 15. **Scenario-Based Interview Questions & Answers**

#### Incident Handling
- **Q:** Describe a time when a deployment failed in production. How did you handle it?
  - **A:** When a deployment failed due to a misconfigured environment variable, I immediately checked the deployment logs and rolled back to the previous stable release using our CI/CD pipeline. I coordinated with the team to fix the configuration, redeployed, and monitored the system health. Afterward, we added automated checks for environment variables to prevent similar issues.

#### Automating Manual Tasks
- **Q:** Give an example of how you automated a manual process.
  - **A:** We used to manually provision and configure servers for new environments. I automated this using Terraform and Ansible, creating reusable templates and playbooks. This reduced setup time from hours to minutes and eliminated configuration drift.

#### Handling High CPU Usage
- **Q:** A production server is experiencing high CPU usage. What steps would you take?
  - **A:** I would first use monitoring tools and commands like `top` or `htop` to identify the process causing the spike. I’d check logs and recent changes, then determine if it’s due to a code deployment or external factors. If necessary, I’d scale resources, restart affected services, and coordinate with developers for a fix.

#### Security Breach
- **Q:** How would you respond to a security breach detected in one of your containers?
  - **A:** I’d isolate the affected container, analyze logs and network traffic, and determine the attack vector. I’d patch the vulnerability, scan other containers for similar issues, and update our images. Finally, I’d conduct a postmortem and improve security controls like image scanning and network segmentation.

#### Scaling Application
- **Q:** Your application is experiencing a sudden increase in traffic. How do you handle it?
  - **A:** I’d use auto-scaling features of our cloud provider or Kubernetes HPA to add more instances. I’d monitor system metrics and ensure the database and storage can handle the load. If necessary, I’d optimize caching and review resource limits.

#### Cloud Cost Optimization
- **Q:** How have you optimized cloud costs in your previous projects?
  - **A:** I implemented resource tagging and regular audits, rightsized instances based on usage, used reserved instances, and automated shutdown of non-critical resources after hours. I also used cost monitoring tools to proactively identify and eliminate waste.

#### Disaster Recovery
- **Q:** How do you ensure disaster recovery for critical services?
  - **A:** I set up automated backups, multi-region replication, and infrastructure as code for reproducibility. We conduct regular DR drills to validate our recovery procedures and update documentation accordingly.

---

## **Quick Cheatsheet: Key Commands**

```sh
# Git
git clone <repo>
git branch, git merge, git rebase

# Docker
docker build -t <image> .
docker run -d -p 8080:80 <image>
docker ps -a
docker rm <container>
docker pull <image>
docker commit <container> <new-image>

# Kubernetes
kubectl get pods
kubectl apply -f <manifest>
kubectl logs <pod>
kubectl delete pod <pod>

# Terraform
terraform init
terraform plan
terraform apply
terraform destroy

# Ansible
ansible-playbook <playbook.yml>
```

---

## **General Interview Tips**
- Be ready to whiteboard architectures and workflows.
- Be honest about what you don’t know—show willingness to learn.
- Highlight teamwork and communication skills.
- Share real-world examples from your experience.
- Ask questions about the team’s DevOps culture and future roadmap.
- Always explain your thought process.
- Relate your answers to real scenarios.
- Show awareness of security and automation.
- Ask clarifying questions if needed.

---

**Ready for mock questions, deep dives, or scenario-based practice? Let me know your priority!**
