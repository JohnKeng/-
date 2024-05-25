下載
```
homebrew
chrome
iterm2
VScode
```

-----------------------------------------------------------------------

設定 iTrem2 theme 
```
Setting > Profiles > 匯入 終端機.json > 設為 Default

Setting > Profiles > Terminal > Show mark indicators 關閉
```

設定 zsh oh-my-zsh
```
# 先檢查有沒有安裝
$ cat /etc/shells

# 如果沒有在用下列指令安裝，如果有就跳過
$ brew install zsh 

# 修改預設的 shell 為 zsh
$ chsh -s /bin/zsh


# install oh-my-zsh
$ sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

# 安裝語法高亮
$ brew install zsh-syntax-highlighting
$ source /usr/local/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh

```

修改 ~/.zshrc
```
export ZSH="$HOME/.oh-my-zsh"

# Which plugins would you like to load?
plugins=(git)

# Load oh-my-zsh
source $ZSH/oh-my-zsh.sh

# Load zsh-syntax-highlighting
# source $(brew --prefix)/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh

# Load zsh-autosuggestions
# source $(brew --prefix)/share/zsh-autosuggestions/zsh-autosuggestions.zsh


# Custom PROMPT
NEWLINE=$'\n'
# 自定義提示符設置
PROMPT='%{$fg_bold[green]%}%p%{$fg[cyan]%}%~ %{$fg_bold[blue]%}$(git_prompt_info)%{$fg_bold[blue]%}% %{$fg[magenta]%}%(?..%?%1v)%{$fg_bold[blue]%} ${NEWLINE} 💀 %{$fg[red]%}$ '
```

快捷 aliases 連結至 iCloud/local/bash_profile

指定電腦 .bash_profile 連結至 :cloud/local/bash_profile
```
ln -s ~/Library/Mobile\ Documents/com~apple~CloudDocs/local/bash_profile ~/.bash_profile
```
Zsh 
```
ln -s ~/Library/Mobile\ Documents/com~apple~CloudDocs/local/bash_profile ~/.oh-my-zsh/lib/aliases.zsh
```

最後 source 關聯
```
source ~/.bash_profile
```


-----------------------------------------------------------------------



連結 ssh 至 iCloud/local/ssh
```
ln -s ~/Library/Mobile\ Documents/com~apple~CloudDocs/local/ssh ~/.ssh

cd ~/.ssh
```

測試連結是否成功
```
ssh -T git@github.com
```


-----------------------------------------------------------------------
-----------------------------------------------------------------------

nodeJS
```
brew install node

brew install pnpm
```

go
```
brew install go
```

php
```
brew install php
```
-----------------------------------------------------------------------

Docker
```
brew install orbstack
```

Docker mysql
```
# 拉取鏡像
docker pull mysql:latest

# 運行（MYSQL_ROOT_PASSWORD 自行更換）
docker run --name mysql-server -e MYSQL_ROOT_PASSWORD=myroot -p 3306:3306 -d mysql:latest

# cli 連接
docker exec -it mysql-server mysql -uroot -p
```

Docker Mongodb
```
# image
docker pull mongo:latest

# run
docker run --name mongodb-server -p 27017:27017 -d mongo:latest

# cli
docker exec -it mongodb-server mongo
```

Docker Redis
```
# image
docker pull redis:latest

# run
docker run --name redis-server -p 6379:6379 -d redis:latest

# cli
docker exec -it redis-server redis-cli
```






-----------------------------------------------------------------------
Other
```
# VLC media player
brew install --cask vlc

```

-----------------------------------------------------------------------

App
```
https://folivora.ai/keyboardcleantool
https://freemacsoft.net/appcleaner/
https://github.com/Ji4n1ng/OpenInTerminal/blob/master/Resources/README-Lite-zh.md

```

Font
```
https://github.com/tonsky/FiraCode/releases
```
