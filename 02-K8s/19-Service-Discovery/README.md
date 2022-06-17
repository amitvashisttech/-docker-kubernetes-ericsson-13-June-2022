```
  678  cd 02-K8s/
  679  ls
  680  cd 12-Service-Discovery/
  681  ls
  682  cat secrets.yaml
  683  cat database.yaml
  684  ls
  685  cat database-service.yml
  686  ls
  687  kubectl apply -f secrets.yaml
  688  kubectl apply -f database.yaml
  689  kubectl apply -f database-service.yml
  690  ls
  691  cat helloworld-app-deployment.yml
  692  kubectl  get svc
  693  ls
  694  kubectl get pods
  695  kubectl delete -f ../10-Wordpress-Multi-Container-Pod/
  696  ls
  697  kubectl apply -f helloworld-app-deployment.yml
  698  kubectl apply -f helloworld-app-svc.yml
  699  cat helloworld-app-svc.yml
  700  kubectl get pods
  701  cat helloworld-app-deployment.yml
  702  cat helloworld-app-svc.yml
  703  kubectl get pods
  704  kubectl  get svc
  705  curl 172.31.0.101:32621
  706  kubectl  get pods
  707  kubectl exec -it database -- mysql -u root -p
  708  kubectl  get pods
  709  kubectl exec -it helloworld-deployment-7c557cd984-74jpl -- env

```
