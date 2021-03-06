ACT.TPMonitor
=============

TPMonitor for FFXIV on ACT

<img src="https://raw.githubusercontent.com/GB19xx/ACT.TPMonitor/master/img/Sample.png" alt="Sample">

Latest Version
----------------
[ACT.TPMonitor.zip](https://github.com/GB19xx/ACT.TPMonitor/releases/latest)

How to install
----------------
1. [ACT](http://advancedcombattracker.com/download.php)より、本体とPluginをダウンロード  
2. ACT、FFXIVプラグイン導入  
3. [ACT.TPMonitor_xxxx.zip](https://github.com/GB19xx/ACT.TPMonitor/releases/download/1.5.0.1/ACT.TPMonitor_1.5.0.1.zip)をダウンロードし、展開  
4. Advanced Combat Tracker.exeと同じフォルダに「FFXIV_ACT_Plugin.dll」と「ACT.TPMonitor.dll」を配置  
5. Plugin -> Plugin Listingタブから、上記4.「ACT.TPMonitor.dll」を選択  
6. Add/Enable Pluginクリック  
7. TPMonitorタブ選択  
8. キャラクターフォルダー設定  
【キャラクターフォルダーの特定方法】  
	8-1. ログイン後、HUDを保存する  
	8-2. ADDON.DATの更新日時が近いとそのフォルダ  
	
<img src="https://raw.githubusercontent.com/GB19xx/ACT.TPMonitor/master/img/Settings.png" alt="Settings">

How to uninstall
----------------
1.	Plugin -> Plugin Listingタブから、[x]  
2.	配置したACT.TPMonitor.dllを削除  
3.	設定ファイルの削除  
%AppData%\Roaming\Advanced Combat Tracker\Config\ACT.TPMonitor.config.xml  

Usage
------
###Commands
/e TP _Command_  

<table>
<tr>
<td>Command</td><td>Description</td>
</tr>
<tr>
<td>2 - 8:&lt;2&gt; - &lt;8&gt;</td><td>
パーティメンバーの名前を取得します<br>
パーティメンバーが変わるたび実行する必要があります<br>
<font color="red">※ログ設定のイニシャルに注意。</font><br>
<br>
また、指定なしにすることで任意のTPを非表示にできます<br>
ex) 3人目、4人目を非表示 <br>
　/e TP 2:&lt;2&gt;  <br>
　/e TP 3:<br>
　/e TP 4:<br>
　/e TP 5:&lt;5&gt;  <br>
　/e TP 6:&lt;6&gt;  <br>
　/e TP 7:&lt;7&gt;  <br>
　/e TP 8:&lt;8&gt;  <br>
　/e TP /Show  
</td>
</tr>
<tr>
<td>/Show</td><td>TPMonitorの表示・再表示</td>
</tr>
<tr>
<td>/Hide</td><td>TPMonitorの非表示</td>
</tr>
<tr>
<td>/Adjust</td><td>自動的に表示位置を調整します<br>
・HUD変更<br>
・ゲーム画面を移動（ウィンドウモードの場合）<br>
※なんか位置がおかしいな？と思ったら実行<br>
</td>
</tr>
</table>

下記をマクロにすると便利
  
	/e TP 2:<2>  
	/e TP 3:<3>  
	/e TP 4:<4>  
	/e TP 5:<5>  
	/e TP 6:<6>  
	/e TP 7:<7>  
	/e TP 8:<8>  
	/e TP /Show  

チャットログの名前をフルネーム以外でプレイしている場合、上記マクロの前後にテキストコマンドを追記することで取得できます  
/chatlog name 0 (先頭に追記）  
/chatlog name 1~3 (最後に追記）
  
0：フルネーム  
1：姓のみイニシャル  
2：名のみイニシャル  
3：姓名ともにイニシャル  

Option
------
+ パーティ解散を契機に非表示  
+ ID終了時に非表示  
+ 自分のTPも表示（Fixed Mode時のみ有効）  
+ ゲーム画面が非アクティブ時は非表示  

Display Job
------
+ 特定ジョブのTPを非表示にできます  
+ 記載のないジョブは表示されます  

Settings  
------
###Party List
+ Offset  
Offsetにて微調整可能
+ Fixed mode  
マルチディスプレイの方はこちらを使用してください  

###Alliance
+ X, Y 指定して表示  
<img src="https://raw.githubusercontent.com/GB19xx/ACT.TPMonitor/master/img/AllianceSample.png" alt="AllianceSample">

###Scale
+ UIのScaleより優先されます  

###Color Setting
+ StartTP  
+ EndTP  
+ Color(ReadOnly)  
+ Edit Color(Show Dialog)  

Examples:
<table>
<tr>
<td> </td><td>StartTP</td><td>EndTP</td><td>Color</td>
</tr>
<tr>
<td> </td><td>0</td><td>400</td><td>Red</td>
</tr>
<tr>
<td> </td><td>400</td><td>800</td><td>Aqua</td>
</tr>
<tr>
<td> </td><td>800</td><td>1000</td><td>White</td>
</tr>
</table>

Remarks
-----------
+ Win7(64bit)のみ動作確認  
+ マルチディスプレイ未検証  
+ サブキャラクター未検証  
+ チャットの種別がないので、他人のコマンドにも反応します

Licenses
-------
三条項BSDライセンス (3-clause BSD license)  

記載されている会社名・製品名・システム名などは、各社の商標、または登録商標です。  
Copyright (C) 2010 - 2014 SQUARE ENIX CO., LTD. All Rights Reserved.  

・[DotNetZip](https://github.com/haf/DotNetZip.Semverd/blob/master/LICENSE) (Ms-PL)  
・[Json.Net](https://json.codeplex.com/license) (MIT License)  
・UpdateChecker.cs by grindingcoil ([Originally under 3-clause BSD license](https://github.com/grindingcoil/act_timeline/blob/master/LICENSE.txt))

Special thanks
----------------
+ [RainbowMage氏](https://github.com/RainbowMage)  
  FFXIVPluginの動的ロード、マルチモニタの修正いただきました！  

+ [madogiwa氏](https://github.com/madogiwa)  
  UIスケール対応いただきました！  

+ [grindingcoil氏](https://github.com/grindingcoil)  
  更新チェックのソース流用いたしました！  

+ [pirulen](http://typodermicfonts.com/pirulen/)  
  Free Font! GREATE JOB!

