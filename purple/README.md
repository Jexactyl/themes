# Deep Ocean (Purple) Theme
This theme is designed to introduce a dark and ocean-like look to your Panel.
It's easy to install and setup, with just 4 steps required.

## 1) Install build dependencies
You need to install the packages and tools required to build Jexactyl's frontend.
You can do this with the commands below:
```bash
curl -sL https://deb.nodesource.com/setup_16.x | sudo -E bash -
apt install -y nodejs
npm i -g yarn
```
Then, navigate to the `/var/www/jexactyl/directory` and install the Yarn packages.
```bash
cd /var/www/jexactyl/
yarn
```

## 2) Add new Tailwind file
In this folder you'll find a file named `tailwind.config.js`. This file needs to be present
in your `/var/www/jexactyl` directory in order for the theme to be added. Even if a tailwind config
file already exists in this directory, overwrite it.
```bash
cd /var/www/jexactyl
rm tailwind.config.js # Delete old TailwindCSS configuration
curl -Lo tailwind.config.js https://raw.githubusercontent.com/Jexactyl/themes/main/purple/tailwind.config.js # Download the new config for this theme
```

## 3) Build Jexactyl with theme installed
Once you've downloaded the new configuration file, you can rebuild the Panel.
```bash
cd /var/www/jexactyl
yarn build:production
```
This operation may take some time depending on your machines specifications.xactyl.

## Install complete!
Assuming you've followed all the previous steps correctly, your Panel should now have the light theme installed.
