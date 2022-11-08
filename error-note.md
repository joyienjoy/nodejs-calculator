
NOTE 1: For using a Slave machine:
-----------------------------------
POSSIBLE ERROR:
----------------------------------
docker build -t joydeep2022/nodejs-calculator:3 .
Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Post "http://%2Fvar%2Frun%2Fdocker.sock/v1.24/build?buildargs=%7B%7D&cachefrom=%5B%5D&cgroupparent=&cpuperiod=0&cpuquota=0&cpusetcpus=&cpusetmems=&cpushares=0&dockerfile=Dockerfile&labels=%7B%7D&memory=0&memswap=0&networkmode=default&rm=1&shmsize=0&t=joydeep2022%2Fnodejs-calculator%3A3&target=&ulimits=null&version=1": dial unix /var/run/docker.sock: connect: permission denied
----------------------------------
sudo adduser jenkins                #Create a User named "jenkins"

cat /etc/passwd                     #Check

sudo usermod -aG docker jenkins     #Add user "jenkins" to "docker" group

sudo chown root:docker /var/run/docker.sock      #Give ownership to file





