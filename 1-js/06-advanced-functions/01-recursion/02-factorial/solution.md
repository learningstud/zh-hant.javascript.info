根據定義，`n!` 可以寫做 `n * (n-1)!`。

換言之，`factorial(n)` 的值可以算做 `n` 乘以 `factorial(n-1)` 的值，且關於 `n-1` 的函數呼叫可以遞迴地不斷下降直至 `1`。

```js run
function factorial(n) {
  return (n != 1) ? n * factorial(n - 1) : 1;
}

alert( factorial(5) ); // 120
```

遞迴的基底是 `1` 。此例中，我們也可以令基底為 `0`，這沒什麼影響，但會導致一個額外的遞迴步驟：

```js run
function factorial(n) {
  return n ? n * factorial(n - 1) : 1;
}

alert( factorial(5) ); // 120
```
