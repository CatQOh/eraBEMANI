﻿App name:EmueraEE Latest update:2022/02/06
Version:1.824+v13+EEv8
Developer:Enter
Original Application:Emuera1.824+v13（Developed by 妊）|дﾟ)の中の人 and MinorShift）
Contact:Twitter/@eraBEMANI Discord/https://discord.gg/p5rb5uK

※eramaker's dev,MinorShift and 妊の人 were not relate EmueraEE's development.
If you get error please report above addres.


[Summary]
・PLAYSOUND "filename.extension"
Once play sound file in "sound" directory.

・STOPSOUND
Stop sound file played by "PLAYSOUND".

・PLAYBGM "filename.extension"
Loop play sound file in "sound" directory.

・STOPBGM
Stop sound file played by "PLAYBGM".

・EXISTSOUND "filename.extension", EXISTSOUND("filename.extension")
Check exist sound file in "sound" directory. If exist will return 1, not exist will return 0.

・SETSOUNDVOLUME int
Change PLAYSOUND's volume. Can change 0 to 100.

・SETBGMVOLUME
Change PLAYBGM's volume. Can change 0 to 100.

These functions are using Windows Media Player library. I think can play sound files in WMP, Can play in EmueraEE too.

・Can use button notation in "INPUTMOUSEKEY"
If RESULT:0=1(Left click), Button number will set to RESULT:5.

・GDRAWTEXT gID, "text", X, Y
Draw text strings to gID. Can abbreviate X and Y.
This function is using brush of set by "GSETBRUSH".
If succeed will set 1 to RESULT:0, width to RESULT:1, height to RESULT:2.

・GGETFONT gID
Get gID's font name set by "GSETFONT".

・GGETFONTSIZE gID
Get gID's font size set by "GSETFONT".

・Can specifying filename and extension in "OUTPUTLOG"
Can specifying output file name and directry by argument. Can abbreviate argument, That case will output "emuera.log".

・EXISTFUNCTION("function name")
Check exist function. If function is exist and normal function will return 1,
Integer user function will return 2, String user function will return 3.
But can't check system function, This case will return 0.

・Can specifying font style in "GSETFONT"
Specifying GSETFONT's fourth argument 4 bit integer(1=bold 2=italic 4=strike 8=underline). Can abbreviate this.

・GGETFONT gID
Get 4 bit integer of gID's font style set by "GSETFONT".

・GGETTEXTSIZE "text", fontname, fontsize, fontstyle(4 bit int)
Return width(RESULT:0) and height(RESULT:1) case of runned GDRAWTEXT with same argument.

・TRYCALLF funtionName
Do CALLF with TRY.

・TRYCALLFORMF functionName
Do CALLFORMF with TRY.


[Usage]
Copy and run on eragames directory.

[License]
Please read Emuera_readme.txt in same directory.
EmueraEE's dev(Enter) don't assert any right.

