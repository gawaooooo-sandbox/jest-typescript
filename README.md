# jest-typescript

TypeScript + jest sample

## 参考

- https://jestjs.io/docs/ja/getting-started
- https://typescript-jp.gitbook.io/deep-dive/intro-1/jest
- https://github.com/kulshekhar/ts-jest
- https://kulshekhar.github.io/ts-jest/
- https://qiita.com/mangano-ito/items/99dedf88d972e7e631b7
- https://webbibouroku.com/Blog/Article/typescript-jest

## TypeScript + jest 環境構築

### 必要 package install & config ファイル作成

```bash
# install packages
$ npm i -D typescript jest ts-jest @types/jest
# jest.config.js file作成
$ npx ts-jest config:init

# tsconfig.json file作成
$ npx tsc --init
message TS6071: Successfully created a tsconfig.json file.
```

### tsconfig.json 修正

- `lib`, `outDir` の変更
- `include` 追加

### package.json npm scripts 追加

- `test` , `build` を追加

### サンプルファイル追加

- `src`以下に追加
- `test`以下に `xxx.spec.ts` テストファイルを追加

### test 実行

```bash
❯ npm t

> jest-typescript@1.0.0 test
> jest

 PASS  test/sum.spec.ts
  ✓ adds 1 + 2 to equal 3
  sum() のテスト
    ✓ sum(1, 2) == 3 (1 ms)

Test Suites: 1 passed, 1 total
Tests:       2 passed, 2 total
Snapshots:   0 total
Time:        0.306 s, estimated 1 s
Ran all test suites.
```
