# Hyperbolic-GPU

# How to Generate SSH Keys for Accessing a Rented GPU
## Step 1: Open a Terminal
###  Windows Users: Open Git Bash, PowerShell, or WSL.
### macOS/Linux Users: Open the Terminal.

## Step 2: Generate the SSH Key Pair
### Type the following command and press Enter:
```bash
ssh-keygen
```
## Step 3: Choose a Save Location
### You will see a prompt like this:
```bash
Enter file in which to save the key (/home/yourusername/.ssh/id_rsa):
Press Enter to accept the default location (~/.ssh/id_rsa).
```
## Step 4: Set a Passphrase (Optional but Recommended)
### You will see this prompt:
```bash
Enter passphrase (empty for no passphrase):
You have two options:

To use a passphrase: Type a secure passphrase and press Enter, then confirm it.

To skip: Just press Enter twice.
```

## Step 5: Confirm Key Generation
### Once the process completes, you'll see output like:
```bash
Your identification has been saved in /home/yourusername/.ssh/id_rsa
Your public key has been saved in /home/yourusername/.ssh/id_rsa.pub
The key fingerprint is:
SHA256:abcd1234example yourusername@yourdevice
```
## Step 6: Locate Your Public Key
### To display your public key, run:

```bash
cat ~/.ssh/id_rsa.pub
```
or
```bash
Get-Content ~/.ssh/id_rsa.pub   # For PowerShell users
```
## Step 7: Upload Your Public Key

### Visit [Hyperbolic Setting Dashboard](https://app.hyperbolic.xyz/settings)

Copy the contents of id_rsa.pub.

Go to Settings > Public Key on your platform.

Paste the key into the designated field and save.

Create a new Public SSH key and paste your pubkey into it and save it!

✅ You’re now ready to use SSH to access your rented GPU! 🚀


## Step 8: Rent a GPU
* Choose a GPU (.eg RTX 4090) [here](https://app.hyperbolic.xyz/compute) and click on `Rent`
* Make sure you select `1` as `GPU Count`
* Select `pytorch` as `Template`
* Rent it

## Step 9: Copy the GPU SSH command
After your server is `Ready to Connect`, just click on `SSH` button as image below to copy the command

* It must copy a command like this:
```bash
ssh ubuntu@xxxxxx.hyperbolic.xyz -p 312452
```

## Connect to GPU server
* Paste the command you copied in `PowerShell` to access your server.
* Enter the password you set for SSH public key and press enter to open your GPU terminal


