```
 1665  cd 23-Affinity/
 1666  ls
 1667  cat helloworld.yaml
 1668  ls
 1669  kubectl  apply -f helloworld.yaml
 1670  kubectl  get pods
 1671  kubectl  describe pod helloworld-deployment-b64578fb-fk294
 1672  ls
 1673  kubectl  get nodes
 1674  kubectl  label node worker1 env=prod
 1675  kubectl  get pods
 1676  kubectl  get pods -o wide
 1677  kubectl  label node worker2 env=dev
 1678  kubectl get nodes --show-labels
 1679  kubectl  get pods -o wide
 1680  kubectl scale --replicas=5 deploy helloworld-deployment
 1681  kubectl  get pods -o wide
 1682  kubectl scale --replicas=1 deploy helloworld-deployment
 1683  kubectl  get pods -o wide
 1684  ls
 1685  sdiff helloworld.yaml helloworld-dev-prod.yaml
 1686  kubectl  delete -f helloworld.yaml
 1687  ls
 1688  kubectl  get deploy
 1689  kubectl  apply -f helloworld-dev-prod.yaml
 1690  kubectl  get pods -o wide
 1691  ls
 1692  vim helloworld-multi-affinity.yaml
 1693  ls
 1694  kubectl  delete -f helloworld-dev-prod.yaml
 1695  ls
 1696  kubectl get nodes --show-labels
 1697  vim helloworld-multi-affinity.yaml
 1698  ls
 1699  kubectl  apply -f helloworld-multi-affinity.yaml
 1700  kubectl get pods
 1701  kubectl get pods -o wide
 1702  kubectl delete  -f helloworld-multi-affinity.yaml
 1703  kubectl get nodes --show-labels
 1704  kubectl label node worker1 env-
 1705  kubectl label node worker1 env=dev
 1706  kubectl get nodes --show-labels
 1707  kubectl  apply -f helloworld-multi-affinity.yaml
 1708  kubectl  get pods -o wide
 1709  kubectl delete  -f helloworld-multi-affinity.yaml
 1710  ls
 1711  cat helloworld-multi-affinity.yaml
 1712  kubectl label node worker1 team=engineering-project1
 1713  kubectl  apply -f helloworld-multi-affinity.yaml
 1714  kubectl  get pods -o wide
 1715  kubectl scale --replicas=10 deploy helloworld-deployment
 1716  kubectl  get pods -o wide
 1717  kubectl scale --replicas=20 deploy helloworld-deployment
 1718  kubectl  get pods -o wide
 1719  kubectl scale --replicas=2 deploy helloworld-deployment
 1720  kubectl  get pods -o wide
```
