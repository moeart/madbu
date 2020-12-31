# madbu (MorArt's Disk Backup Utility)

### moved to [https://gitlab.com/moeart/madbu](https://gitlab.com/dfc643/datto-backup/-)

A Text based UI to dump live (running) system disk to image file with Volume Shadow Service (VSS or COW) in Linux. need dattobd dkms module support.

![sample.gif](https://gitlab.com/dfc643/datto-backup/-/raw/master/sample.gif)

[![asciicast](https://asciinema.org/a/iDiEb1tIytchcyG4Q9NTy1Z7x.svg)](https://asciinema.org/a/iDiEb1tIytchcyG4Q9NTy1Z7x)

---

## Requirement
* CoW DKMS Module ```dattobd```
* Linux Kernel ```>=4.9``` or ```>5.0``` recommend
* Parallel GZip program ```pigz```
* Base packages ```dialog, pv, dd```


## Task
* [x] Volume Shadow Copy (CoW)
* [x] Umount Device Support
* [ ] English Version
* [ ] Compression Algorithm Optimization
* [ ] Graphical User Interface (?)


## Before Use
1. Please install those packages before use.
    ```bash
    sudo apt install -y dialog pv pigz
    ```
1. And then install ```dattabd``` module.    
**For Debian and Ubuntu**
    ```
    sudo apt-key adv --fetch-keys https://cpkg.datto.com/DATTO-PKGS-GPG-KEY
    echo "deb [arch=amd64] https://cpkg.datto.com/datto-deb/public/$(lsb_release -sc) $(lsb_release -sc) main" | sudo tee /etc/apt/sources.list.d/datto-linux-agent.list
    sudo apt-get update
    sudo apt-get install dattobd-dkms dattobd-utils
    ```
    **For Deepin v20 and UOS v20**
    ```
    sudo apt-key adv --fetch-keys https://cpkg.datto.com/DATTO-PKGS-GPG-KEY
    echo "deb [arch=amd64] https://cpkg.datto.com/datto-deb/public/buster buster main" | sudo tee /etc/apt/sources.list.d/datto-linux-agent.list
    sudo apt-get update
    sudo apt-get install dattobd-dkms dattobd-utils
    ```
3. Reboot your PC or Server.


## Usage
```bash
chmod +x madbu.sh
sudo ./madbu.sh
```

# Copyright
## License
[The MIT License (MIT)](https://gitlab.com/dfc643/datto-backup/-/raw/master/LICENSE)

Copyright (c) 2021 xRetia Labs    
Copyright (c) 2021 MoeArt Inc. (www.acgdraw.com)

## About xRetia Labs
The xRetia Labs is apart of MoeArt Inc. which working for opensource project.    
Copyright (c) 2021 MoeArt Inc. (www.acgdraw.com)
