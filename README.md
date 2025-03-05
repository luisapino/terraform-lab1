# Terraform AKS
## Luisa Fernanda Castaño Pino
## Plataformas 2

First everything was set up so that I could use my azure account.

![Captura de pantalla 2025-03-03 203016](https://github.com/user-attachments/assets/b009ba4b-642c-4c7e-9316-441235fa8187)

with the ID it gave me I can somehow set my account and be able to use it, also I created a folder where I will leave everything from terraform

![image](https://github.com/user-attachments/assets/3ff30104-ebfe-4804-9e16-8d6371267438)

Then the main.tf was modified so that a resource group called "labs_plataformas_rg" could be created, and an aks called lfcp-aks1, a node group, identity, labels, etc.

![image](https://github.com/user-attachments/assets/55f05d0b-d2bd-45fe-bb5f-e1aed59fe516)
![image](https://github.com/user-attachments/assets/83021287-b83c-4dad-8213-a40e3e99015e)

It was necessary to make the subscription_id with the ID that I threw in the first capture, also after giving terraform init and it was successful, I gave terraform fmt, then terraform plan and added 2 with some sensitive outputs to connect to it.

![image](https://github.com/user-attachments/assets/07dffab0-9f16-41b6-aff3-e5482b699724)

![image](https://github.com/user-attachments/assets/1b34832b-1737-4107-8512-066fa54d2c64)

I also changed context, looking for the rg then the aks lfcp-aks1, I verified that it was in the context that was to start creating
![image](https://github.com/user-attachments/assets/d4d3ea4b-8f91-40a2-876c-de5315d6cb23)

In that context I was able to use kubectl, and use it to get the context

![image](https://github.com/user-attachments/assets/c92d984d-3770-408c-a50c-f2bd7e43e851)

and I changed the context so that I could create a pod there:

![image](https://github.com/user-attachments/assets/a4dac221-916c-47ab-a4a3-6b77cffa2c79)

I create a pod called pod-lab1

![image](https://github.com/user-attachments/assets/395a0771-eda4-4df3-8632-cbff3dc792d1)

I expose it to be able to access it from the Internet, and I use the ip address it gives me and I can indeed connect and see the nginx screen.

![image](https://github.com/user-attachments/assets/5ca661cb-465f-40dd-9aed-9047ba52b0ff)

![image](https://github.com/user-attachments/assets/4d7014fe-18f7-4143-91b9-a6402af3cd33)

And now also from the azure portal to see what was created with the terraform, such as the resource groups and within this the aks.

![image](https://github.com/user-attachments/assets/684d6aaa-8bd5-48a1-bd8b-00274f6aa92b)

More detailed information such as subscription id, rg, location etc:

![image](https://github.com/user-attachments/assets/6ed481be-ceaa-42a2-9f00-69fe9a0136d6)

Then aks details, inside this you can see more information such as the running status, the subscription ID, the node pool, etc.

![image](https://github.com/user-attachments/assets/ce2ffcf2-6522-4994-8a66-9c5093ad6e5c)

Then, to use lens which is like a display mode to be able to use it in Windows, two steps were necessary, like WSL do not automatically expose ports to Windows , so kubectl proxy was used to expose port 8001 to the network so I could use the lens on my windows and see the ifnformation from the pods and the YAML helped define the Kubernetes Service that Lens needed to read.

![image](https://github.com/user-attachments/assets/3a0a3254-f90f-43fc-a9cf-762e416a940b)
![image](https://github.com/user-attachments/assets/a8f72b48-c7cd-4b2d-9519-5ff28a79dd4c)

And this is the visualization, like for example I can see my pod-lab1, and see its status like when it was running at that time, the creation date, the usage, etc.

![image](https://github.com/user-attachments/assets/58b87dce-4e85-4107-b970-344bd34b1c98)

The pod was also destroyed at the end and that's it.
![image](https://github.com/user-attachments/assets/c417a1a6-b487-4b0c-81bf-ff92e359966a)

And that's all, thanks for watching :)))
