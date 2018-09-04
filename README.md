## Spring Security Using Mysql Authorization in a Spring Boot App

This example covers the following:
- Authentication using MySql DB Connectivity using custom user details service.
- Authorization using GrantedAuthority roles for method level security
- Leveraging Spring Security's login page for injecting login details

### IMPORT to eclipse
- import -> maven project
- here i am connecting mysql aws rds DB. if localhost available we can use that as well
- currently DB connection details are not provided. before running kindly update the applicaiton.properties with that.
- 3 table structures are created. role, user, user_role(map of user and their roles) 
- we are giving update, so tables are created in my sql.we need to insert data.
- here spring jpa is used to retrive data. default hibernate is used by default.

### running url
- no security: http://localhost:8080/rest/hello/all
- with security : http://localhost:8080/rest/hello/secured/all 
it redirect to spring default page. we can give own page by add .loginpage("/login")
- there is a bug in this proram. when we give correct username / any pass it validates to true.
