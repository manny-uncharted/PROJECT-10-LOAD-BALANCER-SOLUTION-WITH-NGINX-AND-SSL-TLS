# LOAD BALANCER SOLUTION WITH NGINX AND SSL/TLS

## Table of Contents
- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Configure Nginx as a Load Balancer](#configure-nginx-as-a-load-balancer)


## Introduction
By now you have learned what Load Balancing is used for and have configured an LB solution using Apache, but a DevOps engineer must be a versatile professional and know different alternative solutions for the same problem. That is why in this project we will configure an Nginx Load Balancer solution.

It is also extremely important to ensure that connections to your Web solutions are secure and information is encrypted in transit – we will also cover connection over secured HTTP (HTTPS protocol), its purpose and what is required to implement it.

When data is moving between a client (browser) and a Web Server over the Internet – it passes through multiple network devices and, if the data is not encrypted, it can be relatively easily intercepted by someone who has access to the intermediate equipment. This kind of information security threat is called Man-In-The-Middle (MIMT) attack.

This threat is real – users that share sensitive information (bank details, social media access credentials, etc.) via non-secured channels, risk their data being compromised and used by cybercriminals.

SSL and its newer version, TSL – is a security technology that protects the connection from MITM attacks by creating an encrypted session between the browser and Web server. Here we will refer to this family of cryptographic protocols as SSL/TLS – even though SSL was replaced by TLS, the term is still being widely used.

SSL/TLS uses digital certificates to identify and validate a Website. A browser reads the certificate issued by a Certificate Authority (CA) to make sure that the website is registered in the CA so it can be trusted to establish a secured connection.

There are different types of SSL/TLS certificates – you can learn more about them here. You can also watch a tutorial on how SSL works here or an additional resource here

In this project you will register your website with LetsEnrcypt Certificate Authority, to automate certificate issuance you will use a shell client recommended by LetsEncrypt – cetrbot.


## Prerequisites
This project consists of two parts:
- Infrastructure: AWS.
- Webserver Linux: Red Hat Enterprise Linux 8.
- Database Server: Ubuntu 20.04 + MySQL.
- Storage Server: Red Hat Enterprise Linux 8 + NFS Server.
- Load Balancer: Ubuntu 20.04.
- Programming Language: PHP.
- Configure Nginx as a Load Balancer
- Register a new domain name and configure a secured connection using SSL/TLS certificates.
- Your target architecture will look like this:
![Target Infrastructure](https://darey.io/wp-content/uploads/2021/07/nginx_lb.png)


## Configure Nginx as a Load Balancer
Here we can decide to create a fresh installation of Linux for Nginx or use the same Linux server that we used for Apache. In this project, we will create a fresh installation of Linux for Nginx.


- Create an EC2 VM based on Ubuntu 20.04 and name it Nginx LB and also open a TCP port 80 for HTTP connections, also open port 443 for HTTPS connections.

Results:
![Nginx LB]()