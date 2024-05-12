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

4. ESLint と formatter の Prettier、その他プラグインをインストール

```
npm i --save-dev prettier eslint typescript-eslint @typescript-eslint/eslint-plugin @typescript-eslint/parser eslint-config-prettier eslint-plugin-prettier eslint-plugin-react eslint-plugin-react-hooks eslint-plugin-import
```

### storybook 設定時のエラー解決について

```


```

- storybook を削除する場合

1. package.json を編集

```
"scripts": {
  "dev": "next dev",
  "build": "next build",
  "start": "next start",
  "lint": "next lint --dir src",
  "format": "next lint --fix --dir src"
},
"devDependencies": {
  "@babel/core": "^7.24.5",
  "@types/node": "^20",
  "@types/react": "17.0.2",
  "@types/react-dom": "17.0.2",
  "@types/styled-components": "^5.1.34",
  "@typescript-eslint/eslint-plugin": "^5.62.0",
  "@typescript-eslint/parser": "^5.62.0",
  "babel-loader": "^8.3.0",
  "eslint": "^8.20.0",
  "eslint-config-next": "12.3.4",
  "eslint-config-prettier": "^8.1.0",
  "eslint-plugin-import": "^2.26.0",
  "eslint-plugin-prettier": "^4.0.0",
  "eslint-plugin-react": "^7.30.0",
  "eslint-plugin-react-hooks": "^4.4.0",
  "prettier": "^2.7.1",
  "typescript": "^4.5.4"
}
2. 依存関係の再インストール
```

rm -rf node_modules
rm package-lock.json
npm cache clean --force
npm install

```

```
