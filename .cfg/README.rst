Config / dotfile
****************

- The best way to store your dotfiles: A bare Git repository:
  https://developer.atlassian.com/blog/2016/02/best-way-to-store-dotfiles-git-bare-repo/
- YouTube Video
  https://www.youtube.com/watch?v=tBoLDpTWVOM&t=3s

Initial Setup (only do once)::

  # using the fish shell
  fish
  # you just need to clone this after it is created
  # git init --bare $HOME/.cfg

New Workstation::

  # create an alias for your fish shell
  alias config="/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME"
  funcsave config
  config config --local status.showUntrackedFiles no

