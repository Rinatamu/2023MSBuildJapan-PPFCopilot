# Power Apps Copilot で 日報アプリ

## 1. 日報アプリの作成

### 1-1. アプリ作成依頼

1. Power Apps を開き、Home画面の Copilot 入力画面を表示します。

![](pasteimage/2023-06-25-20-22-15.png)

2. 入力画面に以下を入力して、送信ボタンを押してみます。

```
Generate Daily Work Report App.
```

![](pasteimage/2023-06-25-20-32-46.png)

3. しばらくすると、テーブル画面が表示され、右側に Copilot の画面が表示されます。

![](pasteimage/2023-06-25-20-33-40.png)

### 1-2. テーブルの修正

このままでもいいのですが、いくつかの変更を Copilot に依頼してみます。

#### 1-2-1. 列の追加

1. Copilot のプロンプトにて、以下を入力します。

```
add column approver format user.
```

![](pasteimage/2023-06-25-20-37-41.png)

2. Approver 列が追加されます。

![](pasteimage/2023-06-25-20-38-40.png)

#### 1-2-2. 選択肢列の選択肢追加

1. Copilot のプロンプトにて、以下を入力します。

```
add status column choice item "pending manager approve".
```

![](pasteimage/2023-06-25-20-42-07.png)

2. Status 列に、"Pending Manager Approve" という選択肢が追加されます。

![](pasteimage/2023-06-25-20-43-29.png)

#### 1-2-3. テーブル名の変更

1. Copilot のプロンプトにて、以下を入力します。

```
Change Table name "Daily Work Report Table".
```

![](pasteimage/2023-06-25-20-44-32.png)

2. テーブル名が Daily Work Report Table に変わることを確認します。

![](pasteimage/2023-06-25-20-45-11.png)

### 1-3. アプリ作成

1. テーブルの修正が終わったら、 Create app をクリックします。

![](pasteimage/2023-06-25-20-46-34.png)

2. アプリが生成されます。

![](pasteimage/2023-06-25-20-48-24.png)

## 2. Copilot コンポーネント

### 2-1. Copilot コンポーネント有効化

1. 「設定」をクリックします。

![](pasteimage/2023-06-25-22-54-08.png)

2. 「近日公開の機能」をクリックします。

![](pasteimage/2023-06-25-22-54-47.png)

3. Copilot コンポーネントをオンに変更します

![](pasteimage/2023-06-25-23-01-10.png)

注意！（2023/6/25現在）<br>
以降は、Copilot コンポーネントを設置するまで、ブラウザやタブを閉じたり、アプリ編集を終了させないでください。<br>
一度編集画面から戻ってしまうと、Copilotコンポーネントを２度と追加できなくなります。

4. 挿入の入力に「Copilot」が追加されることを確認します。

![](pasteimage/2023-06-25-23-08-26.png)

### 2-2. Copilot コンポーネントの設置

1. ツリービューの BodyContainer1 をクリックします。

![](pasteimage/2023-06-25-23-10-21.png)

2. レイアウトから、垂直コンテナーをクリックし、名前を以下のように変更します。

```
CopilotContainer
```

3. CopilotContainer が選択されていることを確認し、挿入から、Copilotをクリックします。

![](pasteimage/2023-06-25-23-12-23.png)

4. Copilot が挿入されましたので、幅を250、高さを650に変更します。

![](pasteimage/2023-06-25-23-14-01.png)

5. データソースを、Daily Work Report Tables に変更します。

![](pasteimage/2023-06-25-23-14-46.png)

6. 作成したアプリに、データソースを元に回答してくれる Copilot が搭載されました。

![](pasteimage/2023-06-25-23-15-41.png)

7. 保存します。

![](pasteimage/2023-06-25-23-16-05.png)
