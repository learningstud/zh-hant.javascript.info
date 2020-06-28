importance: 5

---

# 遞進累加至某數

寫一函數 `sumTo(n)` 求級數 `1 + 2 + ... + n`。

示意：

```js no-beautify
sumTo(1) = 1
sumTo(2) = 2 + 1 = 3
sumTo(3) = 3 + 2 + 1 = 6
sumTo(4) = 4 + 3 + 2 + 1 = 10
...
sumTo(100) = 100 + 99 + ... + 2 + 1 = 5050
```

請提出三種解法：

1. 使用 `for` 迴圈。
2. 使用遞迴，對 `n > 1` 算 `sumTo(n) = n + sumTo(n-1)`。
3. 使用[等差數列](https://zh.wikipedia.org/wiki/%E7%AD%89%E5%B7%AE%E6%95%B0%E5%88%97)求和公式。

輸出範例：

```js
function sumTo(n) { /*... 你的程式碼 ... */ }

alert( sumTo(100) ); // 5050
```

附言：哪種解法執行最快？最慢？為何？

附附言：我們能用遞迴解求 `sumTo(100000)` 嗎？