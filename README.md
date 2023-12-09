# eslint-config-ksw

Javascript 프로젝트에 eslint(air-bnb-base), prettier 설정을 빠르게 적용하기 위한 eslint-config 패키지입니다. <br />
사이드 프로젝트에 활용하기 위해 튜토리얼 용으로 개발했습니다.

### 설치 및 적용

패키지 설치

```
npx install-peerdeps --dev eslint-config-ksw
```

`.eslintrc` 파일 설정

```javascript
module.exports = {
  extends: ["ksw"],
  rules: {},
};
```

`prettier` 규칙을 설정할 경우 전체를 override해야 합니다.

```javascript
module.exports = {
  extends: ["ksw"],
  rules: {
    "prettier/prettier": [
      "error",
      {
        endOfLine: "auto",
        printWidth: 120,
        useTabs: false,
        tabWidth: 2,
        trailingComma: "es5",
        semi: true,
        singleQuote: false,
        bracketSpacing: true,
        arrowParens: "always",
        jsxSingleQuote: false,
        bracketSameLine: false,
        singleAttributePerLine: true,
      },
    ],
  },
};
```