# Zoom_Chat_Attendance
Takes attendance using the saved zoom meeting chats

This file counts the number of zoom chats a student's name shows up in out of all chats for the class. 
It does Not record the number of times they add to the chat, just if they did or not. 

IMPORTANT KNOWN ISSUES
1) Students with the same last name as another student will be counted twice.
2) More than 2 names as full name (ex: Amy Chu Park) will not be counted. Hyphenated last names are counted (Ex: Amy Chu-Park).
3) Full name on Zoom and Canvas must match or they will not be counted

Students with shared last names should be checked manually for issue #1. 
Students with more than 2 names in full name should be manually checked for issue #2.
Students with low attendance or if you know they use a different zoom name should be manually checked for issue #3.

This code will record about 75% of the students correctly, however, due to these known issues, it should NOT be the only method of taking participation/attendance grades

To use: 
1) all meeting chats should be saved in the attendance folder with as a .txt file titled "meeting_saved_chat#" with each file numbered consequetively from 1:n
2) download the gradebook from Canvas, save in the attendance folder, give it an easier to type name
3) In the R code: change mypath variable to file path of attendance folder (chunk 1, line 1)
4) change code for variable roster to name of the gradebook csv (chunk 1, line 2)
5) change sections names to your sections (chunk 1, line 3)
6) Run each code chunk once, the final chunk saves the result as a csv in the attendance folder. 
