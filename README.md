# n8n with PostgreSQL

Starts n8n with PostgreSQL as database.

## Start

To start n8n with PostgreSQL simply start docker-compose by executing the following
command in the current folder.

**IMPORTANT:** But before you do that change the default users and passwords in the [`.env`](.env) file!

```
docker-compose up -d
```

To stop it execute:

```
docker-compose stop
```

## Configuration

The default name of the database, user and password for PostgreSQL can be changed in the [`.env`](.env) file in the current directory.

Verify that pgvector is installed by connecting to your PostgreSQL database:

```
docker-compose exec postgres psql -U postgres -d n8n -c "SELECT * FROM pg_extension WHERE extname = 'vector';"
```

## To install ollama tool

Run this CMD:

```
curl -fsSL https://ollama.com/install.sh | sh
```

Check ollam version:

```
ollama -v
```

Download llama3 with 3B parameters:

```
ollama pull llama3.2:3b
```

Download qwen2.5 with 7B parameters:

```
ollama pull qwen2.5:7b
```

To check ollama model list:

```
ollama list
```
