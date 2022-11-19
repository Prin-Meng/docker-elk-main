### step 1 create tls cert key 

openssl req -new -newkey rsa:2048 -nodes -keyout ELK.project.com.key -out ELK.project.com.csr

CA issue cert

### step2 config elasticsearch ldap

config ldap file and role-mapping

### step3 edit kibana config file

set cert and elasticsearch address

### step4 edit filebeat config file

edit time and enable cisco module

### step5 edit docker-compose.yaml

edit time and use volume input cert,key,ca key and ldap file 

### up docker container

docker-compose up -d 
