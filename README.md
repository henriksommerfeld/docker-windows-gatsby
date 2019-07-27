# Personal Website for Isabel Sommerfeld
Personal website based on GatsbyJS

## Docker
Optional Docker image to use for development. This assumes Windows, where the Docker image is used to get around Windows awkwardness.

### Build
Build the image with `cd scripts; docker build --rm -f Dockerfile -t ubuntu:gatsby .`

### Install zsh theme
Run the image and configure additional settings: 
`docker run --rm -it ubuntu:gatsby`

In the running container:
1. `cd ~`
2. `wget https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O - | zsh`
3. `zsh`
4. Verify that it works as expected

### Persist snapshot (from host)
1. `docker container ls -a`
2. Find the _container id_ for the latest created
2. `docker commit [container id] ubuntu:gatsby-developer`

### Run the image
To run the _ubuntu:gatsby-developer_ image:
* On Linux/MacOS `npm run docker:run`.
* On Windows: `npm run win:run`.

### Watching file changes on Windows
`npm run win:watch`