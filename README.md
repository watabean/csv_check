# CSV 突合したい

## 手順

windows で powershell を立ち上げる。初回のみ下記コマンドが必要。

```powershell
# 初回のみ
Set-ExecutionPolicy RemoteSigned
```

対象のディレクトリに移動して、スクリプトを実行

```powershell
# 対象のスクリプトをおいたディレクトリへ移動
cd C:¥Users¥~~
# 実行
.¥csv_check.ps1
```

csv ファイルを読み込んで、result.csv が生成される。

## csv_check.ps1 の概要

- とりあえずサンプルを落としてきた。
- `Start csv check.`から上は落ちてたものそのまま
- キー項目で結合 `-Where { $args[0].employeeID -eq $args[1].Name }`
- 出力対象の項目を選択 `Select-Object`
