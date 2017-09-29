# Spring Cloud Config Server    

It is HTTP access to local file or git based file configurations

Creating cloud config

1. choose the file format (local, git)/source
2. create boot project 
3. secure the configuration store access


#####1. Local /Git based file system

   - Multiple locations possible
   - Supports labelling
   - Supports placeholders in URI (env in URI)
   - you can use YML / properties file or text file .
   - you can use JSON as well
   - file name contains application name and profile
   - It supports nested structure
   
   when you git based approach you will have full history of the file as it's version control and you don't get same benefits for the local file based approach.
   
   default spring config server asks for git URL - use below config to application search in local
   <pre>
   spring:
     profiles:
       active: native
       </pre>