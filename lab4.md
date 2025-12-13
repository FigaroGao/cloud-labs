Lab 4:

Install docker Desktop:

Mac OS: brew install --cask docker
To install brew, please download brew.pkg here: www.futurelei.com/assets/Homebrew.pkg

Windows: 
Open terminal, and run: wsl --install
Download Docker Desktop and install it.
You have to register it before use.

Install gitea using docker on your computer.

https://about.gitea.com/ 	
https://docs.gitea.com/installation/install-with-docker

a. Does it support LFS? prove it.
b. Create a repo with a large file (1G+)
c. Create a repo for this module and commit your work to this repo.
d. [optional] Backup all data to an external harddrive/USB stick and restore it from another computer.


Install Gitea without docker, feel free to choose the database.

Please take the screenshot of your major steps and submit a lab report.

Lab Report

1. Install Docker

Wsl:  
<img width="616" height="198" alt="image" src="https://github.com/user-attachments/assets/d866fbf2-828b-469e-84d6-4a0447bc2588" />

Docker:  
<img width="1897" height="1079" alt="image" src="https://github.com/user-attachments/assets/9aac54cd-2ab9-494e-9c07-0cb1336ad8fa" />

2. Setting up WSL + Docker environment

PowerShell:  
<img width="867" height="648" alt="image" src="https://github.com/user-attachments/assets/ec646358-72a2-4d78-bc1f-a45ab3dc200e" />

Ubuntu:  
<img width="1002" height="107" alt="image" src="https://github.com/user-attachments/assets/28cfc3ed-4849-4461-8b84-27eac6bd51cb" />

3. Install Gitea Using Docker

Create a persistent data volume and run the Gitea container：  
<img width="998" height="506" alt="image" src="https://github.com/user-attachments/assets/82c42682-7be0-46f5-a47f-fc8db0ac8f57" />

4. Configure Gitea

General Settings：  
<img width="1453" height="601" alt="image" src="https://github.com/user-attachments/assets/3a58fbc2-0d1a-469d-bb10-f07f5741bc4b" />

Support LFS：  
<img width="1344" height="549" alt="image" src="https://github.com/user-attachments/assets/dd386360-2672-4171-9382-9ef7cf6bd3d2" />

Gitea Base URL：  
<img width="1533" height="972" alt="image" src="https://github.com/user-attachments/assets/7822cee2-4f3c-467e-b4f4-e01e24909585" />

Creating an administrator account：  
<img width="1431" height="737" alt="image" src="https://github.com/user-attachments/assets/de911a51-5b61-4110-99c5-9defbe48e057" />

5. Gitea

<img width="2519" height="696" alt="image" src="https://github.com/user-attachments/assets/f2946143-1b1b-4525-ad0a-374cadfddbe8" />
