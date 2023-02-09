![Screenshot of the interface of the Sugar Dark theme for SDDM](preview.png "The default interface of the Sugar Dark theme for SDDM")

# Al-swaiti login theme for SDDM

### Dependencies



**Debian based** distros using the **APT** package manager:  
*(Ubuntu/Kubuntu/Kali/Neon/antiX etc.)*  
<pre>sudo apt install --no-install-recommends sddm sddm-kcm</pre>  

**Arch based** distros using the **pacman** package manger:  
*(Obarun/Artix/Manjaro/KaOS/Chakra etc.)*  
<pre>sudo pacman -S --needed sddm sddm-kcm</pre>  

**openSUSE** using the **zypper** package manager:  
<pre>sudo zypper install sddm sddm-kcm</pre>  

**Red Hat** based distros using the **dnf** package manager:  
*(Fedora/Mageia/RHEL/CentOS)*  
<pre>sudo dnf install sddm sddm-kcm</pre>  

<br/><br/>






### Instalation


```
git clone https://github.com/al-swaiti/al-swaiti-sddm-theme

cd al-swaiti-sddm-theme

sudo tar -xzvf al-swaiti.tar.gz -C /usr/share/sddm/themes


sudo cp -r /usr/share/sddm/themes/al-swaiti/TTF /usr/share/fonts/ 

fc-cache -f -v

```

First be sure that sddm is your default display manager


```
systemctl status display-manager
```
![Alt text](sddm-service.png)

If you have another display-manager (ex:gdm):
```
sudo systemctl disable gdm.service
```

Then:
```
sudo systemctl enable sddm.service
```

Now you have to set [theme] inside sddm.conf
preferrably at `/etc/sddm.conf.d/default.conf`
sometimes `/etc/sddm.conf.d/kde_settings.conf`
**the name it's not important **
if you didnt find any you can create one by :
```
sudo cp /usr/lib/sddm/sddm.conf.d/default.conf /etc/sddm.conf.d/  
```

Now edit file 
```
sudo nano /etc/sddm.conf.d/default.conf
```
`ctrl+o` to save then `ctrl+x' to exit 

**the most important u need to find [Theme] section inside .conf file**
  

In the `[Theme]` section simply add the themes name: `Current=al-swaiti`.
as below
![Alt text](theme.png)

 Also see the [Arch wiki on SDDM](https://wiki.archlinux.org/index.php/SDDM).


Enjoy!





 donation on my [PayPayl](https://paypal.me/abdallalswaiti) or [patreon](https://www.patreon.com/user?u=88585798) account for a cup of coffee.  

