### Chapter 2
## Program Structure

#### Bindings

값을 단순히 선언만 해준다면 사라질 것이다.

JS는 값을 유지하기위해 Binding 또는 변수를 제공해준다.

let과 const 그리고 var가 있다.

정확한 차이는 뒤 챕터에서 다룬다.
const는 constant의 약자로 한 번 할당해주면 재할당을 할 수 없다.

#### Binding Names

이름을 짓는 규칙에 숫자가 포함될 수있다.
하지만 맨 앞자리에는 올 수 없다.

그리고 특수기호는 $와 _는 사용할 수 있으나 다른 문자는 사용할 수없다.

그리고 let과 같은 특수한 의미를 가진 단어도 사용 불가.

break case catch class const continue debugger default
delete do else enum export extends false finally for
function if implements import interface in instanceof let
new package private protected public return static super
switch this throw true try typeof var void while with yield

해당 문자는 Binding Name으로 사용 불가 

#### The Environment

Binding의 모음과 그들의 값이 존재하는 타이밍을 environment라 부른다.(?)

프로그램이 실행될때 environment는 empty가 아니다. 항상 언어의 standard부분과 주변 시스템과 상호작용하기 위한 기능을 제공한다.

예를 들어 브라우저에선 웹사이트가 로드될때 마우스와 키보드인풋을 입력받기 위한 function들이 주어진다.

(정확한 의미는 이해하지 못했으나. JS가 코드가 돌아가는 환경에서 주어진 기능,binding 들에 대해서 이야기 하는것 같다. 브라우저에선 window 객체나 Document객체가 주어진다거나. console.log 등등.. )

#### Functions

기본적인 Environment에서 많은 function들을 제공한다.

함수는 일부 프로그램조각을 value로 감싼 것이다.

var a = function(){
    ...
    ...      // a piece of program
    ...
}

일부 프로그램의 조각을 a라는 변수에 함수로 할당함

함수를 실행하는걸 invoking, calling applying it 이라고 한다.


### Excersizes

#### Looping a triangle

```javascript
for(let i=0;i<7;i++){
	let tempStr = '';
	for(let j=0;j<i+1;j++){
    	tempStr += '#';
	}
	console.log(tempStr);
}
```

#### Fizzbuzz

```javascript
let i=1;

while(i<101){
	if(i%3===0 && i%5===0){
    	console.log("FizzBuzz");
	}else if(i%3===0){
		console.log("Fizz");
    }else if(i%5===0){
		console.log("Buzz");
	}
	i++;
}
```

#### chessBoard

```javascript
let makeChessBoard = function(size){
    let tempRow = '';
    for(let i=1;i<size*size;i++){
        
        //size가 짝수일 때 짝수 행에서 나오는 #이 먼저 나와야 함
        if(size%2===1){
            if(i%2===1){
                tempRow+=' ';
            }else{
                tempRow+='#';
            }  
        }else{
            if(i%2===1&&(i/size)%2===0){
                tempRow+=' ';
            }else{
                tempRow+='#';
            }
        }
        
        if(i%size===0){
                tempRow += '\n';
        }
        
    }
    console.log(tempRow);
}
```