# CSV 突合したい

- とりあえずサンプルを落としてきた。
- `Start csv check.`の上は落ちてたものそのまま
- キー項目で結合 `-Where { $args[0].employeeID -eq $args[1].Name }`
- 出力対象の項目を選択 `Select-Object`
