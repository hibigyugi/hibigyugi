表情を認識するプログラムです。

含まれている内容は以下の2つです。<br>
①顔のパーツを認識<br>
②虹彩の方向を検出

これらの情報を予め作成した3Dのモデルに適応することでアバターに表情や視線の情報を正しく伝え、反映させることが可能です。

Unity上の3Dモデルに反映させた場合の画像は以下の通りです。<br>
<img src="https://github.com/hibigyugi/hibigyugi/blob/main/Picture/%E5%AE%9F%E8%A1%8C%E7%94%BB%E9%9D%A2.PNG"><br>
<br>
画像の認識結果は3次元座標で与えます。<br><br>
0は虹彩の中心を示しており、モデルに反映する際は水平方向に反転しています。<br><br>
虹彩以外にも顔の各パーツにキーポイント（右目の虹彩の場合は0）を設けており、キーポイントと下図に示したような各点との間の距離によってモデルの変形値を計算します。<br><br>
そのため、実際の顔とモデルとの間で顔のパーツの変形の強度を変換し合う関数は個別のモデルごとに用意する必要があります。<br><br>
本手法の新規性はモデルを構築するメッシュにパラメーターを割り振って変形させているため、モデルの作成の際にMayaやBlender上で**予めシェイプキーを設定する必要が無い**という簡便さに集約されます。<br>

<img src="https://raw.githubusercontent.com/hibigyugi/hibigyugi/main/Picture/%E3%82%A2%E3%83%AB%E3%82%B4%E3%83%AA%E3%82%BA%E3%83%A0.PNG">

<br>
本研究の目的は人と人とを強固に繋ぐ新たなコミュニケーションの形を築くことにあります。
