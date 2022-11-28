<div align="center">
  <br>

  <a href="https://heenamgoong.github.io">
    <img src="https://user-images.githubusercontent.com/104904309/204139400-4a45a3d1-5055-480e-b8d9-65e919780d5f.png" width="600">
  </a>

  <h1>❤HEE-NAMGOONG HOMEPAGE❤︎</h1>

</div>

<p align="center">
소프트웨어학부 20223068 남궁희<br>
유레카프로젝트 개인 Git blog 만들기 프로젝트입니다.
</p>


# Build

1. **Repository 생성**
    - 나의 github page에 적용할 테마를 fork
    - fork 후, <username>.github.io 이름의 Repository 생성
  
  
2. **Local과 원격 연동**

    * clone
    ```bash
    $ git clone <Remote Repository의 주소>
    ```
    * add
    ```bash
    $ git add *
    ```
    * commit
    ```bash
    $ git commit -m "<commit msg>"
    ```
    * branch
    ```bash
    $ git branch -M main
    ```
    * push
      - push를 위한 개인 token 생성 필수!
    ```bash
    $ git push origin main
    ```


3. **Install Ruby**

4. **Install Jekyll**

5. **Jekyll 시작하기**

  ```bash
  $ jekyll new . --force # 현재 디렉토리에 Jekyll 설치
  $ bundle exec jekyll serve #Jekyll 시작
  ```
  * `https://localhost:4000` 접속

6. **Theme 적용**

    * [여기](http://jekyllthemes.org)에서 테마 다운 or 내 레포로 fork하기
    * _posts 디렉토리와 confing.yml파일은 나의 폴더와 파이로 대체
    * markdown 형식으로 post파일 만들기
  
 7. **댓글 기능 추가**
  
    * Disqus 가입 & 세팅 (platform : jekyll 선택)
    * _config.yml 파일 수정
    ```markdown
    comment:
      provider: "disqus"
      disqus:
        shortname: "HeeNamgoong"
    ```
    * disqus 홈페이지에서 Universal Code를 _layouts/post.html 에 적용 (PAGE_URL과 PAGE_IDENTIFIER은 나의 정보에 맞게 수정)
    * 내가 만든 각 post파일들에 아래의 코드 추가
    ```markdown
    comments: true
    ```
  
 8. **Google Analytics**
 
    * heenamgoong.github.io 의 Google Analytics post를 만들어 놨다. 참고하면 된다.
    * google analytics 가입
    * _config.yml 파일에 아래 코드 추가
    ```markdown
    analytics:
    provider               : "google-gtag" 
    google:
      tracking_id          : "G-MN3R6WW2Q3"
    ```
    * includes/head.html 파일에 아래 코드 추가
    ```html
    <!-- Google tag (gtag.js) -->
      <script async src="https://www.googletagmanager.com/gtag/js?id=G-SP2R0K5HJ4"></script>
      <script>
      window.dataLayer = window.dataLayer || [];
      function gtag(){dataLayer.push(arguments);}
      gtag('js', new Date());

      gtag('config', 'G-MN3R6WW2Q3');
      </script>
    ```

9. **favicon**

    * _includes/head.html 파일에 아래 코드 추가
    ```html
     <link rel="icon" type="image/png" href="favicon.ico">
    ```



