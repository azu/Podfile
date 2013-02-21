# Library

よく使うライブラリのまとめ。

ライブラリは [CocoaPods] 経由で管理、インストールする。

``Podfile`` もレポジトリに入っています。

# CoreData

* [MagicalRecord]
* [MagicalRecordのREADMEを意訳 - Object for cutie](http://d.hatena.ne.jp/tanaponchikidun/20121202/1354468112 "MagicalRecordのREADMEを意訳 - Object for cutie")

CoreDataを扱いやすくするためのライブラリ

モデルクラス生成は [mogenerator](https://github.com/rentzsch/mogenerator "mogenerator") を使います。

* [mogeneratorと識別子を使ったCoreDataのModelクラス作成パターン | Technology-Gym](http://tech-gym.com/2012/10/ios/890.html "mogeneratorと識別子を使ったCoreDataのModelクラス作成パターン | Technology-Gym")

また、モデルのテストをするのにもとても便利なので、CoreDataを使うときはほぼ必須

# NSDate util

* [NSDate-AZExtensions]

[NSDate-Extensions](https://github.com/erica/NSDate-Extensions "NSDate-Extensions") をforkして、
バグ修正と少しメソッドを追加ものです。

# Objective-C utilities

* [Overline]

NSArrayに#mapや#each、NSString+URLEncodeなどFoundation系のクラスに
便利なメソッドを追加してくれるライブラリです。

[coby](https://github.com/pjaspers/coby "coby") や [Underscore.m](http://underscorem.org/ "Underscore.m") など
この手のジャンルは多いですが、バランスが良くshorthandとObjective-Cらしいメソッドの両方を持っているので気に入っています。

# Image resize util

* [UIImage-Resize]

UIImageのリサイズを行うカテゴリです。
シンプルですが、retina対応もちゃんとしてありサムネイルを作る部分とかでよく使います。

# UI

## Auto complete

* [JCAutocompletingSearch]

用意した配列などから、検索して自動補完に使えるライブラリです。
探索を非同期で行うため、大量のデータでも安定した動作になっています。

UISearchBarを使うので少し見た目を変更しにくいですがUIAppearanceなどを使えば大抵のことはできます。

* [UISearchBarに決定ボタンを追加するカスタマイズ方法について | Technology-Gym](http://tech-gym.com/2013/02/ios/1116.html "UISearchBarに決定ボタンを追加するカスタマイズ方法について | Technology-Gym")

## WebView

* [SVWebViewController]

[汎用の WebViewController をくみこむための THWebViewController っていうのをでっちあげた - tokuhirom's blog.](http://blog.64p.org/entry/20120107/1325914765 "汎用の WebViewController をくみこむための THWebViewController っていうのをでっちあげた - tokuhirom's blog.")
と同じようなWebViewでURLを表示するのを簡単に行うライブラリです。

## HUD

* [SVProgressHUD]

HUD系は大量に存在しますが、昔からこれを使っています。

### similar to Android

* [Toast]

[SVProgressHUD] だと少し大げさすぎるときはToast系の表示を使っています。

# UITextField/View navigation

* [BSKeyboardControls]

UITextViewやUITextFieldのinputViewにprev/nextのボタンを付けて、複数のText間を移動できるようにするシンプルなライブラリ。

既にあるUIText*郡に後付で付けられるので便利です。

UIText*系のサブクラスと合わせて使ったりします。

* [azu/UITextSubClass · GitHub](https://github.com/azu/UITextSubClass "azu/UITextSubClass · GitHub")

# UIAlertView Util

* [UIAlertView-Blocks]

UIAlertViewとUIActionSheetをblocksを使って挙動を定義できるライブラリ。

どちらもdelegateで実装するとスゴく分かりにくくなるため、blocksを使って実装するべきです

# Calendar View

* [AZCalendarView]

UITableView ライクなAPIを持ったカレンダーViewライブラリ.
ヘッダーや曜日、日付のセル、フッターなどをバラしてxibを作成して使えるようにしてあるので、大抵の月カレンダーの見た目は作成できる。

cocoapodsでインストールされるCore側をいじらないで、実装(Implements)の中身だけをいじって作れるようになってる。

# Feedback form

* [AAMFeedback]

[fladdict/AAMFeedback · GitHub](https://github.com/fladdict/AAMFeedback "fladdict/AAMFeedback · GitHub") の fork.

本家が止まってたのでforkしたけど、最近活発になってきてるようなので戻してもいいかもしれない。
fork版はローカライズファイルもcocoapodsで持ってこれるのと、背景画像など必要になったものを少し追加してある。

端末名情報はライブラリから外して、 [UIDeviceIdentifier](https://github.com/squarefrog/UIDeviceIdentifier "UIDeviceIdentifier") に依存するような作りに変更してある。


# DEBUG

* [PonyDebugger]

Chromeのremote debuggerを使ったデバッガ.

インスペクタ系は色々あるけど一番使いやすく、CoreDataやネットワークなどにも対応してる。

* [DCIntrospect](https://github.com/domesticcatsoftware/DCIntrospect "DCIntrospect")
* [CBIntrospector](https://github.com/cbess/CBIntrospector "CBIntrospector")
* [iOS-Hierarchy-Viewer](https://github.com/glock45/iOS-Hierarchy-Viewer "iOS-Hierarchy-Viewer")

## TestFlight

* [TestFlight SDK]

TestFlightのSDK

# Test

* [Kiwi]

BDD系のテスティングフレームワーク.

MockやStubsも持っているため、これ一つでひと通りはできる。
比較的安定していて、2.0への開発も進んでいるため将来的もそこまで心配していない。

* [OCHamcrest]

テストのmatcherライブラリ

好みの構文なのでたまに利用する。

---

[CocoaPods]: http://cocoapods.org/  "CocoaPods: The Objective-C Library Manager"

[MagicalRecord]: https://github.com/magicalpanda/MagicalRecord  "magicalpanda/MagicalRecord ? GitHub"
[NSDate-AZExtensions]: https://github.com/azu/NSDate-AZExtensions  "azu/NSDate-AZExtensions ? GitHub"
[Overline]: https://github.com/yaakaito/Overline  "yaakaito/Overline ? GitHub"
[UIImage-Resize]: https://github.com/AliSoftware/UIImage-Resize  "AliSoftware/UIImage-Resize · GitHub"
[JCAutocompletingSearch]: https://github.com/jcoleman/JCAutocompletingSearch  "jcoleman/JCAutocompletingSearch · GitHub"
[SVWebViewController]: https://github.com/samvermette/SVWebViewController  "samvermette/SVWebViewController · GitHub"
[SVProgressHUD]: https://github.com/samvermette/SVProgressHUD  "samvermette/SVProgressHUD · GitHub"
[Toast]: https://github.com/scalessec/Toast  "scalessec/Toast · GitHub"
[BSKeyboardControls]: https://github.com/simonbs/BSKeyboardControls  "simonbs/BSKeyboardControls · GitHub"
[UIAlertView-Blocks]: https://github.com/jivadevoe/UIAlertView-Blocks  "jivadevoe/UIAlertView-Blocks · GitHub"
[AZCalendarView]: https://github.com/azu/AZCalendarView  "azu/AZCalendarView · GitHub"
[AAMFeedback]: https://github.com/azu/AAMFeedback  "AAMFeedback"
[PonyDebugger]: https://github.com/square/PonyDebugger  "square/PonyDebugger · GitHub"
[TestFlight SDK]: https://testflightapp.com/sdk/  "TestFlight » Beta Testing On The Fly"

[Kiwi]: https://github.com/allending/Kiwi  "allending/Kiwi · GitHub"
[OCHamcrest]: https://github.com/hamcrest/OCHamcrest  "hamcrest/OCHamcrest · GitHub"