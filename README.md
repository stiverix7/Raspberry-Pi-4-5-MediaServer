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

C. A new window oppened, enter your password. After that press Congratulations! You are now connected to your pi and can begin your media server!


