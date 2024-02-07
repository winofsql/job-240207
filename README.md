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
