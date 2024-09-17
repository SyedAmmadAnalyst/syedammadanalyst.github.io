# Data Protfolio


![excel-sql-power bi](assets/images/kaggle_to_powerbi.gif)

# Table of Content

-  [Project 1](#Project-1)
  -  [Subheader]()
-  [Project 2](#Project-2)
-  [Project 3](#Project-3)

```sql
/*
# Data cleaning steps
1. Remove unnecesary columns by only selecting the ones we need
2. Extract the YouTube channel name from the first column.
3. Rename the column names
*/
--SELECT 
--	NOMBRE,
--	total_subscribers,
--	total_views,
--	total_videos
--FROM
--	top_uk_youtubers_2024

--CHARINDEX
```
```sql
SELECT CHARINDEX ('@', NOMBRE),NOMBRE FROM top_uk_youtubers_2024

--SUBSTRING
CREATE VIEW view_uk_youtubers_2024 AS 
SELECT CAST(SUBSTRING(NOMBRE,1,CHARINDEX ('@', NOMBRE)-1) AS varchar (100)) AS channel_name,
	total_subscribers,
	total_views,
	total_videos
FROM top_uk_youtubers_2024
```

## 1. Who are the top 10 youtuber with the most subscribers

| Rank | Channel Name | Subscribers |
| 1  |  NoCopyrightSounds  |	33600000  |
| 2  | DanTDM |28600000|
| 3  |  Dan Rhodes  |26500000|
| 4  | Miss Katy |24500000|
| 5  | Mister Max |24400000|
| 6  | KSI |24100000|
| 7  | Jelly |23500000|
| 8  | Dua Lipa |23300000|
| 9  | Sidemen |21000000|
| 10  | Ali-A |18900000|
