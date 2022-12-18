## 1.js 파일 위치
    **head**
    : head에 넣으면 js 파일이 큰 경우 
    js파일을 다운로드 하기 전에는 html 파일을 확인할 수 없다.

    **body**
    : body 끝에 넣으면 js 파일의 경우
    사용자와 상호작용이 이뤄지는 js코드가 있는 경우 html이 전부
    받아진 다음 실행이 되기 때문에 사용자에게 늦게 제공될 수 있다.
    
    **head asyn 사용**
    : 브라우저가 html을 다운받아 파싱하다가 js파일 불러오는 코드에 asyn를 만나면
    병렬처리하여 html 파싱과 js 파일로드를 같이 진행하다가 js파일이 로드되면
    js 파일을 실행시킨다.
    
    - body 끝에 넣는 것 보다 시간이 단축된다.
    
    - js 파일이 html 파싱이 끝나기 전에 js파일이 다운로드 되면 js파일이 실행되기 때문에
    js파일에서 html 문서에 접근해야 하는 경우 문제가 발생할 수 있다.
    
    - js 파일 여러개가 있는 경우 작성 순서가 아닌 다운로드 된 순서대로 js 파일이 실행된다.
    
    **head에 defer 사용**
    : html 파싱을 먼저 시작하고 js 파일 로드하는 코드를 확인할 경우 병렬로 다운로드를 받고 html 파싱이 끝나게 되면 js파일을 실행시킨다.
    
## 2.변수(const, let, var)
    
    @ const
    - 상수
    
    @ let
    - 변수
    
    @ var변수
    - var변수는 {} 중괄호 안에 선언해도 밖에서 사용이 가능하다.
    ex)
    if(true){
    var a = 10;
    
    }
    console.log(a);
    
    결과: 10
    
    - 만약 var이 아닌 const나 let의 경우는 에러 발생