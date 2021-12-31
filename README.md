# Pihole_DOH
El proyecto Pi-hole® es para bloqueo de anuncios en toda la red a través de su propio hardware Linux. Pi-hole® es un sumidero de DNS que protege sus dispositivos de contenidos no deseados sin necesidad de instalar ningún software del lado del cliente.

#

<p align="center">
    <a href="https://pi-hole.net/">
        <img src="https://github.com/JuanRodenas/Pihole_DOH/blob/main/pihole.png" alt="Pi-hole">
    </a>
    <br>
    <strong>Network-wide ad blocking via your own Linux hardware</strong>
</p>
<!-- markdownlint-enable MD033 -->

#

📁 [Documentación oficial](https://docs.pi-hole.net/)

# INSTALAR DOCKER-COMPOSE.YML DE PIHOLE_DOH
Edit the following variables, with the correct interface, IP and volume.
> Descargar [docker-compose.yml](https://github.com/JuanRodenas/Pihole_DOH/blob/main/docker-compose.yml)
>~~~
>INTERFACE:
>ServerIP:
>WEBPASSWORD:
>~~~

#### Running
~~~
docker-compose up -d
~~~

#### Check
~~~
docker ps -a
~~~

Edit the following variables, with the correct interface and IP.

#### Password acceso web
Accedemos al contenedor:
~~~
docker exec -u root -t -i pihole /bin/bash
~~~
Cambiamos la password:
~~~
pihole -a -p
~~~

#### Acceso al dashboard
There are several ways to [access the dashboard](https://discourse.pi-hole.net/t/how-do-i-access-pi-holes-dashboard-admin-interface/3168):

1. `http://pi.hole/admin/` (when using Pi-hole as your DNS server)
2. `http://<IP_ADDPRESS_OF_YOUR_PI_HOLE>/admin/`



# Listas para Pihole

## Main black Lists
~~~
https://dbl.oisd.nl 
~~~
~~~
https://sysctl.org/cameleon/hosts 
~~~
~~~
https://s3.amazonaws.com/lists.disconnect.me/simple_ad.txt 
~~~
~~~
http://winhelp2002.mvps.org/hosts.txt 
~~~
~~~
https://s3.amazonaws.com/lists.disconnect.me/simple_malvertising.txt 
~~~
~~~
https://someonewhocares.org/hosts/hosts 
~~~
~~~
https://adaway.org/hosts.txt 
~~~
~~~
https://pgl.yoyo.org/adservers/serverlist.php?hostformat=hosts&showintro=0&mimetype=plaintext 
~~~
~~~
https://v.firebog.net/hosts/Easyprivacy.txt 
~~~
~~~
https://v.firebog.net/hosts/AdguardDNS.txt 
~~~
~~~
https://v.firebog.net/hosts/Easylist.txt 
~~~
~~~
https://raw.githubusercontent.com/Perflyst/PiHoleBlocklist/master/SmartTV.txt 
~~~
~~~
https://phishing.army/download/phishing_army_blocklist_extended.txt 
~~~
~~~
https://raw.githubusercontent.com/Spam404/lists/master/main-blacklist.txt 
~~~
~~~
https://hostfiles.frogeye.fr/firstparty-trackers-hosts.txt 
~~~
~~~
https://zerodot1.gitlab.io/CoinBlockerLists/hosts_browser 
~~~
~~~
https://raw.githubusercontent.com/FadeMind/hosts.extras/master/add.Risk/hosts 
~~~
~~~
https://raw.githubusercontent.com/anudeepND/blacklist/master/adservers.txt 
~~~
~~~
https://www.github.developerdan.com/hosts/lists/ads-and-tracking-extended.txt 
~~~
~~~
https://raw.githubusercontent.com/crazy-max/WindowsSpyBlocker/master/data/hosts/spy.txt 
~~~
~~~
https://raw.githubusercontent.com/StevenBlack/hosts/master/hosts 
~~~
~~~
https://raw.githubusercontent.com/AzagraMac/PiHoleDocker/master/list/urlhaus-filter-domains.txt 
~~~
~~~
https://raw.githubusercontent.com/kboghdady/youTube_ads_4_pi-hole/master/youtubelist.txt 
~~~
~~~
https://raw.githubusercontent.com/AzagraMac/PiHoleDocker/master/list/outapzazaList.txt 
~~~
~~~
https://raw.githubusercontent.com/AzagraMac/PiHoleDocker/master/list/NSABlocklist.txt 
~~~
~~~
https://raw.githubusercontent.com/hoshsadiq/adblock-nocoin-list/master/hosts.txt 
~~~
~~~
https://raw.githubusercontent.com/AzagraMac/PiHoleDocker/master/list/AndroidTracking.txt 
~~~
~~~
https://v.firebog.net/hosts/Prigent-Ads.txt 
~~~
~~~
https://raw.githubusercontent.com/matomo-org/referrer-spam-blacklist/master/spammers.txt 
~~~
~~~
https://raw.githubusercontent.com/Zelo72/adguard/main/d3host.adblock
~~~
~~~
https://raw.githubusercontent.com/jerryn70/GoodbyeAds/master/Hosts/GoodbyeAds-Ultra.txt
~~~
~~~
https://raw.githubusercontent.com/notracking/hosts-blocklists/master/adblock/adblock.txt
~~~
To Block Facebook/Instagram/Whatsapp
~~~
https://github.com/jmdugan/blocklists/blob/master/corporations/facebook/all
~~~
To Block Facebook/Instagram but leave Whatsapp open
~~~
https://raw.githubusercontent.com/jmdugan/blocklists/master/corporations/facebook/all-but-whatsapp
~~~
To Block Google:
~~~
https://raw.githubusercontent.com/jmdugan/blocklists/master/corporations/google/all
~~~
To Block Mozilla tracking
~~~
https://raw.githubusercontent.com/jmdugan/blocklists/master/corporations/mozilla/all
~~~
To Block Microsoft
~~~
https://raw.githubusercontent.com/jmdugan/blocklists/master/corporations/microsoft/all
~~~

# Regenerar listas
Accedemos al contenedor:
~~~
docker exec -u root -t -i pihole /bin/bash
~~~
Regeneramos las listas:
~~~
pihole -g
~~~

## Ready!
