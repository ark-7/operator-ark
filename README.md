# operator-ark

Kubernetes operator for arkLB

Operator-Ark is a Kubernetes operator designed to manage the deployment and configuration of Project Ark using Helm charts. This operator simplifies the process of deploying and managing Project Ark on Kubernetes clusters.

## How to run the operator?

Here are the following steps to run the operator in your kubernetes cluster

1. Install necessary dependencies: make, operator-sdk, helm
2. Run the following command
```bash
make install run
```
3. Then run the following command in other terminal
```bash
make deploy
```

After some time, the operator is deployed in your cluster
4. To check if the operator is deployed and works properly, run the kubectl command
```bash
kubectl apply -f config/samples/charts_v1alpha1_arklb.yaml
```

You'd see that two pods would be deployed together in the cluster

### How to stop?

Run the following commands

```bash
kubectl delete -f config/samples/charts_v1alpha1_arklb.yaml
make undeploy
```
