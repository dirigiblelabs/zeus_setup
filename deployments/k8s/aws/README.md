# Kubernetes & AWS
Here are described the steps of how to deploy the [Zeus](https://github.com/dirigiblelabs/zeus) Cloud Management Suite in Kubernetes Cluster running on AWS.

## Prerequisites
- AWS credentials
- Kubernetes Cluster up and running on AWS
- Configured Kubernetes CLI

## Deploy
Run the following command to deploy the Zeus in the Kubernetes Cluster.

`kubectl create -f https://raw.githubusercontent.com/dirigiblelabs/zeus_setup/master/deployments/k8s/aws/zeus.yml`

#### The following resources will be created:
- [Namespace](https://kubernetes.io/docs/resources-reference/v1.6/#namespace-v1-core) - *zeus*
- [StatefulSet](https://kubernetes.io/docs/resources-reference/v1.6/#statefulset-v1beta1-apps) - *zeus* 
- [Service](https://kubernetes.io/docs/resources-reference/v1.6/#service-v1-core) - *zeus*
- [Ingress](https://kubernetes.io/docs/resources-reference/v1.6/#ingress-v1beta1-extensions) - *zeus*
- [ServiceAccount](https://kubernetes.io/docs/resources-reference/v1.6/#serviceaccount-v1-core) - *zeus*
- [ClusterRole](https://kubernetes.io/docs/resources-reference/v1.6/#clusterrole-v1beta1-rbac) - *zeus*
- [ClusterRoleBinding](https://kubernetes.io/docs/resources-reference/v1.6/#clusterrolebinding-v1beta1-rbac) - *zeus*
  - _**Note:** currently the ingress is configured to work with the proprietary ***.sap.onvms.com** DNS_

## Access
Run the following command to retrieve the access point of the Zes in the Kubernetes Cluster.

`kubectl get ingress -n zeus`

## Undeploy
Run the following command to undeploy the Zeus and the created resources from the Kubernetes Cluster.

`kubectl delete -f https://raw.githubusercontent.com/dirigiblelabs/zeus_setup/master/deployments/k8s/aws/zeus.yml`

