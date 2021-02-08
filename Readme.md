# DemoDb

.
## Requirements
* Docker
* Docker hub

## How to run the databse  ?

 1- To build  the database image  type  *`docker build -t demo-db .`*

 note : the default  credentials are  `username:demo` `password :demo`  `databsename : postgres`exposed on the adress :`0.0.0.0:5432` you can change them in the docker file if you want

 2- To run the database after the build type :
 *`docker run --name DemoDb   -p 5432:5432  -d demo-db`*

 3-  To enter to the container after the run type :  *`docker exec -it DemoDb  bash  `*


## Update database image on the registry ?

* After you build the image 

* ` docker login registry.gitlab.com `

* ` docker docker tag demo-db registry.gitlab.com/master-thesis8/database `

* ` docker push registry.gitlab.com/master-thesis8/database `

## Pull new version of the database 

* ` docker login registry.gitlab.com `

* ` docker pull registry.gitlab.com/master-thesis8/database `