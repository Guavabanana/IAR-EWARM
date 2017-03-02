# IAR-EWARM

Tips about IAR EWARM
==========================


Project & Workspace Rename IAR 專案重新命名
-----------------------------------------

Tools:  IAR-EWARM and Sublime Text 2 or 3


Goal:   Given that we have a IAR project called "sample1", we want to rename the project as "sample2" and keep the project work well as usual.  


修改IAR專案“sample1"名稱為“sample2",且專案依舊能順利執行.  

##Step1:Open the project folder "sample1", then rename "sample1" as "sample2".  


打開名為"sample1"的專案資料夾,重新命名"sample1"資料夾為"sample2".  

##Step2: Open the EWARM folder under the "sample2" folder. Rename the folder "sample1" as "sample2".  


在“sample2”資料夾中打開EWARM資料夾, 找到“sample1”資料夾後重新命名該資料夾為“sample2".  
        
##Step3: In the EWARM folder, rename the following files:
        

在EWARM 資料夾中, 重新命名以下檔案名稱：
        
        old file names  | new file names
        
        sample1.dep    -> sample2.dep
        
        sample1.ewd    -> sample2.ewd
        
        sample1.ewp    -> sample2.ewp
        
        sample1.ewt    -> sample2.ewt
        
##Step4:  Open files Project.eww, sample2.dep, sample2.ewd, sample2.ewp and sample2.ewt in Sublime Text.  


利用Sublime Text開啟Project.eww, sample2.dep, sample2.ewd, sample2.ewp 和 sample2.ewt.
        
        
##Step5:  In Sublime Text, execute "Search and Replace".

        for MAC: press command + shift + F
        
        for Windows: press Ctrl + H  
        
        
find the variable name "sample1" and replace "sample1" as "sample2". Next, save all files.  

##Step6:  Close all files. Open Project.eww through IAR EWARM workbench.  

##Step7:  In the IAR EWARM workspace, right click on "sample2". Click_Rebuild All_ on the menu.  

##Step8:  Done!
        
        
        
        
        
