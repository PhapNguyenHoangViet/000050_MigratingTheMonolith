+++
title = "Setup the Database"
date = "`r Sys.Date()`"
weight = 4
chapter = false
pre = "<b>2.4. </b>"
+++

#### Setup the Database
1. Connect to the Windows Instance, open the command prompt
2. Execute the below command, change **<rds_host>** by **RDS endpoint**
```
mysql -u root --password=labpassword -h <rds_host>
```


3. Execute the below command to select the database named **travelbuddy**
```
use travelbuddy
```

4. Execute the below command to watch the tables in the database.
```
show tables;
```

- We will see 2 tables in the database