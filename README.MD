# Template order.stickys.com

## Setup development environment with docker
  1. Install Docker for Ubuntu server ([https://docs.docker.com/install/linux/docker-ce/ubuntu/](https://docs.docker.com/install/linux/docker-ce/ubuntu/))
      - Set up the repository
        ```bash
        sudo apt-get update
        sudo apt-get install apt-transport-https ca-certificates curl gnupg-agent software-properties-common
        curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
        sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
        ```

      - Install docker engine
        ```bash
        sudo apt-get update
        sudo apt-get install docker-ce docker-ce-cli containerd.io
        docker --version # For testing, docker installed.
        ```
  2. Install Docker Compose ([https://docs.docker.com/compose/install/](https://docs.docker.com/compose/install/))
      ```bash
      sudo curl -L "https://github.com/docker/compose/releases/download/1.24.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
      sudo chmod +x /usr/local/bin/docker-compose
      docker-compose --version # For testing, docker-compose installed.
      ```
  3. Create and start containers
      ```bash
      docker-compose up --build --detach
      ```
  4. Test app
      ```bash
      Go to http://localhost
      ```

  5. Stop and remove containers
      ```bash
      docker-compose down --volume
      ```
