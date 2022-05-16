**Lab 10**

**CI Workflow Part 1**

**Searching for workflow**
![image](https://user-images.githubusercontent.com/86587313/168496748-d2e96488-7b34-4efb-bdeb-0c342ddfe783.png)

**Setting up workflow**
![image](https://user-images.githubusercontent.com/86587313/168496813-7f899a61-cd05-4e19-ab8f-d694ac08f093.png)

**Result**
![image](https://user-images.githubusercontent.com/86587313/168496901-7e1e89a3-4345-4347-9212-c79d1a6fd7e8.png)

---------------------------------------------------------------------------------------------------------------------

**CI Workflow Part 2**

1. Ensure that your repository contains the necessary configuration for your Google Kubernetes Engine cluster, including deployment.yml, kustomization.yml, service.yml, etc.

![image](https://user-images.githubusercontent.com/86587313/168497767-b5533593-af8d-45a2-acb8-51a67afadd85.png)

2. Set up secrets in your workspace: GKE_PROJECT with the name of the project and GKE_SA_KEY with the Base64 encoded JSON service account key

GKE_SA_KEY
![image](https://user-images.githubusercontent.com/86587313/168498623-e3f8ecff-9fe1-49e2-9d44-1e5695307038.png)

GKE_PROJECT:
![image](https://user-images.githubusercontent.com/86587313/168498366-3a13f4c9-ee18-4c25-8f78-a5d13621a9e1.png)

![image](https://user-images.githubusercontent.com/86587313/168498775-f9c48fb2-9c64-4c3e-9f9d-4741ab66d4bc.png)


3.Change the values for the GKE_ZONE, GKE_CLUSTER, IMAGE, and DEPLOYMENT_NAME environment variables (see example below).

Changes:
![image](https://user-images.githubusercontent.com/86587313/168499723-9f7d72af-8c93-4bcd-8a62-1681f222832e.png)

Creating service account
![image](https://user-images.githubusercontent.com/86587313/168498539-d588fdbf-92fc-4755-b297-cb644d804070.png)

Adding key 
![image](https://user-images.githubusercontent.com/86587313/168498567-9d4e8d58-fd61-4a76-88be-6eb5b82817fa.png)

4. Trigger a CD Deployment by creating a new GitHub Release

![image](https://user-images.githubusercontent.com/86587313/168501121-504727b1-0302-4f8b-98ad-96429cec00bf.png)
Error: I am able to run through docker but I am facing issues with GCP 

Notes: 
- After uploading deployment, ingress, and service yaml files to GCP, it is not recognizing the files properly. 
- I believe it has something to do with some minor changes I need to make to the yaml files but I am not 100% sure which ones to make
- Also there may have been an error in using gradle commands 
