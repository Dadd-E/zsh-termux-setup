
termux customize
To install zsh, zsh-autosuggestions, zsh-syntax-highlighting, and powerlevel10k in Termux, follow these steps:

Step 1: Update Termux Packages
pkg update && pkg upgrade -y
Step 2: Install Required Packages
Install zsh, git, and curl:

pkg install -y zsh git curl
Step 3: Install Oh My Zsh
Run the Oh My Zsh installer:

sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
When prompted, confirm to set zsh as your default shell.
Step 4: Install Plugins
zsh-autosuggestions (auto-completion):
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
zsh-syntax-highlighting (colorful syntax):
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
Step 5: Install Powerlevel10k Theme
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
Step 6: Configure .zshrc
Open your .zshrc file:
nano ~/.zshrc
Set the theme:
ZSH_THEME="powerlevel10k/powerlevel10k"
Enable plugins (add to the plugins line):
plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
Save changes (Ctrl + S) and exit (Ctrl + X).
Step 7: Apply Changes
Reload your shell configuration:

source ~/.zshrc
The Powerlevel10k configuration wizard will start. Follow the prompts to customize your prompt. If you skip it, run p10k configure later.

Step 8: Fix Font Issues (Optional)
Powerlevel10k requires special fonts for icons. Install Termux:Styling from the Play Store/F-Droid to set a compatible font (e.g., MesloLGS NF). Alternatively, configure Powerlevel10k to use ASCII mode during setup.

Troubleshooting
If plugins don’t load, ensure the paths in .zshrc are correct.
Use exec zsh to restart Zsh if needed.
For Powerlevel10k issues, visit: Powerlevel10k GitHub
Enjoy your customized Zsh setup in Termux! 🚀
