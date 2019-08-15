# プレミアムトリビア - スキル内課金を使ったスキルの作成
<img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/quiz-game/header._TTH_.png" />

## Alexa スキルのテスト

ここまでで、[音声ユーザーインターフェース](./1-setup-vui-alexa-hosted.md)と [Lambda 関数](./2-create-alexa-hosted-function.md)を作成し、[スキル内商品の作成](./3-create-isp.md)を行いました。これでサンプルスキルのテストをおする準備が整いました。

1. [Alexa開発者ポータル](https://developer.amazon.com/edw/home.html#/skills/list)に戻り、作成したスキルを選択します。

2. トップのナビゲーションメニューから **テスト** タブを選択し **Alexaシミュレータ**を表示します。ブラウザによってはマイクへのアクセス許可を要求する場合があります。マイクを有効にすることを推奨しますが、テキスト入力によるテストも可能です。

3. 上部のナビゲーションメニューのすぐ下にあるドロップダウンから、**開発中** を選択して、テストを有効にします。テストが有効になると**開発中**と表示されます。

4. **Alexaシミュレータ** で、あなたのスキルが期待どおりに動作するかをテストします。テキストボックスに文字を入力するか、マイクアイコンを押しながらパソコンのマイクに向かって話しかけてみてください。
	1. **文字入力** [Step 1](./1-voice-user-interface.md)で指定したスキルの **呼び出し名** に続き "を開いて" とタイプしてください。(例："プレミアムトリビアを開いて")
	2. **音声** テキストボックス横のマイクアイコンをクリックした状態で、スキルの **呼び出し名** に続き "を開いて" と発話してください。
	3. スキルの **呼び出し名** を忘れた場合、トップナビゲーションメニューから **ビルド** タブを選択し、左側パネルの **呼び出し名** で確認してください。

5. 次のようなフレーズをテストしてみてください
        
      * トリビアを教えて
      * 歴史のトリビア
      * 何が買える?
      * 歴史パックを購入する

      > 注意: 音声による意図しない購入を防ぐために、確認コードを有効にしている場合、スキル内課金のプロセスで商品を購入する前に確認コードが要求されます。 Alexaシミュレーターで確認コードをタイプ入力する場合は、「1234」 ではなく「一二三四」と漢数字で入力してください。

6. スキルが期待どおりに動作するかテストします。

	* Alexaシミュレータで検証をしたら、スキルI/O パネルの **JSON入力** と **JSON出力** ボックスを参照します。上部にある **デバイスのログ** を有効にすると、動作ステップも参照できます。
	* もし期待通りの動作をしない場合は、上記のスキルI/Oパネルが実際に Lambda 関数とやり取りしている入出力となりますので、問題解析のヒントにしてください。もちろん AWS Lambda も問題解決のための追加ツールを用意しています。

      > スキルに紐づいている開発者アカウントを使用している限り、スキル内では課金されることはありません。スキル内課金のテストに関する詳細は、[スキル内課金のテストガイド](https://developer.amazon.com/docs/in-skill-purchase/isp-test-guide.html) を参照してください。

      > Alexa 開発者コンソールのスキル内商品のページから、テスト購入をリセットすることができます。(**スキル内商品** のメニューは、**ビルド** の画面の左側にあります。見当たらない場合は、スキルビルダーのチェックリストから、スキル内商品をクリックしてください。) 商品の **テスト購入をリセット** をクリックするとリセットすることができます。 これは、スキル内商品が開発者コンソールから登録されたか ASK CLI で登録されたからに関わらず利用することができます。

      > スキル内商品は、スキルの設定と同一の地域でのみ購入することができます。日本では amazon.co.jp のアカウントで登録されたデバイスから使うことができます。また、請求先住所も同じように国内で設定されている必要があります。

      > **高度なTIP**: シミュレータで、「**終了**」とタイプするか、マイクで入力することにより、それぞれのテストパスの前にセッションをリセットすることができます。 シミュレータは、テストを容易にするために、通常のデバイスよりも長い時間セッションを開き続けます。「**終了**」 と発話することで、これにより簡単にセッションを閉じることができます。

## その他のテスト方法

* Alexa搭載デバイスやアプリケーションでのテスト: あなたの Alexa 開発者アカウントで登録されているデバイスは、開発中のスキルが有効化されており、開発モードでテストすることができます。 シミュレータだけでなく、必ず実際のデバイスでもテストするようにしてください。 スキル内商品は全てのデバイスで購入できないかもしれませんが、購入済みの商品はすべてのデバイスで有効になります。

*  [Echosim.io](https://echosim.io) はブラウザベースのAlexaスキルのテストツールです。実機デバイスがなくてもテストできるので便利です。

*  [Unit Testing with Alexa](https://github.com/alexa/alexa-cookbook/tree/master/testing/postman/README.md) は [Postman](http://getpostman.com) と [Amazon API Gateway](http://aws.amazon.com/apigateway) を使用したモダンなユニットテストのアプローチです。


**サンプルスキルが正常に動作することを確認できたら、このスキルをカスタマイズしましょう。**

[![Next](https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/general/buttons/button_next_customization._TTH_.png)](./5-customization.md)