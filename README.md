1. Hvað er null og undefined?

  Null er þegar það er enginn value eða ekki til , Null er líka Object
  Undefined er þegar Varible er hlutur en Varible á eftir að fá skilgriening.

2. Hvað gerir 'use strict' í JavaScript kóða?

  Use Strict er merkið ";" það gerir það að verkum að kóðinn verður hraðari.

3. Hver er munurinn á let og var?

  Let festi það í Scope á sérstökum stöðum
  Var gerir það sem global object skiptir engu máli hvar þar er

4. Skilgreindu fall á þrjá mismunandi vegu með kóðasýnidæmi.
```javascript

Anonymous function definition:
var anon = function() {
  alert('I am anonymous');
}
anon();

Normal function:
function hello() {
  alert('Hello world');
}
hello();
```

5. Útskýrðu hvað eftirfarandi kóði gerir, hvað gera svigarnir?
```javascript

 (function() { alert('Hello World'); })();

 ```

 það er að búa til fall á staðnum sem gerir alert sem stendur "hello world" í. og svo er síðasti sviginn að kalla á þaða fall strax

6. Í hvaða röð er kóðinn keyrður í raun eftir að JS þýðandinn (e. interpreter) er búinn að fá
hann til sín? Raðaðu kóðanum rétt fyrir JS þýðandanum. Afhverju er útkoman 8? Útskýrðu.

Kóðinn verður raðaður eftir svona fyrir neðan. þar sem allt var undir skrítna sviginn þá gildir neðsta function bar() , Þetta er kallað Hoisting
```javascript

  function foo(){
  function bar() { return 3; }
  function bar() { return 8; }
  return bar();
  }
  alert(foo());
```

7. Hver er munurinn á for, for-in og for-of lykkjum?
```javascript

  For lykkjan
    for (i = 0; i < 10; i++) {
    // do something
    }

  For..In lykkjan
    Array.prototype.newArr = () => {};
    Array.prototype.anotherNewArr = () => {};
    const array = ['foo', 'bar', 'baz'];

    for (const value in array) {
      console.log(value);
    }
    // 0
    // 1
    // 2

  For..of lykkjan
    Array.prototype.newArr = () => {};
    const array = ['foo', 'bar', 'baz'];

    for (const value of array) {
      console.log(value);
    }
    // foo
    // bar
    // baz
```
  Stærsti munurinn af For..In og For..of lykkjuna er það að for of gefur okkur strenginn en for in gefur okkur bara númerin hvar hlutirnir eru í röðinni.

8. forEach() Leystu lið 20 í Arrays á Udacity https://classroom.udacity.com/courses/ud803
```javascript

var test = [12, 929, 11, 3, 199, 1000, 7, 1, 24, 37, 4,
  19, 300, 3775, 299, 36, 209, 148, 169, 299,
  6, 109, 20, 58, 139, 59, 3, 1, 139];

// Write your code here
test.forEach(function(num , index){
if (num % 3 === 0) {
  test[index] += 100
}
})
console.log(test)

```
9. Hvað gerir .map() fylkjaaðferðin? Leystu lið 22 í Arrays á Udacity

https://classroom.udacity.com/courses/ud803
```javascript

var bills = [50.23, 19.12, 34.01,
    100.11, 12.15, 9.90, 29.11, 12.99,
    10.00, 99.22, 102.20, 100.10, 6.77, 2.22
];
var totals = bills.map(function(money){money *= 1.15
    return Number(money.toFixed(2));
});
console.log(totals)

```

10. Leystu lið 25 í Arrays í lesson 6 á Udacity https://classroom.udacity.com/courses/ud803
Skil á verkefni
```javascript

var numbers = [
    [243, 12, 23, 12, 45, 45, 78, 66, 223, 3],
    [34, 2, 1, 553, 23, 4, 66, 23, 4, 55],
    [67, 56, 45, 553, 44, 55, 5, 428, 452, 3],
    [12, 31, 55, 445, 79, 44, 674, 224, 4, 21],
    [4, 2, 3, 52, 13, 51, 44, 1, 67, 5],
    [5, 65, 4, 5, 5, 6, 5, 43, 23, 4424],
    [74, 532, 6, 7, 35, 17, 89, 43, 43, 66],
    [53, 6, 89, 10, 23, 52, 111, 44, 109, 80],
    [67, 6, 53, 537, 2, 168, 16, 2, 1, 8],
    [76, 7, 9, 6, 3, 73, 77, 100, 56, 100]
];

// your code goes here
for (var arr = 0; arr < numbers.length; arr++){
    for (var num = 0; num < numbers[arr].length; num++){
        if (numbers[arr][num] % 2 === 0 ){
            numbers[arr][num] = 'even' ;
            } else { numbers[arr][num] = 'odd'
        }
    }
}

```
