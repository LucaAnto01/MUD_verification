# SettiUp Homebrew and Installing Tamarin Prover

```bash
ulimit -S -n 4096 #Set the maximum number of open file descriptors --> prevent errors during tamarin installation
sudo apt install curl

#Install Homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

#Update the .bashrc file
echo >> /home/luca/.bashrc
echo 'eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"' >> /home/luca/.bashrc
eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"

#Install essential build tools
sudo apt-get install build-essential

#Install GCC using Homebrew
brew install gcc

#Install Tamarin Prover
brew install tamarin-prover/tap/tamarin-prover