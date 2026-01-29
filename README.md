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
- Para fazer `docker push` pelo host, exponha o NodePort via k3d:
  ```bash
  k3d cluster edit <nome-do-cluster> --port-add 5001:30000@loadbalancer
  ```
  Depois use `localhost:5001` para push.
- O manifesto do registry local fica em `cluster-manifests/registry.yaml`.
