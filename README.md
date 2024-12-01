# CSRF-Demo-Security-Lab
Authors: <br />
[Michał Chmiel](https://github.com/Spren3) <br />
[Mateusz Sznurawa](https://github.com/mateusznu) <br />
[Dawid Gruszecki](https://github.com/Dawid0508) <br />

Repository created in the purpose of getting familiar with OWASP CSRF attacks, [vulnerabilities](https://owasp.org/www-community/attacks/csrf) and [prevention.](https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html)

As a part of a project, we changed our [app](github.com/Spren3/FileStorageSite) to show its vulnerablities to Cross-site Request Forgeries attacks.
Check details in our directory [tasks](https://github.com/Dawid0508/CSRF-Demo-Security-Lab/tree/main/tasks), where you can find tasks to perform CSRF attacks by your own, also get to know how to protect an app! <br/>
Instruction is in polish in [tasks.md](https://github.com/Dawid0508/CSRF-Demo-Security-Lab/blob/main/tasks/tasks.md)

### Instruction
Preparation of environment is very simple, first you have to install [Docker](https://docs.docker.com/engine/install/). <br/>
Then type the command in the terminal `git clone https://github.com/Dawid0508/CSRF-Demo-Security-Lab` <br/>
Navigate to the main folder and create a docker image. To do this, use the command: `docker build -t CSRF` <br/>
To start the container with the built image, use the following command: `docker run -d -p 5000:5000 CSRF` <br/>
In web browser search `http://localhost:5000`.
>You can use docker ps command to check the status of containers and its ID. <br/> If you want to suspend, type `docker stop <container_id>` to stop the selected container.

