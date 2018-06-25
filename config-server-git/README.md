# Spring Cloud Config Server    

It was designed to solve very specific problem statement.

Each of microservices is nothing but small application and hence it requires it's own configuration but it is not manageable as no of microservices will grow and difficult to manage these configuration.

Spring cloud config provides central configuration and it helps to manage configutation.


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
 
 
 The biggest benefit is "It is HTTP based approach so any NON spring application also can consume this".
 
 i.e it is <i>client agnostic<i>