#### Deploy react app in ec2 server

- Launch an ec2 server.
- Install the dependencies to run the react app.
- Create a react app and deploy it in the server.
- Read about the file structure and use of each file in react.

---

#### First step: Create an EC2 server

  - Firstly, log in to the AWS management console.
  - After login, navigate to the search bar, type EC2, and select EC2
  - Now, the EC2 dashboard will appear. Click Instances
  - Click the Launch instances button.
  - To launch an EC2 instance, a few details are required, i.e., instance name, OS image (AMI), instance type, etc.
  - Select a key pair to attach with the instance to log in with that key.
  - Take the public IP from the EC2 dashboard and use it to login inside the instance using ssh.
  - Finally, it will be logged in successfully if everything is configured correctly.

---

#### Step-3: On 2nd server, install the dependencies to run the react app

First, we need to install nodejs. npm comes with nodejs bundled. To install nodejs, use below commands:

  ```sh
  curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
  sudo apt-get install -y nodejs
  ```

To check nodejs is successfully installed or not use 

```sh
node -v
```

Also, npm is already installed. Use check version of npm

```sh
npm -v
```
- Now Create a react project 

To install the base project, run the following command:(In my case project name react_deployment)

```sh
npx create-react-app react_deployment
```

This command will kick off a build process that will download the base code along with a number of dependencies.

To run any npm script, you just need to type

```sh
npm run build
``` 

![project output](https://user-images.githubusercontent.com/106643382/200764079-9ddfc1f0-171f-474f-99e1-0bdf1b2b9b31.png "project output")

![built output](https://user-images.githubusercontent.com/106643382/200764340-102f100f-3ec5-446a-acb1-2167642c192f.png "built output")
















