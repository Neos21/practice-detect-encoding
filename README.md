# practice-detect-encoding : Detect Encoding Practice

テキストファイルの文字コードや改行コードを判別・変換する練習用リポジトリ。


## `$ file`

```sh
$ file ./files/*
./files/eucjp-crlf.txt:    ISO-8859 text, with CRLF line terminators
./files/eucjp-lf.txt:      ISO-8859 text
./files/shiftjis-crlf.txt: Non-ISO extended-ASCII text, with CRLF line terminators
./files/shiftjis-lf.txt:   Non-ISO extended-ASCII text
./files/utf8bom-crlf.txt:  UTF-8 Unicode (with BOM) text, with CRLF line terminators
./files/utf8bom-lf.txt:    UTF-8 Unicode (with BOM) text
./files/utf8-crlf.txt:     UTF-8 Unicode text, with CRLF line terminators
./files/utf8-lf.txt:       UTF-8 Unicode text
```


## `$ nkf --guess`

```sh
$ nkf --guess ./files/*
./files/eucjp-crlf.txt:EUC-JP (CRLF)
./files/eucjp-lf.txt:EUC-JP (CR)
./files/shiftjis-crlf.txt:Shift_JIS (CRLF)
./files/shiftjis-lf.txt:Shift_JIS (CR)
./files/utf8bom-crlf.txt:UTF-8 (CRLF)
./files/utf8bom-lf.txt:UTF-8 (CR)
./files/utf8-crlf.txt:UTF-8 (CRLF)
./files/utf8-lf.txt:UTF-8 (CR)
```


## Etc

- `$ cat -A ./files/utf8-crlf.txt`
- `$ cat -e ./files/utf8-crlf.txt`
- `$ od -a ./files/utf8-crlf.txt`
- `$ od -c ./files/utf8-crlf.txt`
- `$ grep -lzUP '\r' ./files/*` … CR を含むファイル名を列挙する

## Author

[Neo](http://neo.s21.xrea.com/) ([@Neos21](https://twitter.com/Neos21))

- [GitHub - practice-detect-encoding](https://github.com/Neos21/practice-detect-encoding)
- [Corredor -  コマンドラインで文字コードや改行コードを調べる方法まとめ](http://neos21.hatenablog.com/entry/2018/04/11/080000)


## Links

- [Neo's World](http://neo.s21.xrea.com/)
- [Corredor](http://neos21.hatenablog.com/)
- [Murga](http://neos21.hatenablog.jp/)
- [El Mylar](http://neos21.hateblo.jp/)
- [Bit-Archer](http://bit-archer.hatenablog.com/)
- [GitHub - Neos21](https://github.com/Neos21/)
