lenovo@worker01:~/lkd/ht/apps_kubehelm_eth/src/app$ sudo helm install lkd-eth  eth
NAME: lkd-eth
LAST DEPLOYED: Sun Dec 26 09:59:48 2021
NAMESPACE: default
STATUS: deployed
REVISION: 1
TEST SUITE: None
NOTES:
1. View the EthStats dashboard at:
  export SERVICE_IP=$(kubectl get svc --namespace default lkd-eth-ethereum-ethstats-service -o jsonpath='{.status.loadBalancer.ingress[0].ip}')
  echo http://$SERVICE_IP

  NOTE: It may take a few minutes for the LoadBalancer IP to be available.
        You can watch the status of by running 'kubectl get svc -w lkd-eth-ethereum-ethstats-service'

2. Connect to Geth transaction nodes (through RPC or WS) at the following IP:
  export POD_NAME=$(kubectl get pods --namespace default -l "app=lkd-eth-ethereum-geth-tx-service,release=lkd-eth" -o jsonpath="{.items[0].metadata.name}")
  kubectl port-forward $POD_NAME 8545:8545 8546:8546
lenovo@worker01:~/lkd/ht/apps_kubehelm_eth/src/app$ 


## JTRACZ-ETH

[sudo] password for lenovo: 
NAME: jtracz-eth
LAST DEPLOYED: Sun Dec 26 10:27:27 2021
NAMESPACE: default
STATUS: deployed
REVISION: 1
TEST SUITE: None
NOTES:
1. View the EthStats dashboard at:
  export SERVICE_IP=$(kubectl get svc --namespace default jtracz-eth-ethereum-ethstats-service -o jsonpath='{.status.loadBalancer.ingress[0].ip}')
  echo http://$SERVICE_IP

  NOTE: It may take a few minutes for the LoadBalancer IP to be available.
        You can watch the status of by running 'kubectl get svc -w jtracz-eth-ethereum-ethstats-service'

2. Connect to Geth transaction nodes (through RPC or WS) at the following IP:
  export POD_NAME=$(kubectl get pods --namespace default -l "app=jtracz-eth-ethereum-geth-tx-service,release=jtracz-eth" -o jsonpath="{.items[0].metadata.name}")
  kubectl port-forward $POD_NAME 8545:8545 8546:8546
lenovo@worker01:~/lkd/ht/apps_kubehelm_eth/src/app$ 
