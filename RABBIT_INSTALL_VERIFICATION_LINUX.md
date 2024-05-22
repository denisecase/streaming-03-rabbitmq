# RABBIT_INSTALL_VERIFICATION_LINUX.md

> RabbitMQ Installation Verification for Linux

To verify that RabbitMQ is installed on your Linux system, follow these steps:

## Check the Service Status

Open a terminal and run:

```bash
sudo systemctl status rabbitmq-server
```

If RabbitMQ is installed, this command will show the status of the RabbitMQ server.

## Check the RabbitMQ Version

You can also check the RabbitMQ version to confirm installation:

```bash
rabbitmqctl status
```

This should display the RabbitMQ status information, including the version number.

## Verify RabbitMQ is in your Environment Path

Ensure that RabbitMQ is in your system's PATH. Open a terminal and run:

```bash
which rabbitmqctl
```

If the command returns the path to rabbitmqctl, then RabbitMQ is installed and available in your path. 
When a program is available in your path, you can just type the program name without the fully qualified path to where it resides on your machine. 

