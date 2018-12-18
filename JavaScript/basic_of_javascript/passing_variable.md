# Passing variables

- JS 변수에는 두가지 타입이 존재
    1. primitive type
    2. reference type, compound type

- primitive type

        var a = 1;

    말 그대로 문자나 숫자 리터럴을 저장하는 경우 해당 값 그 자체를 저장함

- reference type

        var a = [1,2,3];

    배열이나 객체를 생성해 변수에 binding 할 경우 배열이 있는 메모리의 주소를 a의 변수에 binding 되어진다!

    var a = 1;
    
    function hello (arg){
    	arg++
    }
    
    hello(a);
    console.log(a) // 그대로 1이 나옴

    var a = [1,2,3];
    
    function hello (arg){
    	arg[0]++
    }
    
    hello(a);
    console.log(a) // 2가 나온다

위와 같은 결과가 나오는 이유는 배열이나 객체 primitive type이 아닌 value를 인자로 넘겨줄 경우 해당 인자가 위치한 주소값을 넘겨주기 때문이다!

그렇다면 아래는 어떠한 결과가 나올까

    var a = [1,2,3];
    
    function hello (arg){
    	arg = [4,5,6];
    }
    
    hello(a);
    console.log(a) // [1,2,3]이 나온다

주소값을 passing variable로 넘겼음에도 a의 value가 바뀌지 않은 이유는 함수내에서 새로운 객체의 주소값을 할당해 주었기 때문에 variable로 넘겨진 주소값의 [1,2,3]은 변경 되지 않는 것이다.