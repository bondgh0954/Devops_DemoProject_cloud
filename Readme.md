# Cloud & Infrastructure as Service Basics

# Demo Project

Create server and deploy application on DigitalOcean



# Technologies used

DigitalOcean
Linux
Java
Gradle


# Project Description:

1. Setup and configure a server on DigitalOcean
  
   Create a droplet on DigitalOcean
   create a firewall configuration  and add the droplet
   copy the public key from   .ssh/id_rsa.pub  and paste it 
   into digital ocean to ssh into server without username and
   password.
   ssh into the server as rootuser (ssh root@publicIpAddress )
   
   




2. Create and configure a new linux user on the Droplet
(security best practice)
  
  Create a newuser using the (adduser command)
  eg adduser oteng
  give the new user a sudo access (usermod -aG sudo username)
  
  # for the created user to be able to login from commandline
      copy the public key from (.ssh/id_rsa.pub)
      ssh into the server as root
      switch to the new user (su - username)
      create a new directory (.ssh)  
      inside the newly created .ssh directory create a file (authorized_keys)
      paste the public key inside the authorized_keys
  
3. Deploy and run a java Gradle application on Droplet
   install java on the server
   build the application artifact  (eg. gradle build) from the code repo
   copy the artifact to the server

   run with (java -jar nameofartifact)
