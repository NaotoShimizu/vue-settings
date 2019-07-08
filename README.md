# kanban-app
//あくまで参考書を読み、タイピングが面倒くさい所の補助レベルでお使いいただけると！

## アプリケーションのビルドについて
### 初期設定

``` bash
npm install -g @vue/cli
npm vue init webpack kanban-app

cd kanban-app
npm install

//npm installでおそらくエラーがでる
//それぞれエラーが出たパッケージをインストール。npm auditするとエラーのあるパッケージのインストール方法などが表示される
npm audit
npm run dev
```


### 追加機能セットアップ

``` bash
//ディレクトリ作成
touch ./build/dev-server.js

mkdir -p src/store
touch src/store/index.js
touch src/store/mutation-types.js
touch src/store/mutations.js
touch src/store/getters.js
touch src/store/actions.js

mkdir -p src/api
touch src/api/index.js
mkdir -p test/e2e/custom-commands

touch test/e2e/custom-commands/trigger.js
touch test/e2e/custom-commands/enterValue.js

//追加機能インストール
//参考書通り(npm install —-save-dev eslint-plugin-vue@4.7.1)だとエラーが出てしまうため、以下のコマンドに変更※あくまで私の環境
//もしすでにインストールしていたら一度削除する必要。
//その場合、vue uiで管理画面を起動し、GUIから削除がおすすめ
npm install --save-dev eslint-plugin-vue
npm install --save-dev body-parser
npm install --save vuex es6-promise
npm install --save axios
npm install --save-dev @vue/test-utils@1.0.0-beta.24
```
