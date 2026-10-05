# Kind (Kubernetes in Docker) Installation Guide for Windows

This guide covers how to quickly spin up a local Kubernetes cluster on Windows and linux using **Kind** for development, testing, or demonstration purposes.

---

##  Prerequisites

Before installing Kind, ensure your system meets the following requirements:
* **Docker Desktop:** Installed, running, and configured with the **WSL 2 backend**.
* **Terminal:** PowerShell or Command Prompt opened with **Administrator privileges**.

---

##  Installation Methods (For Windows)

Choose **one** of the two methods below to install Kind on your Windows machine.

### Method 1: Using Release Binaries (PowerShell)

This method manually downloads the execution binary and configures your system environment path.

1. **Open PowerShell as an Administrator** and download the latest Windows binary using `curl.exe`:
   ```powershell
   curl.exe -Lo kind-windows-amd64.exe https://kind.sigs.k8s.io/dl/latest/kind-windows-amd64
   ```

2. **Create a dedicated folder** and move the downloaded binary into it while renaming it to `kind.exe`:
   ```powershell
   New-Item -ItemType Directory -Path "C:\Program Files\kind" -Force
   Move-Item .\kind-windows-amd64.exe "C:\Program Files\kind\kind.exe"
   ```

3. **Add Kind to your System PATH** so you can run the command from any terminal window:
   ```powershell
   setx PATH "\$Env:PATH;C:\Program Files\kind" /M
   ```
   *(Note: Restart your terminal after running this command for the changes to take effect).*

### Method 2: Using Chocolatey Package Manager

If you use the Chocolatey package manager, you can install Kind with a single command.

1. **Open an administrative terminal** (PowerShell or Command Prompt).
2. **Run the installation command:**
   ```powershell
   choco install kind
   ```

---

##  Verification & Usage

Once installed, use these steps to verify your terminal can see Kind and deploy your first cluster.

1. **Verify the installation:**
   ```powershell
   kind --version
   ```

2. **Create your first local Kubernetes cluster:**
   ```powershell
   kind create cluster
   ```

3. **Delete the cluster (Optional cleanup):**
   ```powershell
   kind delete cluster
   ```


##  Installation Methods (For Linux)

### 1. Installing KIND and kubectl
Install KIND and kubectl using the provided install_for_linux.sh

### 2. Setting up kind cluster
Create a KIND cluster using the given config file

```
kind create cluster --config kind-config.yaml --name test-kind-cluster
```

Verify the cluster:

```
kubectl get nodes
kubectl cluster-info
```

### 3. Accessing the cluster
Use kubectl to interact with the cluster:
```
kubectl cluster-info
```
