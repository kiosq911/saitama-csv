# saitama-csv

**CSV と Excel のファイルを、待たずに開く Windows 用ビューア。**

大きいファイルでも、開いた直後から先頭を表示します。残りは裏で読み込みます。

インストール不要。ZIP を展開して `saitama-csv.exe` を起動するだけです。レジストリには書き込みません。
設定は `saitama-csv.exe` の隣の `_configs` フォルダに置きます。
**やめるときは、展開したフォルダを削除して終わりです。**

> ⚠ **動作の確認を進めている段階です。** 大切なファイルは、まずコピーで試してください。

---

## 開けるファイル

| 種類 | 拡張子 |
|---|---|
| CSV・TSV | `.csv` `.tsv`（UTF-8・Shift_JIS・UTF-16） |
| Excel | `.xlsx` `.xlsm` `.xlsb` `.xls` |
| OpenDocument | `.ods` |

- 表示できるのは、Excel と同じ 1,048,576 行・16,384 列までです。それを超えた行・列があるときは、画面下の帯に数を出します

## 使い方

- `saitama-csv.exe` へファイルをドラッグ＆ドロップする、窓へファイルを落とす、または上の「開く」から選びます
- セルを選ぶと、上の帯に中身（数式）が出ます。範囲を選んでコピーできます
- 列の見出しの境目をドラッグすると、列の幅を変えられます
- セルを書き換えて、「別名で保存」で別のファイルへ保存できます
- 「⚙ 設定」で、行番号のカンマ・選んだ行と列の色づけ・フォントを変えられます

## 「WindowsによってPCが保護されました」と出たときは

署名証明書を付けていないため、初めて起動したときに Microsoft Defender SmartScreen の青い画面が出ます。
これはウイルスが見つかったという意味ではなく、「この配布元をまだ見たことがない」という意味です。

1. 「詳細情報」を押します
2. 「実行」を押します

公開した ZIP は、公開の前に VirusTotal で検査しています。結果は各リリースの本文にあります。

## 通信について

**saitama-csv は通信を一切行いません。** 開いたファイルの中身や利用者の情報を、どこへも送りません。

## 同梱ファイル

| ファイル | 中身 |
|---|---|
| `saitama-csv.exe` | 本体 |
| `README.txt` | この説明 |
| `LICENSE` | 使用許諾条件 |

## 更新のしかた

1. [Releases](https://github.com/kiosq911/saitama-csv/releases/latest) から新しい `saitama-csv.zip` を取ります
2. saitama-csv を閉じます
3. ZIP の中の `saitama-csv.exe` で、前の `saitama-csv.exe` を置き換えます（`_configs` フォルダはそのまま残すと、設定を引き継ぎます）

ZIP が壊れていないかは、リリースの本文にある SHA-256 と照らして確かめられます。

```powershell
Get-FileHash saitama-csv.zip -Algorithm SHA256
```

## 不具合の報告・要望

[Issues](https://github.com/kiosq911/saitama-csv/issues) へどうぞ。
開いたファイルの中身は書かないでください（他の人も読めます）。

## ライセンス

無償で使えます。改変しないかぎり再配布できます。販売は禁止です。詳しくは [LICENSE](LICENSE) を見てください。
使っている部品のライセンスは [docs/THIRD_PARTY_LICENSES.txt](docs/THIRD_PARTY_LICENSES.txt) にあります。
