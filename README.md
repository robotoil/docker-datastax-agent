# docker-datastax-agent

Docker image of DataStax Agent for use with Cassandra and OpsCenter

Running
-------

DataStax Agent needs read access to Cassandra's configuration file (/etc/cassandra/cassandra.yaml) and Cassandras data directory (/var/lib/cassandra).

Start the offical Cassandra container

    docker run -d -v /etc/cassandra/cassandra.yaml:/etc/cassandra/cassandra.yaml -v /var/lib/cassandra:/var/lib/cassandra cassandra
    
then start DataStax Agent

    docker run -d -v /etc/cassandra/cassandra.yaml:/etc/cassandra/cassandra.yaml -v /var/lib/cassandra:/var/lib/cassandra kapschtrafficcom/datastax-agent
