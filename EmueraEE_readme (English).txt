App name:EmueraEE Latest update:2021/11/20
Version:1.824+v13+EEv7plus
Developer:Enter
Original Application:Emuera1.824+v13�iDeveloped by �D�j|�t�)�̒��̐l and MinorShift�j
Contact:Twitter/@eraBEMANI Discord/https://discord.gg/p5rb5uK

��eramaker's dev,MinorShift and �D�̐l were not relate EmueraEE's development.
If you get error please report above addres.


[Summary]
�EPLAYSOUND "filename.extension"
Once play sound file in "sound" directory.

�ESTOPSOUND
Stop sound file played by "PLAYSOUND".

�EPLAYBGM "filename.extension"
Loop play sound file in "sound" directory.

�ESTOPBGM
Stop sound file played by "PLAYBGM".

�EEXISTSOUND "filename.extension", EXISTSOUND("filename.extension")
Check exist sound file in "sound" directory. If exist will return 1, not exist will return 0.

�ESETSOUNDVOLUME int
Change PLAYSOUND's volume. Can change 0 to 100.

�ESETBGMVOLUME
Change PLAYBGM's volume. Can change 0 to 100.

These functions are using Windows Media Player library. I think can play sound files in WMP, Can play in EmueraEE too.

�ECan use button notation in "INPUTMOUSEKEY"
If RESULT:0=1(Left click), Button number will set to RESULT:5.

�EGDRAWTEXT gID, "text", X, Y
Draw text strings to gID. Can abbreviate X and Y.
This function is using brush of set by "GSETBRUSH".
If succeed will set 1 to RESULT:0, width to RESULT:1, height to RESULT:2.

�EGGETFONT gID
Get gID's font name set by "GSETFONT".

�EGGETFONTSIZE gID
Get gID's font size set by "GSETFONT".

�ECan specifying filename and extension in "OUTPUTLOG"
Can specifying output file name and directry by argument. Can abbreviate argument, That case will output "emuera.log".

�EEXISTFUNCTION("function name")
Check exist function. If function is exist and normal function will return 1,
Integer user function will return 2, String user function will return 3.
But can't check system function, This case will return 0.

�ECan specifying font style in "GSETFONT"
Specifying GSETFONT's fourth argument 4 bit integer(1=bold 2=italic 4=strike 8=underline). Can abbreviate this.

�EGGETFONT gID
Get 4 bit integer of gID's font style set by "GSETFONT".

�EGGETTEXTSIZE "text", fontname, fontsize, fontstyle(4 bit int)
Return width(RESULT:0) and height(RESULT:1) case of runned GDRAWTEXT with same argument.


[Usage]
Copy and run on eragames directory.

[License]
Please read Emuera_readme.txt in same directory.
EmueraEE's dev(Enter) don't assert any right.

