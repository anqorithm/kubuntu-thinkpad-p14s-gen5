# My Kubuntu Setup - ThinkPad P14s Gen 5

This is my dev setup. I code every day on this. Used to use Windows + WSL. Now I use Kubuntu. Much better.

## My Setup in Action

![Kubuntu Desktop Overview](./assets/4.png)
<p align="center"><i>My daily driver - Kubuntu 25.04 with KDE Plasma</i></p>

![Clean KDE Plasma Desktop](./assets/1.png)
<p align="center"><i>Clean and minimal KDE desktop - fast and responsive</i></p>

![Development Environment Setup](./assets/2.png)
<p align="center"><i>Konsole terminal - where the magic happens</i></p>

![System Resource Monitor](./assets/3.png)
<p align="center"><i>Ram & CPU utlization (better than WSL :D)</i></p>

![KDE System Monitor](./assets/5.png)
<p align="center"><i>KDE System Monitor - tracking CPU, memory, and network usage</i></p>

## Why I Quit Windows + WSL

I used WSL since version 1. Stuck with it for years. Even had a laptop with 32GB RAM and fast CPU. Didn't matter. WSL still sucked.

npm install took 2 minutes. Now it takes 30 seconds. Docker was slow as hell. File watching didn't work half the time. WSL ate 8-10GB of RAM doing nothing. It crashed all the time. Lost my work multiple times. VPNs broke it. File permissions were a mess.

WSL sucks. Period.

## Why Kubuntu is Better

Kubuntu is amazing for coding. Everything just works. Boots in 15 seconds. Battery lasts 7 hours instead of 4. Uses only 1GB RAM when idle.

Docker runs native - no VM crap. Hot reload actually works. Git is super fast. No crashes. No permission problems. This is how coding should be.

## What I Use

I code in VS Code. Use Docker for containers. nvm for Node versions. pyenv for Python versions. PostgreSQL and Redis for databases.

Terminal is Bash with Oh My Bash (or Zsh with Oh My Zsh). Starship prompt shows git info. tmux for multiple terminals.

Apps: Spotify, Telegram, Discord, VLC, OBS.

## How to Set Everything Up

### Quick Install Guide

| What | Command | Why |
|------|---------|-----|
| System Update | `sudo apt update && sudo apt upgrade` | Get latest packages |
| Basic Tools | `sudo apt install build-essential git curl wget vim htop neofetch` | Essential dev tools |

### Development Tools

| Tool | Install Commands | Purpose |
|------|-----------------|---------|
| Docker | `sudo apt install docker.io docker-compose`<br>`sudo usermod -aG docker $USER`<br>`sudo systemctl enable docker` | Containers |
| Node.js | `curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh \| bash`<br>Restart terminal<br>`nvm install --lts` | JavaScript |
| Python | `curl https://pyenv.run \| bash`<br>Add to shell config<br>`pyenv install 3.11.5` | Python dev |
| VS Code | `sudo snap install code --classic` | Code editor |

### Terminal Setup

| Option | Commands | Result |
|--------|----------|--------|
| Bash + Oh My Bash | `bash -c "$(curl -fsSL https://raw.githubusercontent.com/ohmybash/oh-my-bash/master/tools/install.sh)"` | Better Bash |
| Zsh + Oh My Zsh | `sudo apt install zsh`<br>`chsh -s $(which zsh)`<br>`sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"` | Better Zsh |
| Starship Prompt | `curl -sS https://starship.rs/install.sh \| sh`<br>Add to `.bashrc` or `.zshrc` | Cool prompt |

### Apps Installation

| Type | Command | Apps |
|------|---------|------|
| Flatpak Setup | `sudo apt install flatpak`<br>`sudo flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo` | Enable Flatpak |
| Media Apps | `flatpak install flathub com.spotify.Client`<br>`flatpak install flathub org.videolan.VLC`<br>`flatpak install flathub com.obsproject.Studio` | Spotify, VLC, OBS |
| Chat Apps | `flatpak install flathub org.telegram.desktop`<br>`flatpak install flathub com.discordapp.Discord` | Telegram, Discord |
| Work Apps | `sudo snap install postman`<br>`sudo snap install notion-snap-reborn`<br>`flatpak install flathub md.obsidian.Obsidian` | Postman, Notion, Obsidian |

### CLI Tools

| Tool | Install | What it does |
|------|---------|--------------|
| Dev Tools | `sudo apt install tmux postgresql-client redis-tools httpie jq ripgrep` | Terminal tools |
| LazyDocker | `curl https://raw.githubusercontent.com/jesseduffield/lazydocker/master/scripts/install_update_linux.sh \| bash` | Docker UI |
| LazySQL | `go install github.com/jorgerojas26/lazysql@latest` | Database UI |

## Speed Difference

| What | Windows + WSL | Kubuntu |
|------|---------------|---------|
| Boot | 45 seconds | 15 seconds |
| npm install | 2+ minutes | 30 seconds |
| Docker build | 3 minutes | 1 minute |
| RAM (idle) | 4.5 GB | 1.2 GB |
| Battery | 4 hours | 6-7 hours |

## Helpful Links

* [Kubuntu](https://kubuntu.org/) - Official Kubuntu site
* [KDE](https://kde.org/) - KDE Plasma desktop
* [Linux Journey](https://linuxjourney.com/) - Learn Linux basics
* [Arch Wiki](https://wiki.archlinux.org/) - Has answers for everything  
* [Docker Docs](https://docs.docker.com/) - Docker help
* [Ask Ubuntu](https://askubuntu.com/) - Get help
* [r/linux](https://reddit.com/r/linux) - Linux community
* [TLP](https://linrunner.de/tlp/) - Save battery
* [Timeshift](https://github.com/linuxmint/timeshift) - Backup your system

## My Advice

If you're thinking about switching from Windows, just do it. Try dual boot first if you're scared. Give it a month. Things will break sometimes. You'll figure it out. Google helps. Arch Wiki has all answers.

Linux is worth it. No more Windows updates. No more bloat. No more WSL problems. Just a fast computer that works.

---

**Bottom line:** WSL = slow and broken. Linux = fast and works.

Ask me anything!

---

*ThinkPad P14s Gen 5 AMD | Kubuntu 24.04 LTS | Happy coder*