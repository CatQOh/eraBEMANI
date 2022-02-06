タイトル：EmueraEE 最終更新日:2022/02/06
バージョン：1.824+v13+EE+v8
改変者：Enter
元となったアプリケーション：Emuera1.824+v13（妊）|дﾟ)の中の人、及びMinorShift制作）
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
成功すればRESULT:0に1が、RESULT:1には生成したテキスト画像の幅が、RESULT:2には高さが入る(高さはほぼGSETFONTで指定した値)
v7plusから描画フォーマットをGenericTypographicsに変更 実際のPRINT描画と同じ位置になるように

・GGETFONT gID
指定したIDの、GSETFONTで指定したフォント名を呼び出す

・GGETFONTSIZE gID
指定したIDの、GSETFONTで指定したフォントサイズを呼び出す

・OUTPUTLOGでファイル名と拡張子を指定可能に
OUTPUTLOGに引数指定することでそのファイル名.拡張子で出力できる リテラルはPRINTSとかと同じ
v5fixで親ディレクトリを指定できる脆弱性を修正 子ディレクトリは指定可能

・EXISTFUNCTION("関数名")
名前の通り関数が存在するかの式中関数 通常関数なら1を、式中関数(数値型)なら2を、式中関数(文字列型)なら3を返す
TRYC系でCALL機能を付随させたくない場合にお使いください また、システム関数やシステム組み込み式中関数は0を返す

・GSETFONTでフォントスタイルを指定できるように
第4引数にSETFONTと同じ4ビット数(1=太字 2=斜体 4=打ち消し線 8=下線)指定で装飾を付けられるように 省略可能

・GGETFONT gID
指定したIDの、GSETFONTで指定したフォントスタイルを数値で返す

・GGETTEXTSIZE "テキスト", フォント名, フォントサイズ, フォントスタイル
指定の引数でGDRAWTEXTを行った場合のサイズを取得する 第4引数(フォントスタイル)は省略可能
FONTBOLD相当のスタイルの場合、サイズが微妙に大きくなるため注意

・resourcesフォルダ内の拡張子「csv」が含まれるファイルを全て読み込んでしまう不具合、及びエラーファイルのパスを正常に取得できない不具合を修正（私家版対応までの暫定措置）

・TRYCALLF 関数名
CALLFのTRY命令 CALLF同様に返り値は破棄されるが、関数が無くてもエラーにならない

・TRYCALLFORMF 関数名
CALLFORMFのTRY命令 CALLFORMF同様に返り値は破棄されるが、関数が無くてもエラーにならない
上記2つをTRYC～CATCH式に使う場合はEXISTFUNCTIONと併用してください


[使用方法]
Emueraが正常に動作するeraバリアントのディレクトリにてEmueraと同様の方法でお使いください

[ライセンス]
同フォルダ内のEmuera_readme.txtの[ライセンス]の項に準じます
私、Enterは一切の権利を主張しません


