# Simple Configuration

```console
az k8sconfiguration create \
        --resource-group AzureArc \
        --cluster-name ${CLUSTER_NAME} \
        --name simple-config \
        --operator-scope namespace \
        --operator-namespace simple-config \
        --operator-instance-name simple-config \
        --operator-params '--git-path simple --git-readonly --registry-disable-scanning --sync-garbage-collection' \
        --enable-helm-operator false \
        --repository-url git://github.com/slack/gitops-tests.git
```

```console
az k8sconfiguration delete
        --resource-group AzureArc \
        --cluster-name ${CLUSTER_NAME} \
        --name simple-config
```
