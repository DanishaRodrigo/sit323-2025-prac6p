Kubernetes Deployment for Node.js App

11. Build and Push Docker Image
Make sure Docker Desktop is running.
docker build -t danishaa/node-app .
docker push danishaa/node-app


2. Start Minikube
minikube start --driver=docker

Check Minikube status:
minikube status

3. Deploy to Kubernetes
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml

Check resources:
kubectl get pods
kubectl get service

4. Access the Application
Use Minikube to open the service in your browser:
minikube service node-app-service

This will launch your Node.js app in the browser.
