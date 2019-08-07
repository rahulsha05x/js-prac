# js-prac

## Q1. Create a function addNum which takes the argument n and return a method which adds n number of parameters passed.
  ### For example 
  ### let add3 = addNum(3)
      add3(1)(2)(3) // 6;
  
  ```javascript
    function addNum(totalArgs) {
                        totalArgs = totalArgs;
                        return function recursor() {
                          return arguments.length < totalArgs ? recursor.bind(this, ...arguments) : add.call(this, ...arguments);
                        }
                        function add(...args) {
                          let total = 0;
                          for (let i of args) {
                            total += i;
                          }
                          return total;
                        }
                      }
```
