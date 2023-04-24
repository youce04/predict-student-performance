# Dataset

|カラム|説明|処理方法|注記|
|---|-------|------|------|
|session_id| イベントが行われたセッションのID|groupbyのキー|
|index| そのセッションのイベントのインデックス|groupby max()|早くクリックされたとき、順番が正しくないというエラー *(1)*|
|elapsed_time|セッション開始からイベント記録までの経過時間（ミリ秒単位) 積み上げ方式で、最終行がゲームの終了時間|groupby max()|一個前との差分、上と同じエラー *(1)*|
|event_name| イベントタイプの名前|各イベント名でgropuby.count()|
|name| イベント名（例えば、notebook_clickがノートブックを開いているのか閉じているのかを識別する）|ワンホット|
|level| どの階層で起きた出来事か（0〜22）|sum, mean, median, countをそれぞれ入れてみる　後から入れたほうがいいか？|逆転だったり、抜けだったり *(1)*|
|page| イベントのページ番号（ノートブック関連イベントの場合のみ）|Drop||
|room_coor_x| ゲーム内のルームを基準としたクリックの座標（クリックイベント時のみ）|Drop||
|room_coor_y| ゲーム内のルームを基準としたクリックの座標（クリックイベント時のみ）|Drop||
|screen_coor_x| プレイヤーの画面を基準としたクリックの座標（クリックイベント時のみ）|Drop||
|screen_coor_y| プレイヤーの画面を基準としたクリックの座標（クリックイベント時のみ）|Drop||
|hover_duration| ホバーが発生した時間（ミリ秒）（ホバーイベントの場合のみ）|NaNを除外してMean →後で入れる|ホバー時間が長い＝迷っているとかはありそうだが、もっとよく見る必要あり|
|text| このイベントの間、プレーヤーに表示されるテキスト| Drop||
|fqid| イベントの完全修飾ID| Drop||
|room_fqid| イベントが行われた部屋の完全修飾ID| Drop||
|text_fqid| 完全修飾ID|　Drop||
|fullscreen| プレーヤーがフルスクリーンモードであるかどうか|そのまま使う||
|hq| 高画質かどうか|そのまま使う|
|music| ゲーム音楽のON/OFF|そのまま使う
|level_group| この行がどのレベルグループ（および問題グループ）に属するか（0～4、5～12、13～22）| |ポイントが2つだったり4個以上だったりする *(1)*|

■参考URL  
(1) https://www.kaggle.com/competitions/predict-student-performance-from-game-play/discussion/395250

# 評価指標
sklearn.metrics.f1_score(true, pred, average='macro')  
We compute the f1_score for class 0 then compute the f1_score for class 1 then average the two equally. Blog explains this here


# 考えること
ゲームの内容は問題の正答率を1対1で結びつけることは不可  
各生徒の主成分みたいなものの抽出　&　問題の主成分を抽出　→　それぞれをマッチングみたいな考え方？  
要素を圧縮する？  
各問題がどのような要素と結びついているか  
特定の行動（画面のクリック回数とかクリック場所とか）と全体の正答率　および　各問題の正答率の関係  
問題が出てきたときに出てくる特定の文章　全体の正答率との関係はわかる　どうやって各問題の正誤と結びつけるか？


# 証明パートの誤答
Chapter2  
that is definitely no slip  
that doesn't prove your case.  
that doesn't prove your case.  
that doesn't prove your case.  
that doesn't prove your case.  
that doesn't prove your case.  
that doesn't prove your case.  
that doesn't prove your case.  
that doesn't prove your case.  
that doesn't prove your case.  

# Markdownの書き方
https://un4navi.com/prologue/20079/
