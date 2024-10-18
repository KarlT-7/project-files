run the following on a new VM instance:

Step 1:
sudo snap install docker

Step 2:
*upload docker-compose.yml, hadoop.env (to new .project-files directory) and data files (to new /data directory) supplied in my submission zip*

Step 2 (alternative):
git clone https://github.com/KarlT-7/project-files.git && cd project-files

Step 3:
sudo docker-compose up -d

Step 4:
sudo docker exec <namenode_container> hdfs dfs -put /home/data/ufc_event_data.csv /ufc_event_data.csv
sudo docker exec <namonode_container> hdfs dfs -put /home/data/ufc_fight_data.csv /ufc_fight_data.csv
sudo docker exec <namenode_container> hdfs dfs -put /home/data/ufc_fight_stat_data.csv /ufc_fight_stat_data.csv
sudo docker exec <namenode_container> hdfs dfs -put /home/data/ufc_fighter_data.csv /ufc_fighter_data.csv

Step 5:
*visit http://<external_ip>:8888 and then upload project.ipynb supplied in zip file and run
