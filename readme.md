# Checkin

GitHub Actions 实现 [GLaDOS][glados] 自动签到

([GLaDOS][glados] 可用邀请码: `0S5JS-QLFOM-N3NYY-ZVQ2Q`, 双方都有奖励天数)

## 使用说明

### 1. Fork 这个仓库

### 2. 获取 GLaDOS Cookie

（1）打开[GLaDOS][glados]签到页面，

（2）按F12（或者 Ctrl+Shift+I）打开「开发者工具」，按F5刷新页面

（3）点出「Network」→「All」→「info」→「Request Headers」→「Cookie」,找到Cookie,格式类似 koa:sess=xxxxxx; koa:sess.sig=xxxxxx, 复制出来备用

![01](https://github.com/user-attachments/assets/42f3568f-4ce2-4663-b9c0-9cdab8c06a88)

### 3. 设置 GitHub Actions

（1）打开 GitHub 仓库设置 Settings → Secrets and variables → Actions → New repository secret

![02](https://github.com/user-attachments/assets/4e8e1fcd-3336-4240-be23-c4f3308da506)

（2）Name: GLADOS，    Secret: 前面获取的 GLaDOS Cookie 值

![03](https://github.com/user-attachments/assets/83a33754-60f2-470c-8617-1df377e46daa)

### 4. 启用 Actions, 每天北京时间 00:10 自动签到

（1）打开 GitHub 仓库 Actions 标签页, 点击 I understand my workflows, go ahead and enable them

![04](https://github.com/user-attachments/assets/f76103b4-b945-41f4-869e-50df31e7dd77)

（2）点击run → Enable workflow，完成

![05](https://github.com/user-attachments/assets/2d539ba3-377d-4e43-8668-f6a893641943)

### 5. 通过[PushPlus][pushplus]设置微信通知（如果不需要微信通知, 可以跳过这一步）
（1）打开[PushPlus][pushplus]，微信扫码登录并实名认证（需支付1元认证费），点出「一键复制」，复制token

![06](https://github.com/user-attachments/assets/031bc083-7103-4a09-b1f3-dc1315486e06)

（2）打开 GitHub 仓库设置 Settings → Secrets and variables → Actions → New repository secret

![07](https://github.com/user-attachments/assets/be995443-1264-4631-adb7-3e624e3f4edf)

（3）Name: Notify，    Secret: 前面获取token

![08](https://github.com/user-attachments/assets/78067ee0-0cbc-459c-9ee0-5d0bdea9a0d2)

[glados]: https://glados.rocks/console/checkin
[pushplus]: https://www.pushplus.plus/push1.html
