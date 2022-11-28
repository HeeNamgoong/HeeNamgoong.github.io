---
layout: post
title: File Hashing
subtitle: how to hash file
categories: markdown
tags: [test]
comments: true
---


 


![Untitled](https://user-images.githubusercontent.com/104904309/203974892-9a007496-a69a-46f5-a436-0761b78de87b.png)


사전에 sha256을 사용하기 위해서 

**npm install sha256-file**(sha256 cmd 명령어) 로 설치해줍니다.

```bash
npm install sha256-file
```

---



코드 형태 : sha256File(path, callback)

‘path’에 **파일 경로**를 적어줍니다.

```jsx
var sha256File = require('sha256-file');

sha256File('C:/Users/user/OneDrive/바탕 화면/test1.txt', function (error, sum) {
  if (error) return console.log(error);
  console.log(sum)
})
```

---


![Untitled(2)](https://user-images.githubusercontent.com/104904309/203974888-bf03b96c-1342-47dc-ac54-bbcb0da6cd08.png)

파일 안의 내용을 해싱하는 건지, 파일 자체를 해싱하는 건지를 알기 위해서

다른 파일 이름으로 같은 내용을 해싱한 결과(파일이름 각각 : test1, test2 / 내용 : 해싱 테스트입니다.)

해싱 암호가 같았음

—>**파일 안의 내용**을 해싱하는 것이 맞음.

js에서도 마찬가지입니다.

