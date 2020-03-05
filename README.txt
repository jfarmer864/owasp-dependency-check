
This project uses the Dependency Check image from OWASP to scan an intentionally
vulnerable application (WebGoat) and post the results on a browser page

how to run:
vagrant up and vagrant ssh into the virtual machine

to get the program we need to scan we use:
- wget https://github.com/WebGoat/WebGoat/releases/download/v8.0.0.M21/webgoat-server-8.0.0.M21.jar
 into the /home/ubuntu/dependency-check folder next to new-check.sh

to run the dependency check we use:
- sudo sh /home/ubuntu/dependency-check/new-check.sh

we then follow the path ~/OWASP-Dependency-Check/reports to find our reports,
we will be using the html version

once inside the reports folder we use
- sudo cp dependency-check-report.html /var/www/html
which will let our apache web server use this html as a page

to access the page on the browser we use 
- http://192.168.6.12/dependency-check-report.html
