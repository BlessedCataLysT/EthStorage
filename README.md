# EthStorage
EthStorage V1 Trusted Ceremoney Setup

<img width="1000" height="560" alt="image" src="https://github.com/user-attachments/assets/b92b4730-e19d-47ba-9098-3e260833e5b1" />

## Requirements for Participation

### 1. Operating System
A Linux or macOS system, or Windows Subsystem for Linux 2 (WSL2) if you are on Windows.

### 2. GitHub Account
Your GitHub account must be active and meet the following criteria:

+ Your account must be at least a month old.
+ Your account must have at least one public repository.
+ Your account must follow at least 5 GitHub accounts and have at least 1 follower.
+ You must allow the ceremony tools to read and write GitHub Gists on your account.

### 3. Internet Connection
A stable and reliable internet connection is required. The most common cause of failure is a timeout due to slow or unstable uploads. To avoid this, ensure you have a good upload bandwidth while participating in the ceremony.

Tips:
+ Use VPS if you can't keep your PC & internet open 24/7 till you contribute
+ Use PC if you can.
---
## 1. For MacOS, run Brew commands first
   
i. 
```
xcode-select —install
```
ii.
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
iii.
```
brew update && brew upgrade
```
- Check brew is installed correctly or not, run  ```brew -version```  If it returns the version name it is correctly installed.
  
iv. Installing dependencies
```
brew install curl screen iptables git wget lz4 jq nano automake autoconf tmux htop leveldb pkg-config openssl@3 ncdu unzip
```
---
## 1. For Windows, intall WSL

* Install Windows Subsystem for Linux (WSL) if haven't already, use this guide to install Linux on Windows: https://github.com/BlessedCataLysT/WSL/blob/main/intall-wsl.md
---

Install Dependecies (WSL/Linux)

Packages:
```
sudo apt-get update && sudo apt-get upgrade -y
```
```
sudo apt install curl screen iptables build-essential git wget lz4 jq make gcc nano automake autoconf tmux htop nvme-cli libgbm1 pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev ca-certificates  -y
```
---

## Common Steps after installing Dependencies for MacOS, Linux, WSL

### 2. Install NVM 
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
source .bashrc
```

### 3. Install Node.js 18 
```
nvm install 18 
nvm use 18
```
```
source ~/.bashrc
```

### 4. Install Ceremony

Step 1. Create a directory in your home folder to run the ceremony from:
```
mkdir ~/trusted-setup-tmp && cd ~/trusted-setup-tmp
```
Step 2: Install CLI:
```
npm install -g @p0tion/phase2cli
```
Step 3: Authenticate with GitHub:

To contribute to the ceremony, you’ll need a legit GitHub account as per requirements mentioned above.
Run this command in your terminal:
```
phase2cli auth
```

+ This will prompt you to open a browser and visit https://github.com/login/device
+ Copy the provided auth code in terminal and paste in the auth page . Click "Authorize ethstorage" to continue.


### 5. Contribute Ceremony

* Open a screen (For VPS only)

Open a screen so the ceremony keeps going in the background, it might take hours before it’s your turn.

Screen is useful for VPS only, not WSL or MacOS. If you close the terminal in WSL, your screen session is killed
```
screen -S ceremony
```

#### Contribute to the ceremony (ALL)
```
phase2cli contribute -c ethstorage-v1-trusted-setup-ceremony
```

You can either hit enter for randomly, or pick manually and type any letter or number yourself.

## Screen commands

Minimize screen: Ctrl+A+D
Return to screen: ```screen -r ceremony```

## Notes:

+ Contributing may take some time, depending on the current queue of contributors.
+ If your connection is interrupted or an error occurs, simply re-run the same command — it will pick up from where it left off.

After completing your contribution, you will be invited to share a message on X or your preferred social platform! 🎉


## Cleanup & Logout

After completing your contribution to the ceremony, it’s recommended to clean up your local files and revoke GitHub authorization for security:
```
phase2cli clean
phase2cli logout
```
Delete the ceremony folder too if you don’t need it:
```
rm -rf ~/trusted-setup-tmp
```
ALL DONE!
