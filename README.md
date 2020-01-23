# flask-k8s-app
to deploy flask python notejam app in k8s 
 you need to change the following 
1) insert Databaseurl into notejam-secret-app.yaml 
DATABASE_URL="postgresql://username:password@IP:5432/dbname"
2) you need to change IP Address of nodeport in  notejam-app-service

3) run the following commands
1-  sudo kubectl create -f  postgres--deployment.yaml 
2-  sudo kubectl create -f  postgres-service.yaml
3-  sudo kubectl create -f  notejam-app-secrets.yaml
4-  sudo kubectl create -f  notejam-app.yaml 
5-  sudo kubectl create -f  notejam-app-service.yaml


