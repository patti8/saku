1. gipudo -> command gipudo main --no-cache , bisa tanpa argumen tapi wajib branch name
alias gipudo='function _gipudo() {
  branch="$1"
  cache_flag="$2"

  if [ -z "$branch" ]; then
    echo "Usage: gipudo <branch> [--no-cache]"
    return 1
  fi

  git pull origin "$branch" && \
  docker-compose down && \
  docker-compose build $cache_flag && \
  docker-compose up
}; _gipudo'
