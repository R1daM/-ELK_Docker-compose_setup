1. docker-compose
      docker-compose up -d 
2. login into elasticsearch container :
      docker exec -it -u 0 id_container bash
3. enable xpack in elasticsearch.yml :
    check the elasticsearch.yml file in this repository
4. Setup default user passwords :
    cd /usr/share/elasticsearch/bin
    sudo ./elasticsearch-setup-passwords auto #make sure to save all those passwords on a safe place !!
5. run this command : 
    curl -XGET -u elastic:Wu7zEqYfm5SAQVrvGQVE http://host_ip:9200/_cluster/health?pretty 
6. Add the default username in kibana.yml file 
    elasticsearch.username: "kibana"
    elasticsearch.password: "new_password" #you will find this password in 4th step !
7. let's see if this is working or not :
    run http://localhost:5601 on your browser


    !! restart your containers after any changes !! 


