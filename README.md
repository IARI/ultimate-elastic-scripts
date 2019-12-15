# ultimate-elastic-scripts

This repository contains a set of configuration scripts for elastic stack components
to analyze Ultimate logs and corresponding Benchexec scripts.   
The setp process is described below. 

## Installation (elastic stack)
The following four components from the elastic stack are required to be installed.
(Get the latest version - 7.5 as of december 2019 - of the components at the corresponding links below) 

* Elasticsearch:  
https://www.elastic.co/downloads/elasticsearch
* Kibana  
https://www.elastic.co/downloads/kibana
* Logstash  
https://www.elastic.co/downloads/logstash
* Filebeat  
https://www.elastic.co/downloads/beats/filebeat

Unpack the contents of the archives to your preferred installation-path. 

## Configuration Files

Dor each of the above components, place the configuration files 
from below the `/config` directory of this repository at the following locations:

* Elasticsearch:  
TODO: ...
* Kibana  
TODO: ...
* Logstash  
TODO: ...
* Filebeat  
TODO: ...

## Test data
The following datasets are used for testing the setup:

1. https://struebli.informatik.uni-freiburg.de/logs/index.php?dir=manual-svcomp-automizer/20190114-110636-manual-svcomp-automizer-0ed9222f2a  

2. https://struebli.informatik.uni-freiburg.de/logs/index.php?dir=manual-svcomp-automizer/20190102-120200-manual-svcomp-automizer-2e94e6aad8-M


## Start the Services

The binaries for the tools are located in the `bin/` (except for filebeat where they are directly on the root level)

* Elasticsearch:  
```
elasticsearch
```
* Kibana
```
kibana.bat
```
* Logstash  
```
logstash.bat -f ..\config\logstash-ultimate.conf
```
* Filebeat  
```
filebeat.exe
```


## Delete data

* Delete all logstash data:
```
curl -XDELETE localhost:9200/logstash*
```
* Delete filebeat registry:
```
rm data\registry data\registry.old```
