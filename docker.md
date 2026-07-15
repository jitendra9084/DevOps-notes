# Docker notes

## 1. What is a Container?

Answer:
A container is an isolated environment where an application runs along with all its dependencies. Multiple containers can run on the same host machine while sharing the same operating system kernel.

## 2. Why do we use Containers?

Answer:

Application isolation
Faster deployment
Easy portability
Consistent environment
Efficient resource usage
## 3. What is the difference between a Container and a Virtual Machine?
Container	Virtual Machine
Shares host OS kernel	Has its own operating system
Lightweight	Heavyweight
Starts in seconds	Takes minutes to boot
Uses less memory	Uses more memory
## 4. What is Isolation in Containers?

Answer:
Isolation means one container cannot directly access another container's processes, files, or network unless explicitly allowed.

## 5. Which Linux feature provides isolation?

Answer:
Namespaces provide isolation in Linux.

## 6. What are Linux Namespaces?

Answer:
Namespaces are a Linux kernel feature that creates isolated environments for processes, networking, users, and filesystems.

## 7. What is a PID Namespace?

Answer:
A PID (Process ID) Namespace isolates processes so that a container can only see and manage its own processes.

## 8. What is a Network Namespace?

Answer:
A Network Namespace gives each container its own:

IP address
Network interface
Routing table
## 9. What is a Mount Namespace?

Answer:
A Mount Namespace gives each container its own filesystem view, isolated from the host unless volumes are mounted.

## 10. What is a User Namespace?

Answer:
A User Namespace allows a container to have its own users and groups, improving security.

## 11. What are cgroups?

Answer:
cgroups (Control Groups) are a Linux kernel feature used to limit and monitor resource usage like CPU, memory, and disk I/O.

## 12. What resources can cgroups limit?

Answer:

CPU
RAM (Memory)
Disk I/O
Network (in some configurations)
## 13. What is the difference between Namespaces and cgroups?
Namespaces	cgroups
Provide isolation	Provide resource limits
Separate processes and resources	Control CPU, memory, disk usage
## 14. Does Docker create Namespaces manually?

Answer:
No. Docker automatically creates and manages Namespaces and cgroups.

## 15. What is Docker Engine?

Answer:
Docker Engine is the core component of Docker that creates, runs, and manages containers.

## 16. Why is Docker easier than using Linux Namespaces directly?

Answer:
Because Docker automatically handles Namespaces, cgroups, networking, storage, and container lifecycle without requiring manual Linux kernel commands.

## 17. Can multiple containers run on one host?

Answer:
Yes. A single host machine can run many containers simultaneously.

## 18. Do all containers have separate operating systems?

Answer:
No. Containers share the host operating system kernel.

## 19. What is the Host Machine?

Answer:
The host machine is the physical or virtual machine on which Docker and containers run.

## 20. What is the role of the Linux Kernel in Docker?

Answer:
The Linux kernel provides the Namespaces (for isolation) and cgroups (for resource control) that Docker uses to run containers.

# DevOps Fresher Interview Questions

## 1. What is a Dockerfile?

Answer:
A Dockerfile is a text file containing instructions to build a Docker image.

## 2. What is the difference between an Image and a Container?

Answer:

Image: A read-only template.
Container: A running instance of an image.
## 3. What is Attached Mode?

Answer:
In attached mode, the container runs in the foreground, and logs are displayed directly in the terminal.

## 4. What is Detached Mode?

Answer:
Detached mode runs the container in the background using the -d option, allowing the terminal to remain free.

## 5. What is Interactive Mode?

Answer:
Interactive mode (-it) opens a shell inside the container so you can execute commands interactively.

## 6. What is docker exec?

Answer:
docker exec is used to execute commands inside an already running container.

## 7. What is the purpose of the FROM instruction?

Answer:
It specifies the base image for the Docker image.

## 8. What is the purpose of the RUN instruction?

Answer:
It executes commands during the image build process.

## 9. What is the purpose of the CMD instruction?

Answer:
It specifies the default command that runs when a container starts.

## 10. What is the purpose of the COPY instruction?

Answer:
It copies files and directories from the local machine into the Docker image.

## 11. What is the purpose of the ADD instruction?

Answer:
It copies files into the image and can also download files from URLs or automatically extract compressed archives.

## 12. What is the difference between COPY and ADD?
COPY	ADD
Copies local files only	Copies local files, supports URLs, and extracts archives
Simpler and preferred	More powerful but used only when needed
## 13. What is the purpose of the EXPOSE instruction?

Answer:
It documents the port on which the application inside the container listens.

## 14. How do you build a Docker image?

Answer:

docker image build -t myimage:1.0 .
## 15. What does the -t option do in docker build?

Answer:
It assigns a name (tag) and optional version to the Docker image.
1. Tell me about yourself

2. 
Answer:
"Good morning, sir/madam. My name is Jitendra Singh. I have recently completed my B.Tech in Computer Science and Engineering. I have hands-on experience with Linux, Git, Docker, AWS, Terraform, Jenkins, GitHub Actions, and Nginx through practical projects. I am looking for an opportunity to start my career as a DevOps Engineer, where I can learn, grow, and contribute to the organization."
3. What is DevOps?
Answer:
"DevOps is a combination of Development and Operations. It helps automate software development, testing, and deployment, enabling faster and more reliable software delivery."
4. What is CI/CD?
Answer:
"CI (Continuous Integration) automatically builds and tests code whenever changes are made. CD (Continuous Delivery/Deployment) automates the release of applications, making deployments faster and more reliable."
5. Explain your GitHub Actions project.
Answer:
"I created a GitHub Actions workflow that automatically builds my project whenever code is pushed to GitHub. This removes manual work and ensures the project builds successfully every time."
6. Difference between Docker Image and Container.
Answer:
"A Docker image is a blueprint that contains the application and its dependencies. A Docker container is the running instance of that image."
7. Explain your Dockerfile.
Answer:
"My Dockerfile uses a base image, copies the application into the image, exposes the required port, and defines the command to start the application."
8. Difference between COPY and ADD.
Answer:
"COPY only copies files and folders into the Docker image. ADD can also extract local archive files and download files from URLs, but COPY is preferred in most cases."
9. What is a Docker Volume?
Answer:
"A Docker volume stores data outside the container. It keeps the data safe even if the container is removed."
10. What happens when you run docker build -t app .?
Answer:
"Docker reads the Dockerfile, executes each instruction, creates a Docker image, and tags it with the name 'app'."
11. Explain your AWS project.
Answer:
"I launched an EC2 instance, connected using SSH, installed Docker and Nginx, deployed my application, and configured Security Groups to allow access."
12. Difference between Security Group and NACL.
Answer:
"Security Groups work at the instance level and are stateful. NACLs work at the subnet level, are stateless, and support both allow and deny rules."
13. What is Terraform?
Answer:
"Terraform is an Infrastructure as Code (IaC) tool. It allows us to create and manage cloud resources using code instead of manual configuration."
14. Nginx service is not working. What will you do?
Answer:
"I will check the service status, review the logs, verify the configuration, and make sure the required port is not already in use. Then I will restart the service if needed."
15. Networking Basics
DNS:
"DNS converts a domain name into an IP address."
HTTP vs HTTPS:
"HTTP transfers data without encryption, while HTTPS encrypts data using SSL/TLS for secure communication."
SSH:
"SSH is a secure protocol used to connect to remote Linux servers."
TCP vs UDP:
"TCP is reliable and guarantees data delivery. UDP is faster but does not guarantee delivery."
16. Why should we hire you?
Answer:
"I have a strong foundation in DevOps tools and practical project experience. I am a quick learner, hardworking, and eager to contribute while continuously improving my skills."
17. Do you have any questions for us?
Answer:
"Yes, thank you. What technologies does your DevOps team use? What kind of training or learning opportunities are available for freshers? And what will be my responsibilities in the first few months?"
⭐ Bonus: If the interviewer asks, "Introduce your projects"
Answer:
"I have completed projects on Docker, GitHub Actions, AWS, Terraform, and Nginx. My projects include deploying a Spring Boot application with Docker, hosting a React application on Nginx, creating a CI/CD pipeline using GitHub Actions, and provisioning AWS infrastructure using Terraform."
These answers are at the right length for a fresher interview and are easy to remember. Since you've already practiced these tools in your projects, try to relate your answers to your own hands-on experience whenever possible.
