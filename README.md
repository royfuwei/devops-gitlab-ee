docker-compose gitlab
===

## Usage

```sh
# .env 設定變數
cp .env.example .env
vim .env

# gitlab.rb 設定檔
cp ./config/gitlab.rb.example ./config/gitlab.rb
vim ./config/gitlab.rb

# root_password.txt gitlab root password
cp ./config/root_password.txt.example ./config/root_password.txt
vim ./config/root_password.txt


mkdir gitlab
mkdir gitlab/config
mkdir gitlab/data
mkdir gitlab/log

# mkdir gitlab-runner

docker-compose up -d
```

```sh

docker exec -it gitlab bash

# 使用指令重新載入設定檔。
gitlab-ctl reconfigure

# 使用指令進入 GitLab 主控台。
gitlab-rails console
# irb(main):001:0> Notify.test_email('收件者信箱', '標題', '內文').deliver_now
```

<!-- // TODO: 先記錄一些筆記之後整理 -->

## issue

* google smtp
> 使用 Gmail SMTP 寄信時，如果遭遇身分驗證錯誤，可參考 Google 官網文件：[允許安全性較低的應用程式使用您的帳戶](https://support.google.com/accounts/answer/6010255) 或是 [啟用兩步驟驗證功能](https://support.google.com/accounts/answer/185839) 使用 [使用應用程式密碼登入](https://support.google.com/mail/answer/185833)。