### Termux

```bash
git clone https://github.com/avline97/D445
cd D445
chmod 777 termux_install.sh
./termux_install.sh
```

## Usage

```bash
python3 seeker.py -h
usage: seeker.py [-h] [-s SUBDOMAIN]
optional arguments:
  -h, --help                              show this help message and exit
  -s SUBDOMAIN, --subdomain Subdomain 	  Provide Subdomain for Serveo URL ( Optional )
  -k KML, --kml KML                       Provide KML Filename ( Optional )
  -t TUNNEL, --tunnel TUNNEL              Specify Tunnel Mode [manual]
# Example
# SERVEO 
########
python3 seeker.py
# NGROK ETC.
############
# In First Terminal Start seeker in Manual mode like this
python3 seeker.py -t manual
# In Second Terminal Start Ngrok or any other tunnel service on port 8080
./ngrok http 8080
#-----------------------------------#
# Subdomain
########### 
python3 seeker.py --subdomain google
python3 seeker.py --tunnel manual --subdomain zomato
#-----------------------------------#
# Docker Usage
##############
# SERVEO
########
docker run -t --rm thewhiteh4t/seeker
# NGROK
#######
# Step 1
docker network create ngroknet
# Step 2
docker run --rm -t --net ngroknet --name seeker thewhiteh4t/seeker python3 seeker.py -t manual
# Step 3
docker run --rm -t --net ngroknet --name ngrok wernight/ngrok ngrok http seeker:8080
```
##By D445
