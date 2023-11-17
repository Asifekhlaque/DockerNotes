# DockerNotes
<img src="https://github.com/Asifekhlaque/DockerNotes/assets/132199879/f20f4255-10d6-4bae-947e-e49f2fde79ad">
<h1>What is Docker?</h1>
<ul>
  <li>Docker is a software platform that allows you to build, test, and deploy applications quickly. </li>
  <li>It’s a client site application programme and it’s a service where you can deploy your code to any place or server.</li>
  <li>Docker packages software into standardized units called containers that have everything the software needs to run including libraries, system tools, code, and runtime.</li>
</ul>
<h1>Important command used in Docker are: -</h1>

   <ol>
     <li>docker run (Image Name): Install the docker image</li>
     <li>docker run -d -p 8080:80 (Image Name): Map it to this local port</li>
     <li>docker ps: How many docker program run in the background</li>
     <li>docker stop (Container ID): Stop the docker file</li>
     <li>docker ps -a: Show all the docker container if it is running or stop</li>
   </ol>  

<h1>How to make Docker image?</h1>
<b>Step 1:</b> Open docker on your desktop
<img src="https://github.com/Asifekhlaque/DockerNotes/assets/132199879/9ac039ef-655e-4cd6-848a-5cac4166d3c2" >

<b>Step 2:</b> Make a folder and write your html content and also make Dockerfile

# Docker File content:

      FROM redhat/ubi8

      LABEL maintainer="IIBM Patna"

      RUN yum -y install httpd

      COPY index.html /var/www/html

      ENTRYPOINT ["/usr/sbin/httpd", "-D", "FOREGROUND"]

      EXPOSE 80

<b>Step 3:</b>

     docker build -t (imagenameallareinsmallletter) .
<img src="https://github.com/Asifekhlaque/DockerNotes/assets/132199879/ac432497-1ed8-4b3f-8b32-effbfd5ef571">

And your docker file will upload 🎉🎉🎉

<b>Step 4:</b> For hosting your docker image

     docker run -d -p 8080:80 (Image Name)

For stop it 

    docker stop (Container ID) 
