# Ikoch-project - main

Project Flow : 

Using Terraform, A EC2 instance will be created with jenkins installed on it by using scripts 

![image](https://user-images.githubusercontent.com/35003840/206586937-e1c3b8f2-e502-4469-bf87-825bdf564261.png)

![image](https://user-images.githubusercontent.com/35003840/206587014-c792e021-14a4-4bbc-b29b-485aa8c015b3.png)

Using AWS, We will create a ansible server(dummy WebApp) where our application will be executed 

![image](https://user-images.githubusercontent.com/35003840/206587103-eb31e87a-2481-4942-ad16-4d5726623470.png)

Building Jenkins pipeline : 

Stage 1: The Spring boot application code from Github 

Whenever there is any change in your Github repo, a JENKINS job will be created by using `GITHUB WEBHOOKS`

![image](https://user-images.githubusercontent.com/35003840/207897270-c08b9e3c-ff26-4e48-8206-9a4869650be1.png)


Stage 2: Ansible will be installed into dummy server and `code` will be sent to `WebApp server` 

Stage 3: using `Ansible`, Docker will be installed by using `ansible-playbook (inventories)`

Stage 4: Building `Docker image` and Running `container` in the WebApp server 

Below is the pipeline flow : 

![image](https://user-images.githubusercontent.com/35003840/206587817-5c8a4e87-e1e4-478e-b5ca-33bff73385c7.png)

Note : Getting small error while deploying the application and it is due to the java release versions.
Due to limited time, could not troubleshoot more!

Error : Java 11 issues


![image](https://user-images.githubusercontent.com/35003840/206588672-3674af29-116e-4477-8c93-1290ae43d61d.png)

----- EOF --- 



