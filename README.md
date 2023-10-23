# MobileGame #

Bu dosyada partnerlerin ilk 15 gun icerisine kullanim sikligini analiz ettim. 
Dosyada ilk olarak ek veri kumesi actim, buraya oyunun partnerler tarafindan minimal baslangic kullanim tarihlerini ekledim.
daha sonra yarattigim bu yeni kume ile date kumesini ciktim, "1)oyun1=oyun_csv %>% group_by(`Game Name`,`Partner Group`) %>% summarise(min_date=min(Date),Players,Date),2)oyun1$ferq=oyun1$date-oyun1$min_date".
Aldigim bu sonuclari gostermek icin yeni bir kume actim(Ferq) , Burada gun araliklarini gosterdim. 
Son olarak "oyun1_filtered = oyun1 %>% filter(ferq > 14)" 14 gune kadar olan partnerleri kumede tutmak icin filterledim. 
Power Bi ekleyerek sonucu size gosteriyorum . ![image](https://github.com/arazgarayev/MobileGame/assets/124186024/aa1d464b-33d4-4450-bbbe-4683c8b2ba7c)
