## DOCKER API WITH FLASK

#### ENDPOINTS:





- __route("/")==> index__
  

-  __route("/images")==> list_images__
    


- __route("/containers")==> list_containers__
   


- __route("/container/stats")==> container_stats__
   

- __route("/container/run")==> run_container__

    arguments:
    
        name: String
        
        image: String
        
        version: String optional [ default: latest ]


- __route("/networks")==> container_networks__
   

- __route("/network/create")==> container_network_create__

  arguments:
  
      name: String
      
      driver_name: String optional [ default: 'bridge' ]
    


- __oute("/volumes")==> container_volumes__



- __route("/volume/create")==> container_volume_create__

  arguments:
  
      name: String
      
      driver_name: String optional [ default: 'local' ]




- __route("/image/search")==> image_search__

  arguments:
  
      name: String

  
    
- __route("/container/stop")==> container_stop__

  arguments:
  
      name: String
    
    
    
- __route("/container/remove")==> container_remove__

  arguments:
  
      name: String
    
    
- __route("/container/remove/all")==> container_remove_all__



 for example: 
 
 http://IP:5000/containers : to list all running containers
 
 http://IP:5000/container/run?name=my-con&image=centos : with argument to run the my-con container from centos image
