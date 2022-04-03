# HELM

https://artifacthub.io/packages/search?kind=0

Gestão de pacotes para o Kubernetes.

```bash
helm list
helm repo add
helm search repo
helm install
helm upgrade
helm rollback
helm create
helm status
```

## Chart

É um conjunto de templates

## Values

Configurar o chart, com dados específicos.

## Templates

Usa os values para criar o yaml final.

No final usa os values nos templates para gerar o yaml final.

## Releases

É uma instalação dos templates.

Como instalar uma release:

```bash
# install new release
helm install web ./helm-rotten-potatoes

# upgrade existing release
helm upgrade web ./helm-rotten-potatoes

# upgrade with different values or using set
helm install web ./helm-rotten-potatoes --values values.yaml
# OR
# --set tem precedencia sobre o value.yaml
helm install web ./helm-rotten-potatoes --set web.servie.type=LoadBalancer

# check release history
helm history web

# rollback to previous or specific release
helm rollback web
```
