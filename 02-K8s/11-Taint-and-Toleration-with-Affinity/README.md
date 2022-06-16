```
 641  cd 11-Taint-and-Toleration-with-Affinity/
  642  ls
  643  kubectl  get nodes --show-labels
  644  kubectl label node worker1 env-
  645  kubectl label node worker2 env-
  646  ls
  647  cp -rf ../05-Deployments/helloworld.yaml .
  648  ls
  649  mv helloworld.yaml 01-helloworld.yaml
  650  ls
  651  cat 01-helloworld.yaml
  652  kubectl  apply -f 01-helloworld.yaml
  653  ls
  654  cp -rf ../10-Affinity/01-helloworld.yaml 02-helloworld-with-affinity.yaml
  655  ls
  656  kubectl  delete -f 01-helloworld.yaml
  657  ls
  658  vim 02-helloworld-with-affinity.yaml
  659  kubectl  apply -f 02-helloworld-with-affinity.yaml
  660  kubectl label node worker2 env=prod
  661  kubectl label node worker1 env=prod
  662  kubectl  delete  -f 02-helloworld-with-affinity.yaml
  663  kubectl  apply -f 02-helloworld-with-affinity.yaml
  664  kubectl apply -f 01-helloworld.yaml
  665  kubectl  delete  -f 02-helloworld-with-affinity.yaml
  666  kubectl  delete  -f 01-helloworld.yaml
  667  ls
  668  cp -rf 02-helloworld-with-affinity.yaml 03-helloworld-with-affinity-tolerations.yaml
  669  ls
  670  vim 03-helloworld-with-affinity-tolerations.yaml
  671  ls
  672  kubectl taint nodes worker2 app=myapp:NoSchedule
  673  ls
  674  kubectl  apply -f 01-helloworld.yaml
  675  kubectl label node worker1 env-
  676  kubectl  apply -f 02-helloworld-with-affinity.yaml
  677  kubectl  apply -f 03-helloworld-with-affinity-tolerations.yaml
  678  ls
  679  cd ..
  680  ls
  681  kubectl  delete -f 11-Taint-and-Toleration-with-Affinity/
```
