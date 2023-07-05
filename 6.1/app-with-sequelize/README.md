docker container run --name container-mysql -e MYSQL_ROOT_PASSWORD=senha_mysql -d -p 3306:3306 mysql:8.0.29

env $(cat .env) npx sequelize db:create

docker exec -it container-mysql bash

mysql -u root -p

show databases;