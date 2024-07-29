# Queuing System in JS

This project focuses on building a queuing system using Node.js, Redis, and Kue. The project encompasses setting up Redis, using Redis with Node.js for various operations, and integrating a queuing system using Kue.

## Table of Contents

- [Curriculum](#curriculum)
- [Resources](#resources)
- [Learning Objectives](#learning-objectives)
- [Requirements](#requirements)
- [Required Files](#required-files)
- [Tasks](#tasks)
- [Contributing](#contributing)
- [License](#license)

## Curriculum

### Short Specializations
- **Back-end**
- **JavaScript**
- **ES6**
- **Redis**
- **NodeJS**
- **ExpressJS**
- **Kue**

**Project Weight:** 1  
**Start Date:** July 29, 2024  
**End Date:** August 1, 2024  

## Resources

Read or watch:

- [Redis quick start](https://redis.io/docs/getting-started/)
- [Redis client interface](https://redis.io/docs/clients/)
- [Redis client for Node JS](https://github.com/NodeRedis/node-redis)
- [Kue](https://github.com/Automattic/kue) (deprecated but still used in the industry)

## Learning Objectives

By the end of this project, you should be able to:

- Run a Redis server on your machine.
- Perform basic operations using the Redis client.
- Use a Redis client with Node.js for basic operations.
- Store hash values in Redis.
- Handle async operations with Redis.
- Use Kue as a queue system.
- Build a basic Express app interacting with a Redis server.
- Build a basic Express app interacting with a Redis server and queue.

## Requirements

- Your code will be compiled/interpreted on Ubuntu 18.04, Node 12.x, and Redis 5.0.7.
- All files should end with a new line.
- A `README.md` file at the root of the project folder is mandatory.
- Your code should use the `.js` extension.

## Required Files

- `package.json`
- `.babelrc`

Ensure to run `$ npm install` when you have the `package.json` file.

## Tasks

### Task 0: Install a Redis instance

Download, extract, and compile the latest stable Redis version:

```bash
$ wget http://download.redis.io/releases/redis-6.0.10.tar.gz
$ tar xzf redis-6.0.10.tar.gz
$ cd redis-6.0.10
$ make
```

Start Redis in the background:

```bash
$ src/redis-server &
```

Verify the server is working:

```bash
$ src/redis-cli ping
PONG
```

Set and get a value using Redis client:

```bash
127.0.0.1:[Port]> set Holberton School
OK
127.0.0.1:[Port]> get Holberton
"School"
```

Kill the server:

```bash
$ kill [PID_OF_Redis_Server]
```

Copy the `dump.rdb` file to the root of the Queuing project.

### Task 1: Node Redis Client

Install `node_redis` using npm and create a script `0-redis_client.js` to connect to the Redis server.

### Task 2: Node Redis Client and Basic Operations

Create a script `1-redis_op.js` to perform basic operations like setting and getting values in Redis.

### Task 3: Node Redis Client and Async Operations

Create a script `2-redis_op_async.js` to use `promisify` for async/await operations.

### Task 4: Node Redis Client and Advanced Operations

Create a script `4-redis_advanced_op.js` to store and display hash values in Redis.

### Task 5: Node Redis Client Publisher and Subscriber

Create two scripts `5-subscriber.js` and `5-publisher.js` to handle message publishing and subscribing.

### Task 6: Create the Job Creator

Create a script `6-job_creator.js` to create jobs in the queue with Kue.

### Task 7: Create the Job Processor

Create a script `6-job_processor.js` to process jobs from the queue with Kue.

### Task 8: Track Progress and Errors with Kue: Create the Job Creator

Create a script `7-job_creator.js` to create multiple jobs and track their progress.

### Task 9: Track Progress and Errors with Kue: Create the Job Processor

Create a script `7-job_processor.js` to process jobs and handle blacklisted phone numbers.

## Contributing

Please fork the repository and create a pull request for any changes you'd like to make. Ensure your changes are well-documented and include relevant test cases.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Happy coding!
