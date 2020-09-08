# Side-apollo-server
테스트용 Apollo server 

## GraphQL이란
GraphQL은 페이스북에서 개발한, 데이터베이스 쿼리 언어 중 하나이다. 개인적으로 쿼리문 작성이 직관적인 것이 장점이라고 생각한다. 아래 사이트는 GraphQL 공식 사이트인데 GraphQL 처리 과정이 시각적으로 잘 표현되어 있어서 이해에 도움이 될 것이다.
https://graphql.org/

## 기술 스택
* apollo-server
* graphql
* nodemon
* babel

## Apollo Server 및 GraphQL 설치
> yarn add apollo-server graphql

## 개발 도구 설치 (선택)
> yarn add nodemon @babel/core @babel/node @babel/preset-env --dev

* nodemon
실행 중인 Javascript 파일 변경을 감지하고, 파일이 변경되면 Node를 재실행해 변경 사항이 자동으로 반영되게 도와준다. 많이 쓰는 패키지라서 yarn global add nodemon으로 설치하면 좋다.

* babel
우리가 Javascript 최신 문법을 사용하면 자동으로 각 브라우저가 지원하는 Javascript 버전에 맞게 문법을 바꿔준다.

### .babelrc 파일 생성 (선택)
// .babelrc
{
    "presets" : ["@babel/preset-env"]
}

### package.json 파일 수정
// package.json
{
  ...
  "scripts": {
    "start": "nodemon --exec babel-node src/index.js"
  }
  ...
}