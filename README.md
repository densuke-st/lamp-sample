# これはなに?

LAMP構築の一例として、Ansibleを用いた構成の自動化を表現したものになっています。
YAMLという書式にて記述されています(YAML自体は広く使われるデータ表現形式です)。

# 構成内容

ざっくりこんなことを確認・処理させてます。

- apache2, php, mysql(-server)のインストール
- www-dataにvboxsfのケイパビリティを付与
- htmlディレクトリを共有ディレクトリ上に差し替え(`/media/VirtualBox_Shared`固定)
- 各サービスの自動起動設定および起動状態

# どうやって使うの?

利用するには、Ansibleのインストールが必要です。
それなりに準備にストレージが必要です。

```bash
$ sudo apt update
$ sudo apt install -y ansible
```

あとはPlaybookを適用していきます。

```bash
$ ansible-playbook -i host site.yml
```

# 参照情報

- 授業資料
- [Ansible](https://www.ansible.com/)
- [Ansibleドキュメント](https://docs.ansible.com/ansible/2.9_ja/index.html)
