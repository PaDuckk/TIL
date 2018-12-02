### Chapter 3
## Functions


#### Defining a Function

함수 정의는 기본적인 바인딩으로 할 수있다.

함수는 여러개의 파라미터를 가질수도 있지만 안 가질수도 있고

single statmente더 라도 {}로 감싸주어야 한다.

return으로 value를 만들어 낼 수도 있고 없을수도 있다.

#### Bindings and Scopes

각각의 binding들은 범위를 가진다.

바인딩이 어떠한 펑션이나 블록 밖에서 정의된다면 범위는 프로그램의 전체이다. ==> global이라 함

그러나 함수의 파라미터이거나 함수 내부에서 정의된 binding은 로컬 binding이라 한다. 

로컬 binding은 각 함수내부에만 존재하므로 함수간의 분리를 이루고
이는 global environment와 무관하게 해당 함수의 내부를 이해하는 데 수월하게 해준다.

(const와 let은 블록 scope를 가지고 var는 function scope를 가진다.

따라서 const와 let과 다르게 var는 if문 이나 function이 아닌 블록에서 선언되어지면 바깥에서도 사용되어질 수 있다.

또한 Hoisting으로 인해  function 내부에서 하단에 var로 선언되어 졌다하더라도 상단으로 끌어올려져 먼저 undefined로 선언되어지고 
할당되는 줄에서 할당되어진다. 해당 혼란을 피하기위해 함수내에서 var를 선언할 경우 상단에서 전부 선언해주는게 좋은 Coding Convention이 될 수 있다.)

#### Nested Scope

펑션은 스코프를 가지고 펑션 내부의 펑션도 스코프를 가진다.

내부의 펑션 자신을 포함하고 있는 외부 스코프에 접근 할 수 있다! 이것을 lexical scope라 한다.

반대는 불가능 ...

#### Optional argument

JS에선 function argument를 임의로 추가 할 수도 있다.

단점은 실수로 argument의 수를 잘 못 입력하면 알 수가 없지만

장점은 입력되어지는 argument의 수에 따라 function을 제어 할 수 있다.

그리고 함수선언시 argument뒤에 ' = 값' 으로 입력되지 않았을 때 기본 값을 미리 지정 해둘 수 있다.

#### Closure

클로저는 


