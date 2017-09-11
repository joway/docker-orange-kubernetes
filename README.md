# Orange in Kubernetes 


## Get Start

> you need to set env : ORANGE_DB_SETUP when first start 

    ```bash
    docker run -d --name orange \
        --link orange-database:orange-database \
        -p 7777:7777 \
        -p 8888:80 \
        -p 9999:9999 \
        --security-opt seccomp:unconfined \
        -e ORANGE_DATABASE={your_database_name} \
        -e ORANGE_HOST=orange-database \
        -e ORANGE_PORT={your_database_port} \
        -e ORANGE_USER={your_database_user} \
        -e ORANGE_PWD={your_database_password} \
        -e ORANGE_DB_SETUP=true \
        syhily/orange
    ```
