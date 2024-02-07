# job-240207


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
  ```
  chrome://policy/
  ```

  ![image](https://github.com/winofsql/log-240207/assets/1501327/37f4414e-1494-44ba-b9e1-45291d96f4a2)


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

  - 保護のついたままこの PDF をダブルクリックすると、本来の Chrome が実行されずに HP 内の特殊 Chrome が起動します
    ![image](https://github.com/winofsql/log-240207/assets/1501327/9d41e020-356f-4f43-b81e-a62f62522fe6)

    ![image](https://github.com/winofsql/log-240207/assets/1501327/8f05e679-04d1-4fce-b026-032050415f03)

  - ## 🌉 HP の Wallpapaer の場所
    - C:\Windows\Web\Wallpaper\HP

## Windows11 の右クリックで Windows10 のポップアップメニューを表示する 
  - 🔴 プログラマ的には運用上こちらである必要があります( 管理がすぐに実行できる )
  - ( ポップアップメニューのショートカットは SHIFT + F10 )\
  ![image](https://github.com/winofsql/job-240207/assets/1501327/b1816c8c-7fee-427f-951e-658ec2b7dbbd)
- ### 設定
  ```reg
  reg add "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /f 
  ```

- 実行後エクスプローラ再起動
  ![image](https://github.com/winofsql/job-240207/assets/1501327/cdee5bc9-b139-4178-8b7d-5ccd60b921ce)


- ### 元に戻す
  ```reg
  reg delete "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /f 
  ```
  ![image](https://github.com/winofsql/job-240207/assets/1501327/3dd3a09b-f56b-4393-8fc5-3a5c97305336)

  この状態からは、その他のオプションで Windows10 のポップアップメニューが表示されます


- ### Windows11 のタスクバーメニューの左寄せと右端でデスクトップ表示
  ```
  reg add "HKCU\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced" /v "TaskbarAl" /t REG_DWORD /d 0 /f
  reg add "HKCU\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced" /v "TaskbarSd" /t REG_DWORD /d 1 /f
  
  ```

  ![image](https://github.com/winofsql/subject-windows11/assets/1501327/d1b830c6-7737-43ca-9689-b147e240493e)
  
  ![image](https://github.com/winofsql/subject-windows11/assets/1501327/6002978d-7c30-4019-86d8-9084ef12d03b)
  
  ![image](https://github.com/winofsql/subject-windows11/assets/1501327/8bb8e170-46e7-43af-8619-9e6630f86683)
