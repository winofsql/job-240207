# log-240207


## chrome-policy-settings.reg
- 
  | キーワード                        | 値              | 制御内容                                                     |
  |----------------------------------|-----------------|--------------------------------------------------------------|
  | ShowHomeButton                   | dword:00000001  | ホームボタンの表示を有効にする                                |
  | AutofillAddressEnabled           | dword:00000000  | 住所の自動入力を無効にする                                    |
  | HomepageLocation                 | "https://www.google.com/" | ホームページの場所を指定する                              |
  | BrowserThemeColor                | "#FFFFFF"       | ブラウザのテーマカラーを指定する                              |
  | PromptForDownloadLocation        | dword:00000001  | ダウンロード場所の指定をプロンプトする                        |
  | AutofillCreditCardEnabled        | dword:00000000  | クレジットカードの自動入力を無効にする                        |
  | ShowAppsShortcutInBookmarkBar    | dword:00000000  | ブックマークバーにアプリショートカットを表示しない             |
  | HomepageIsNewTabPage             | dword:00000000  | ホームページが新しいタブページであるかどうかを指定する         |
  | PasswordManagerEnabled           | dword:00000000  | パスワードマネージャーを無効にする                            |
  | TaskManagerEndProcessEnabled     | dword:00000001  | タスクマネージャーでプロセスの終了を許可する                  |
  | TranslateEnabled                 | dword:00000001  | ページの翻訳を有効にする                                      |
  | BrowserAddPersonEnabled          | dword:00000000  | ブラウザにユーザーを追加する機能を無効にする                  |
  | NTPCustomBackgroundEnabled       | dword:00000000  | 新しいタブページのカスタム背景を無効にする                    |

- 🔼 [この内容は ChatGPT3.5 が作成しました](https://chat.openai.com/share/72f5d2e4-8738-465c-9ce3-32b17ccbb984)
  - [GPT4 で実行するとこうなります](https://chat.openai.com/share/b84c0f93-3df5-4a38-bd7b-e7f6ba719049)
    - HomepageIsNewTabPage がきちんと説明されました
- 🔴 この内容は chrome://policy/ で参照できます

- ### 以下は Chrome を閉じた時にログアウトする URL の一覧です
  ```
  [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Google\Chrome\CookiesSessionOnlyForUrls]
  "1"="[*.]google.com"
  "2"="github.com"
  "3"="replit.com"
  "4"="[*.]lolipop.jp"
  "5"="paiza.jp"
  "6"="[*.]zoom.us"
  "7"="twitter.com"
  ```

## HPの保護マークのついたファイル の保護の解除
  ![image](https://github.com/winofsql/log-240207/assets/1501327/6c2f01f8-25f8-49ee-8128-dd9bdf777139)
