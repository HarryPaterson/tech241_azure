<h1 style="text-align: center;">Azure</h1>

### Contents
* Cloud overview

* Setting up a virtual machine


### Cloud overview
Azure is a cloud computing platform provided by Microsoft.
It offers a wide range of services and solutions for building, deploying, and managing applications and services through Microsoft-managed data centers.
Azure provides Infrastructure as a Service (IaaS), Platform as a Service (PaaS), and Software as a Service (SaaS) offerings.
With Azure, you can create virtual machines, storage accounts, and networks to build your infrastructure.
Azure offers a variety of services such as virtual machines, databases, web apps, AI services, IoT, and more, enabling developers to leverage different technologies and frameworks.

#### Advantages of Using the Cloud:

Scalability and Flexibility: The cloud offers the ability to scale resources up or down quickly based on demand, allowing organizations to efficiently manage fluctuating workloads.
Cost Efficiency: Cloud services follow a pay-as-you-go model, enabling organizations to reduce capital expenditures on hardware and infrastructure. They only pay for the resources they consume.
High Availability and Reliability: Cloud providers typically offer robust infrastructure with redundancy and failover mechanisms, ensuring high availability and minimizing downtime.
Global Accessibility: Cloud services can be accessed from anywhere with an internet connection, allowing remote work and facilitating collaboration across geographically dispersed teams.
Automatic Updates and Patch Management: Cloud providers handle system updates and security patches, alleviating the burden of maintenance and ensuring systems are up-to-date.
Data Backup and Disaster Recovery: Cloud services often include built-in data backup and disaster recovery mechanisms, providing data redundancy and minimizing the risk of data loss.
Elasticity: The cloud allows organizations to quickly scale resources up or down as needed, accommodating changing business requirements and ensuring optimal performance.
Innovation and Advanced Technologies: Cloud providers offer a wide range of services, including AI, machine learning, big data analytics, and IoT, enabling organizations to leverage advanced technologies without heavy upfront investments.

#### Disadvantages of Using the Cloud:

Dependency on Internet Connectivity: Cloud services require a stable and reliable internet connection. Downtime or network disruptions can hinder access to critical applications and data.
Data Security and Privacy Concerns: Organizations need to carefully consider data security and privacy when moving sensitive or confidential data to the cloud. They must ensure proper security measures and compliance with regulations.
Limited Control over Infrastructure: With the cloud, organizations rely on the cloud provider for infrastructure management, limiting their control over hardware, software, and network configurations.
Potential Vendor Lock-In: Switching cloud providers or migrating applications and data between providers can be complex and may result in vendor lock-in, making it challenging to transition to alternative solutions.
Cost Management and Ongoing Expenses: While cloud services offer cost efficiency, ongoing usage and potential overprovisioning can lead to unexpected expenses if not closely monitored and managed.
Disadvantages of Hybrid Cloud or Multi-Cloud:

Complexity: Managing and integrating multiple cloud environments or a combination of cloud and on-premises infrastructure can introduce complexity, requiring specialized expertise and additional resources.
Data and Application Portability: Ensuring seamless data and application portability across multiple cloud environments or on-premises infrastructure can be challenging, leading to potential compatibility issues.
Increased Management Overhead: Managing different cloud platforms or a hybrid environment may require additional effort in terms of monitoring, governance, security, and compliance.


#### On-Premises vs. Cloud: Cost Considerations:
Determining cost effectiveness between on-premises and the cloud depends on various factors:

Initial Investment: On-premises typically involves higher upfront costs for hardware, software licenses, and infrastructure setup.
Maintenance and Upgrades: On-premises requires ongoing maintenance, upgrade expenses, and potential hardware refresh cycles.
Scaling and Resource Usage: Cloud offers flexibility in scaling resources as needed, allowing cost optimization by paying for what is used.
Staffing and Expertise: On-premises requires skilled IT staff for infrastructure management, while cloud offloads certain responsibilities to the provider.
Long-Term Growth and Changes: Cloud can be more cost-effective for organizations experiencing rapid growth, as it provides scalability without significant upfront investment.

#### Determining the Best Cloud Provider:
The choice of the best cloud provider depends on specific organizational needs, requirements, and preferences. Different providers offer varying strengths and capabilities, and the decision should consider factors such as:

Service Offerings: Assess whether the provider offers the required services and features aligned with your organization's needs.
Scalability and Performance: Consider the provider's ability to scale resources, handle peak workloads, and deliver consistent performance.
Reliability and Availability: Evaluate the provider's service-level agreements (SLAs) and track record in terms of uptime and reliability.
Security and Compliance: Examine the provider's security practices, certifications, and compliance with industry standards relevant to your organization.
Pricing and Cost Structure: Compare pricing models, consider cost management tools, and evaluate the provider's transparency regarding pricing.
Support and Customer Service: Consider the quality and responsiveness of the provider's support and customer service.
Integration and Interoperability: Assess how well the provider's services integrate with your existing systems and whether they support interoperability with other platforms.
### Setting up a virtual machine


#### Example
```
User@DESKTOP-SF0773P MINGW64 ~/.ssh
$ pwd
/c/Users/User/.ssh

User@DESKTOP-SF0773P MINGW64 ~/.ssh
$ ^C

User@DESKTOP-SF0773P MINGW64 ~/.ssh
$ ssh-keygen -t rsa -b 4096 -C "harry.c.paterson@gmail.com"
Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/User/.ssh/id_rsa): tech241-henry-az-key
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in tech241-henry-az-key
Your public key has been saved in tech241-henry-az-key.pub
The key fingerprint is:
SHA256:DCyVDiGjhwEtIUPUhsxRRvOaNU/Q8Oev2Ue75FCQphQ harry.c.paterson@gmail.com
The key's randomart image is:
+---[RSA 4096]----+
|%*O=.++. E       |
|oOo=+o+.  . .    |
|o.o .*oo o +     |
| .  +.=o+ o .    |
|   o   .So   .   |
|          . ..   |
|           o...  |
|          + +o   |
|         o ..o.  |
+----[SHA256]-----+

User@DESKTOP-SF0773P MINGW64 ~/.ssh
$ cat tech241-henry-az-key.pub
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAACAQCotMAivS8GF3GLj5keZYGH60ep4rZlCFvRCpMpX49VUomEsEAX315YtH0rwa0T2oDZVW/XfEs8R5CMHJJ8p5Xy74+txbl0wG61zCOVE1MO4WV7HoNGd5rlqzgoTqS3Pv8MdS0+5NwxXJFKcvJKYi/qH4nm44oeT7ScbOzIByoVMo2T6y6rEhWBYaKczbphsS+8bvhkr09LSuac1Jp5ua8DRZFdzzsZTGLRiF86OTknyzft23VLrwoFI9MU2RUNU8psArNKdaoTkIksgrKRb2FuPhD/gauXWfY31nkCeWEJ5uwp3np1D2UJsUIYYCMzUrxqyhfkVeAVIZBDRm+q9F/fKIYLlrbeAdP6H0DltDEGm4DcmSNFerfWZyOjGu311aJg50xae58StTHLGPglUPPGAYZI9M6h6LERmxpjF7700Ou53V2zGMlfztzn92KhE6ZXyIfXA8J4/El5pv7nsaJV39KshviOyGhhBpusDcvsfsHVm+6ES+pB6JQKx4Q/iizSAuHYS93OggoHqam6kqjLPVPNqIGshKsrevcbwvdN1LLHPjD5k5bSyZupeM5ezILQMlPZi9etQykfmlDYsXRL7w6TcoyZJC2KyfMP8RsRAGdq0rLcKTl+PU+6uE4AV6ONQCF+sQb0wumdcFY5kIHbHvvowRGxMYkMwb9KwB8HEw== harry.c.paterson@gmail.com

User@DESKTOP-SF0773P MINGW64 ~/.ssh
$ ^C

User@DESKTOP-SF0773P MINGW64 ~/.ssh
$ chmod 400 tech241-henry-az-key

User@DESKTOP-SF0773P MINGW64 ~/.ssh
$ ls -l
total 13
-rw-r--r-- 1 User 197121  862 Jun 16  2022 known_hosts
-rw-r--r-- 1 User 197121  130 Jun 13  2022 known_hosts.old
-r--r--r-- 1 User 197121 3389 Jun 20 15:47 tech241-henry-az-key
-rw-r--r-- 1 User 197121  752 Jun 20 15:47 tech241-henry-az-key.pub

User@DESKTOP-SF0773P MINGW64 ~/.ssh
$ ssh -i ~/.ssh/tech241-henry-az-key adminuser@20.58.16.115
The authenticity of host '20.58.16.115 (20.58.16.115)' can't be established.
ED25519 key fingerprint is SHA256:mYFCu5wTuS65GbiqsjwsFCsocjMHWPP8JOrDzSS4ttA.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '20.58.16.115' (ED25519) to the list of known hosts.
Connection closed by 20.58.16.115 port 22

User@DESKTOP-SF0773P MINGW64 ~/.ssh
$ ssh -i ~/.ssh/tech241-henry-az-key adminuser@20.58.16.115
Welcome to Ubuntu 18.04.6 LTS (GNU/Linux 5.4.0-1108-azure x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

  System information as of Tue Jun 20 15:46:07 UTC 2023

  System load:  0.0               Processes:           100
  Usage of /:   5.6% of 28.89GB   Users logged in:     0
  Memory usage: 26%               IP address for eth0: 10.0.1.9
  Swap usage:   0%

Expanded Security Maintenance for Infrastructure is not enabled.

45 updates can be applied immediately.
32 of these updates are standard security updates.
To see these additional updates run: apt list --upgradable

27 additional security updates can be applied with ESM Infra.
Learn more about enabling ESM Infra service for Ubuntu 18.04 at
https://ubuntu.com/18-04



The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

To run a command as administrator (user "root"), use "sudo <command>".
See "man sudo_root" for details.

adminuser@tech241-henry-man-app:~$ exit
logout
Connection to 20.58.16.115 closed.

```