# **1,2주차 회고**

## 1. CLI 주요 명령어

### 1. pwd:

    현재 작업중인 폴더 위치 확인 가능.

### 2. mkdir {디렉토리 이름}

    현재 폴더에 디렉토리 이름 정해서 생성 가능.

### 3. cd {디렉토리 경로}

    디렉토리 경로로 이동 가능.
    (cd ..) : 상위 경로로 한 단계 이동 가능.

### 4. ls {디렉토리 경로}

    디렉토리 경로에 있는 파일 출력 가능.
    (ls -a {디렉토리 경로} ) :
    숨겨진 파일까지 출력 가능.

### 5. touch {파일 이름}

    빈 파일 생성 가능.
    (echo '코드' > 파일 이름) : 코드가 삽입된 파일을 생성 가능.

### 6. cat {파일 이름}

    파일 내용 화면 출력 가능.

### 7. rm {파일 이름}

    파일 삭제 가능.

### 8. rmdir {디렉토리 이름}

    디렉토리 삭제 가능.

---

## 2. Git 주요 명령어

### 1. git status:

    저장소 생성.

### 2. git add:

    파일의 변경 사항을 인덱스(Staging Area)에 추가.

### 3. git commit:

    파일의 변경 사항에 대한 이력 생성.
    git commit --amend:
    마지막 커밋 메시지 수정 가능.

### 4. git rebase -i <hash>:

    특정 커밋 수정.
    reword로 수정 후 커밋 메시지 수정 가능.

### 5. git log --oneline:

    커밋 이력을 한줄 형태로 보기 가능.

### 6. git branch:

    브렌치 생성 및 이동.

### 7. git remote:

    git remote -v:
    리모트 브렌치 조회.

    git remote add origin 주소:
    리모트 브렌치 추가.

    git remote rm origin:
    리모트 브렌치 삭제.

### 8. git push:

    로컬 변경 이력을 원격으로 전송.

### 9. git pull:

    원격 내용을 로컬로 가져올 때 사용.

---

## 3. Node와 NPM (2/11)

### 1. Node.js:

    외부에서 CLI와 서버 측 스크립트를 작성 가능한 JavaScript 런타임 환경.

### 2. NPM:

    자바스크립트 프로그래밍 환경에서 패키지 설치하고 관리하는 도구.

    각자 공유,배포도 가능.

    (1) 전역으로 설치법:

    npm i -g <패키지명>

    (2) 로컬로 설치법:

    npm i <패키지명>

### 3. NPM 설치법:

    (1) package.json:
    Node.js 프로젝트에서 사용되는 메타데이터 파일 --> (장부).

    *npm init -y

    (2) add-gitignore:
    협업 때 불필요한 파일 커밋 및 충돌을 방지하기 위함.

    *npm install --global add-gitignore:
    먼저 add-gitignore 패키지를 설치하고

    *add-gitignore node windows osx visualstudiocode:
    설치한 add-gitignore 패키지를 사용하여 .gitignore를 생성함.

### 4. live-server:

    웹 개발을 할 때 HTML,자바스크립트 파일을 실시간으로 업데이트하면서 볼 수 있도록 도와주는 로컬 개빌 서버.

    *전역 설치가 아닌 로컬로 설치해야 협업에 유리하다.

    *전역 설치하면 프로젝트 별 버전관리와 다른 개발자가 환경 맞추기기 어렵기 때문.

### 5. live-server 사용법:

    (1) learn-node 하위폴더는 src:

    mkdir src
    touch src/index.html

    (2) !하여 html 기본 코드 추가.

    (3) npm i -D live-server:

    learn-node 폴더에 live-server 패키지를 로켤로 설치.

    (4) live-server 실행.

    *npx live-server src --port=8090 --host=localhost --no-browser

    (5) package.json에 다음의 코드를 추가한다.

    *"scripts": {
        "start": "live-server src --port=8080 --host=localhost --no-browser"
      },

    (6) npm start

### 6. Prettier:

    코드 포맷터.

### 7. Prettier 설치,적용법:

    (1) npm i -D prettier

    (2) package.json 파일에 format 명령 등록.

    *"scripts": {
    "format": "prettier --write . --ignore-path .gitignore",
    }

    (3) 별칭으로 등록된 명령 실행:

    *npm run format

---

## 3. HTML (2/12, 2/13)

### 1. HTML 정의:

    웹사이트 콘텐츠를 설명하는데 사용되는 마크업 언어.

### 2. HTML 기본 구조:

    (1) <head>:

    소개 및 탐색, 사람이 읽을 수 없는 문서 정보.

    (2) <body>:

    웹페이지의 본문 영역, 사용자가 브라우저에서 볼 수 있는 컨텐츠가 들어가는 곳.


    (3) <title>:

    브라우저의 제목 표시줄, 탭 문서 정의.

    (4) <meta>:

    charset, name, content 설정.

    (5) <link>:

    현재 문서와 외부 리소스의 관계 명시.

    ex. href = "..css"

    (6) <style>:

    문서나 문서 일부에 대한 스타일 정보 포함.

    (7) <base>:

    문서 안의 모든 상대 URL이 사용할 기준 URL을 지정함.

### 3. HTML 제목과 단락:

    (1) <h1> ~ <h6>:

    h1 요소가 가장 높은 크기 수준, h6가 가장 낮은 크기 수준.

    (2) <p>:
    하나의 문단.

    (3) <ul>:
    졍렬되지 않은 목록.

    (4) <section>:
    독립적인 구획 나타남.

### 4. HTML 이미지와 피규어:

    (1) <img>:

    이미지 삽입.

    *src: 이미지 경로
    *alt: 이미지에 나오는 글자로 설명

    (2) <figure> , <figcaption>:

    figure는 독립적인 컨텐츠 표현하고 figcaption에 설명을 붙일 수 있음.

    *피규어, 설명, 콘텐츠는 하나의 단위로 참조.

    EX.
    <figure>
      <img src="/src/assets/drama/good-partner-narrow.webp" alt="굿파트너" />
      <figcaption>드라마 굿파트너 속 장나라</figcaption>
    </figure>

### 5. HTML 하이퍼링크:

    (1) <a>:

    href 특성을 통해 다른 페이지나 같은 페이지의 URL로 연결할 수 있는 하이퍼링크를 만듦.

    EX.
    <a
      href="https://www.naver.com/"
      title="네이버 사이트로 이동합니다. (새창)"
      target="_blank"
      rel="noopener noreferrer"
    >
      네이버
    </a>

### 6. 그 외 태그 및 속성:

    (1) <hr />:
    수평줄을 표시하는 요소.

    (2) <br />:
    줄바꿈을 삽입하는 태그.

    (3) <svg>:
    확대해도 깨지지 않는 벡터 그래픽을 표현하는 HTML 태그.

    (4) <li>:
    목록 항목을 나타내고 반드시 ul, ol, menu 안에 위치해야 함.

    (5) target: blank, _blank

    *blank: 탭을 띄우고 다른 링크 누를 때, 그 탭에서 바뀜.

    *_blank: 탭을 띄우고 다른 링크 누를 때, 초반 탭 유지되면서 새로운 창이 열림.

    (6) noopner, noreferrer:

    보안과 개인정보 보호를 위해 추가하는 속성

    *noopener:
    새 창으로 열리는 링크가 부모창을 조작하지 못하도록 막음.

    *noreferrer:
    새 창으로 열린 페이지가 원래 페이지의 정보를 받을 수 없도록 함.

### 6. 기본 구조 예시:

    <!doctype html>
    <html lang="ko-KR">
      <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>하이퍼링크</title>
      </head>
      <body>
        <h1>하이퍼링크</h1>
        <h2>이미지 UI 예제(링크)</h2>
        <figure>
          <img src="/src/assets/cafew/card-02-@1x.jpg" alt="" />
          <figcaption>
            <p>RESPONSIVE WEB <br />DESIGN STRATEGIES</p>
            <p>반응형 웹디자인 전략</p>
          </figcaption>
        </figure>
        <a href="/">강의정보</a>

        <h2>텍스트 링크</h2>
        <a href="https://bootcamp.likelion.net/" target="_blank"
          >멋쟁이 사자처럼 부트캠프</a
        >
        <br />
        <a
          href="https://www.naver.com/"
          title="네이버 사이트로 이동합니다. (새창)"
          target="_blank"
          rel="noopener noreferrer"
          >네이버
        </a>

        <br />
        <h2>이미지 링크</h2>
        <a href="https://www.apple.com"
          ><img src="/src/assets/apple/apple_watch.jpeg" alt="애플워치" width="200"
        /></a>
        <h2>PDF 링크</h2>
        <a
          href="/src/assets/pdf/google-seo-guide-ko.pdf"
          download="google-seo-guide-ko.pdf"
          >구글 SEO 가이드</a
        >

        <h2>전화번호 또는 이메일 주소로 하이퍼 링크</h2>
        <a href="mailto:seulbinim@gmail.com?subject=문의사항"
          >seulbinim@gmail.com</a
        >
        <br />
        <a href="tel:+821023456789">고객센터 010-2345-6789</a>
      </body>
    </html>
