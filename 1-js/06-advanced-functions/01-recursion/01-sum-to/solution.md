迴圈解：

```js run
function sumTo(n) {
  let sum = 0;
  for (let i = 1; i <= n; i++) {
    sum += i;
  }
  return sum;
}

alert( sumTo(100) );
```

遞迴解：

```js run
function sumTo(n) {
  if (n == 1) return 1;
  return n + sumTo(n - 1);
}

alert( sumTo(100) );
```

公式解: `sumTo(n) = n*(n+1)/2`:

```js run
function sumTo(n) {
  return n * (n + 1) / 2;
}

alert( sumTo(100) );
```

附言：顯然公式解的執行速度最快？對任何 `n` 它只用三個運算。數學幫了大忙！

迴圈解的執行速度次之。遞迴解與迴圈解皆需累加相同的數字，但是遞迴牽涉到巢狀呼叫和執行脈絡堆疊的維護，這會消耗資源，執行速度也就更慢。


附附言：某些引擎支援 "tail call" 優化：若函數的最後一行是遞迴呼叫（如上述的 `sumTo`），外層函數將不須恢復執行，引擎也就不用記錄其執行脈絡，這便減輕了記憶體的負擔，所以 `sumTo(100000)` 行得通。要是 JavaScript 引擎不支援 "tail call" 優化（大多不支援），將引發錯誤：堆疊上限溢位，因為堆疊大小通常都會設限。