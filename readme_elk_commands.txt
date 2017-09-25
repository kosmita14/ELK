sudo /usr/share/logstash/bin/logstash --path.settings /etc/logstash -f ./conf.d
sudo /usr/share/logstash/bin/logstash --path.settings /etc/logstash -f ./conf.d/nfchce-logstash.conf
sudo /usr/share/logstash/bin/logstash --path.settings /etc/logstash -f ./conf.d/mb-logstash.yml -w 1


sudo /usr/share/filebeat/bin/filebeat -c ./filebeat/filebeat.yml 
sudo /usr/share/filebeat/bin/filebeat -c ./filebeat/filebeat.yml -once
sudo /usr/share/filebeat/bin/filebeat -path.home=/usr/share/filebeat -path.config=/home/pi/Dokumenty/logi/filebeat -c filebeat_mb.yml -e -once




sudo rm /usr/share/filebeat/bin/data/registry
