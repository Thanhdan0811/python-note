# flask , flask_restful, flask_cors
- py -3.12 -m pip install -U flask-cors
- py -3.12 -m pip install -U flask
- py -3.12 -m pip install -U flask_restful

## flask
- from flask import jsonify, redirect


## flask_cors
```
from flask_cors import CORS
CORS(app)
```

# bs4 chuyển đổi thành html từ response
- from bs4 import BeautifulSoup


# xử lý date : pytz
- from datetime import datetime, date
```
excel_name = datetime.now().strftime("%d-%m-%Y")
dt = datetime.now().replace(hour=17, minute=41, second=00, microsecond=00)
datetime.now().replace(hour=17, minute=55, second=00, microsecond=00)
```
- pytz : set timezone

```
pytz.timezone("Asia/Ho_Chi_Minh")
datetime.fromtimestamp(get_timestamp(st["TradingDate"]) / 1000, pytz.timezone("Asia/Ho_Chi_Minh"))
```

# set interval task : apscheduler
- from apscheduler.schedulers.blocking import BlockingScheduler

```
sched = BlockingScheduler()
```

# pandas
```
DF_stock = {
            "Ngày lấy dữ liệu": [], 
            "Ngày dữ liệu":[], 
            "VS-Sector": [], 
            "Thay đổi": [], 
            "% thay đổi": [], 
            "Khối lượng": [], 
            "Giá trị": [], 
            "KL NĐTNN Mua": [], 
            "KL NĐTNN Bán": []
        }
for st in data:
    # "/Date(1704992400000)/"
    time_process = datetime.datetime.fromtimestamp(get_timestamp(st["TradingDate"]) / 1000, pytz.timezone("Asia/Ho_Chi_Minh"))
    time_process = time_process.strftime("%d-%m-%Y")
    DF_stock["Ngày lấy dữ liệu"].append(datetime.datetime.now().strftime("%d-%m-%Y"))
    DF_stock["Ngày dữ liệu"].append(time_process)
    DF_stock["VS-Sector"].append(st["Text"])
    DF_stock["Thay đổi"].append("{:,.2f}".format(st["CloseIndex"]))
    DF_stock["% thay đổi"].append("{:,.2f}%".format(st["ChangeClose"]))
    DF_stock["Khối lượng"].append("{:,}".format(st["Vol"]))
    DF_stock["Giá trị"].append("{:,}".format(st["Val"]))
    DF_stock["KL NĐTNN Mua"].append("{:,}".format(st["ForeignBuyVol"]))
    DF_stock["KL NĐTNN Bán"].append("{:,}".format(st["ForeignSellVol"]))
    # print(type(DF_stock["Khối lượng"][0]))

df = pd.DataFrame(data=DF_stock)
```

# các module khác :
- sys, os.path
- 
