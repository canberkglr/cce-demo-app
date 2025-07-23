
# Install kubectl

1. Install <span style="background-color:rgb(96, 96, 96)"> kubectl.exe </span>
```powershell
curl.exe -LO "https://dl.k8s.io/release/v1.32.0/bin/windows/amd64/kubectl.exe"
```

2. Inswtall checksum and validatae
```powershell
curl.exe -LO "https://dl.k8s.io/v1.32.0/bin/windows/amd64/kubectl.exe.sha256"
```
```powershell
 $(Get-FileHash -Algorithm SHA256 .\kubectl.exe).Hash -eq $(Get-Content .\kubectl.exe.sha256)
```

3. Test to ensure the <span style="background-color:rgb(96, 96, 96)">kubectl </span> successfully installed and added to your <span style="background-color:rgb(96, 96, 96)">PATH </span>

```powershell
kubectl version --client
```

```powershell
kubectl version --client --output=yaml
```
# Installation Minikube

1. Download and place minikube exe file using powershell

```powershell
New-Item -Path 'c:\' -Name 'minikube' -ItemType Directory -Force
Invoke-WebRequest -OutFile 'c:\minikube\minikube.exe' -Uri 'https://github.com/kubernetes/minikube/releases/latest/download/minikube-windows-amd64.exe' -UseBasicParsing
```

2. Add the minikube binary to you <span style="background-color:rgb(96, 96, 96)">PATH </span>

```powershell
$oldPath = [Environment]::GetEnvironmentVariable('Path', [EnvironmentVariableTarget]::Machine)
if ($oldPath.Split(';') -inotcontains 'C:\minikube'){
  [Environment]::SetEnvironmentVariable('Path', $('{0};C:\minikube' -f $oldPath), [EnvironmentVariableTarget]::Machine)
}

```

3. Start cluster

```powershell
minikube start
```

4. Install the dashboard with following command 

```powershell
minikube dashboard --url
```
This will enable the dashboard add-on, and open the proxy in the default web browser.
# Installation Helm

with using winget you can install helm chart  easily 

```powershell
winget install Helm.Helm
```
