# MobileGame #

In this file, I analyzed the usage frequency of partners within the first 15 days. Initially, I imported additional dataset where I added the minimal start usage dates of the game by partners. Subsequently, I created a new dataset using this newly added information, and I removed the "Date" column using the following steps:

First, I grouped the data by 'Game Name' and 'Partner Group', calculated the minimum usage date, and retained the 'Players' and 'Date' columns using the code:

oyun1 = oyun_csv %>%
  group_by(`Game Name`, `Partner Group`) %>%
  summarise(min_date = min(Date), Players, Date)
Then, I calculated the 'ferq' (difference in days) by subtracting 'min_date' from 'Date' with the following code:


oyun1$ferq = oyun1$Date - oyun1$min_date
I then created a new dataset ('Ferq') to display the day intervals. Finally, to keep only the partners who used the game within the first 14 days, I filtered the data using the code:


oyun1_filtered = oyun1 %>% filter(ferq > 14)
By adding this data to Power BI, I'm showing you the results.

Please note that this analysis aimed to retain only those partners who engaged with the game for the first 14 days, and it's visualized in Power BI.





. ![image](https://github.com/arazgarayev/MobileGame/assets/124186024/aa1d464b-33d4-4450-bbbe-4683c8b2ba7c)
