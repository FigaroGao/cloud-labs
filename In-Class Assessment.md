Please answer the following questions and submit it to your git repo with name "In-Class Assessment 1"

(a)	Describe the three primary cloud service models in cloud computing infrastructure as a Service (IaaS), Platform as a Service (PaaS), and Software as a Service (SaaS). Provide specific examples of how each model can be applied in the context of software development.  
Iass: AWS;Azure;VMware  
e.g. IT administrator Network architects  
Pass: Flynn;Cloud Foundry;Heroku  
e.g. Software engineer  
Sass: Gmail;Slack;Office365  
e.g. enduser  
(b)	What is Docker? Describe a scenario where you would use containerization technologies such as Docker in software development. How does containerization contribute to the development and deployment process of software in this scenario?  
Docker is a container platform that packages applications and their dependencies together, ensuring they can run in different environments.
For example, when a development team is working on a web application, they can use Docker to package the environment (Node.js + DB) and run the container directly.  
Pro: consistent environment, fast deployment, and no interference.  
(c) Deploy n8n (n8n.io) with Docker and capture a screenshot of http://127.0.0.1:5678. Please explain the docker command in detail.


<img width="848" height="321" alt="image" src="https://github.com/user-attachments/assets/407d2985-97b0-446e-8434-e4453c00305c" />


<img width="972" height="446" alt="image" src="https://github.com/user-attachments/assets/f367c673-e373-4789-b191-77bb1cf620b4" />\


docker run -it --rm --name n8n -p 5678:5678 -v n8n_data:/home/node/.n8n n8nio/n8n  
This experiment used Docker to launch the official n8n image.  The command `docker run -it --rm --name n8n -p 5678:5678 -v n8n_data:/home/node/.n8n n8nio/n8n` created an interactive container, mapping host port 5678 to container port 5678, allowing access to the n8n web interface via a browser.  Data persistence was ensured through a Docker volume, guaranteeing that workflows and configurations are preserved even after the container is removed.
