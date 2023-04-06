# Dataset

|カラム|説明|処理方法|
|---|-------|------|
|session_id| イベントが行われたセッションのID||
|index| そのセッションのイベントのインデックス|早くクリックされたとき、順番が正しくないというエラー  https://www.kaggle.com/competitions/predict-student-performance-from-game-play/discussion/395250|
|elapsed_time|セッション開始からイベント記録までの経過時間（ミリ秒単位) 積み上げ方式で、最終行がゲームの終了時間|一個前との差分、上と同じエラー|
|event_name| イベントタイプの名前|ワンホット|
|name| イベント名（例えば、notebook_clickがノートブックを開いているのか閉じているのかを識別する）|ワンホット|
|level| どの階層で起きた出来事か（0〜22）||
|page| イベントのページ番号（ノートブック関連イベントの場合のみ）||
|room_coor_x| ゲーム内のルームを基準としたクリックの座標（クリックイベント時のみ）||
|room_coor_y| ゲーム内のルームを基準としたクリックの座標（クリックイベント時のみ）|
|screen_coor_x| プレイヤーの画面を基準としたクリックの座標（クリックイベント時のみ）|
|screen_coor_y| プレイヤーの画面を基準としたクリックの座標（クリックイベント時のみ）|
|hover_duration| ホバーが発生した時間（ミリ秒）（ホバーイベントの場合のみ）|
|text| このイベントの間、プレーヤーに表示されるテキスト| Drop|
|fqid| イベントの完全修飾ID| Drop|
|room_fqid| イベントが行われた部屋の完全修飾ID| Drop|
|text_fqid| 完全修飾ID|　Drop|
|fullscreen| プレーヤーがフルスクリーンモードであるかどうか|
|hq| 高画質かどうか|
|music| ゲーム音楽のON/OFF|
|level_group| この行がどのレベルグループ（および問題グループ）に属するか（0～4、5～12、13～22）|


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
