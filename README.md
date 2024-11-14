# Kubernetes
First of all create a ec2 instance in ubuntu in t2 medium 

and connect to the server

change user to the root user by the cmd sudo su -

Update the server by the command apt update -y

# install minikube by the belown commands

         sudo curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
         
         sudo mv minikube-linux-amd64 /usr/local/bin/minikube
         
         sudo chmod +x /usr/local/bin/minikube
         
         sudo minikube version

# install kubectl by the belown commands

           sudo curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
           
           sudo curl -LO "https://dl.k8s.io/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl.sha256"
           
           sudo echo "$(cat kubectl.sha256) kubectl" | sha256sum --check 
           
           sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
           
           sudo kubectl version --client
           
           sudo kubectl version --client --output=yaml
           
           sudo minikube start --driver=docker --force

# POD CREATION:
          	Two ways to create the pod :
                   •Imperative method
                   •Declarative method
                   
    # Imperative method:
    
              kubectl run pod-1 --image=nginx
               pod-1 : name of pod
              nginx : name of image
              Kubectl get pods – to see the created pods
              
      # Declarative method:
                   create the yaml file by the command vi file-name.yml Write the script in the yml editor
![Screenshot 2024-11-14 193004](https://github.com/user-attachments/assets/29ce70b7-2dfe-4b35-8818-0fe0f3f6eb96)
![Screenshot 2024-11-14 191742](https://github.com/user-attachments/assets/460d3074-6870-42cb-b42a-a52678085c7f)
