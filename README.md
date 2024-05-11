# NEXTJS-GIHYO-BOOK

## 参考

```
https://github.com/gihyo-book/ts-nextbook-json?tab=readme-ov-file
https://github.com/gihyo-book/ts-nextbook-app/tree/main
```

## 環境構築

### styled-components の設定

CSS-in-JS のライブラリ styled-components を使用。

```
npm install styled-components
npm install --save-dev @types/styled-components
```

### ESLint 導入時のエラー解決について

eslint-config-next が依存している@typescript-eslint/parser のバージョンと競合

1. eslint-config-next をアンインストール

```
   npm uninstall eslint-config-next
```

2. 必要な@typescript-eslint パッケージをインストール

```
   npm install --save-dev @typescript-eslint/parser@7.8.0 @typescript-eslint/eslint-plugin@7.8.0
```

3. eslint-config-next を再インストール

```
   npm install --save-dev eslint-config-next
```

4. ESLintとformatterのPrettier、その他プラグインをインストール

```
npm i --save-dev prettier eslint typescript-eslint @typescript-eslint/eslint-plugin @typescript-eslint/parser eslint-config-prettier eslint-plugin-prettier eslint-plugin-react eslint-plugin-react-hooks eslint-plugin-import
```
