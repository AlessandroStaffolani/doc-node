# DOC

[![Join the chat at https://gitter.im/doc-node/community](https://badges.gitter.im/doc-node/community.svg)](https://gitter.im/doc-node/community?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Node service to execute backup 

### Set up
To start the node:

1. clone the repository
2. install node modules
3. start the server

```
# clone
git clone https://github.com/ale8193/doc-node.git
cd doc-node

# install dependences
yarn install

# start server
yarn start
```

### Generate documentation
##### Code documentation
The documentation of the code will be generated inside `<project_root>/docs`using the following command:
```
yarn docs
```
##### Swagger api documentation
The `swagger.yml` with the openapi documentation is provided inside the root of the project.

### Run on docker
Firstly, build the image:
```
docker build -t doc-node .
```
Secondly, run the container:
```
docker run -d --name doc-node -p 5555:5555 -v /var/run/docker.sock:/var/run/docker.sock doc-node
```
