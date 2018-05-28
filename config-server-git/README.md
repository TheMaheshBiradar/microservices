# Spring Cloud Config Server    

It is HTTP access to git based file configurations

Creating cloud config

configuration points to git repo.

There are many options including encryption and decryption

   <pre>
spring:
  cloud:
    config:
      server:
        git:
          uri: https://github.com/TheMaheshBiradar/config-repo.git
       </pre>
       
       
 
 URL to access specific file is :
 
    context path /{identifier}/{profile}
 
 
 if you have more than one folder you have to specifies 
 
    --searchpaths options
    
 you can also have mutliple repos based on identifiers
 
        -repo options
  
  config server always returns all the matching values back.
  i.e application.properties
 