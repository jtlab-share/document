# documents
クラーク記念国際高等学校旭川キャンパス　「レゴで体験するロボットプログラミング」　講義資料

[ここをクリックして講義資料を開いてください](https://github.com/clark-share/documents/raw/main/221013%E3%82%AF%E3%83%A9%E3%83%BC%E3%82%AF.pdf)

## プログラミングの前準備
※講義開始前に手順を追っておくとスムーズに進めることができます。

1. 「Microsoft MakeCode for micro:bit」のサイトにアクセス→ https://makecode.microbit.org/

![image](https://user-images.githubusercontent.com/115523011/195230500-034bb7f0-1207-4a3c-b483-23f7bfe873cb.png)

2. 画面右側の`↑読み込む`ボタンを押します。

![image](https://user-images.githubusercontent.com/115523011/195231230-74bf343d-c12c-4859-9db9-273f0a9c2c5f.png)

3. 「読み込む」ダイアログ真ん中の`URLから読み込む...`を選択します。

![image](https://user-images.githubusercontent.com/115523011/195231351-300a1931-cefe-472f-96d7-5ac73feb651c.png)

4. 「プロジェクトのURLを開きます」ダイアログの`このプロジェクトのURLをコピーする。`欄に、以下のURLをコピペします。下のURL右端にある二重□ボタンを押すとコピーできますので、ダイアログのテキストボックスを選択してから`[Ctrl]`+`[V]`キーを押して貼り付けてください。
```
https://github.com/clark-share/signal0
```

![image](https://user-images.githubusercontent.com/115523011/195231979-b1b7aec6-5b55-47e4-acc9-07cd4e553145.png)

5. `つづける`ボタンを押すと、プログラミングのための画面が開きます。

![image](https://user-images.githubusercontent.com/115523011/195232214-4e4b43ae-e7d3-48fd-bbf4-2e93098bd7ef.png)

実際の対面授業では、レゴを用いた信号機を接続し、ここで行ったプログラムに従って光らせるのですが、レゴの信号機が手元になくても、画面左側のmicro:bitシミュレータ上で動作を確認することができます。実機ではP0に青(緑)色、P1に黄色、P2に赤色のLEDが接続されていて、それぞれ5秒-2秒-5秒間、ピンの上の数字が1000-500-100と変化すると思います。

例えば信号が青になっている時間を1秒にしたい場合（実際にあったらひどい信号ですが！）、ブロックが並んでいる中の左下の方
- ずっと
  - 変数 signal を 1 にする
  - 一時停止（ミリ秒） 5000
の`5000`をクリックして`1 second`を選択すると、ここの部分を1000(ミリ秒＝1秒)に変更できます。

![image](https://user-images.githubusercontent.com/115523011/195233627-802c3a9a-3595-44b4-9da4-d13b6eab5368.png)

シミュレータ上で動作も確認してみてください。

![image](https://user-images.githubusercontent.com/115523011/195233842-1a11eab2-a963-40b1-b7c7-6a84bdcfae3c.png)

6. 画面最下段に「信号機-0」というテキストボックスがあると思うのですが、そのすぐ右側にGitHubボタン（猫↑マーク）があるので、それを押します。

![image](https://user-images.githubusercontent.com/115523011/195234045-2e6027e7-6643-4b93-a88a-1aede4c9604c.png)

今回の講義では、遠隔受講している生徒さんと対面受講している生徒さんで協力してプログラミングを行います。基本的には遠隔受講をしている生徒さん側のプログラム画面をZoomで共有しながら話し合って作成し、対面受講の生徒さんとGitHubを用いてプログラムの同期を行い、対面受講の学生さんが実際に動作させる、という手法を用います。

同期するには、`変更をコミットしてプッシュ`ボタンを押します。

![image](https://user-images.githubusercontent.com/115523011/195235089-ce2f2da7-40f5-48a3-a9df-76069e8df3a3.png)

7. 「GitHubでサインイン」ダイアログが表示されます。**※自分でGitHubアカウントをお持ちの方は自分のアカウントでサインインして構いません、その場合はこの手順を読み飛ばしてください。**

`開発者トークンを使用する`リンクをクリックしてください。

![image](https://user-images.githubusercontent.com/115523011/195235647-66fc0c45-45c2-46dd-b265-b23bf1ae1830.png)

`GitHub トークンをここに貼り付ける：`欄に`ghp_`と入力し、その後ろに以下のテキストをコピペしてください。コピペ手順は先ほどのURLと同じです。
```
pYMQJcJ3eTcbD8KUhgRXlpPZ5pRZTW2bgnwA
```
** 10/12 15:30頃更新しました、前に貼ったトークンが無効になりました、トークンの貼り付けがダメなようです（そりゃそうなんだけど）。**
注：このトークンは講義終了後に無効になります。もしも自分でGitHubアカウントを作成したい場合は、[こちら](https://qiita.com/jtFuruhata/items/0f28ebe5828005eae9b7)を参考にしてください。

貼り付けたら`サインイン`ボタンを押します。

![image](https://user-images.githubusercontent.com/115523011/195236279-cf40ff37-c71f-4f58-b29f-47e2966f6c9e.png)

8. 対面で受講する方は、右上の`✓ 変更を取得（プル）`ボタンを押すと、相手が保存したプログラムを手元に取り込むことができます。同時に編集もできますが結構厄介なことになりますので、今日は編集するのはどちらかに統一した方がいいです。

![image](https://user-images.githubusercontent.com/115523011/195245451-252a2f21-de85-4ee3-8ae2-6f155bf16180.png)

9. 「履歴」の`コミットを表示する`ボタンを押すと、このページから同期した任意の時点のプログラムへ戻ることができます。

![image](https://user-images.githubusercontent.com/115523011/195237302-93ea5ffb-99fc-4b63-a6e9-84b6a2e49986.png)

ボタンを押すと日付表示に代わりますので、その右の `↑ 3` の部分をクリックします。数字はもっと大きいかもしれません。

![image](https://user-images.githubusercontent.com/115523011/195237522-cfa168b9-bc14-45f3-9afe-31702be375ab.png)

その下に3項目（もっと多いかもしれません）表示されます。そのうちの下から2番目`MakeCodeプロジェクトの初期ファイル`を押すと、`復元`ボタンが出てきます。

![image](https://user-images.githubusercontent.com/115523011/195237862-a3a6ac16-33a4-4438-b438-b7a89bf4d839.png)

このボタンを押すと、今日加えた変更をすべて元に戻して、一番最初の状態にすることができます（ので、使う時は充分注意してください...）。確認ダイアログが出ますので、`復元`ボタンを押してください。

![image](https://user-images.githubusercontent.com/115523011/195237926-98f9d496-c8ed-4fee-b0b5-d3e1271ff774.png)

先ほど5000を1000に変更した部分が元に戻っていることを確認頂けると思います。

![image](https://user-images.githubusercontent.com/115523011/195238068-b7c14b9c-c1a7-4b12-bdde-134597ca3d76.png)

プログラムの前準備は以上です。実際の講義では、原則として遠隔と対面二人一組で、各組別々のプログラム（「信号機-1」など）を編集していきます。この`-0`は練習用として自由に使って頂いて構いません。
