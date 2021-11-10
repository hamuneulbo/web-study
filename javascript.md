JavaScript 공부 요약본 - 김하늘 
====
1-01 Hello JavaScript
----

1. 콘솔에 특정 내용 출력
	console.log('Hello JavaScript!');
    console.log(1+2+3+4);
    
2. 선언
특정 이름에 특정 값을 선언 
* 변수 : 한번 선언 후 바꿀 수 있다 ; let 키워드 사용 
한번 선언 이후 똑같은 이름 선언 불가
	let value = 1;
    console.log(value);
    value = 2;
    console.log(value);
* 상수 : 한번 선언하고 값이 바뀌지 않는 값 ; const 키워드 사용 
한번 선언 이후 똑같은 이름 선언 불가
	const a = 1;
    a = 2; // 불가능 
    
1-02 변수
-----

1. 문자열
	let text = 'hello';
2. 참/거짓(Boolean)
	let good = true;
    let loading = false;
    
3. null과 undefined
	const frined = null;
    
    let criminal;
    console.log(criminal); // undefined
    

1-03 연산자
----

* '=' ; 대입연산자
* + - * / ; 산술연산자 
* ! && || ; 논리연산자
	const a = !true;
    console.log(a);
not -> and -> or 순서
* '===' ; 비교 연산자
* '==' ; type 비교 x, false=0, null=undefined
* '!==' '!='

문자열 붙이기 '+'

1-04 조건문
----
1. if문
	const b = 1;
    if(true){
     const b = 2;
     console.log('if문 안의 b 값은' + b);
    }
    console.log('if문 밖의 b 값은' + b);

2. switch / case문
	const device = 'iphone';
    
    switch (device) {
       case 'iphone' :
       console.log('아이폰!');
       break;
       case 'ipad' :
       console.log('아이패드!');
       break;
       default:
       console.log('모르겠네요..');
    }

1-05 함수
----
1. function 키워드 사용 
	   function add(a, b){
       return a+b;
    	}
    	const sum = add(1,2);
    	console.log(sum);
    
    	function hello(name){
    	console.log('Hello, '+name+'!');
    	}
    	hello('korea');

2. 템플릿 리터럴 통한 문자열 합하기
	function hello2(name){
    console.log(`Hello, ${name}!`);
    }
    hello('KOREA');

3. 화살표 함수
	const add = (a, b) => {
    return a+b;
    }
    console.log(add(1,2));
    
    const add = (a, b) => a+b;
    console.log(add(1,2));
    
    
1-06 객체
----
변수 혹은 상수를 사용하게 될 때, 하나의 이름에 여러 종류의 값을 넣을 수 있도록 한다.
const dog = {
name: '멍멍이',
age: 2
 };

 console.log(dog.name);
 console.log(dog.age);

키: 원하는 값
이때 키는 공백이 없어야 한다. 공백을 넣고 싶으면 따옴표로 감싸 문자열로 넣는다.
*객체 비구조화 할당 const {   ,   ,   } = hero;
*객체 안에 함수 넣기  this는 자신이 속해있는 객체 가르킴

const doginfo = {
  name: '몽룡',
  sound: '멍멍',
  say: function say(){
    console.log(this.sound);
  }
}
doginfo.say();
* getter와 setter 
   getter는 조회할 때 마다 연산 
   setter는 값이 바뀔때마다 연산
   
1-07 배열
----
const array = [1,2,3,4,5];
objects[n]; n=0, 1, ...
objects.push
objects.length

1-08 반복문
----
length를 이용해 배열 안 원소 나열 가능 
for...of

Object.entries: [[키, 값], [키, 값]] 형태의 배열로 변환
Object.keys: [키, 키, 키] 형태의 배열로 변환
Object.values: [값, 값, 값] 형태의 배열로 변환

for...in
	for(let key in doggy){}

continue - 다음 루프 돌게함

1-10
----
객체 생성자는 함수를 통해서 새로운 객체를 만들고 그 안에 넣고 싶은 값 혹은 함수들을 구현 할 수 있게 해줍니다.
객체 생성자를 사용 할 때는 보통 함수의 이름을 대문자로 시작하고, 새로운 객체를 만들 때에는 new 키워드를 앞에 붙여주어야 합니다.

프로토타입
프로토타입은 다음과 같이 객체 생성자 함수 아래에 .prototype.[원하는키] = 코드를 입력하여 설정 할 수 있습니다.

객체 생성자 상속받기
새로 만든 Dog 와 Cat 함수에서 Animal.call 을 호출해주고 있는데요, 여기서 첫번째 인자에는 this 를 넣어주어야 하고, 그 이후에는 Animal 객체 생성자 함수에서 필요로 하는 파라미터를 넣어주어야 합니다.

추가적으로 prototype 을 공유해야 하기 때문에 상속받은 객체 생성자 함수를 만들고 나서 prototype 값을 Animal.prototype 으로 설정해주었습니다.

클래스

여기서 우리가 say 라는 함수를 클래스 내부에 선언하였는데요, 클래스 내부의 함수를 '메서드'라고 부릅니다. 이렇게 메서드를 만들면 자동으로 prototype 으로 등록이 됩니다.

상속을 할 때는 extends 키워드를 사용하며, constructor에서 사용하는 super() 함수가 상속받은 클래스의 생성자를 가르킵니다.





















































