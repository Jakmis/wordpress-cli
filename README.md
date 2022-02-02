Automate your WordPress development workflow.
# INSTALL 
git clone https://github.com/petrgru/wordpress-docker

cd wordpress-docker

cp env.config .env

nano .env #change what is need password!!!!!!!!

# INSTALL WORDPRESS BY CLI
docker-compose run -rm wpcli wp core install

# BACKUP WORDPRESS BY CLI
docker-compose exec -it [db] mysqldump -u [user] -p[password] [database] > [file.sql]

# BACKUP FILE SYSTEM
tar cvfz wordpress.tar.gz build/wordpress

# RESTORE FILE SYSTEM
tar xvfz wordpress.tar.gz -C build/wordpress
