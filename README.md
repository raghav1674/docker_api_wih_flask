DOCKER API WITH FLASK

ENDPOINTS:





route("/")==> index
  

route("/images")==> list_images
    


route("/containers")==> list_containers
   


route("/container/stats")==> container_stats
   

route("/container/run")==> run_container
arguments:
    name: String
    image: String
    version: String optional [ default: latest ]


route("/networks")==> container_networks
   

route("/network/create")==> container_network_create
arguments:
    name: String
    driver_name: String optional [ default: 'bridge' ]
    


route("/volumes")==> container_volumes



route("/volume/create")==> container_volume_create
arguments:
    name: String
    driver_name: String optional [ default: 'local' ]




route("/image/search")==> image_search
arguments:
    name: String
  
  
    
route("/container/stop")==> container_stop
arguments:
    name: String
    
    
    
route("/container/remove")==> container_remove
arguments:
    name: String
    
    
route("/container/remove/all")==> container_remove_all
