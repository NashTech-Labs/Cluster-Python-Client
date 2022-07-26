### Install Kubernetes Python Client:

`git clone --recursive https://github.com/kubernetes-client/python.git cd`

`cd python`

`python setup.py install`

### Installation from pip:

`pip install kubernetes`

For Cluster, we use CoreV1Api class from client module.


### Authentication to the Kubernetes Python Client in other cluster is done by: 

`configuration.api_key = {"authorization": "Bearer" + bearer_token}`

We will use here the Bearer Token which enable requests to authenticate using an access key.

In cluster-python-client.py file there is a functions for creating Cluster:


1. Create Cluster

In this we have to pass the namespace in which we will create cluster:
namespace="default"

Give your cluster details:
```
cluster_details={
        "bearer_token":"Your_cluster_bearer_token",
        "api_server_endpoint":"Your_cluster_IP"
    }
```

### Running the File:
```
python3 cluster-python-client.py
```

### Check the Cluster:
```
kubectl get Cluster
```