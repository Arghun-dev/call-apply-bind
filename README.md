# call-apply-bind

```js
const obj = {
  num: 3
}

const functionName = (arg1, arg2, arg3) => {
  return this.num + arg1 + arg2 + arg3;
}

functionName.call(obj, arg1, arg2, arg3);

functionName.apply(obj, [arg1, arg2, arg3]);

const bound = functionName(obj);
bound(arg1, arg2, arg3);
```

**all of them attaches the function into the object (addes the function as a method into that object)**

**call and apply are exactly the same, they are simultaniously executing the function with given arguments. But `bind` does not execute the function, it actually returns the function itself, and you can call or execute that function and give it some arguments.**
