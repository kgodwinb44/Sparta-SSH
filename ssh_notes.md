# SSH - Secure Shell

## It is protocol
## Port 22
## Used to securely connect to a shell for a specific server

### Shell - Like terminals closest thing to the OS, just a command centre

## How it works
### When we create a SSH Key Pair
- we create a Private key (needs to be kept secure, confidential)
- we create a Public key
- uses encryption

![](/images/ssh_keypair.PNG)

## Where to store private keys
- There is a hidden folder
- . folders are hidden .ssh
- Generate key pair:
- ssh-keygen -t rsa -b 4096 -C "lfairbrass@spartaglobal.com"
- ssh-keygen generate key
- -t rsa type of gen
- -b how long in bits
- -C just to add some personalisatiopn on the end of the key
- kyle-github-keypair (private)  kyle-github-keypair.pub (public padlock)
- Okay to add contects of public key to github
- $ cat kyle-github-keypair.pub
- Copy and paste key into ssh key on github
- Check to see if key pair working
- Use eval to store private key for the session
- eval 'ssh-agent -s'
- Start an agent

- Set the environment variables

- Be ready to use ssh-add right after

- echo Agent pid 1948;
- ADD ssh-add nameky
- TEST ssh -T git@github.com
## Use SSH key pair to make a push