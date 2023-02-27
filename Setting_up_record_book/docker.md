**Code used: **

`docker load -i ~/Desktop/bioinfo_PartI-PartII-PartIII1-3.tar.gz  `


<img width="569" alt="image" src="https://user-images.githubusercontent.com/111068556/221463100-bec10f16-9dee-42b7-a4fc-f65ea14c4624.png">



`mkdir ~/Users/silaschw/Desktop/silas_bioinfo_tsinghua_share`

`docker run --name=sunchuhanwen_linux -dt  -h bioinfo_docker --restart unless-stopped -v ~/Users/silaschw/Desktop/silas_bioinfo_tsinghua_share:/home/test/share xfliu1995/bioinfo_tsinghua:2`

<img width="571" alt="image" src="https://user-images.githubusercontent.com/111068556/221463141-41ca8b24-664e-4a4b-b34a-90d7c2cad75f.png">


`docker exec -it sunchuhanwen_linux bash`

<img width="565" alt="image" src="https://user-images.githubusercontent.com/111068556/221463167-42dfad39-562c-4d66-9f78-c14482964ebc.png">


`exit`

<img width="315" alt="image" src="https://user-images.githubusercontent.com/111068556/221463188-487ea49f-ded4-4651-8665-06a07410580d.png">


