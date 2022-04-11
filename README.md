Code is not available to the public at the moment.

# Order Bot

Latest video demo [here](https://x1a-alioss.oss-cn-shenzhen.aliyuncs.com/OrderBot_v02_demo.mov)

---
## Version 0.2 Released (2022.04.13)
What's new in the version: (Watch the [video demo](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/a360605a-336e-47ce-9b95-8fc9ddc9e9c2/Untitled.qt?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220411%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220411T125353Z&X-Amz-Expires=86400&X-Amz-Signature=c56fd5ba2111a549371b7d3333a3e610678028299d015ba8afff2da71875fd57&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.qt%22&x-id=GetObject) for new features!)

nlu:
- add intent-payment and action-action_payment
```
- user: 我要埋单
- bot: 你嘅購物車為空，唔得結帳喔～
```
- today's menu recommendation
```
- user: 你好
- bot: 你好！歡迎嚟到SMART茶餐廳～ 如果中途遇到bug，可輸入 \restart 重新開始～ 
      今日推薦菜單：
      - 牛肉通粉 35元
      - 火腿通粉 36元
      - 和風蜆肉烏冬 39元
```
- cantoneseization
```
好嘅，已將其加入購物車。請問你還需要其他咩？我哋有飲品和小食～
你依家嘅購物車如下：{}，總共{}元。請問你還需要乜～
...
```
- feedback filling
```
- bot: 感謝你嘅反饋！你可以點擊以下鏈接或掃描二維碼填寫對機器人嘅意見和建議～ https://workspace.jianguoyun.com/inbox/collect/487cf93eab65443181e68daa0260b15c/submit
```
<img src="https://x1a-alioss.oss-cn-shenzhen.aliyuncs.com/feedback_QR.png"  width = "200" height = "200"/>

core:
- match 'food_name', 'food_type' based on text similarity
```
- user: 一個雞排飯
- bot: 好的，你想要1份蘑菇雞排飯，總價37元，對嗎
- user: 我要吃牛腩
- bot: 好像沒有呢，為你推薦xxx
```
- add validation for entities


---

## Version 0.1 Released (2022.03.30)

What's new in the version: (Watch the [video demo](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/a812fd6a-6dac-4163-bb72-cac597e33867/Screen_Recording_2022-03-29_at_00.20.59.mov?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220329%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220329T040935Z&X-Amz-Expires=86400&X-Amz-Signature=1d62e9f2c0398cbe9073cbf755c4f3b3c2c89bd146d34ceff9310e250a42f99a&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screen%2520Recording%25202022-03-29%2520at%252000.20.59.mov%22&x-id=GetObject) for new features!)

nlu:

- improve nlu robustness by adding more name and food name training data

core:

- qurery shopping cart
```
- user: 點幾個菜啦
- bot: 你嘅訂單編號為{}，訂單內容為：{}。總共{}元，請問系線上支付仲系線下支付？
```
- customer satisfaction survey
```
- bot: 請畀本次點菜服務評分
    1. 系否用戶友好？（5最優，1最差）
    2. 對話系否流暢？（5最優，1最差）
    3. 系否成功完成訂單？（5最優，1最差）
```

---

## Version 0.0 Released (2022.03.23)

What's new in the version: (Watch the [video demo](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/28fa8ec5-8b4b-4995-accf-f95aa095fe07/Screen_Recording_2022-03-22_at_14.07.37.mov?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220329%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220329T041014Z&X-Amz-Expires=86400&X-Amz-Signature=1aa6cf78e0362424140c91ededbc8211d77fdd7fb52d9fd74c73a099c10fda4f&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screen%2520Recording%25202022-03-22%2520at%252014.07.37.mov%22&x-id=GetObject) for new features!)

nlu:

- entity extraction and intent detection
- self-defined tokenized dictionary
- regex feature extraction
- lookup table feature extraction
- synonym mapping

core:

- dialogue flow
- query food menu and price
```
- user: 有什麼飯
- bot: 今天的飯有：
[['野菌燴飯' '35元']
 ['祖傳肉燥飯' '36元']
 ['蘑菇雞扒飯' '37元']
 ['龍蝦汁燴石斑飯' '38元']]
```
- make order
```
- user: 我要藍莓芝士蛋糕
- bot: 你要幾個
- user: 1個
- bot: 好的，你想要1份藍莓芝士蛋糕，總價15元，對嗎
- user: 對的
- bot: 好嘅，已將其加入購物車。請問你還需要其他咩？我哋有飲品和小食～
```
- modify order
```
- user: 我要一個藍莓芝士蛋糕
- bot: 好的，你想要1份藍莓芝士蛋糕，總價15元，對嗎
- user: 換成意式提拉米蘇
- bot: 好的，你想要1份意式提拉米蘇，總價16元，對嗎
```
- add order
```
- bot: 好嘅，已將其加入購物車。請問你還需要其他咩？我哋有飲品和小食～
- user: 我還要兩個台南芋糕
- bot: 好的，你想要2份台南芋糕，總價26元，對嗎
```
- personal information
```
- bot: 請提供你嘅姓名和房間號（3-4位數字），以方便工作人員送餐。
- user: 李先生 123
```
- order payment
```
- bot: 你已掂下單！訂單編號為'李先生_123'，訂單內容為：['1份藍莓芝士蛋糕' 和 '1份意式提拉米蘇' 和 '2份台南芋糕']。總共57元，請問系線上支付仲系線下支付？
- user: wechat
- bot: 即將跳轉到支付平台...你嘅柯打已掂支付，餐食將會喺15分鍾後送達你嘅房間，請你心機等待～
```

---

## Configuration

Config the enviorment:

```
cd OrderBot/env
pip install -r requirements.txt
# or conda create --OrderBot —OrderBot.yaml
```

Train the nlu model and valid on train and test set:

```
conda activate OrderBot
rasa data split nlu --training-fraction 0.8
rasa train --data train_test_split/training_data.yml
rasa test nlu --nlu train_test_split/test_data.yml --out results/test
rasa test nlu --nlu train_test_split/training_data.yml --out results/train
```

Train the model :

```
conda activate OrderBot
rasa train --data data/
```

Talk to - bot:

```
conda activate OrderBot
rasa run actions
```

```
conda activate OrderBot
rasa shell
```

Interactivate on trained model:

```
conda activate OrderBot
rasa run actions
```

```
conda activate OrderBot
rasa interactive -m models  --skip-visualization
```

[demo](https://x1a-alioss.oss-cn-shenzhen.aliyuncs.com/OrderBot_v02_demo.mov) input:
```
你好 -- greeting
結帳 -- payment
有炒飯嗎 -- ask submenu with 飯
一個雞扒飯 -- item_start_generic with fuzzy name
對 -- confirm order
有炸雞嗎 -- add order (path2), matching dish names to 小吃 categories based on 炸雞
一個芝士蛋糕 -- item_start_generic with fuzzy name
換成提拉米蘇 -- change order food_name
兩個 -- change order food_amount
嗯嗯 -- confirm order
還要一個鳳梨蝦球 -- add order (path1)
是的 -- confirm order
現在點幾個菜啦 -- query shopping cart
還有什麼喝的 -- ask submenu with 飲品
一杯latte -- item_start_generic
對 -- confirm order
不用了
李先生 123 -- customer infomation
wechat -- pay_online
```
