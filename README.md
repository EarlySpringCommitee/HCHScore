<p align="center">
  <img src="https://github.com/TWScore/Logo/blob/master/%E3%84%92%E3%84%93%E3%84%8D%E3%84%93.png?raw=true">
</p>

# HCHScore
這是一個好棒棒的新竹高中成績系統 API

## HCHScore
用法:

    import HCHScore
    HCHScore.get(ACCOUNT, PASSWORD, MODE)
其中

`ACCOUNT` 是你的學號

`PASSWORD` 是你的密碼

`MODE` 是模式選擇器:

| 模式 | 資料 |
| :---: | -- |
| s | 學期成績 |
| S | 歷年學期成績 (尚未開發) |
| y | 學年成績 (尚未開發) |
| Y | 歷年學年成績 (尚未開發) |
| r | 重修科目 (尚未開發) |
| g | 擔任幹部 (尚未開發) |
| c | 學分資訊 (尚未開發) |
| C | 社團 (尚未開發) |
| p | 學期獎懲 (尚未開發) |
| P | 歷年獎懲 (尚未開發) |
| n | 學期缺曠 (尚未開發) |
| N | 歷年缺曠 (尚未開發) |

### 範例

    import HCHScore
    data_s = HCHScore.get('410999', 'my_password', 's') # 獲取學期成績
    data_sy = HCHScore.get('410999', 'my_password', 'sy') # 獲取學期成績和學年成績


## HCHScore API

用法:

    python api.py

API 的 host 和 port 在 config.ini

### 範例
#### 使用 GET 向伺服器要求學期成績

    curl -X GET "http://127.0.0.1:5000" -d "account=410999&password=my_password&mode=s"
