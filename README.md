# docker-practice

## このリポジトリは？
docker練習用のリポジトリである。
実際にローカルでdockerを立ち上げてみる。
## 利用手順
1. リポジトリをクローン
    ```shell
   git clone git@github.com:Akitsu-Lab/docker-practice.git
    ```
2. 環境変数を設定
   ```shell
   read PASS
   ```
   ```shell
   export DB_ROOT_PASS=PASS
   ```
   ```shell
   read USER_PASS
   ```
   ```shell
   export DB_USER_PASS=USER_PASS
   ```
3. コンテナの立ち上げ
    ```shell
    docker-compose up -d
    ```
3. コンテナに入る
   - コンテナIDを調べる
    ```shell
    docker ps 
    ```
   - コンテナIDを指定し、コンテナに入る
    ```shell
    docker exec -it コンテナID /bin/bash
    ```
4. mysqlにログイン
   - パスワードはdocker-compose.ymlのMYSQL_ROOT_PASSWORDを使用
    ```shell
    mysql -u root -p
    ```
   - mysqlからログアウト
    ```shell
    exit
    ```
5. コンテナからログアウト
    ```shell
    exit
    ```
6. コンテナのストップ＆停止
    ```shell
    docker-compose down
    ```

### その他のコマンド
- 再起動
    ```shell
    docker-compose restart
    ```
- docker-compose.ymlで管理されているコンテナの一覧を取得
    ```shell
    docker-compose ps
    ```

