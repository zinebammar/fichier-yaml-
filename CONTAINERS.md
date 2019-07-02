## Using Docker Compose

Make sure you have docker installed lcoally as well as the docker-compose utility. You can find more information about docker-compose at this link:

https://docs.docker.com/compose/install/

You want to have the latest 1.23.x installed. 

## USAGE

To initially get the images down, you need to run this command.  

```
    docker-compose up --no-start
```

This will download and create all the containers locally from the images downloaded.  

When you are ready to start the containers, use this command:

```
    docker-compose start
```

Conversely when you want to stop them, you can use this command globally:

``` 
    docker-compose stop
```

To view logs, for all the containers, you can use this command:

```
   docker-compose logs
```

Since we specified service names in the docker-comppose.. any of the start, stop, logs commands can be isolated to a particular service by using the following syntax:

```
   docker-compose start [service]
   docker-compose stop [service]
   docker-compose logs [service]
```

Where service can be either of these values:  **msdata | mscompotes | mscredits | mstransactions**

