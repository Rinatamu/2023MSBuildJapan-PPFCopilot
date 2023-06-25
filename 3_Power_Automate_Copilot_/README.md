# Power Automate

## 1. 日報アプリの作成

## 1. SharePoint List の作成

トリガー実行用のSharePoint List を作成します。

### 1-1. サイトの作成

1. SharePoint にアクセスします。

![](pasteimage/2023-06-26-01-25-08.png)

2. サイトの作成をクリックします。

![](pasteimage/2023-06-26-01-25-46.png)

3. チームサイトをクリックします。

![](pasteimage/2023-06-26-01-26-22.png)

4. サイト名を「経費精算サイト」とします。

![](pasteimage/2023-06-26-01-27-48.png)

5. グループメールアドレスを以下のようにします。

```
keihi-seisan
```

![](pasteimage/2023-06-26-01-29-04.png)

6. 言語の選択を、日本語に変更して、「次へ」をクリックします。

![](pasteimage/2023-06-26-01-29-57.png)

7. しばらく待って、「完了」をクリックします。

![](pasteimage/2023-06-26-01-31-00.png)

8. サイトが作成されます。

![](pasteimage/2023-06-26-01-32-02.png)

### 1-2. リストの作成

1. サイトコンテンツをクリックします。

![](pasteimage/2023-06-26-01-33-15.png)

2. 新規から、リストをクリックします。

![](pasteimage/2023-06-26-01-34-03.png)

3. 空白のリストをクリックします。

![](pasteimage/2023-06-26-01-35-14.png)

4. 以下の名前を設定して、「作成」をクリックします。

```
経費申請
```

![](pasteimage/2023-06-26-01-36-05.png)

5. 列の追加から、選択肢をクリックし、次へをクリックします。

![](pasteimage/2023-06-26-01-37-42.png)

6. 以下の図のように設定し、「保存」をクリックします。

![](pasteimage/2023-06-26-01-39-09.png)

7. 列の追加から、通貨をクリックし、次へをクリックします。

![](pasteimage/2023-06-26-01-40-35.png)

8. 以下の図のように設定し、「保存」をクリックします。

![](pasteimage/2023-06-26-01-41-45.png)

## 2. Power Automate 作成

### 2-1. Power Automate フロー作成依頼

1. Power Automate の Home 画面の Copilot 入力画面を表示します。

![](pasteimage/2023-06-26-00-18-25.png)

2. 入力画面に以下を入力して、送信ボタンを押してみます。

```
create a new item to sharepoint list and approval.
```

![](pasteimage/2023-06-26-01-45-34.png)

3. 質問内容を読み取り、作成予定のフローが表示されます。「Next」をクリックします。

![](pasteimage/2023-06-26-01-46-37.png)

4. 接続情報の確認画面が表示されます。「Next」をクリックします。

![](pasteimage/2023-06-26-01-48-15.png)

5. 各項目を可能な限りそれぞれ埋めていきます。

![](pasteimage/2023-06-26-01-50-49.png)

6. Create flow をクリックします。

![](pasteimage/2023-06-26-01-51-28.png)


7. フローが作成されます。

![](pasteimage/2023-06-26-01-52-42.png)

### 2-2. Copilot 操作

1. Copilot 画面で以下のように支持します。

```
add SharePoint Update Item to after the Condition False.
```

2. Condition False の後続に、SharePoint の Update Item アクションが追加されることを確認します。

![](pasteimage/2023-06-26-02-02-17.png)

3. Copilot 画面で以下のように支持します。

```
Change Action "Send an Email" to Teams post messege.
```

4. Outlook のメール送信アクションが、Teams のメッセージ送信アクションに変わったことを確認します。

![](pasteimage/2023-06-26-02-05-24.png)

5. Copilot 画面で以下のように支持します。

```
Set Parameter SharePoint Update Item Action's Site Address to "作成したサイトのURL".
```

6. SharePoint の Update Item の Site Address が指定したパラメータになっていることを確認します。

![](pasteimage/2023-06-26-02-10-35.png)

7. Copilot 画面で以下のように支持します。

```
Set Parameter SharePoint Update Item Action's List Name to "経費申請".
```

8. Update Item の List Name が "経費申請" となっていることを確認します。

![](pasteimage/2023-06-26-02-13-19.png)
