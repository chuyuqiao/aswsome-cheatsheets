# 以Ubuntu 14.04 为准 #
## 安装jdk 1.8.0_131  ##
1. [下载jdk 1.8.0_131](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
2. 下载安装elasticsearch

    	curl -L -O https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-5.5.2.tar.gz

    	tar -xvf elasticsearch-5.5.2.tar.gz

    	cd elasticsearch-5.5.2/bin

    	./elasticsearch -Ecluster.name=pof -Enode.name=ip