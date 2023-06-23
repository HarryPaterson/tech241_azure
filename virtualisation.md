# Virtualisation
### What is virtualisation?
Virtualization is the process of creating a virtual (rather than physical) version of something, such as an operating system, a server, storage device, or network resources. It allows multiple instances of different operating systems or applications to run simultaneously on a single physical machine, known as the host.

### What is a virtual machine?
A virtual machine (VM) is a software emulation of a physical computer system. It behaves like a complete computer, running an operating system and applications. A VM runs on a hypervisor, which is a virtualization software layer installed on the host machine.

### Where can they be run?
Virtual machines can be run on various types of host machines, including:

* Desktop computers or laptops
* Servers (both on-premises and in the cloud)
* Data centers
* Mainframes 
### What determines how many can run?
The number of virtual machines that can run on a host machine simultaneously depends on several factors:

* Physical resources of the host machine, such as CPU, memory, and storage capacity
* Physical resources of the host machine, such as CPU, memory, and storage capacity
* The resource requirements of each virtual machine, including CPU cores, RAM, disk space, and network bandwidth
* The capabilities and limitations of the hypervisor or virtualization software being used
### What does a virtual machine include?
A virtual machine typically includes the following components:

* Virtual hardware, including virtual CPU, memory, disk drives, and network interfaces
* An operating system installed within the VM, just like on a physical machine
* Applications or services running within the VM
### What software is required to orchestrate/run the virtual machines?
To orchestrate and run virtual machines, you need the following software:

* A hypervisor or virtualisation platform, such as VMware vSphere, Microsoft Hyper-V, or KVM (Kernel-based Virtual Machine)
* Virtual machine management tools or an orchestrator, which provides functionalities for creating, configuring, and monitoring virtual machines. Examples include VMware vCenter, Microsoft System Center Virtual Machine Manager, or OpenStack.
### What is the importance of an image when creating a VM?
An image is a template or snapshot of a virtual machine's state at a specific point in time. It captures the operating system, applications, configurations, and data associated with a VM. When creating a virtual machine, an image serves as the foundation or starting point.

The importance of an image in VM creation includes:

* Ensuring consistency: Images provide a standardized and consistent base for creating multiple VM instances with identical configurations.
* Simplifying deployment: Images simplify the process of deploying new virtual machines by pre-configuring the necessary software and settings.
* Enabling scalability: Images facilitate the rapid creation and scaling of VMs, allowing for quick replication and provisioning of resources.