importance: 5

---

# 斐波那契数

[斐波那契數列](https://zh.wikipedia.org/wiki/%E6%96%90%E6%B3%A2%E9%82%A3%E5%A5%91%E6%95%B0%E5%88%97)滿足方程 <code>F<sub>n</sub> = F<sub>n-1</sub> + F<sub>n-2</sub></code>。換言之，任一項是其前兩項之和。

首二項皆為 `1`，接著是 `2(1+1)`，然後是`3(1+2)`、`5(2+3)`，以此類推：`1, 1, 2, 3, 5, 8, 13, 21...`。

斐波那契數和[黃金比例](https://zh.wikipedia.org/wiki/%E9%BB%84%E9%87%91%E5%88%86%E5%89%B2%E7%8E%87)以及其他常見的自然現象息息相關。

寫一函數 `fib(n)` 求第 `n` 個斐波那契數列。

示意：

```js
function fib(n) { /* your code */ }

alert(fib(3)); // 2
alert(fib(7)); // 13
alert(fib(77)); // 5527939700884757
```

附言：這函數跑起來應該要很快，`fib(77)` 的執行時間遠不須一秒。