# Kubernetes Workshop Repository

Welcome to the Kubernetes Workshop repository for students of IIPS, DAVV. This repository is designed to help learners understand Kubernetes in a structured way, starting from the basics of containers and gradually moving toward real-world deployment concepts.

The main idea of this workshop is to teach students how Kubernetes manages applications using declarative configuration files called manifests. These files describe the desired state of resources such as Pods, Deployments, Services, ConfigMaps, Ingress, and StatefulSets.

---

## Why this repository exists

This workshop is meant to help students:
- understand the role of containers in modern application deployment
- learn how Kubernetes organizes and manages workloads
- understand the purpose of manifest files
- practice common Kubernetes patterns with real examples
- gain hands-on understanding of deployment, networking, storage, and service discovery

---

## Repository structure and purpose

### 1. Docker/
This folder introduces the concept of containerization.

It explains:
- what Docker is
- why containers are useful
- how Docker images and containers work
- how applications are packaged and run in isolated environments
- Docker networking, storage, and Compose

This directory is important because Kubernetes runs containers. Before learning Kubernetes, students must understand how containerized applications are built and managed.

---

### 2. kind-installation/
This folder is for setting up a local Kubernetes cluster using Kind.

It helps students:
- install Kind on their system
- create a local cluster
- prepare a Kubernetes environment for learning and testing without cloud infrastructure

This directory is useful for beginners because it provides a straightforward way to run Kubernetes locally.

---

### 3. kubernetes/
This is the main directory of the workshop and contains multiple Kubernetes examples. Each subfolder focuses on a specific concept.

#### kubernetes/pods/
This folder teaches the most basic Kubernetes object: the Pod.

A Pod is the smallest unit that runs one or more containers. These manifests help students understand:
- how containers run inside Pods
- init containers
- sidecars
- basic pod behavior

These examples are useful for learning the base model of Kubernetes.

---

#### kubernetes/deployments/
This folder is about Deployments.

Deployments are used for running application workloads in a controlled and scalable way. They help students understand:
- how applications are managed over time
- how Kubernetes creates replicas
- how updates can be rolled out safely
- how applications remain available even when instances are replaced

This is one of the most important topics in Kubernetes because real applications are usually deployed using Deployments.

---

#### kubernetes/services/
This folder explains Services, which are used to expose application workloads inside the cluster or to users.

Services help students understand:
- how applications are accessed consistently
- how traffic is routed to one or more Pods
- how service discovery works
- why Pod IP addresses are not stable

This directory shows how Kubernetes keeps networking simple and reliable.

---

#### kubernetes/service-discovery/
This folder demonstrates how different application components communicate with each other using names rather than static IP addresses.

It teaches:
- how microservices find each other
- how Kubernetes DNS works
- the role of Service objects in application communication

This is useful for understanding how applications interact in a Kubernetes environment.

---

#### kubernetes/configmaps/
This folder focuses on configuration management.

ConfigMaps are used to store configuration data separately from the application code. These examples help students learn:
- how to pass environment variables
- how to load configuration files into Pods
- how to separate settings from application logic
- how to keep applications flexible and reusable

This is especially useful for understanding deployment best practices.

---

#### kubernetes/namespaces/
This folder introduces Namespaces.

Namespaces help divide a cluster into logical sections. They are used to:
- separate environments such as dev, test, and production
- organize workloads by team or project
- isolate resources within the same Kubernetes cluster

This folder teaches how cluster resources can be organized cleanly.

---

#### kubernetes/ingress/
This folder covers Ingress, which manages external traffic routing.

Ingress is used for:
- routing HTTP and HTTPS traffic
- exposing services through hostnames or paths
- creating a gateway for multiple applications

Students learn how external users reach services inside the cluster using routing rules.

---

#### kubernetes/api/
This folder contains examples related to Kubernetes API resources and custom resource patterns.

It helps explain:
- how Kubernetes resources are represented
- how the cluster is controlled through API objects
- the declarative nature of Kubernetes configuration

This area is useful for understanding the API-driven design of Kubernetes.

---

#### kubernetes/psa/
This folder introduces Pod Security Admission.

It helps students understand:
- how Kubernetes enforces security policies
- how workloads can be restricted based on safety rules
- why security controls are important in cluster design

This is a beginner-friendly introduction to Kubernetes security enforcement.

---

#### kubernetes/statefulsets/
This folder is for StatefulSets, which are used for stateful applications.

StatefulSets are important for workloads like:
- databases
- distributed systems
- applications that need stable identity and persistent storage

This folder helps students understand:
- how stateful workloads differ from stateless workloads
- stable pod identities
- headless services
- storage integration for stateful apps

---

#### kubernetes/storage/
This folder is about persistent storage in Kubernetes.

It explains:
- why container data is not permanent by default
- how PersistentVolume and PersistentVolumeClaim work
- how storage classes are used
- how databases and other stateful apps keep data safe

This is an essential topic for production-like Kubernetes usage.

---

#### kubernetes/wasm/
This folder introduces a more modern workload model using WebAssembly.

It helps students understand that Kubernetes is not limited to traditional container-based apps and can support different execution models in modern environments.

---

#### kubernetes/web-app/
This folder contains sample web applications that are used to demonstrate different deployment versions and patterns.

It is useful for:
- understanding how an application evolves over time
- comparing versions
- showcasing deployment changes
- understanding how rolling updates and app variants work in practice

This gives students a realistic view of how applications are managed in real environments.

---

## What is a Kubernetes manifest file?

A manifest file is a YAML or JSON file that describes the desired state of a Kubernetes resource.

It tells Kubernetes:
- what kind of object it is
- what the application is called
- where it should run
- how it should be exposed
- which configuration values it needs
- which storage or networking rules apply

In simple terms, the manifest is the instruction file that tells Kubernetes what should exist and how it should behave.

Examples of resources represented by manifests in this repository:
- Pods
- Deployments
- Services
- ConfigMaps
- Secrets
- Ingress
- StatefulSets
- Namespaces
- Storage resources

---

## Learning flow for students

This repository is organized to make learning easier. A good flow is:

1. Learn Docker and container basics
2. Set up a local cluster with Kind
3. Understand Pods
4. Learn Services and networking
5. Learn Deployments for app management
6. Understand ConfigMaps and Secrets
7. Learn Ingress and routing
8. Explore storage and StatefulSets
9. Study security and cluster isolation
10. Review application examples and deployment patterns

This path makes the concepts build on one another naturally.

---

## Final understanding

This repository is designed to teach students that Kubernetes is not just about running software — it is about describing, managing, scaling, and securing application infrastructure in a repeatable and automated way.

Every directory and manifest is there to show a specific part of this system:
- how workloads run
- how they communicate
- how they are configured
- how they are exposed
- how they are stored
- how they are secured

That is the core idea behind this workshop.

---
