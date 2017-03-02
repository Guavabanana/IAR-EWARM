# IAR-EWARM

Tips about IAR EWARM
==========================


Project & Workspace Rename IAR 專案重新命名
-----------------------------------------

Tools:  IAR-EWARM and Sublime Text 2 or 3

Goal:   Given that we have a IAR project called "sample1", we want to rename the project as "sample2" and keep the project work well as usual.
       
        修改IAR專案“sample1"名稱為“sample2",且專案依舊能順利執行.

Step1:  Open the project folder "sample1", then rename "sample1" as "sample2". 

        打開名為"sample1"的專案資料夾,重新命名"sample1"資料夾為"sample2".
        
Step2:  Open the EWARM folder under the "sample2" folder. Rename the folder "sample1" as "sample2".
        
        在“sample2”資料夾中打開EWARM資料夾, 找到“sample1”資料夾後重新命名該資料夾為“sample2".
        
Step3:  in the EWARM folder, rename the following files:
        
        在EWARM 資料夾中, 重新命名以下檔案名稱：
        
        old file names  | new file names
        sample1.dep    -> sample2.dep
        sample1.ewd    -> sample2.ewd
        sample1.ewp    -> sample2.ewp
        sample1.ewt    -> sample2.ewt
        
Step4:  Open files sample2.dep, sample2.ewd, sample2.ewp and sample2.ewt in Sublime Text.
        利用Sublime Text開啟sample2.dep, sample2.ewd, sample2.ewp 和 sample2.ewt.
        
Step5:  In Sublime Text, press _command + shift + F_
        
        
更改IAR 的Workspace filename 的方式
?
在工作中, 我們常常遇到編寫例程後, 在此PROJECT 基礎上, 改寫為正式項目名的例子. 或者是項目移植升級的例子, 都需要我們重新修改項目名.
?
比方說, 從sample1.eww -> sample2.eww, 可是修改方式不是只修改項目名這麼簡單.
?
我們將嘗試的修改步驟, 羅列如下:
??? (1)重命名sample1.eww為sample2.eww. 
?? ?(2)編輯sample2.eww,將內容sample1.ewp修改為sample2.ewp. 
?? ?(3)重命名sample1.ewp為sample2.ewp. 
?? ?(4) Open sample2.eww後進入debug config.調整到your config(debug似乎是默認). 
?? ?(5)在Option -> Output converter中,生成sample1.bin修改為$PROJ_FNAME$.out. 
?? ?(6)在Option -> Linker -> Output中,將sample1.out修改為$PROJ_FNAME$.out. 
?? ?(7)在Option -> Debugger -> Setup中,將Driver選擇回? your driver,如CMSIS DAP. 
?? ?(8)在Option -> Debugger -> Download中,選中: Verify download, Use flash loader. 
?? ?(9) Project -> Clear.-> Rebuild all. 
?? ?(10)清除全部sample1相關無用文件.
?
在我們完成這樣修改後, rebuild/download/debug 的過程, 目前均無異常.
?
PS 我們使用IAR 當前版本6.50.3, 並且eww 只包含單PROJECT.
?
Allen Zhan
Release on EETC
