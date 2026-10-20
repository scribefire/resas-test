# 日本の賃金を地図とグラフで見る

CSVに収録した賃金データを、Streamlitで可視化するアプリです。都道府県、年齢、産業ごとの傾向を切り替えて確認できます。

## 見られる内容

- 2019年の都道府県別賃金ヒートマップ
- 選んだ都道府県と全国の賃金推移
- 年齢別の賃金・賞与の推移
- 産業大分類ごとの賃金比較

## 起動

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install streamlit pandas numpy matplotlib pillow pydeck plotly
streamlit run 2-3.py
```

## 地図表示に必要なファイル

賃金データは `csv_data/` にあります。地図用の `pref_lat_lon.csv` はリポジトリに入っていないため、起動前にルートディレクトリへ用意してください。列は `pref_name`、`lat`、`lon` を使います。

グラフはPandasでデータを結合・集計し、地図をPyDeck、その他の可視化をPlotly Expressで表示しています。
