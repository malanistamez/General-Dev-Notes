# Github Configurations

1. Check if Git is already installed by running the following command:
    ```
    git --version
    ```
   - If Git is not installed, you will be prompted to install the Xcode Command Line Tools. Follow the prompts to install it.
   - After installation, verify that Git is now installed by running `git --version` again.

2. **Configure Git**: Before using Git, you should configure it with your name and email address. Replace `Your Name` and `youremail@example.com` with your actual name and email.
    ```
    git config --global user.name "Your Name"
    git config --global user.email youremail@example.com
    ```

3. **Generate SSH Key (optional but recommended for secure access)**: SSH keys provide a secure way to authenticate with GitHub. If you want to use SSH, you can generate a new SSH key pair:
   - Check for existing SSH keys:
     ```
     ls -al ~/.ssh
     ```
   - Generate a new SSH key:
     ```
     ssh-keygen -t ed25519 -C "youremail@example.com"
     ```
   - Follow the prompts to create the SSH key. By default, the key pair will be stored in `~/.ssh/id_ed25519` for the private key and `~/.ssh/id_ed25519.pub` for the public key.
   - Add your SSH key to the SSH agent:
     ```
     eval "$(ssh-agent -s)"
     ssh-add ~/.ssh/id_ed25519
     ```
   - Copy your SSH public key to your clipboard:
     ```
     pbcopy < ~/.ssh/id_ed25519.pub
     ```

