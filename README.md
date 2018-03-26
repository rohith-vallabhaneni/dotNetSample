# dotNetSample

To run this application using docker, the docker version should be greater than 14.0 as I'm using docker multi-stage build.

Run the following commands:

    sudo docker build -t sample .
    sudo docker images
  
To run the image, use any of the following

    docker run -itd -e PORT=30001 -p 30001:30001 sample
   -Your application will run on 30001
        
    curl localhost:30001/api/values
   
   --------------------------------------------------------------
   
    docker run -itdP -e PORT=30001 --expose 30001 sample
  
    docker ps 
   
   - find the port on which your application is running
      
          curl localhost:{port_assigned_by_docker}/api/values
