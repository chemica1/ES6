이터러블(iterable)은 **개별값을 순회 가능한 객체**다. 배열이 대표적인 이터러블 객체임.

spread operator는 함수 인자나 원소(배열 리터럴)가 여럿 나오는 곳이면 어디에도 쓸 수 있음

es5이전에는 배열값을 함수 인자로 넘기려면 함수의 apply()내장 메소드를 이용했었음

es6부턴 이렇게 한다.

```
function myFunction(a, b)
{
return a + b;
}

let data = [1, 4];
let result = myFunction(...data);
console.log(result); //5
```

참고 : spread operator는 apply()메소드를 호출하지 않고 ...data -> 1, 4 이렇게 바로 바꿈

이떄 이 연산자는 이터러블 객체를 함수 인자로 펼치는 역할뿐만아니라 원소가 많이 나오는 곳이면 어디라도 활용가능하다.

```
let array = [1, ...number, 5, 6, 7];
...[3, 4] -> 3, 4
let array =[1] -> ...array -> 1
```