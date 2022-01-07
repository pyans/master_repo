All files in this directory are encoded by UTF-8 (LF).

京都工芸繊維大学大学院 工芸科学研究科 情報工学専攻
京都工芸繊維大学 工芸科学部 情報工学課程
京都工芸繊維大学 工芸科学部 先端科学技術課程
京都工芸繊維大学 工芸学部 電子情報工学科（昼間コース／夜間主コース）


　　卒業研究（セミナー）報告書・修士論文　作成用 LaTeX スタイルファイル


このディレクトリには以下のファイルがあります．

readme.txt　　　　このファイル
bachelor/
  coverpage.eps   表紙例
  kit-is.bst      文献スタイルファイル
  kit-is-b.sty    卒業研究報告書作成用スタイルファイル
  sample.bib      文献データベース（例）
  sample_b.tex    「修士論文・卒業研究報告書の書き方」
　　　　　　　　　　　　　　　　（卒業研究報告書・セミナー報告書形式）
master/
  coverpage.eps   表紙例
  kit-is.bst      文献スタイルファイル
  kit-is-m.sty    修士論文作成用スタイルファイル
  sample.bib      文献データベース（例）
  sample_m.tex    「修士論文・卒業研究報告書の書き方」（修士論文形式）


【コンパイル方法】

platex sample_b.tex （または sample_m.tex）
pbibtex sample_b （または sample_m）
platex sample_b.tex （または sample_m.tex）
platex sample_b.tex （または sample_m.tex）(注)

(注)相互参照を解決するために，
"LaTeX Warning: Label(s) may have changed. Rerun to get cross-references right."
のようなメッセージが表示される場合は，再度 platex を実行する必要があります．
（これを忘れると，参考文献の番号や図表番号が ? になってしまいます．）

platex コマンドや pbibtex コマンドの名前は環境によって異なる場合があります．


【TeXファイルの書き方】

sample_[bm].tex ファイル内のコメントを参照してください．

参考文献リストの作成には，表記の一貫性を保つため，pbibtex を使うことを
推奨します．


【注意】

・修士論文作成用スタイルファイルでは英文概要も作成しますが，
　学務課が指定している様式（Form 2）とは厳密には一致していません．
　学務課へは Word 形式の電子ファイルも提出する必要がありますので，
　学務課へ提出する英文概要は Word で印刷してください．

・両面印刷を想定した DVI ファイルを作成します．両面印刷の設定で全体を
　印刷することで，表紙と概要は裏面が白紙になるようになっています．

・文献スタイルファイル kit-is.bst の v1.2.0 (2010/11/10) 以降は，
　従来の @webpage 型と互換性がありません．


【不具合の報告先】

この LaTeX スタイルファイルについて不具合がありましたら，布目まで
お願いします．

Email: nunome@kit.ac.jp
