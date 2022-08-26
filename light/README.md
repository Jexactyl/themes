# Paperback
This theme is designed to introduce a light and vibrant look to your Panel.
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
curl -Lo tailwind.config.js https://raw.githubusercontent.com/Jexactyl/themes/main/flashbang/tailwind.config.js # Download the new config for this theme
```

## 3) Add extra theme files needed
This theme requires you to replace files `GlobalStylesheet.ts` and `TitledGreyBox.tsx`, so everything
looks correct once installed.
Doing this is straightforward and can be done with the following commands:
```bash
cd /var/www/jexactyl/resources/assets/css
rm GlobalStylesheet.ts
curl -Lo GlobalStylesheet.ts https://raw.githubusercontent.com/Jexactyl/themes/main/light/resources/assets/css/GlobalStylesheet.ts

cd /var/www/jexactyl/resources/scripts/components/elements
rm TitledGreyBox.tsx
curl -Lo TitledGreyBox.tsx https://raw.githubusercontent.com/Jexactyl/themes/main/light/resources/scripts/components/elements/TitledGreyBox.tsx
```
After you've gone ahead and added this file, you can move onto stage 4.

## 4) Build Jexactyl with theme installed
Once you've downloaded the new configuration file, you can rebuild the Panel.
```bash
cd /var/www/jexactyl
yarn build:production
```
This operation may take some time depending on your machines specifications.xactyl.

## Install complete!
Assuming you've followed all the previous steps correctly, your Panel should now have the light theme installed.
