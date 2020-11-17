# *Meishi RE4 : A Lighting Equpment(?)*

<img src="https://raw.githubusercontent.com/Lekipon/Meishi_RE4/main/img/re4_01.JPG" width="640" />



------



## **概要**

Meishi RE4は一見ロータリーエンコーダ一を4つ備えたマクロパッドに見えますが、実際には照明器具です。

キットの組立に関しては別途必要な部品を揃えていただき、写真の見た目通りに組めばいいので特に言及すべきことはありません。

なお、ファームウェアは [QMK Firmware](https://github.com/qmk/qmk_firmware) を使用しています。

<br>

## 特徴

- ロータリーエンコーダを4個搭載可能（CherryMX互換スイッチも使用可能）。

- 4ピンのピンソケットから3本の配線（VCC、DATA、GND）を取り出して、WS2812BのLEDテープ等を光らせることが出来ます。

- PCのUSBコネクタから電源を供給している場合は、基板に実装した3つのLEDが「CapsLock」「NumLock」「ScrollLock」のインジゲータとして機能します。
- ProMicroは700mil幅のMini-Bタイプおよび通常の600mil幅の両方に対応しています。<br>


<br>

## キットに含まれている部品

1：PCB 1枚（WS2812Bを表面に3カ所＋4ピンピンソケットを実装済）

2：ゴム足（小4個）

<br>

## キットとは別に用意が必要な部品

- スイッチ付きロータリーエンコーダおよびツマミ（各4個）
- ProMicro（1個）
- 12ピンのコンスルーまたは12ピンのピンヘッダ（2本）
- 2ピンのタクタイルスイッチ（1個）
- USBケーブル

<br>

## 必要な工具類

- ハンダごて
- ハンダこて台
- 普通のハンダ（スズ60％/鉛40％）

<br>

## QMKファームウェアについて

- デフォルトの[HEXファイル](https://github.com/Lekipon/ASTRA515/blob/master/hex/lekipon_astra515_default.hex)を用意していますので、QMK Toolbox等でProMicroに書込して使用してください。なお、デフォルトでは外部LEDの個数は8個に設定しています。

- デフォルトでは以下の写真のように機能が設定されています。

  <img src="https://raw.githubusercontent.com/Lekipon/Meishi_RE4/main/img/re4_03.JPG" width="640" />  

  

  

  QMKの[本家](https://github.com/qmk/qmk_firmware)には「Meishi RE4」のコードはまだマージされていませんので、デフォルトファームウェアをカスタマイズしたい場合は当面の間[このフォークしたQMK](https://github.com/Lekipon/qmk_firmware)を使用してください。

  

- 既にQMKファームウェアのビルド環境を構築をしている方は、ダウンロードしたqmk_firmware-master.zipを解凍して、出来上がった「qmk_firmware-master/」フォルダの中から「keyboards/lekipon」以下の中身をご自身のビルド環境にコピーしても大丈夫だと思います（lekiponフォルダには作者が他に開発したキーボードのファームウェアも一緒に入っています）。
- ビルドする際にはコマンドライン上でQMKビルド環境のルートフォルダに入って、以下のコマンドでコンパイルします。

```
make lekipon/meishi_re4:default
```

- これでQMKビルド環境のルートフォルダに「lekipon_meishi_re4_default.hex」というファイルが生成されます。このファイルをQMK ToolboxでProMicroに書き込みます。

<br>

- コマンドライン上でそのままProMicroに直接書き込む時は以下のコマンドとなります。

```
make lekipon/meishi_re4:default:flash
```

<br>

<br>

## 使用例

<img src="https://raw.githubusercontent.com/Lekipon/Meishi_RE4/main/img/re4_02.JPG" width="640" />

- 写真では、PCデスクの天板の裏にLEDテープを8個分貼付して、手元の照明に使用しています。
- 作者自身は今のところLEDの点灯テストや照明器具としての用途しか考慮していませんが、他に有効な活用方法を見つけていただけたら幸いです。



<br><br>