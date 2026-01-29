# Manifests do Testapp

Manifests Kubernetes simples para a aplicacao **testapp**.

## Arquivos

- `configmap.yaml`: Variaveis de ambiente (PORT, NODE_ENV)
- `deployment.yaml`: Deployment do testapp
- `pod.yaml`: Pod standalone do testapp
- `service.yaml`: Service para expor o app no cluster

## Como aplicar

```bash
kubectl apply -f testapp-manifests
```

## Observacoes

- A imagem usada e `localhost:30000/testapp:latest`. Ajuste conforme o registry em uso.
