# Sonar_Scanner_Installation
Step-1:
wget https://binaries.sonarsource.com/Distribution/sonar-scanner-cli/sonar-scanner-cli-4.2.0.1873-linux.zip
unzip sonar-scanner-cli-4.2.0.1873-linux.zip
mv sonar-scanner-4.2.0.1873-linux /opt/sonar-scanner
Step-2:
vi /opt/sonar-scanner/conf/sonar-scanner.properties
 ---->   sonar.host.url=http://localhost:9000
 ---->   sonar.sourceEncoding=UTF-8
 Step-3
 vi /etc/profile.d/sonar-scanner.sh
 ---> #/bin/bash
      export PATH="$PATH:/opt/sonar-scanner/bin"
Step-4:
reboot
source /etc/profile.d/sonar-scanner.sh
Step-5:
env | grep PATH
PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/opt/sonar-scanner/bin
Step-6:
sonar-scanner -v
 
 
