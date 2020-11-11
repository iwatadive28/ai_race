# setup

* インストール手順を自動化するスクリプト
* 失敗した時点で停止します。状況により手動インストールを併用下さい。
* （場合により全自動にならないことがあります。Pull Requestのボランティア募集中です。） <br>

## 使い方

### sudo apt-get update 時にパスワードを聞かれないようにする（[参考](https://www.hiroom2.com/2018/10/23/ubuntu-1810-sudo-ja/)）

```
$ sudo visudo    # user:jetsonの場合
# Allow members of group sudo to execute any command
%sudo  ALL=(ALL:ALL) NOPASSWD:ALL
```

備考： "esc+:wq" でエディタを終了

### スクリプト実行

```
cd ~
mkdir -p tmp; cd tmp;
git clone https://github.com/seigot/ai_race
cd ai_race/scripts/setup
time ./auto_setup.sh
```

## Tips
* opencvインストール時はgdmを選択