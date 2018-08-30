### Step-1: Install docker engine.

   [Dokcer-Installation-Ubuntu](https://github.com/DevOpsBasicSetup/Phase-2/blob/master/Docker/DockerEngine/2.1.Dokcer-Installation-Ubuntu.md)

### Step-2: Install docker-compose.

  [Dokcer-compose-Installation-Ubuntu](https://github.com/DevOpsBasicSetup/Phase-2/blob/master/Docker/DockerCompose/Installation-and-example-1.md)

### Step-3: Install docker-machine.

  [Dokcer-Machine-Installation-Ubuntu](https://github.com/DevOpsBasicSetup/Phase-2/blob/master/Docker/DokcerMachine/Installation-and-example.md)

##### 3.1. Create 2 docker hosts using docker-machine.
  
      docker-machine create --driver amazonec2 --amazonec2-access-key AKI********** --amazonec2-secret-key UeI4G**********ots7z9Xo --amazonec2-region us-east-2 --amazonec2-zone "b" docker-w-1

      docker-machine create --driver amazonec2 --amazonec2-access-key AKI********** --amazonec2-secret-key UeI4G**********ots7z9Xo --amazonec2-region us-east-2 --amazonec2-zone "c" docker-w-2

    * docker-machine ls

### Step-3: Swam mode:

    docker swarm init --advertise-addr 18.218.203.69

    docker node ls

    docker-machine ssh docker-w-1

    sudo -i

    docker swarm join --token SWMTKN-1-0c62o5bu8cuhgtwnw5ja5ohiju3vsec7h4lwdldc0toxmqr3a2-2ktuqceisbznx1c1mmvbmanzh 18.218.203.69:2377

    exit
    exit

    docker-machine ssh docker-w-2

    sudo -i

    docker swarm join --token SWMTKN-1-0c62o5bu8cuhgtwnw5ja5ohiju3vsec7h4lwdldc0toxmqr3a2-2ktuqceisbznx1c1mmvbmanzh 18.218.203.69:2377

    exit
    exit


    docker node ls
    
    Now the current mjachine is acting as a leader.
    

### Step-4: docker stack:

