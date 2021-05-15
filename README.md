# wordpress-minikube
To deploy wordpress on minikube K8

#Requirements:
1. Minikube
2. Kubectl
3. Text Editor (eg: VS Code)

# Create a folder
On terminal run below to create a folder

$mkdir <name of your folder>

Navigate to the folder:

$ cd <name of your folder>

# Create Kubernetes Secret

On terminal run the code below to create a base63 represtation of your password:

$ echo -n 'yourPassword' | base64

Copy the output. 

#Create a file secrets.yml and it will carry the base64 representation of your password.

Execute below command to create the secret

 $ kubectl apply  -f secrets.yml

 You can see the secret created from dashboard by running;

 $ minikube dashboard

 # Deployments

Clone the two files in the repo:
 1. wordpress-deployment.yaml
 2. mysql-deployment.yaml

 Run the below command to create the mysql deployment and other K8 resources:

 $ kubectl apply -f mysql-deployment.yaml

 and the below to create wordpress deployment and other K8 resources:

$ kubectl apply -f wordpress-deployment.yaml

# Author;
Noah Makau.





