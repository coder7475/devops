# SSH (Secure Shell)

## Definition

- A cryptographic network protocol used for secure communication

- Provides secure channel over which user can manage remote server.

- SSH uses public-key cryptography for authentication and encryption, ensuring data privacy and integrity.

- Commonly used by system administrator and developers for remote server access and management.

## Installation

To install SSH Client run the following commands:

```bash
  sudo apt-get update
  sudo apt-get upgrade
  sudo apt-get install openssh-client
```

## How to connect to remote server

Lets say you have server named `testServer` with IPv4 address of `192.168.2.13` and there is a user named `admin`.

To connect with the serve either use name of the ip address:

```bash
  ssh admin@testServer
  # OR
  ssh admin@192.168.2.13
```

## How to copy between local and remote server

To copy files between hosts on network. Use

```bash
  # Syntax
  scp file user@server:/path/to/dest/
  # Example
  scp demo.txt admin@192.168.2.13:/tmp/
```

## Adding a new SSH Key for GitHub account

1. Check for existing SSH keys. Run:

```bash
  ls -al ~/.ssh
```

2. Check the directory listing to see if you already have a public SSH key. By default, the filenames of supported public keys for GitHub are one of the following.

```
id_rsa.pub
id_ecdsa.pub
id_ed25519.pub
```

3. If you don't have a SSH key, generate a new key. Run:

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

This creates a new SSH key, using the provided email as a label. Use enter for any question asked by the terminal.

4. Start the ssh-agent in the background.

```bash
$ eval "$(ssh-agent -s)"
# Output: Agent pid 59566
```

5. Add your SSH private key to ssh-agent. (the one without .pub)

```bash
  ssh-add ~/.ssh/id_ed25519
```

6. Now Find copy your public SSH key. Find by

```bash
  cat ~/.ssh/id_ed25519.pub
```

7. Copy the text. Go to your github account settings > SSH and GPG keys > click new ssh key > paste the copied text > click the add button

Now, you can clone your repository using ssh. :)

### References

- https://systemweakness.com/ssh-server-secure-configuration-in-linux-4cbbc43f0b46

- https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

- https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account?tool=cli

- https://docs.github.com/en/authentication/connecting-to-github-with-ssh/checking-for-existing-ssh-keys
