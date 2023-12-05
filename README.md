# ChatGPTクローンの作成方法（Streamlit版）

実際に動くものは以下のリンクがあります。

- https://doc-chat-llm.streamlit.app/~/+/?embed=true#chatgpt-like-clone
    - Streamlitが公開しているもの。
    - 10回のやり取りに制限されている。
- 

このREADMEは、Streamlitを使用してChatGPTのクローンを作る方法を説明します。以下のステップに従ってください。
基本的に最終的な成果物は
[Build a basic LLM chat app](docs.streamlit.io/knowledge-base/tutorials/build-conversational-apps#build-a-chatgpt-like-app)
ですが、GitHubなどの扱いが難しいと理解し難かったり、
インデントがわかりづらかったりするので補足してあります。


## 1. プロジェクトのクローン

まず、プロジェクトをあなたのマシンにクローンします。

```bash
git clone git@github.com:kishiyamat/chatgpt-like-clone-clone.git
cd chatgpt-like-clone-clone/
```

## 2. 仮想環境の設定

次に、Pythonの仮想環境を作成してアクティベートします。

```bash
python -V  # Python 3.9.10がインストールされていることを確認
python -m venv venv
activate venv/bin/python3.9
```

## 3. 必要なライブラリのインストール

プロジェクトで必要なライブラリをインストールします。

```bash
pip install -r requirements.txt
```

## 4. OpenAI APIキーの設定

OpenAIのAPIキーを取得し、プロジェクトに設定します。これは、アプリケーションがOpenAIのサービスにアクセスするために必要です。

```bash
mkdir .streamlit
touch .streamlit/secret.toml
echo 'OPENAI_API_KEY = "sk-HERECOMESYOUROPENAITOKEN"' > .streamlit/secret.toml
# 注意: OPENAI_API_KEYの名前を変更しないでください（例: OPENAI_KEYやOPENAIAPIKEYは使用不可）
```

## 5. アプリケーションの起動

最後に、Streamlitアプリケーションを起動します。

```bash
streamlit run app.py
```

アプリケーションが起動したら、以下のURLでアクセスできます：

- ローカルURL: [http://localhost:8501](http://localhost:8501)
- ネットワークURL: [http://192.168.3.3:8501](http://192.168.3.3:8501)

これで、Streamlitを使ってChatGPTのクローンがローカル環境で動作するようになります。

