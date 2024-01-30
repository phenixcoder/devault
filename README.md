# DeVault CLI

Welcome to DeVault CLI, your dependable solution for streamlined management of credentials and secrets in development environments. Built with GoLang, DeVault CLI simplifies the process of securely storing and retrieving sensitive information across different stages of your development workflow.

## Installation

To install DeVault CLI, you can download the binary for your operating system from the [releases page](https://github.com/yourusername/devault-cli/releases) or build it from source.

### Building from Source

1. Clone the DeVault CLI repository:

   ```bash
   git clone https://github.com/yourusername/devault-cli.git
   ```

2. Navigate to the cloned directory:

   ```bash
   cd devault-cli
   ```

3. Build the DeVault CLI binary:

   ```bash
   go build -o devault
   ```

4. Move the binary to your PATH for global access:

   ```bash
   mv devault /usr/local/bin
   ```

Now, you can use DeVault CLI globally on your system.

## Getting Started

### Initialization

To get started with DeVault CLI, initialize your configuration file using the following command:

```bash
devault init
```

This command will guide you through the setup process, allowing you to define your preferred provider and configure access credentials accordingly.

### Configuration

DeVault CLI operates based on a structured configuration file (`devault.json` by default). This file defines the secrets, environments, and provider details necessary for DeVault CLI to function effectively.

An example configuration file might look like this:

```json
{
  "vault": {
    "type": "file",
    "path": "path/to/config/file"
  },
  "environments": [
    "dev",
    "qa",
    "prod"
  ],
  "secrets": {
    "API_KEY": "path/to/secret/in/vault",
    "DB_PASSWORD": "path/to/{ENV}/secret/in/vault"
  }
}
```

### Command Usage

DeVault CLI offers intuitive commands to interact with the tool:

- **Credential Retrieval**:

  To load credentials for a specific environment, use:

  ```bash
  devault [environment]
  ```

  If no environment is specified, it defaults to 'dev' or the first environment defined in the configuration.

## Available Providers

DeVault CLI supports multiple providers for storing and retrieving secrets:

### File

The File provider offers a straightforward solution, storing secrets in an encrypted file.

### AWS Secrets Manager

Utilize AWS Secrets Manager to securely store and manage secrets, seamlessly integrating with AWS SDK.

### HashiCorp Vault

For HashiCorp Vault users, DeVault CLI seamlessly interacts with Vault instances, leveraging configured credentials for secure access.

## Contributing

Contributions to DeVault CLI are welcome! Feel free to submit bug reports, feature requests, or even pull requests to help improve the tool for everyone.

## License

DeVault CLI is licensed under the [MIT License](LICENSE). Feel free to use, modify, and distribute the software according to the terms of the license.

---

Thank you for choosing DeVault CLI to streamline your secret management workflow. Happy coding!
