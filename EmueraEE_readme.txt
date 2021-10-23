タイトル：EmueraEE 最終更新日:2021/10/23
バージョン：1.824+v11+EE+v5
改変者：Enter
元となったアプリケーション：Emuera1.824+v11（妊）|дﾟ)の中の人、及びMinorShift制作）
連絡先：Twitter/@eraBEMANI Discord/https://discord.gg/p5rb5uK

※eramakerの作者様及びMinorShift様、妊の人様はEmueraEEの製作には関与していません。
当アプリの不具合は上記連絡先にご報告ください


[概要]
Emueraをベースに改造を施したバージョンです。追加された機能は以下の通り

・PLAYSOUND "ファイル名.拡張子"
「sound」フォルダ内にある音声ファイルを1回再生します

・STOPSOUND
PLAYSOUNDで再生中の音声ファイルを停止します

・PLAYBGM "ファイル名.拡張子"
「sound」フォルダ内にある音声ファイルをループ再生します

・STOPBGM
PLAYBGMで再生中の音声ファイルを停止します

・EXISTSOUND "ファイル名.拡張子"
「sound」フォルダ内に指定した音声ファイルが存在するか判定します。存在すれば1が、しなければ0がRESULTに入ります

・EXISTSOUND("ファイル名.拡張子")
同名命令の式中関数版

・SETSOUNDVOLUME int
PLAYSOUNDの音量を変更します。引数には0～100を指定できます

・SETBGMVOLUME
PLAYBGMの音量を変更します。引数には0～100を指定できます

Windows Media Playerのライブラリを使っているのでWMPがインストールされてるPCであれば、
WMPで動く音声ファイルは全て動くと思います。

・INPUTMOUSEKEYでボタン使用可能に
命令実行時にRESULT:0=1(マウスクリック時)だった場合にRESULT:5にボタンの数値が入ります

・GDRAWTEXT gID, "テキスト", X座標, Y座標
指定したgIDにテキストを描写する 座標は省略可能
GSETBRUSH cARGBと組み合わせることで文字の濃度と色を変更できる cARGBは濃度+文字色の16進数8桁

・GGETFONT gID
指定したIDの、GSETFONTで指定したフォント名を呼び出す

・GGETFONTSIZE
指定したIDの、GSETFONTで指定したフォントサイズを呼び出す

・OUTPUTLOGでファイル名と拡張子を指定可能に
OUTPUTLOGに引数指定することでそのファイル名.拡張子で出力できる リテラルはPRINTSとかと同じ


[使用方法]
Emueraが正常に動作するeraバリアントのディレクトリにてEmueraと同様の方法でお使いください

[ライセンス]
同フォルダ内のEmuera_readme.txtの[ライセンス]の項に準じます
私、Enterは一切の権利を主張しません


