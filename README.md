# V2b-Theme-Sleek暗黑主题
> 前后端分离主题 可搭建多个前端应用 <br>
> 请注意同源策略 <br>
> 支持Workers或Pages <br>


## 安装教程
- 后端：修改v2b后端支付回调文件 
  > 前后端分离重要步骤 
  - 进入目录 `app/Services/PaymentService.php`

  - 文件第50行 `'return_url' => config('v2board.app_url') . '/#/order/' . $order['trade_no'],`
  - 修改成：` 'return_url' => $_SERVER['HTTP_ORIGIN'] . "/#/dashboard",` 

    - 前端：可以直接放到 Workers或Pages 也可以直接放到网站目录使用
    - 前端配置部分都在config.js 文件里
    - 修改config.js的hosturl 填写后端网址 `https://xxxx.xx/` 格式
    - 在线客服请到index.html里插入代码
    - 网页标题和svg都在index.html 自行更改 有能力的可自行混淆config.js 文件

### 注意事项
> - v2b后台的邀请限制不要为0 不然会报错 
> - 用https 不然某些功能用不了 
> - 注意cors策略!!



基于[V2b-Theme-Sleek](https://github.com/binglog/V2b-Theme-Sleek)修改
