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


# H tag 사용법
# # H1
## ## H2
### ### H3
#### #### H4
##### ##### H5
###### ###### H6


>## 라인 인덴트(BlockQuote)
> (>) 단독 사용할때 마다 인덴트 라인을 넣어줌.
> 1개
> > 2개
> > > 3개
>
>
>## 리스트 사용법
>### 1. ul
>* ( *,+,- 내용 ) 사용시 ul의 효과
>   * tab * 사용시 모양이 변함
>       * tab tab * 사용시 리스트 모양이 변함(여기까지)
>               다음라인에서 tab tab 후 글자를 입력하면 블록이 생김.
>
>### 2. ol
>1. ( 1. 내용, 2.내용 ) 사용시 ol의 효과
>       1. tab tab * 사용시 모양이 변함
>           1. tab tab tab * 사용시 리스트 모양이 변함(여기까지)
>                   2. tab(*5번)` 글자를 입력하면 블록이 생김.
>
>### 3. 텍스트 블록(코드블럭) 사용법
>1. 
>
    Enter tab 후 내용( * 인덴트{BlockQuote} 사용불가 )
    다음줄 같은 tab의 위치
tab없이 내용 삽입 = 블록 종료
>
>2. 
><pre><code> pre>code tag 사용시 코드블럭 사용 </code></pre>
>
>3. 
>```
>` => 그레이브(GRAVE), backquote
>``` 태그 대용으로 열고 닫기 사용시 코드블럭 사용 ```
>```
>
>4. 문법강조(Syntax highlighting)가 가능.
>```
        ```[언어]
        [코드 내용]
        ```
>```
#### 예제
>```java
>** java 언어로 설정 **
>public class BootSpringBootApplication {
>  public static void main(String[] args) {
>    System.out.println("Hello, Honeymon");
>  }
>}
>```
>
>```javascript
>** javascript 언어로 설정 **
>function BootSpringBootApplication() {
>   console.log("Hello, World");
>}
>```
>
>### 4. 라인 생성
> *, - 을 3번이상 연속적으로 사용하면 라인이 생성된다.
***
>
>### 5. 링크
> * 사용문법   : `[Text](link)`   
> * 사용법예제 : `[구글(링크의텍스트)](https://google.com)`   
> * 예제적용   :  [구글(링크의텍스트)](https://google.com)
> * 참조사이트 : [MarkDown 사용법](https://gist.github.com/ihoneymon/652be052a0727ad59601)
>
>### 6. 강조
> * *, _ , ~ 를 사용해서 문자를 강조함.
> * 강조문자 앞,뒤에 붙여줌.
> * 중간에 강조문자가 위치시 앞,뒤 문자에 공백이 있어야함.
> * 예제
>   * 1개 = italic체, 2개 = bold, 3개 = italic체 + bold
>   * 1개 = 문자1 *강조문자* 문자2
>   * 2개 = 문자1 **강조문자** 문자2
>   * 3개 = 문자1 ***강조문자*** 문자2
>   * 2개 = 문자1 ~~강조문자~~ 문자2
>
>### 7. 이미지 첨부
>* ```
 ![image 없을 경우 텍스트명](image 경로) -> !표가 없을 경우 link로 변경됨.
>```
>![image 없음](./image.jpg)
>
>* 마크다운에서 html tag 사용가능.
>* 이미지 태그를 사용해서 img의 사이즈를 조절한다.
```
사용법 예제
<img src="./image.jpg" width="450px" height="300px" title="px(픽셀) 크기 설정" alt="RubberDuck"></img>
```
><img src="./image.jpg" width="450px" height="300px" title="px(픽셀) 크기 설정" alt="RubberDuck"></img><br/>
>
>### 8. 줄바꿈
>* 입력 문자의 마지막에 공백3개 이상입력(스페이스)
>```
    * (줄바꿈X) 입력글자의 마지막 문장에 공백 3개 이상 추가해야 줄바꿈이 됨. (여기서 공백 3개 입력시 줄바꿈이 되지않는다.)   줄바꿈 후 문자입력
    * (줄바꿈O) 입력글자의 마지막 문장에 공백 3개 이상 추가해야 줄바꿈이 됨. (여기서 공백 3개 입력시 줄바꿈이 되지않는다.)   
      줄바꿈 후 문자입력 처럼 Enter로 라인 변경전에 공백 3칸 이상 입력.
>```
>* 예제
>   * 입력글자의 마지막 문장에 공백 3개 이상 추가해야 줄바꿈이 됨. (여기서 공백 3개 입력시 줄바꿈이 되지않는다.)   줄바꿈 후 문자입력
>   * 입력글자의 마지막 문장에 공백 3개 이상 추가해야 줄바꿈이 됨. (여기서 공백 3개 입력시 줄바꿈이 되지않는다.)   
>      줄바꿈 후 문자입력 처럼 Enter로 라인 변경전에 공백 3칸 이상 입력.
>
>### 9.마지막
>*  html tag를 삽입 할 수 있기 때문에 스타일도 꾸밀 수 있다.
>   * 해당문서를 스타일링 함.



