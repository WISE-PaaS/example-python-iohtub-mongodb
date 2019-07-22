# Example-python-Iothub-MongoDB


This is WIES-PaaS example-code include the mongodb and rabbitmq service。

**https://wise-paas.advantech.com/en-us**

## Quick Start

    git clone this respository
    
    #cf login -skip-ssl-validation -a {api.domain_name}  -u "account" -p "password"
    
    cf login –skip-ssl-validation -a api.wise-paas.io -u xxxxx@advtech.com.tw -p xxxxxx
    
    #check the cf status
    cf target


open the **`manifest.yml`** and editor the application name to yours，because the appication can't duplicate。

(you need to check the service name in `index.py` and WISE-PaaS)
![https://github.com/WISE-PaaS/example-python-iohtub-mongodb/blob/master/source/service-name.PNG](https://github.com/WISE-PaaS/example-python-iohtub-mongodb/blob/master/source/service-name.PNG)
![https://github.com/WISE-PaaS/example-python-iohtub-mongodb/blob/master/source/code_image.PNG](https://github.com/WISE-PaaS/example-python-iohtub-mongodb/blob/master/source/code_image.PNG)

    #cf push {application name}
    cf push python-demo-mongodb
    
    #get the application environment
    cf env {application name} > env.json 
    
    
Edit the **publisher.py** `broker、port、username、password` you can find in env.json

* bokrer:"VCAP_SERVICES => p-rabbitmq => externalHosts"
* port :"VCAP_SERVICES => p-rabbitmq => mqtt => port"
* username :"VCAP_SERVICES => p-rabbitmq => mqtt => username"
* password: "VCAP_SERVICES => p-rabbitmq => mqtt => password"

open two terminal
    
    #cf logs {application name}
    cf logs python-demo-mongodb

.

    python publisher.py

![https://github.com/WISE-PaaS/example-python-iohtub-mongodb/blob/master/source/ALREADY.PNG](https://github.com/WISE-PaaS/example-python-iohtub-mongodb/blob/master/source/ALREADY.PNG)

![https://github.com/WISE-PaaS/example-python-iohtub-mongodb/blob/master/source/TEMP.PNG](https://github.com/WISE-PaaS/example-python-iohtub-mongodb/blob/master/source/TEMP.PNG)

# Step By Step Tutorial

[https://github.com/WISE-PaaS/example-python-iohtub-mongodb/blob/master/source/README.md](https://github.com/WISE-PaaS/example-python-iohtub-mongodb/blob/master/source/README.md)
