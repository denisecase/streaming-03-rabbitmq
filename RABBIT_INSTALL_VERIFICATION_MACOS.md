# RABBIT_INSTALL_VERIFICATION_MACOS.md

> RabbitMQ Installation Verification for macOS

To verify that RabbitMQ is installed on your macOS system, follow these steps.

## Check the Service Status

Open a terminal and run:

```zsh
brew services list
```

If RabbitMQ is installed via Homebrew, it should appear in the list of services with its status.

## Check the RabbitMQ Version

Run the following command in the terminal:

```zsh
rabbitmqctl status
```

This will show the status information and confirm the version of RabbitMQ.

## Verify RabbitMQ is in your Environment Path

Ensure that RabbitMQ is in your system's PATH. Open a terminal and run:

```zsh
which rabbitmqctl
```

If the command returns the path to rabbitmqctl, then RabbitMQ is installed and available in your path. 
When a program is available in your path,
you can just type the program name without the fully qualified path to where it resides on your machine.
