# NOT FINISHED! WORK IN  PROGRESS
# this repository is only public for sharing files, but the tutorial has not been finished yet
# you may of course use the files present, they are fully operational.

# Raspberry-Pi-4-5-MediaServer

This is a beginner project for anyone that has a Raspberry Pi or any other computer with whicj they would like to turn into an automatic MediaServer!

It uses qbittorent for direct Movies and TvShows downloads, Seerr for a Netflix like Interface that directly downloads content, and jellyfin/plex
As well as Sonarr/Radarr who manage download requests, and jackett who manages the indexers 
__#DISCLAIMER:#__
I do not indorse pirating, you can very ell use legitimate sources like the Internet Archive with this project.

It also includes 2 networks, a main one and a VPN(with gluetun). I decided to use OpenVpn for this project, to change that please refer online or, you know, ask ChatGpt :)  Jackett and Qbittorent are put in the VPN enclosure to ensure protection.

Las but not least, this tutorial is made for beginners, when i first wanted to make such a project most tutorials were outdated, protocols changed, software was updated, and i found myself with a bunch of errors. Its is intended to use with a Raspberry Pi but it works with any linux based system, you may just have to change some paths here and there.

## Step1:

I recommend you use VsCode on another computer, with an ssh connexion to the pi, see here for ssh if you didn't set it up yet: (link)

A. Firstly, Open VsCode on your computer and press __Ctrl+Shift+P__ , select "connect to host" -> "add new ssh host" or first install the ssh plugin via the extensions tab.

B. Then enter your pi's ip adress (Wich is found by using __hostname -I__ on your remote) and press enter. The select either __/home__ or __/etc__. 
  A popup will appear, press "connect".

C. A new window opened, enter your password. After that press that little file icon -> __Open folder__ -> __OK__ then enter your password again. Congratulations! You are now connected to your pi and can begin your media server!


## Step2:

Let's now import the docker-compose.yml, i suggest you take a quick look at their tutorial on how to use docker compose, as you will greatly benefit from it: (link)

A. On this github page, press the green __Code__ button -> __Download zip__ and extract that zip file. 

B. Create a new folder on your remote, ideally directly on your user, but it HAS to be on the pi's SD card. All this via VS code of course as we connected all of the remote's files directly :)
  Think of VS code as a direct window to your pi.

C. Just drag and drop the extracted github folder on the new folder in VS code, wait a bit then all is transfered! We will now do a thiiiiny bit of coding, but it's simple don't worry ;)


## Step2:

So you transfered all your files, you will notice there is not much, just a docker compose yaml, a script and a .env, But you will see that as soon as you start your containers a whole architecture of folders will be made automatically, those will be the __config__ folders, but we'l come back to them mater.

A. see that terminal button on the top right corner? press that -> new terminal. This is now a direct terminal to your remote!

B. We will start simple, we just want to go in the media server to prepare the terminal for later. Run this command:

    ```bash
docker compose up -d


