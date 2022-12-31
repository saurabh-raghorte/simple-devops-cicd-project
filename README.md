# Simple DevOps Project
<p align="center">
  <img src="https://github.com/devopswithprince/simple-devops-cicd-project/blob/image/_readme_images/project-architecture.png?raw=true" alt="Sublime's custom image"/>
</p>

## This DevOps project can be implemented on laptop ***(no cloud account required)*** consist of following technologies-
- IDE - **VScode, Pycharm**, etc (Recommended but not mandatory)
- Source Code Management as **GitHub**
- CICD tool - **Jenkins**
- Containerization tool - **Docker** (Docker Desktop on Windows/ Mac / Linux)
- **Kubernetes** using docker-dekstop
- CICD tool - **Jenkins**
- IDE - **VScode, Pycharm**, etc (Recommended but not mandatory)


## Git installation
Download and install Git on your local machine - https://git-scm.com/downloads.

Enter below command in terminal(Mac/Linux)/command-prompt(Windows) to clone the project repository-
```bat
git clone https://github.com/devopswithprince/simple-devops-cicd-project.git
```

## IDE installation **(Recommended)**
I recommend any IDE or code editor from below to understand scripts, dockerfile, yaml files, etc in more depth-
- VS code - https://code.visualstudio.com/download
- PyCharm(Community edition) - https://www.jetbrains.com/pycharm/download/
- Sublime - https://www.sublimetext.com/3
- Atom - https://atom.en.softonic.com/download

Click file->Open folder and open the cloned repository here

## Install Docker-Desktop
Download docker-desktop as per your local machines platform - https://www.docker.com/products/docker-desktop/

Windows users might face issue while starting docker-desktop, see below steps-
- Restart docker service in services management console(open run-> enter services.msc)
- Refer below links-
    - https://learn.microsoft.com/en-us/windows/wsl/tutorials/wsl-containers
    - https://docs.docker.com/desktop/windows/wsl/

I recommend enabling below highlighted options inorder to run the project successfully-

<p align="center">
  <img src="https://github.com/devopswithprince/simple-devops-cicd-project/blob/image/_readme_images/docker-desktop1.png?raw=true" alt="Sublime's custom image"/>
</p>

- Daemon expose option is available in windows docker-desktop. Mac/Linux users can ignore

<p align="center">
  <img src="https://github.com/devopswithprince/simple-devops-cicd-project/blob/image/_readme_images/docker-desktop2.png?raw=true" alt="Sublime's custom image"/>
</p>

- Click on Apply & restart

## Kubernetes configuration
In above step, if you enable Kubernetes, a single node cluster will automatically get created.

Please check if config file is created in below path-
```bat
Windows-
C:\Users\give_your_user_account\.kube
```
```sh
Mac or Linux-
~./kube/
```
## Jenkins setup
Jenkins can be installed locally on your base machine like any other software or can be used as a container.

In my setup, I have installed on base machine for more feasibility.

Jenkins can be downloaded and installed as shown in below links-

- Windows - https://www.jenkins.io/doc/book/installing/windows/
- Mac - https://www.jenkins.io/doc/book/installing/macos/
- Linux - https://www.jenkins.io/doc/book/installing/linux/
- Through Docker as container - https://www.jenkins.io/doc/book/installing/docker/

After Installation, get Administrator password from below-

```powershell
Windows
Get-Content 'C:\Program Files\Jenkins\secrets\initialAdminPassword'
```

```sh
Mac/Linux
cat /var/jenkins_home/secrets/initialAdminPassword
```

```sh
Docker
docker ps

CONTAINER ID   IMAGE                     COMMAND                  CREATED          STATUS          PORTS                                              NAMES
12027cbeebc7   jenkins/jenkins:2.375.1   "/usr/bin/tini -- /u…"   7 seconds ago    Up 6 seconds    0.0.0.0:8080->8080/tcp, 0.0.0.0:50000->50000/tcp   myjenkins

#Take your container id, as shown above and replace with your container id in below command-

docker exec -it 12027cbeebc7 sh -c "cat /var/jenkins_home/secrets/initialAdminPassword"
```
## Application Deployment-
[1. Docker-Compose](#docker-compose)

### Docker-Compose












[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Dillinger is a cloud-enabled, mobile-ready, offline-storage compatible,
AngularJS-powered HTML5 Markdown editor.

- Type some Markdown on the left
- See HTML in the right
- ✨Magic ✨

## Features

- Import a HTML file and watch it magically convert to Markdown
- Drag and drop images (requires your Dropbox account be linked)
- Import and save files from GitHub, Dropbox, Google Drive and One Drive
- Drag and drop markdown and HTML files into Dillinger
- Export documents as Markdown, HTML and PDF

Markdown is a lightweight markup language based on the formatting conventions
that people naturally use in email.
As [John Gruber] writes on the [Markdown site][df1]

> The overriding design goal for Markdown's
> formatting syntax is to make it as readable
> as possible. The idea is that a
> Markdown-formatted document should be
> publishable as-is, as plain text, without
> looking like it's been marked up with tags
> or formatting instructions.

This text you see here is *actually- written in Markdown! To get a feel
for Markdown's syntax, type some text into the left window and
watch the results in the right.

## Tech

Dillinger uses a number of open source projects to work properly:

- [AngularJS] - HTML enhanced for web apps!
- [Ace Editor] - awesome web-based text editor
- [markdown-it] - Markdown parser done right. Fast and easy to extend.
- [Twitter Bootstrap] - great UI boilerplate for modern web apps
- [node.js] - evented I/O for the backend
- [Express] - fast node.js network app framework [@tjholowaychuk]
- [Gulp] - the streaming build system
- [Breakdance](https://breakdance.github.io/breakdance/) - HTML
to Markdown converter
- [jQuery] - duh

And of course Dillinger itself is open source with a [public repository][dill]
 on GitHub.

## Installation

Dillinger requires [Node.js](https://nodejs.org/) v10+ to run.

Install the dependencies and devDependencies and start the server.

```python
cd dillinger
npm i
node app
```

For production environments...

```sh
npm install --production
NODE_ENV=production node app
```

## Plugins

Dillinger is currently extended with the following plugins.
Instructions on how to use them in your own application are linked below.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |

## Development

Want to contribute? Great!

Dillinger uses Gulp + Webpack for fast developing.
Make a change in your file and instantaneously see your updates!

Open your favorite Terminal and run these commands.

First Tab:

```sh
node app
```

Second Tab:

```sh
gulp watch
```

(optional) Third:

```sh
karma test 
```

#### Building for source

For production release:

```sh
gulp build --prod
```

Generating pre-built zip archives for distribution:

```sh
gulp build dist --prod
```

## Docker

Dillinger is very easy to install and deploy in a Docker container.

By default, the Docker will expose port 8080, so change this within the
Dockerfile if necessary. When ready, simply use the Dockerfile to
build the image.

```sh
cd dillinger
docker build -t <youruser>/dillinger:${package.json.version} .
```

This will create the dillinger image and pull in the necessary dependencies.
Be sure to swap out `${package.json.version}` with the actual
version of Dillinger.

Once done, run the Docker image and map the port to whatever you wish on
your host. In this example, we simply map port 8000 of the host to
port 8080 of the Docker (or whatever port was exposed in the Dockerfile):

```sh
docker run -d -p 8000:8080 --restart=always --cap-add=SYS_ADMIN --name=dillinger <youruser>/dillinger:${package.json.version}
```

> Note: `--capt-add=SYS-ADMIN` is required for PDF rendering.

Verify the deployment by navigating to your server address in
your preferred browser.

```sh
127.0.0.1:8000
```

## License

MIT

**Free Software, Hell Yeah!**

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [dill]: <https://github.com/joemccann/dillinger>
   [git]: <https://git-scm.com/downloads>
   [git-repo-url]: <https://github.com/joemccann/dillinger.git>
   [john gruber]: <http://daringfireball.net>
   [df1]: <http://daringfireball.net/projects/markdown/>
   [markdown-it]: <https://github.com/markdown-it/markdown-it>
   [Ace Editor]: <http://ace.ajax.org>
   [node.js]: <http://nodejs.org>
   [Twitter Bootstrap]: <http://twitter.github.com/bootstrap/>
   [jQuery]: <http://jquery.com>
   [@tjholowaychuk]: <http://twitter.com/tjholowaychuk>
   [express]: <http://expressjs.com>
   [AngularJS]: <http://angularjs.org>
   [Gulp]: <http://gulpjs.com>

   [PlDb]: <https://github.com/joemccann/dillinger/tree/master/plugins/dropbox/README.md>
   [PlGh]: <https://github.com/joemccann/dillinger/tree/master/plugins/github/README.md>
   [PlGd]: <https://github.com/joemccann/dillinger/tree/master/plugins/googledrive/README.md>
   [PlOd]: <https://github.com/joemccann/dillinger/tree/master/plugins/onedrive/README.md>
   [PlMe]: <https://github.com/joemccann/dillinger/tree/master/plugins/medium/README.md>
   [PlGa]: <https://github.com/RahulHP/dillinger/blob/master/plugins/googleanalytics/README.md>
[def]: #section-3
