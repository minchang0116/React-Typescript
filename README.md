# React & Typescript

## Slack Clone 코딩
- DM기능 (일대일 채팅 기능)
- 퍼블릭 채널 (단체 채팅방)
- 최적화와 배포

## 환경설정
### backend
1. npm install
2. .env 파일 만들고 COOKIE_SECRET=[아무값] MYSQL_PASSWORD=[db패스워드] 입력
3. config/config.json 설정
4. npx sequelize db:create (스키마 생성)
5. npm run dev
6. npx sequelize db:seed:all (테이블 생성)
7. npm run dev

### frontend

<img src="https://img.shields.io/badge/React-3766AB?style=flat-square&logo=React&logoColor=white"/></a>
<img src="https://img.shields.io/badge/Typescript-3766AB?style=flat-square&logo=Typescript&logoColor=white"/></a>
<img src="https://img.shields.io/badge/Babel-3766AB?style=flat-square&logo=Babel&logoColor=white"/></a>
<img src="https://img.shields.io/badge/Emotion JS-3766AB?style=flat-square&logo=EmotionJS&logoColor=white"/></a>

코드 퀄리티 툴 : <img src="https://img.shields.io/badge/ESLint-3766AB?style=flat-square&logo=ESLint&logoColor=white"/></a>
<img src="https://img.shields.io/badge/Prettier-3766AB?style=flat-square&logo=Prettier&logoColor=white"/></a>

1. npm init ( Node 프로젝트를 실행하기 전에는 항상 실행해야함 -> react, typescript 모두 Node 프로젝트)
package.json : 프로젝트가 어떻게 구성되어있는지 설명해주는 파일
2. npm i react react-dom
웹에서 사용할 때 react-dom
실무에서는 npm 개인공부에서는 직접구현
3. npm i typescript
4. npm i @types/react @types/react-dom
CRA는 Webpack, Babel, CSS, Typescript를 바로 세팅해줘서 편함
5. npm i -D eslint prettier eslint-config-prettier eslint-plugin-prettier
-D는 개발 할 때만 쓰이는 패키지들
npm i 할때 node_modules가 생각보다 많은 이유 : npm i react를 하면 react의 dependencies, getDependencies도 설치되기 때문
6. .eslintrc 와 .prettierrc 파일을 만듦

.eslintrc
```
{
    "extends": ["plugin:prettier/recommended"]
}
```
.prettierrc
```
{
    "printWidth": 120,      // 한 줄당 120글자를 맥스로
    "tabWidth": 2,          // 들여쓰기 2칸
    "singleQuote": true,    // 작은 따옴표로
    "trailingComma": "all", // 마지막에 콤마 붙일건지
    "semi": true            // 세미콜론
}
```
eslint를 사용하지만 대부분의 권한을 prettier로 넘김

7. tsconfig.json 파일을 만듦
```
{
    "compilerOptions": {
        "esModuleInterop": true,                
        "sourceMap": true,
        "lib": ["ES2020", "DOM"],
        "jsx": "react",
        "module": "esnext",
        "moduleResolution": "Node",
        "target": "es5",
        "strict": true,
        "resolveJsonModule": true,
        "baseUrl": ".",
        "paths": {
            "@hooks/*": ["hooks/*"],
            "@components/*": ["componets/*"],
            "@layouts/*": ["layouts/*"],
            "@pages/*": ["pages/*"],
            "@utils/*": ["utils/*"],
            "@typings/*": ["typings/*"]
        }
    }
}
```
타입스크립트는 컴파일러가 필요함 ( 컴파일러 통해서 타입스크립트에서 자바스크립트로 변환되는 언어 )
자바스크립트는 보통 인터프리터 언어라고 해서 컴파일러 설정을 따로 하지 않아도 됨

8. 
