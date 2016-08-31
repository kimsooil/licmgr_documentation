# licmgr
Requirements: Grails 2.5.4+, JDK 8, Tomcat8, Git

### How to install:
- 1) get clone from git (password protected)
```sh
git clone https://github.com/kimsooil/licmgr.git
cd licmgr
```
- 2) Build .war with development environment & H2 memory db
```sh
grails dev war ROOT.war
```
- 3) Or build ROOT.war with  production environment & H2 file db
```sh
grails prod war ROOT.war
```
- 4) copy (or replacing) ROOT.war into TOMCAT_DIR/webapps
```sh
sudo cp ROOT.war /usr/share/tomcat8/webapps/
```
- 5) start tomcat (if not yet running) or restart it (if already running)
```sh
sudo service tomcat8 start
or
sudo service tomcat8 restart
```
- 6) Open Browser (licmgr app will be running at ROOT)
```sh
http://localhost:8080  or http://AMAZON_EC2_PUBLIC_IP:8080
 ```
* to see live log, run 'sudo tail -f /var/log/tomcat8/catalina.out'
* to check the memory usage during tomcat is running, run 'free -m'
* H2 db files are in /usr/share/tomcat8/ (names start "prodDb...") or tomcat's home dir
