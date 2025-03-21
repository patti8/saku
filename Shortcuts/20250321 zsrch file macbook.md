#alias dokku='ssh dokku@dokku.docker'

#alias liserve='root@62.72.51.3'

alias codingtime='cd /Users/imac/Documents/DEVELOPER && echo "Whatever you do, work at it with all your heart, as working for the Lord, not for human masters 🔥" && ls'

alias notetaking='cd "/Users/imac/Library/Mobile Documents/com~apple~CloudDocs/RSBM/RSBM" && echo "📌 Welcome! Capture your thoughts and ideas here." && ls'

alias r='rails'

alias pre="assets:precompile"

#alias setvim='nvim /Users/imac/.config/nvim/init.lua'

#alias embulk='java -jar /Users/imac/Documents/DEVELOPER/ETL/embulk.jar'

alias dcompose='docker compose'

alias conf='nvim ~/.zshrc'

alias gsend='f() { git add . && git commit -m "$1" && git push origin "$2"; }; f'

alias svconf="source ~/.zshrc && echo 'configuration saved.✌️'"

#export PATH="/Users/imac/Documents/DEVELOPER/ETL:$PATH"

  

ZSH_THEME="powerlevel9k/powerlevel9k"

  

export PATH="/Users/imac/my_gems/bin:$PATH"

export PATH=/opt/homebrew/bin:/usr/local/bin:/System/Cryptexes/App/usr/bin:/usr/bin:/bin:/usr/sbin:/sbin:/var/run/com.apple.security.cryptexd/codex.system/bootstrap/usr/local/bin:/var/run/com.apple.security.cryptexd/codex.system/bootstrap/usr/bin:/var/run/com.apple.security.cryptexd/codex.system/bootstrap/usr/appleinternal/bin:/Library/Apple/usr/bin

export PATH="/opt/homebrew/opt/ruby/bin:$PATH"

#export PATH="/Users/imac/Library/Android/sdk/platform-tools"

  

#eval "$(~/.local/bin/mise activate)"

#eval "$(/var/root/.local/bin/mise activate zsh)"

  

# >>> conda initialize >>>

# !! Contents within this block are managed by 'conda init' !!

__conda_setup="$('/opt/anaconda3/bin/conda' 'shell.zsh' 'hook' 2> /dev/null)"

if [ $? -eq 0 ]; then

eval "$__conda_setup"

else

if [ -f "/opt/anaconda3/etc/profile.d/conda.sh" ]; then

. "/opt/anaconda3/etc/profile.d/conda.sh"

else

export PATH="/opt/anaconda3/bin:$PATH"

fi

fi

unset __conda_setup

# <<< conda initialize <<<

  

export PATH="/Users/imac/Library/Android/sdk/platform-tools:$PATH"

export PATH="/usr/local/opt/node@22/bin:$PATH"

export PATH="/usr/local/opt/node@22/bin:$PATH"

export PATH="/opt/homebrew/opt/node@22/bin:$PATH"

eval "$(~/.local/bin/mise activate)"

# kill port

killport() { kill -9 $(lsof -ti :$1); }