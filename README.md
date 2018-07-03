# CSV 突合したい

## 手動で実施する場合

1.  powershell を立ち上げる
2.  対象のディレクトリまで移動

```powershell
cd C:¥User¥~~ # 対象のディレクトリ
```

3.  下記コマンドを順次打ち込む

```powershell
$A = Get-Content user1.csv #ここは比較したいファイル名１
$B = Get-Contetn user2.csv #ここは比較したいファイル名２
Compare-Object $A $B
```

4.  結果を見る。

## 自動で実行する場合

1.  おなじ
2.  おなじ
3.  初回のみ下記コマンド

```powershell
# 初回のみ
Set-ExecutionPolicy RemoteSigned
```

4.  実行

```powershell
# 中身は手動のと一緒
.¥csv_check.ps1
```
