# Hello-World

Repository preliminare dell'applicazione di esempio "Hello World", sviluppato nella prima fase del progetto di tirocinio confluito nella tesi di laurea triennale *"DevOps: Automazione del deployment su Kubernetes di applicazioni con ArgoCD e ArgoCD Image Updater"* (Università degli Studi di Ferrara, A.A. 2023/2024).

> **Nota:** questa è la versione iniziale del progetto, usata per verificare il corretto funzionamento di Docker, Kubernetes e ArgoCD. Codice applicativo e manifest di configurazione sono qui ancora nello stesso repository. Nella fase successiva del progetto, i due aspetti sono stati separati in due repository dedicati — [HelloWorld2-dev](https://github.com/lorenzoBagossi/HelloWorld2-dev) (configurazione) e [HelloWorld2-cod](https://github.com/lorenzoBagossi/HelloWorld2-cod) (codice) — per rispettare la buona pratica GitOps di separazione tra codice e configurazione.

## Descrizione

Applicazione Flask minimale ("Hello World") completa di Dockerfile e manifest Kubernetes (Deployment + Service), usata per il primo deploy di prova su Minikube e per la prima configurazione di ArgoCD.

## Struttura

```
helloworld/
├── Dockerfile                  # build dell'immagine (Python 3.9-slim-buster + Flask)
├── helloworld.py                # applicazione Flask, espone la rotta "/"
├── requirements.txt             # dipendenze Python
├── helloworld-deployment.yaml   # Deployment Kubernetes
└── helloworld-service.yaml      # Service (NodePort) Kubernetes
```

## Repository successivi (versione finale del progetto)

- [HelloWorld2-dev](https://github.com/lorenzoBagossi/HelloWorld2-dev) — manifest Kubernetes, struttura Kustomize e configurazione ArgoCD/Image Updater
- [HelloWorld2-cod](https://github.com/lorenzoBagossi/HelloWorld2-cod) — codice sorgente e Dockerfile dell'applicazione
