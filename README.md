# openbox-setup-dotfiles
my dotfiles for my personal openbox setup

<h2>Programs/Requirements:</h2>
<ul>
	<li>Stow</li> 
	<li>Openbox, obconf </li>
	<li>Polkit - lxsession</li>
	<li>LightDM</li>
	<li>Terminal - Kitty</li>
	<li>Nitrogen</li>
	<li>Geany</li>
	<li>lxappearance-gtk3</li>
	<li>pcmanfm-gtk3</li>
	<li>obmenu-generator</li>
	<li>gvfs (for trash)</li>
	<li>Polybar</li>
	<li>Rofi</li>
	<li><a href=https://github.com/pijulius/picom> pijulius' picom github </a> | <a href=https://aur.archlinux.org/packages/picom-pijulius-git> AUR </a></li>
	<li>Betterlockscreen</li>
</ul>
<h3>Enable LightDM</h3>
<ol>
	<li>Install a greeter: sudo pacman -S lightdm-slick-greeter</li>
	<li>Set default greeter by changing the [Seat:*] section of the LightDM config file in /etc/lightdm/lightdm.conf:</li>
	greeter-session=lightdm-slick-greeter
	<li>Enable LightDM service: sudo systemctl enable lightdm.service</li>
</ol>

<h2>Fonts:</h2>
<ul>
	<li>Sofia Pro Light</li>
	<li>Japanese Fonts (fcitx, mozc): <a href=https://archlinux.org/packages/?name=adobe-source-han-sans-jp-fonts>adobe-source-han-sans-jp-fonts</a>, <a href=https://archlinux.org/packages/?name=adobe-source-han-serif-jp-fonts>adobe-source-han-serif-jp-fonts</a>, <a href=https://aur.archlinux.org/packages/ttf-vlgothic/>ttf-vlgothic</a> </li>
	<li>Icon: <a href=https://aur.archlinux.org/packages/ttf-material-design-iconic-font>Material Design Iconic</a>, nerd-fonts-jetbrains-mono</li>
	<li>Glyph: nerd-fonts-meslo</li>
</ul>

<h3>To install Japanese fonts</h3>
<ol>
	<li>Install all the Japanese fonts from above</li>
	<li>Install Input Method Framework (fcitx): sudo pacman -S fcitx-im fcitx-configtool</li>
	<li>Install Input Method Engine (mozc): sudo pacman -S fcitx-mozc</li>
	<li>Edit shell profile (.bashrc) to include these lines:</li>
	export GTK_IM_MODULE='fcitx'<br>
	export QT_IM_MODULE='fcitx'<br>
	export SDL_IM_MODULE='fcitx'<br>
	export XMODIFIERS='@im=fcitx'<br>
	<li>Restart or type the command: source .bashrc</li>
	<li>Generate Locales by editing /etc/locale.gen and uncomment "ja_JP.UTF-8 UTF-8". Then type: sudo locale-gen</li>
	<li>Add "fcitx -d" to autostart.sh of openbox</li>
	<li>Open fcitx-configtool in terminal. Then in Input Method, click the plus button on the lower left, unclick "Only show current langauge", search for Mozc, then click ok</li>
</ol>

<h2>To add:</h2>
<ul>
	<li>Kitty Theme (Kanagawa)</li>
	<li>libnotify, Dunst (with history)</li>
	<li>Dock?</li>
	<li>Systray</li>
	<li>Screenshot tool</li>
	<li>Script to automate the process</li>
</ul>
