1. What is a Container?

Answer:
A container is an isolated environment where an application runs along with all its dependencies. Multiple containers can run on the same host machine while sharing the same operating system kernel.

2. Why do we use Containers?

Answer:

Application isolation
Faster deployment
Easy portability
Consistent environment
Efficient resource usage
3. What is the difference between a Container and a Virtual Machine?
Container	Virtual Machine
Shares host OS kernel	Has its own operating system
Lightweight	Heavyweight
Starts in seconds	Takes minutes to boot
Uses less memory	Uses more memory
4. What is Isolation in Containers?

Answer:
Isolation means one container cannot directly access another container's processes, files, or network unless explicitly allowed.

5. Which Linux feature provides isolation?

Answer:
Namespaces provide isolation in Linux.

6. What are Linux Namespaces?

Answer:
Namespaces are a Linux kernel feature that creates isolated environments for processes, networking, users, and filesystems.

7. What is a PID Namespace?

Answer:
A PID (Process ID) Namespace isolates processes so that a container can only see and manage its own processes.

8. What is a Network Namespace?

Answer:
A Network Namespace gives each container its own:

IP address
Network interface
Routing table
9. What is a Mount Namespace?

Answer:
A Mount Namespace gives each container its own filesystem view, isolated from the host unless volumes are mounted.

10. What is a User Namespace?

Answer:
A User Namespace allows a container to have its own users and groups, improving security.

11. What are cgroups?

Answer:
cgroups (Control Groups) are a Linux kernel feature used to limit and monitor resource usage like CPU, memory, and disk I/O.

12. What resources can cgroups limit?

Answer:

CPU
RAM (Memory)
Disk I/O
Network (in some configurations)
13. What is the difference between Namespaces and cgroups?
Namespaces	cgroups
Provide isolation	Provide resource limits
Separate processes and resources	Control CPU, memory, disk usage
14. Does Docker create Namespaces manually?

Answer:
No. Docker automatically creates and manages Namespaces and cgroups.

15. What is Docker Engine?

Answer:
Docker Engine is the core component of Docker that creates, runs, and manages containers.

16. Why is Docker easier than using Linux Namespaces directly?

Answer:
Because Docker automatically handles Namespaces, cgroups, networking, storage, and container lifecycle without requiring manual Linux kernel commands.

17. Can multiple containers run on one host?

Answer:
Yes. A single host machine can run many containers simultaneously.

18. Do all containers have separate operating systems?

Answer:
No. Containers share the host operating system kernel.

19. What is the Host Machine?

Answer:
The host machine is the physical or virtual machine on which Docker and containers run.

20. What is the role of the Linux Kernel in Docker?

Answer:
The Linux kernel provides the Namespaces (for isolation) and cgroups (for resource control) that Docker uses to run containers.

⭐ Interview Tip (Very Common Questions)

These are the questions interviewers ask most often for freshers:

What is Docker?
What is a Container?
Difference between Container and Virtual Machine?
What are Namespaces?
What are cgroups?
Difference between Namespaces and cgroups?
What is Docker Engine?
Why do we use Containers?
Can multiple containers run on one host?
How does Docker provide isolation?

If you can answer these 10 questions confidently, you'll have a strong foundation for Docker-related DevOps fresher interviews.