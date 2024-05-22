# RABBIT_INSTALL_VERIFICATION_WINDOWS.md

> RabbitMQ Installation Verification for Windows

To verify that RabbitMQ is installed on your Windows system, follow these steps.

## Check the Services

Open the Services application (you can search for "services" in the Start menu) and look for the "RabbitMQ" service. If RabbitMQ is installed, it should appear in the list of services.

## Check the RabbitMQ Version

Open a PowerShell terminal (or an older Command Prompt terminal) and run:

```shell
rabbitmqctl status
```

This command should provide information about the RabbitMQ installation, including the version.

## Verify RabbitMQ is in your Environment Path

Ensure that RabbitMQ is in your system's PATH. Open a PowerShell terminal (or an older Command Prompt terminal) and run:

```
where rabbitmqctl
```

If the command returns the path to rabbitmqctl, then RabbitMQ is installed and available in your path. 
When a program is available in your path,
you can just type the program name without the fully qualified path to where it resides on your machine.
