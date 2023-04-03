# goCrud

Golang CRUD

TO Execute

docker run --name postgres -e POSTGRES_HOST_AUTH_METHOD=trust -p 5432:5432 -d postgres

psql -h localhost -p 5432 -U postgres -c "CREATE USER golang WITH PASSWORD 'golang';"
psql -h localhost -p 5432 -U postgres -c "CREATE DATABASE golang;"
psql -h localhost -p 5432 -U postgres -c "ALTER DATABASE golang OWNER TO golang;"
psql -h localhost -p 5432 -U postgres -c "GRANT ALL PRIVILEGES ON DATABASE golang TO golang;"
psql -h localhost -p 5432 -U golang -d golang -W -c "CREATE TABLE users (id SERIAL PRIMARY KEY, name TEXT, email TEXT);"


go run main.go