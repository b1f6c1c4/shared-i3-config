# Shared i3 config

> Keep your `~/.config/i3/config` synchronized across different computers.

## Usage

1. Fork this repo.
1. Run the following on the computer that has the best `~/.config/i3/config`:

    ```bash
    git clone --depth=1 git@github.com:<your-github-username>/shared-i3-config.git ~/shared-i3-config
    mv -f ~/.config/i3/config ~/shared-i3-config/config
    ln -s ~/shared-git-config/config ~/.config/i3/config
    cd ~/shared-i3-config
    git add config
    git commit
    git push -u origin master
    ```

1. Run the following on all other computers:

    ```bash
    git clone --depth=1 git@github.com:<your-github-username>/shared-i3-config.git ~/shared-i3-config
    mv -f ~/.config/i3/config ~/.config/i3/config.bak
    ln -s ~/shared-git-config/config ~/.config/i3/config
    ```

1. When you have modified your git config and you want to publish it everywhere,

    ```bash
    # On the computer where you modified your git config
    cd ~/shared-i3-config
    git add config
    git commit
    git push -u origin master

    # On other computers
    cd ~/shared-i3-config
    git pull --ff-only
    ```

## Legal

WTFPL
