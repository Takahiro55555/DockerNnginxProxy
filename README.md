# Docker Nginx Proxy

## これは何？
Dockerを使用してウェブシステムなどを公開するためのファイルを置いています。

## 使い方

### 1. サーバーへ接続する
この後、サーバー上のportainerにログインするためにローカルのブラウザからサーバの`9000`ポートにアクセスする必要があります。

そのために、sshポートフォワーディングを使用します。

（ローカルから直接サーバーの9000番ポートにアクセスできないという想定）

```
ssh [HOST] -L 9000:localhost:9000
```

### 2. git clone

```
git clone https://github.com/Takahiro55555/DockerNnginxProxy.git
```

### 3. docker network を作成

```
docker network create nginx-proxy
```

### 4. 起動

```
docker-compose up -d
```

### 5. portainer にアクセスする

[http://localhost:9000](http://localhost:9000)にアクセスして、ユーザ登録を済ませれば初期設定魔完了です。
