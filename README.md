# customer-contact

問い合わせ対応自動化AIエージェント

## 概要
顧客からの問い合わせに対して、AIエージェントが自動で回答を生成するアプリケーションです。

## 必要な環境変数

以下の環境変数を設定する必要があります：

- `OPENAI_API_KEY`: OpenAIのAPIキー
- `SERPAPI_API_KEY`: SerpAPIのAPIキー（Web検索用）
- `SLACK_USER_TOKEN`: Slack連携用のユーザートークン

## Streamlit Cloudでのデプロイ方法

1. Streamlit Cloudで「Manage app」をクリック
2. 「Settings」→「Secrets」に移動
3. 以下の形式で環境変数を設定：

```toml
OPENAI_API_KEY = "your-openai-api-key-here"
SERPAPI_API_KEY = "your-serpapi-api-key-here"
SLACK_USER_TOKEN = "your-slack-token-here"
```

4. 「Save」をクリックしてアプリを再起動

## ローカル環境での実行方法

1. リポジトリをクローン
2. 仮想環境を作成して有効化
3. 依存パッケージをインストール：
   ```
   pip install -r requirements.txt
   ```
4. `.env`ファイルを作成して環境変数を設定
5. アプリを起動：
   ```
   streamlit run main.py
   ```

## 機能

- RAGベースの質問応答
- AIエージェントによる自動ツール選択
- 従業員情報検索
- 問い合わせ履歴検索
- Web検索
- 数学計算
- 現在日時取得
- Slack連携
