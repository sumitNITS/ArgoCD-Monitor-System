## ArgoCD-Monitor-System

Argo CD deployment configuration for Monitor System Application

### Follow the below steps to get started with this application

- Setup Argo CD by following the below commands
```bash
kubectl create namespace argocd
```
```bash
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```
```bash
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 --decode && echo
```
```bash
kubectl port-forward svc/argocd-server -n argocd 8080:443
```

- Run the below command to get started with the Application
```bash
git clone https://github.com/sumitNITS/ArgoCD-Monitor-System.git
```
```bash
cd ArgoCD-Monitor-System
```
```bash
kubectl apply -f argocd-app-config.yml
```
```bash
kubectl port-forward service/monitorsystem-svc <port>:5000 -n monitor-system
```

Now access the application using "localhost":"port" OR "ip-of-machine":"port" 🚀

### Success Outputs

![Kubectl result](https://github.com/sumitNITS/ArgoCD-Monitor-System/assets/37767537/a4119f6c-4acf-4370-890a-a12d536a7ec4)
![argocd result](https://github.com/sumitNITS/ArgoCD-Monitor-System/assets/37767537/5f0113fe-b722-42ef-80ae-4e54574890a6)

