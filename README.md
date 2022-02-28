docker-compose gitlab
===

## Usage

```sh
mkdir gitlab
mkdir gitlab-runner
```

```sh
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