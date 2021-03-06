##CM3D2.AddModsSlider.Plugin

メイドエディット画面中にF5でGUI表示トグル。  
[CM3D2.MaidVoicePitch.Plugin][]の各種機能をスライダー・トグルボタンで操作する事が可能。
![GUI](http://i.imgur.com/vGh1nsh.png  "GUI")  
  
※多数のスライダー表示時に「**スクロールパネルでホイールスクロール**」すると極端に重くなります。  
　その状態になった場合は「**スクロールパネル内をクリックorドラッグ**」すれば元に戻ります。


##導入方法

**前提条件** :  
* UnityInjector
* [CM3D2.MaidVoicePitch.Plugin][]
* [CM3D2.ExternalSaveData.Patcher][]  
上記が導入済みであること。  
  
[![ダウンロードボタン][img_download]][master zip]を押してzipファイルをダウンロード。  
zipファイルの中にあるUnityInjectorフォルダをCM3D2フォルダにD&Dすれば導入完了。  



##更新履歴

###0.1.2.17
* スクロールビューのレイアウト変更。
* Undoボタン追加。ボタン押下でエディット画面開始時の値に。
* Resetボタン追加。ボタン押下で当該valueタグの規定値に。
* Inputフィールド追加。スライダーの値をキーボードで入力できる様に。
* modタグ単位で各スライダーを開閉できるように変更。
* valueタグdefault属性省略時にtype="scale"の規定値が正しく設定されていなかったバグ修正。
 * 上記に伴ってModsParam.xmlの修正。(format="1.21")


#####0.1.1.16
* On/Off付きスライダーの表示/非表示切替が適切に動作してなかったバグ修正。
* On/Offボタン押下時に[CM3D2.MaidVoicePitch.Plugin][]側のメソッドが呼ばれてなかったバグ修正。

#####0.1.1.15
* イニシャライズ時にコンフィグパネル開閉動作をしない様に修正。

#####0.1.1.14
* 初回イニシャライズのみ、コンフィグパネルからボタンを取得するように修正。
* エディット画面に入りなおす毎に徐々にイニシャライズ開始が遅くなるバグ修正。

#####0.1.1.13
* ModsParam.xmlのmodタグtype属性に"toggle,slider"指定でOn/Off付きスライダーを表示する様に。
* GUIのサイズ・位置調整。

#####0.1.1.12
* スライダー操作時に[CM3D2.MaidVoicePitch.Plugin][]側のメソッドを呼び出すように修正。

#####0.1.1.11
* WIDESLIDER ON/OFF時にWIDESLIDER前提項目の表示/非表示切替がされていなかったのを修正。

#####0.1.1.10
* ロード時にGUIが画面右にはみ出るバグ修正。

#####0.1.1.9
* イニシャライズ失敗時にコンフィグパネル連打しないように修正。

###0.1.1.8
* GUIをUnity旧GUIからNGUIに変更。
* 各項目のON/OFF操作をトグル系のみに変更。
* type="scale"のスライダー仕様変更。最小値が1未満の場合は中心が1倍、左側縮小、右側拡大。
* フリーコメントからの読込機能廃止。
* ModsParam.xmlの書式変更(format="1.2")
    * modタグに **visible="false"** 記載でその項目は表示されない様に。
    * valueタグに **visible="false"** 記載でそのvalueのスライダーは表示されない様に。
    * valueタグに **default="..."** 記載でそのvalueの初期値を設定できる様に。


#####0.1.0.7
* エディット画面に入ると一部mod数値が初期化されるバグ修正２。

#####0.1.0.6
* 各mod仕様をCM3D2.MaidVoicePitch.Plugin (0.2.2) に準拠。
* WIDESLIDER必須のmodはWIDESLIDER無効時に自動で無効化する様に。
* on/off不可のmodにはトグルボタンを表示しないように。
* 拡張セーブ時にアクティブメイド以外が保存できないバグ修正。
* エディット画面に入るとmod数値が初期化されるバグ修正。


###0.1.0.5
* CM3D2.ExternalSaveData.Patcherの拡張セーブデータに対応。
* 上記に伴い ModsParam.xml の書式変更。
* ON/OFF系のmodをUIよりトグルボタンで操作可能に。
* UIをドラッグで動かせる様に。
* 夜伽スライダーを別Pluginに分離。


###0.0.3.4
* 夜伽時に興奮・精神・理性を変更できるスライドバーを追加。  
* 夜伽時にFaceBlend（頬・涙・よだれの組合せ）とFaceAnime（エロ○○系表情）を選べるボタンを追加。


#####0.0.2.3
* フォントサイズがウィンドウ幅と比例する様に。
* スクロールバーが滑らかに。
* ModsParam.xmlの<mod>属性 forced="..." が正常に機能していなかったのを修正。
* リフレクションがフレーム毎に実行されてたのを修正。（軽量化）

###0.0.2.2
* ModsParam.xmlの書式を変更。
* ModsParam.xmlで<mod>の属性に forced="true" 指定で、フリーコメント欄にかかわらずそのmodのスライダーが表示される様に。
* <value>の属性でtype="scale"指定の時、最小値をスライダーに反映してなかったのを修正。


###0.0.1.1
* 各mod定義をxmlファイルにして読み込む様に。
* スライダーバーとフリーコメント欄が連動する様に。（改造スレその２>>192）
* EYEBALL,TEST_EYE_ANGの縦横が逆だったのを修正。


###0.0.0.0
* 初版



##注意書き

個人で楽しむ為の非公式Modです。  
転載・再配布・改変・改変物配布等はKISSに迷惑のかからぬ様、  
各自の判断・責任の下で行って下さい。  



[CM3D2.MaidVoicePitch.Plugin]: https://github.com/neguse11/cm3d2_plugins_okiba/tree/master/MaidVoicePitch "neguse11/cm3d2_plugins_okiba/MaidVoicePitch/"
[CM3D2.ExternalSaveData.Patcher]: https://github.com/neguse11/cm3d2_plugins_okiba/tree/master/ExternalSaveData "neguse11/cm3d2_plugins_okiba/ExternalSaveData/"
[master zip]:https://github.com/CM3D2-01/CM3D2.AddModsSlider.Plugin/archive/master.zip "master zip"
[img_download]: http://i.imgur.com/byav3Uf.png "ダウンロードボタン"
