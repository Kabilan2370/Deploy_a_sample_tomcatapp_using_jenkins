# Deploy_a_sample_tomcatapp_using_jenkins

How to deploy a sample tomcat application using jenkins......

1. First,create a one EC2 machine for jenkins dTeployment.I'm also attached a VPC service everthink.this take the machine is ubuntu 22.04.

   ![Alt text](jen/1.png)

2. Use putty for windows or ssh for ubuntu. Here,I'm used ssh client to login in EC2 machine.

   ![Alt text](jen/2.png)
   
   First,Install a java jdk on the machine
   
   ![Alt text](https://download.oracle.com/java/21/latest/jdk-21_linux-x64_bin.deb)

3. Then,Before install a jenkins ,you should add jenkins key and directory

   ![Alt text](jen/2a.png)

4. Click a debian-stable repository to add a key & download jenkins.
   
   ![Alt text](jen/2b.png)

5. After added a key,you should install a jenkins.
   
   ![Alt text](jen/2c.png)

6. Check once your jenkins is working correctly or not.
   
   ![Alt text](jen/2d.png)

7. Now , install apache tomcat on the machine. Here,I used apche tomcat 9.0.91

   ![Alt text](jen/4.png)

8. Check,a tomcat downloaded on your machine.Extract the tomcat .tar file

    sudo tar -xvzf apche-tomcat-9.0.91

9. Here,You should change a tomcat default port number.Because of jenkins & tomcat default port number is 8080.
   you can change any one default port number. Here,I changed tomcat port number as 7079.

   ![Alt text](jen/7.png)

10. Once,did you Changed a port number or tomcat server related operation ? ,you should restart the tomcat.

    ![Alt text](jen/8.png)

11. Now,you can try to access a jenkins machine using your IP:7079 with a port number.

    ![Alt text](jen/9.png)

12. we should a sample java based application code.So ,I download a sample application from the web.

    ![Alt text](jen/3a.png)
    ![Alt text](jen/10.png)

13. The move the sample.war file to cd /var/lib/jenkins/webapps/deplot_a_application
    Above,the line I mentioned a my jenkins newstyle(deplot_a_application) project.

    1[Alt text](jen/11.png)

14. On my project ,in the post build action choose a deploy a continer & give the sample application details.

    ![Alt text](jen/12.png)

    ![Alt text](jen/13.png)

15. While you first time try this project,maybe you can face this error.

    ![Alt text](jen/14.png)

16. Just uncomment a below line into tomcat webapps

    ![Alt text](16.png)
    ![Alt text](15.png)

    If you changed anything,do not forget to restart a service

17. Now, You can run the jenkins job & check the console output

    ![Alt text](jen/17.png)
    ![Alt text](jen/18.png)
    
    
    
    
