# aa
ascii art henkan

# draft
process
```
1.チップセットを決める。
漢字は密度が高く画像プロファイルも豊富な為、平仮名、片仮名、漢字の第一水準と句読点、カギカッコから校正する。
これらを表現文字種と呼ぶ。表現文字種は後々変更出来るようにする。例えば文字列で指示するような。等幅フォントは必須である。
2.表現文字種の画像プロファイルを解析する。
ある区画された画像に、最も近い、画像プロファイルを選択する。
3.画像の輪郭を誇張させる。
二値数のドット絵で表現出来る段階まで誇張させる。
4.画像を区画し、その画像プロファイルを取得する。
画像プロファイルはドット絵と理解すると良い。区画は16*16か32*32、64*64の何れかとする。
もちろん、16*16の方が多数の文字を必要とし、再現度が良いように思われる。
但、反面、比較する情報が少ない為、その分再現度が劣る。最終的に最も良さそうな区画サイズを初期値にする。
5.画像のドット絵と漢字のドット絵を比較し最も近いものを採用する。
6.全て文字変換された後、出力する。
変換した文字数は、変換した文字群＋高さにおける改行数である。

この変換は、対象画像を分割し、適当な文字を割り当てているが、文字ではなく、適当なドット画像でも可能だろう。
何故なら、文字もまた、あるドット画像としてプロファイルを取得するからである。
```
余白の扱い
```
余白は空文字でも良いが、「＋」を使って埋める。その方が、枠を表現しやすいからである。
空文字だけだと、何処までが枠であるのか、わからない。
```
