sudo npm install -g npm

mkdir ~/.npm-global


npm config set prefix ~/.npm-global

export PATH=$PATH:~/.npm-global/bin

source ~/.bashrc  


# Final steps
rm -rf node_modules
rm package-lock.json


npm cache clean --force
npm install -g @angular/cli

## IIIIIII
npm install



npm prefix -g
export PATH="$(npm prefix -g)/bin:$PATH"
source ~/.bashrc  


### ADD THIS
export PATH="$(npm prefix -g)/bin:$PATH"




