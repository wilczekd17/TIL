#OpenDroneMap日本語版パッケージの使い方
仮想環境に6GB割り当ててます。その負荷に耐えられるPCを準備してください。

##使用手順
###①Vagrantの設定と立ち上げ
ターミナルを立ち上げる。

```bash
$ cd vagrant
$ ls
  crisis_odm ←たぶんこういうネーミングのフォルダがあると思います。
$ cd crisis_odm
$ vagrant up
$ vagrant ssh
```

###②OpenDroneMapの動作テスト
```bash
$ cd /vagrant/OpenDroneMap/
$ ./run.py -h
#ここで起動すれば問題なくOpenDroneMapの処理を実行できます
```

###③サンプル・データにアクセスし、処理の実行
```bash
$ mkdir /vagrant/odm_data/
$ cd /vagrant/odm_data/　　#以下のディレクトリにサンプル・データをダウンロードしていきます
$ git clone https://github.com/OpenDroneMap-ja/odm_data_keioSFC.git ←慶應SFCの例
$ cd {data_name/}
$ ./../../OpenDroneMap/run.py
```

##OpenDroneMapのサンプル・データ一覧
OpenDroneMapを用いるためのサンプル・データ一覧です。  
初心者の方は太字に示されているデータから扱うことをオススメします

リポジトリ名 | 画像数 | サイズ (MB) | Coordinates in EXIF: | GCPs in File:
------|:----------:|:-----------:|:----------------------:|:---------------:
odm_data_apt | 76 | 579 | ✕ | ✕
odm_data_benchmark | 25 | 106 | ◯ | ✕
**odm_data_caliterra** | 77 | 272 | ◯ | ✕
odm_data_langley | 200 | 706 | ✕ | ✕
odm_data_pacifica | 12 | 66.4 | ✕ | ✕
odm_data_seneca | 167 | 358 | ◯ | ✕
odm_data_keioSFC | 194 | 979.7 |  ◯ | ✕
odm_data_snowpeak | 140 | 767.3 |  ◯ | ✕