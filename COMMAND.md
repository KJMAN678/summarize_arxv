```sh
# 仮想環境
python3 -m venv .venv

source .venv/bin/activate

pip install --upgrade pip

pip install -r requirements.txt
```

.env ファイルを作成し、下記の [OpenAI API](https://platform.openai.com/account/api-keys) の環境変数を設定すること。

```sh
OPENAI_API_KEY="XXXXXX"
```

```sh
# データ収集
python query_arxiv.py  [-d directory] [-n num-papers] [-y from-year] "search keywords"

# サンプル
KEYWORD="offline imitation learning"
python query_arxiv.py   -n 5 -y 2020 $KEYWORD

# スライド作成
python mkmd.py [-o output.md] [-d directory] "keyword"

# サンプル
python mkmd.py $KEYWORD
```
