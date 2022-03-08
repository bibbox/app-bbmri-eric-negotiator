# BBMRI-ERIC negotiator (dev. version)

This container can be installed as [BIBBOX APP](https://bibbox.readthedocs.io/en/latest/ "BIBBOX") or standalone.
 
After the installation follow these [instructions](INSTALL-APP.md)

## Hints
* approx. time with medium fast internet connection: **15 minutes**
* initial user/passwordd: **....**

## Install within BIBBOX

Within BIBBOX you can use the [BIBBOX](https://bibbox.readthedocs.io/en/latest/ "BIBBOX") to install a lot of software tools. After the installation is finished you can start your application in the dashboard.

### Install Environment Variables

 * DB_USER = Username for the database
 * DB_PASSWORD = Password for the database
 
The default values for the standalone installation are:

 * DB_USER = negotiator
 * DB_PASSWORD = negotiator

## Docker Images Used
 * [BIBBOX/negotiator](https://hub.docker.com/r/bibbox/negotiator) 
 * [PostgreSQL](https://hub.docker.com/_/postgres/), offical PostgreSQL container
 
## Standalone Installation

To install the app locally execute the commands:
* Clone the git repository: 
  * `git clone https://github.com/bibbox/app-molgenis.git`
* Change the current directory to app-bbmri-eric-negotiator: 
  * `cd app-bbmri-eric-negotiator/` 
* Create the docker network `bibbox-default-network`: 
  * `docker network create bibbox-default-network`
* Run **docker-compose up** in the root folder of the project: 
  * `docker-compose up -d`
* **Alternatively** on a *Linux* system run the bash script `intsall.sh` after cloning and change the working directory to the git repository directory.
 

After the installation (might take a few minutes) open **http://localhost:9000** in your browser to access Negotiator Dev Version.


## Mounted Volumes
* ./data/postgres
* ./data/uploads


