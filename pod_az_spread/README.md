Example of pod spread across AZ.
podAntiAffinity for pod AZ spread, topologySpreadConstraints for node AZ spread, karpenter for node provisioning.

# get nodes
kubectl get nodes -l pool=test-app

# get node and AZ
kubectl describe nodes -l pool=test-app | grep -P 'Name:|topology.kubernetes.io/zone='
