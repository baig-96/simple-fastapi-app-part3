# Assignment1-Part-3
First Assignment Part3 Attempt

1. Docker Volume Created	C:\Users\Hassan IPRI\Documents\DevOps Class lab\Assignment 1\Part3>docker volume create my_volume
   
2. Docker Container mount with Docker Volume	C:\Users\Hassan IPRI\Documents\DevOps Class lab\Assignment 1\Part3>docker run --name new_container -v my_volume:/usr/share/nginx/html my_1st_nginx
3. C:\Users\Hassan IPRI\Documents\DevOps Class lab\Assignment 1\Part3>docker cp ./index.html new_container:/usr/share/nginx/html
Successfully copied 2.05kB to new_container:/usr/share/nginx/

4. http://localhost:8080
   Welcome to my Docker Project!
Today's Date and Time is: 13/11/2023, 13:12:32

5. Stop & Remove the Container C:\Users\Hassan IPRI>docker rm my_container2
my_container2

6. HTTPD image created my-apache3, default http://localhost:8081 is running, Created "about.html", Copy the "about.html" and mounted with my_volume, http://localhost:8081/about.html is running properly
   docker run -d -p 8081:80 -v my_volume:/usr/local/apache2/htdocs --name my_apache1 my-apache3
3b5a1c1f73237354e2b26f0caaa0f5e86e41ff911fbc4114f086934a243d11d0

7. Docker stopped and removed
C:\Users\Hassan IPRI\Documents\Httpd\public-html>docker stop my_apache1
my_apache1
C:\Users\Hassan IPRI\Documents\Httpd\public-html>docker rm my_apache1
my_apache1

8. "index.html" and "about.html" files are still available in the "my_volume" volume
   Volume deleted
10. Docker Volume Deleted
    docker volume rm my_volume
my_volume
