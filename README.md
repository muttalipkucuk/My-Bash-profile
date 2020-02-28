alias gbrd='git branch | grep -v "master" | xargs git branch -D'


 ----- MUTTALIP'S SHORTCUTS -----

# nvm, elasticsearch, password vault
export NVM_DIR=~/.nvm
source $(brew --prefix nvm)/nvm.sh
export PATH="/usr/local/opt/elasticsearch@2.4/bin:$PATH"
export PASSWORD_STORE_DIR=/Users/kucukmp/Documents/GitHub/hob-webshop-platform/password-vault

# The next line updates PATH for the Google Cloud SDK.
if [ -f '/Users/kucukmp/Downloads/google-cloud-sdk/path.zsh.inc' ]; then source '/Users/kucukmp/Downloads/google-cloud-sdk/path.zsh.inc'; fi

# The next line enables shell command completion for gcloud.
if [ -f '/Users/kucukmp/Downloads/google-cloud-sdk/completion.zsh.inc' ]; then source '/Users/kucukmp/Downloads/google-cloud-sdk/completion.zsh.inc'; fi

# Auto-complete kubectl (Kubernetes)
#source <(kubectl completion bash)
#if [ -f $(brew --prefix)/etc/bash_completion ]; then
#. $(brew --prefix)/etc/bash_completion
#fi

#plugins=(git git-flow brew history node npm kubectl)


export JAVA_HOME=/Library/Java/Home
export LC_ALL=en_US
export NODE_ICU_DATA=$NVM_BIN/../lib/node_modules/full-icu

# My aliases
alias repo='cd /Users/kucukmp/Documents/GitHub/hob-webshop-platform'

alias g='git'
alias gbr='git branch'
alias gbrd='git branch | grep -v "master" | xargs git branch -D'
alias gst='git status'
alias gdi='git diff'
alias gco='git checkout'
alias gpl='git pull'
alias gfe='git fetch'
alias ga='git add'
alias gcm='git commit'
alias gps='git push'

alias k='kubectl'
alias kgp='kubectl get pods'
alias kgcm='kubectl get configmaps'
alias kgd='kubectl get deployments'
alias kcgc='kubectl config get-contexts'
alias getHashes='kubectl describe pods | grep "Image:" | sort -u

kd() { kubectl describe "$1" "$2" }
kgy() { kubectl get "$1" "$2" -o yaml }
kcuc() { kubectl config use-context "$1" }

alias rm_target='find . -name target -type d -exec rm -rfv \{\} \;

#port forwarding (Circle CI SSH login)
#gcloud compute --project "hob-build" ssh --zone "europe-west3-b" "hob-jumpbox" -- -N -L 9999:3.86.203.180:64535
#ssh -p 9999 127.0.0.1
#vim /Users/kucukmp/.ssh/known_hosts

alias gac='git commit -a -m'

#git log --since="2020-01-24T00:36:00-07:00" --merges
