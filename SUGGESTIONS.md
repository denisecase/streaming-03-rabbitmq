# SUGGESTIONS.md

> Helpful tips and recommendations for working effectively with RabbitMQ.

## 1. If Windows, Install Using Chocolatey

The [official RabbitMQ instructions for installing on Windows](https://www.rabbitmq.com/docs/install-windows) recommend installing RabbitMQ using Chocolately, a popular Windows package manager.
We recommend following their advice. 

## 2. Follow Installation Instructions Closely

Read through all instructions and watch the instructional videos carefully.
Follow the steps closely, and check multiple sources as installations vary.

## 3. Verify Activation of Required Modules

RabbitMQ offers a range of plugins or modules that extend its functionality beyond its core features.
These modules provide capabilities such as message routing, authentication, monitoring, and integration with other systems.
Activating the necessary modules is crucial to ensure that your RabbitMQ instance has the functionality required for your project.
For example, the AMQP Protocol Support module is essential (and usually included by default) and neeeded to ensure proper communication and message exchange within the RabbitMQ ecosystem.

### How to Activate Modules

1. **Access RabbitMQ Management Interface**: Open your web browser and navigate to the RabbitMQ Management Interface, typically available at `http://localhost:15672/` if RabbitMQ is installed on your local machine. Log in with your credentials if prompted.

2. **Navigate to Plugins Section**: Once logged in, go to the "Admin" tab or section in the RabbitMQ Management Interface. Then, click on the "Plugins" tab within the Admin section.

3. **View Available Plugins**: In the Plugins section, you'll see a list of available plugins along with their status (enabled or disabled).

4. **Enable Required Modules**: Locate the modules that you need for your project. If a module is currently disabled, click on the "Enable" button next to its name to activate it. This action enables the module and makes its functionality available.

5. **Restart RabbitMQ**: After enabling the required modules, it's recommended to restart RabbitMQ to ensure that the changes take effect. You can usually restart RabbitMQ through the RabbitMQ service manager or command line interface, depending on your operating system.

6. **Verify Activation**: Once RabbitMQ has restarted, return to the RabbitMQ Management Interface and confirm that the required modules are now enabled. You should see them listed in the Plugins section with a status of "enabled".

---

Have any suggestions to add? We invite your contributions. Just fork the repo into a new clean repo, add your suggestion, and submit a pull request. 
