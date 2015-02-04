The Application Installation Scripts for Linux Mint 17.1
--------------

Clone the repo into directory *~/Installation*. Run the commands from the *Installation* directory (not required for all the commands).
***
Installing the **Numix GTK** theme
```bash
sudo ./numix.sh
```
***
Installing **Cairo Dock**
```bash
sudo ./cairo-dock.sh
```
***
Installing **Kodi**
```bash
sudo ./kodi-add-repos.sh # run only once and only if this workaround is still necessary
sudo ./kodi.sh
```
***
Installing **DeaDBeeF** with **File Browser plugin**

Before running the script:

 * Download debubuntu package file into files/deadbeef as deadbeef-static.deb
 * Extract ddb_misc_filebrowser_GTK2.so and ddb_misc_filebrowser_GTK3.so into files/deadbeef directory
 
```bash
sudo ./deadbeef.sh
```
To activate file browser: View -> Design mode, Replace with.. -> Splitter (left and right), Insert... -> ...
***
Installing **XnViewMP**
```bash
sudo ./xnviewmp.sh
```
***
Installing **Oracle JDK 8** and setting the environment variables for installed JDK
```bash
sudo ./oracle-java.sh
```
***
Installing the newest version of **Docker**

(*The user must re-log after the execution. The specified user doesn't have to use sudo for Docker commands.*)
```bash
sudo ./docker.sh $USERNAME
```
Changing path for the root of the Docker runtime

(*The default location is /var/lib/docker. Docker images are contained in this directory. Changing of the path can be convinient for example in case you don't have enough space on /var partition.*)
```bash
sudo ./docker-change-graph-path.sh $NEW_PATH
```
***
Installing **Docker Compose** (formerly named Fig)
```bash
mkdir files/fig
wget https://github.com/docker/fig/releases/download/1.1.0-rc2/docker-compose-`uname -s`-`uname -m` -O ./files/fig/docker-compose
sudo ./docker-compose.sh
```
***
Installing **IntelliJ IDEA Community Edition** and integrating with desktop (adding desktop menu item...)

Before running the script:

* Download archive as ideaIC.tar.gz into files/idea directory

```bash
sudo ./idea.sh
```
