<style>
    :root {
        --bg-color-black: #2c2c2c;
        --code-block-pink: #ab5656e6;
        --color-text-white: #fffffff0;
        --color-text-blue: #5288c5; /* 초기화 */
    }
    * {
        color:var(--color-text-white);
    }
    html,#_html {
        background:var(--bg-color-black);
    }
    h1,h2,h3 {
        border-bottom: none !important;
    }
    pre {
        background:var(--code-block-pink) !important;
    }

    pre[class*="language"] {
        background:var(--color-text-white) !important;
    }

    a {
        color: var(--color-text-blue) !important;
    }
    
</style>


# Git 사용법 정리

## Git 명령어
### 1. Git add = 스테이지에 올림, commit = 스테이지에 올린 파일을 완료(?저장)처리, push(원격 저장소(remote)에 파일을 올림), pull(원격 저장소(remote)에서 파일을 받아옴)
* ##### git add [스테이지에 올릴 파일 경로]        
    - ex) git add ./file1.js
* ##### git commit -m "[commit 내용 및 log에 남겨질 내용]"        
    - ex) git commit -m "file1 javascript commit"
* ##### git push -u [연결된 remote의 alise명칭 인듯?][branch 명]        
    - ex) git push -u origin master
* ##### git pull [연결된 remote의 alise명칭 인듯?][branch 명]        
    - ex) git pull origin master

***
## Git 브랜치 전략

### 0. 이유 -> 운영시 문제 될 경우 이전 버전으로 효율적으로 돌리기 위함인듯.

### 1. master(main) branch는 테스트까지 완료한 소스코드만 올려둠.
*   ##### 소스코드를 받으면 무조건 실행되는 branch
*   ##### 완료된 운영소스코드로 버전을 관리하기 위함.

### 2. release branch는 테스트 후 버그만 잡는 branch
*   ##### 개발 완료된 소스코드를 release branch로 이동후 테스트에서 발견된 버그를 잡는다.
*   ##### release branch에서 작업 완료된 소스는 꼭 develop branch 와 master(main)에 merge 해줘야함.
    * 이유는 release에서 작업한 내용들이 develop에 반영이 안되면 추후 다시 개발할때 수정여부를 확인 불가, master에는 운영에 반영하기 위함.

### 3. develop branch는 현재 개발중인 소스를 관리하기 위한 branch
*   ##### 

### 4. Feature branch 개발을 하는데 사용되는 실험실
*   ##### 개발하다 망하면 버려도 되는 branch
*   ##### branch 하나당 기능 하나.
*   ##### develop에서 다 같이 개발하면 꼬일 수 있어서 사용하는 독립된 공간.

### 5. Hotfix branch 급하게 수정되어야하는 branch
*   ##### 안정된 branch에서 따서 급하게 수정해서 올려야 할 branch
*   ##### master(main) -> hotfix로 빠르게 작업후 -> master(main)으로 merge할 branch