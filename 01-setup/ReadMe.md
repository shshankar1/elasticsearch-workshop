# Setup Steps:
* Install docker desktop https://docs.docker.com/desktop/install/windows-install/
* Optional Step: install github CLI to run docker commands manually.
* Follow instructions for installation: 
  https://www.elastic.co/guide/en/elasticsearch/reference/current/run-elasticsearch-locally.html <br/>
  <b>[Note: please go through the steps first before running any command as kibana enrollment token remain valid only for 30 mins.]</b>
* Final output of docker run command should look like below:

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
✅ Elasticsearch security features have been automatically configured!
✅ Authentication is enabled and cluster connections are encrypted.

ℹ️  Password for the elastic user (reset with `bin/elasticsearch-reset-password -u elastic`):
WZOYT5*ZPi+9f9vbccAK

ℹ️  HTTP CA certificate SHA-256 fingerprint:
db29843682549173e961d9da4648c2fe9cfd7ece0e11e68f2bd13a7c2d8b8dd7

ℹ️  Configure Kibana to use this cluster:
• Run Kibana and click the configuration link in the terminal when Kibana starts.
• Copy the following enrollment token and paste it into Kibana in your browser (valid for the next 30 minutes):
eyJ2ZXIiOiI4LjExLjMiLCJhZHIiOlsiMTcyLjE4LjAuMjo5MjAwIl0sImZnciI6ImRiMjk4NDM2ODI1NDkxNzNlOTYxZDlkYTQ2NDhjMmZlOWNmZDdlY2UwZTExZTY4ZjJiZDEzYTdjMmQ4YjhkZDciLCJrZXkiOiI4b05WeFl3Qk5VLUlHdklLUTZKZjp6ZldJaHJkSFRCT09xaHM0WE9MNXFRIn0=

ℹ️ Configure other nodes to join this cluster:
• Copy the following enrollment token and start new Elasticsearch nodes with `bin/elasticsearch --enrollment-token <token>` (valid for the next 30 minutes):
eyJ2ZXIiOiI4LjExLjMiLCJhZHIiOlsiMTcyLjE4LjAuMjo5MjAwIl0sImZnciI6ImRiMjk4NDM2ODI1NDkxNzNlOTYxZDlkYTQ2NDhjMmZlOWNmZDdlY2UwZTExZTY4ZjJiZDEzYTdjMmQ4YjhkZDciLCJrZXkiOiI4NE5WeFl3Qk5VLUlHdklLUTZKbjpwemY4UTFndVM1V2ZMQmtfYXAwR0pRIn0=

If you're running in Docker, copy the enrollment token and run:
`docker run -e "ENROLLMENT_TOKEN=<token>" docker.elastic.co/elasticsearch/elasticsearch:8.11.3`
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
* Run below docker command to bring up kibana image: <br/>
  docker pull docker.elastic.co/kibana/kibana:8.11.3
  docker run --name kibana --net elastic -p 5601:5601 docker.elastic.co/kibana/kibana:8.11.3 
  
Final output should look like this:
2024-01-01 19:40:21 i Kibana has not been configured.
2024-01-01 19:40:21
2024-01-01 19:40:21 Go to http://0.0.0.0:5601/?code=258982 to get started.
2024-01-01 19:40:21
2024-01-01 19:40:21