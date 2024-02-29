## Working with Postgresql on Al23 Container

Image used : `public.ecr.aws/amazonlinux/amazonlinux:2023`

- Pull the image and Start the Container

        docker pull public.ecr.aws/amazonlinux/amazonlinux:2023

        docker run -it --name amazonlinux public.ecr.aws/amazonlinux/amazonlinux:2023 /bin/bash

- Installing Postgres

        dnf update -y

        dnf install -y postgresql15.x86_64 postgresql15-server postgresql-devel


- Configuring postgres 
  
        #login as Potsgres user
        su postgres

        #initializing the data dir
        initdb -D /var/lib/pgsql/data

        #creating the Log file
        touch /var/lib/pgsql/logfile
        chmod 666 /var/lib/pgsql/logfile

        #Starting the Server
        pg_ctl -D /var/lib/pgsql/data -l /var/lib/pgsql/logfile start


- Start working 

        psql




