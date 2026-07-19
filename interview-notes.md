# 1. Tell me about yourself

*Answer:*

"Good morning, sir/madam. My name is Jitendra Singh. I have recently completed my B.Tech in Computer Science and Engineering. I have hands-on experience with Linux, Git, Docker, AWS, Terraform, Jenkins, GitHub Actions, and Nginx through practical projects. I am looking for an opportunity to start my career as a DevOps Engineer, where I can learn, grow, and contribute to the organization."

# 2. What is DevOps?
*Answer:*
"DevOps is a combination of Development and Operations. It helps automate software development, testing, and deployment, enabling faster and more reliable software delivery."

# 4. What is CI/CD?
*Answer:*
"CI (Continuous Integration) automatically builds and tests code whenever changes are made. CD (Continuous Delivery/Deployment) automates the release of applications, making deployments faster and more reliable."

# 5. Explain your GitHub Actions project.
*Answer:*
"I created a GitHub Actions workflow that automatically builds my project whenever code is pushed to GitHub. This removes manual work and ensures the project builds successfully every time."

# 6. Difference between Docker Image and Container.

*Answer:*
"A Docker image is a blueprint that contains the application and its dependencies. A Docker container is the running instance of that image."
# 7. Explain your Dockerfile.
Answer:
"My Dockerfile uses a base image, copies the application into the image, exposes the required port, and defines the command to start the application."

# 8. Difference between COPY and ADD.
*Answer:*
"COPY only copies files and folders into the Docker image. ADD can also extract local archive files and download files from URLs, but COPY is preferred in most cases."

# 9. What is a Docker Volume?
*Answer:*
"A Docker volume stores data outside the container. It keeps the data safe even if the container is removed."

# 10. What happens when you run docker build -t app .?
*Answer:*
"Docker reads the Dockerfile, executes each instruction, creates a Docker image, and tags it with the name 'app'."

# 11. Explain your AWS project.
*Answer:*
"I launched an EC2 instance, connected using SSH, installed Docker and Nginx, deployed my application, and configured Security Groups to allow access."

# 12. Difference between Security Group and NACL.
*Answer:*
"Security Groups work at the instance level and are stateful. NACLs work at the subnet level, are stateless, and support both allow and deny rules."

# 13. What is Terraform?
*Answer:*
"Terraform is an Infrastructure as Code (IaC) tool. It allows us to create and manage cloud resources using code instead of manual configuration."

# 14. Nginx service is not working. What will you do?
*Answer:*
"I will check the service status, review the logs, verify the configuration, and make sure the required port is not already in use. Then I will restart the service if needed."

# 15. Networking Basics
*DNS:*
"DNS converts a domain name into an IP address."
HTTP vs HTTPS:
"HTTP transfers data without encryption, while HTTPS encrypts data using SSL/TLS for secure communication."
SSH:
"SSH is a secure protocol used to connect to remote Linux servers."
TCP vs UDP:
"TCP is reliable and guarantees data delivery. UDP is faster but does not guarantee delivery."

# 16. Why should we hire you?
*Answer:*
"I have a strong foundation in DevOps tools and practical project experience. I am a quick learner, hardworking, and eager to contribute while continuously improving my skills."

# 17. Do you have any questions for us?
*Answer:*
"Yes, thank you. What technologies does your DevOps team use? What kind of training or learning opportunities are available for freshers? And what will be my responsibilities in the first few months?"


# ⭐ Bonus: If the interviewer asks, "Introduce your projects"
# Answer:
"I have completed projects on Docker, GitHub Actions, AWS, Terraform, and Nginx. My projects include deploying a Spring Boot application with Docker, hosting a React application on Nginx, creating a CI/CD pipeline using GitHub Actions, and provisioning AWS infrastructure using Terraform."
These answers are at the right length for a fresher interview and are easy to remember. Since you've already practiced these tools in your projects, try to relate your answers to your own hands-on experience whenever possible.

# 1. What is Kubernetes?
>Kubernetes is an open-source container orchestration platform used to deploy, manage, scale, and monitor containerized applications automatically. It helps ensure high availability, self-healing, and load balancing of applications.

# 2. What is a Kubernetes Cluster?
>A Kubernetes cluster is a group of machines (nodes) that work together to run containerized applications. It consists of one or more Master Nodes and one or more Worker Nodes.

# 3. What is a Master Node?
>The Master Node manages the entire Kubernetes cluster. It schedules workloads, maintains the desired state, and controls the Worker Nodes. It does not usually run application workloads.
*Main Components:*
>API Server
>Scheduler
>Controller Manager
>etcd

# 4. What is a Worker Node?
>A Worker Node is the machine where application containers run. It receives instructions from the Master Node and executes them.

>Main Components:
>kubelet
>kube-proxy
>Container Runtime (containerd)

# 5. What is a Pod?
>A Pod is the smallest deployable unit in Kubernetes. It contains one or more containers that share the same network and storage.
>Example:
>If you deploy an Nginx application in Kubernetes, it runs inside a Pod.

# 6. What is kubeadm?
>kubeadm is a tool used to create and configure a Kubernetes cluster. It initializes the Master Node and generates the command to join Worker Nodes.

>Example Command:

>kubeadm init
# 7. What is kubectl?

Answer:

>kubectl is the command-line tool used to interact with a Kubernetes cluster. It allows us to create, view, update, and delete Kubernetes resources.

>Example Commands:

>kubectl get nodes
>kubectl get pods
>kubectl apply -f deployment.yaml
# 8. What is kubelet?

Answer:

>kubelet is an agent that runs on every Worker Node. It communicates with the API Server and ensures that the required Pods are running properly.

# 9. What is containerd?

Answer:

>containerd is a container runtime that creates and runs containers. Kubernetes uses it through the Container Runtime Interface (CRI) to manage containers.

>Interview Point:

>Earlier Kubernetes supported Docker through Docker Shim, but now containerd is commonly used.

# 10. What is CNI?

Answer:

>CNI (Container Network Interface) provides networking between Pods and Nodes in a Kubernetes cluster. It assigns IP addresses and enables Pod-to-Pod communication.

>Popular CNI Plugins:

>Calico
>Weave Net
.Flannel
# ⭐ Bonus Interview Question
>What is the difference between kubeadm, kubectl, and kubelet?
>Tool	Purpose
>kubeadm	Creates and sets up the Kubernetes cluster>
>kubectl	CLI tool used to manage the Kubernetes cluster.
>kubelet	Agent running on each Worker Node that ensures Pods are running correctly.