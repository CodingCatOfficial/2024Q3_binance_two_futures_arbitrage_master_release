# Binance Futures Arbitrage Master

## 項目概述
此程式接受輸入 Binance 兩不同合約交易對以及匯率，並且在偵測滿足價差的情況下使用api進行雙邊下單，以達成 Long Short。


## 使用說明
1. 使用 save_api 來將 `apikey`、`secret` 儲存至 `config.json` 中
2. 打開程式、登入，輸入標的(合約1、合約2) & 合約1、 2的比例，點擊設定
3. 待程式讀取一下，會抓到合約1、2 的買賣 & 溢價資訊，及該帳號的持倉顆數及 IM、MM
4. 設定 下單次數、單次下單數量、掛單簿數量要求、溢價指數小於 x%
5. 按下相對應的按鈕(看要做多誰、做空誰)


### `config.json` 設置說明

-  "api_key": "幣安 api key",
-  "secret_key": "幣安 secret key",
-  "fr1_symbol": "輸入合約1名稱，例如: FETUSDT",
-  "fr2_symbol": "輸入合約1名稱，例如: AGIXUSDT",
-  "fr1_ratio": 合約1 的比例,
-  "fr2_ratio": 合約2 的比例,
-  "fr1_qty": 合約1 單次下單顆數,
-  "fr1_order_book_qty_requirement": 合約1 掛單簿數量要求,
-  "fr2_qty": 合約2 單次下單顆數,
-  "fr2_order_book_qty_requirement": 合約2 掛單簿數量要求,
-  "iterations_entry": 總下單次數

以下為 `config.json` 的範例，請依自行需求做相關設定

```
{
  "api_key": "xxxxxxxxxx",
  "secret_key": "yyyyyyyyy",
  "fr1_symbol": "FETUSDT",
  "fr2_symbol": "AGIXUSDT",
  "fr1_ratio": 433.226,
  "fr2_ratio": 1000,
  "fr1_qty": 13,
  "fr1_order_book_qty_requirement": 50,
  "fr2_qty": 30,
  "fr2_order_book_qty_requirement": 100,
  "iterations_entry": 4
}
```


## 更新日誌
詳情請查看 [CHANGELOG.md](CHANGELOG.md)。

## 版權信息
Copyright (c) 2024 Murmurcats NFT 社團，所有權利保留 [LICENSE](LICENSE)。

## 開發者
[godgiraffe](https://github.com/godgiraffe)

## 協作者
[jeffrey1167](https://github.com/jeffrey1167)
[hyctw](https://github.com/hyc5566)
[RRRobert](https://github.com/yuying990718)
[0xCatduck](https://github.com/0xCatduck)
