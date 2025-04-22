# Starbucks

# Install AWS CLI
'''
sudo apt install unzip -y
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
'''


# Deploy SonarQube container
'''
docker run -d --name sonar -p 9000:9000 sonarqube:lts-community
Use Port: 9000 to run the SonarQube
'''

# Do seetings in Jenkins
Jenkins--> manage jenkins--> Plugnins-> Available Plugins:
i) Eclipse Temurin installer
ii) Sonarqube 
iii) node js
iv) docker
v) Owsap
vi) stage view
vii) Email notofication 

# In Sonarqube-> Administration--> Security--> User-> Click on Update token(3lines)
# Give Token name as --> jenkins and click on Generate Token : squ_bea061f48c758da82afe88c976dcad9229f42c57
# Now go to Jenkins-> Manage Jenkins-> Credentials-> Click on Global-> Click on Add credentials 
# In credentaials -> dropudown choose secret text-> give ID as Sonar-token and past the Sonarqube token in place of secrets

# Now put the docker hub username and password in place of Credentilas in Jenkins-> dropdown choose-> username and password
# Now go to Sonarqube-> Configuration-> webhooks-> create-> Name:jenkins-> Url:http://43.205.216.48:8080/sonarqube-webhook/
# Go to Jenkins-> Tools-> instll JDK, Sonarqube, NodeJs, Dependency Check, Docker, 
# Jenkins--> Manage Jenkins--> Systems--> SonarQube installations
# For email notification: Go to gmail--> Manage your Google Accounts--> Type APP Password(in Search option)-> Give App name(jenkins)- Create: Password will generate
# Go to Jenkins-> Manage jenkins-> credentials-> Global credentials--> enter the details
# Go to Jenkins--> Manage Jenkins-> System -> Send Email notification --> enter the details
