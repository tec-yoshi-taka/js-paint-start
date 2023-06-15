# お絵かきアプリ作成してみよう

![完成をQRで確認しよう](./images/QR.png)

## 完成のリンク

[完成イメージへのリンク](https://tec-yoshi-taka.github.io/js-paint-finish/)
<br><br>

---

# Javascript のコードの部分はこちらを参照してください。

---

## 消しゴム機能を設定してみよう

```Javascript
//消しゴム
eraser.addEventListener('mousedown', (e) => {
  //画面をクリアする
  ctx.clearRect(0, 0, WIDTH, HEIGHT);
  //塗りの色を指定する（白）
  ctx.fillStyle = 'rgb(255,255,255)';
  //四角形を描画する
  ctx.fillRect(0, 0, WIDTH, HEIGHT);
});
```

---

## 色を増やしてみよう

```HTML
<li id="green"><i class="fas fa-fill-drip"></i></li>
<li id="yellow"><i class="fas fa-fill-drip"></i></li>
<li id="black"><i class="fas fa-fill-drip"></i></li>
```

---

## 線の色や太さを指定する

```javascript
//線の色
ctx.strokeStyle = "#ec5064";
//線の太さ
ctx.lineWidth = 2;
//線のボケ具合
ctx.shadowColor = "#ec5064";
```

---

## 線の色や太さを変更できるようにしよう

```javascript
//線の色
ctx.strokeStyle = penColor;
//線の太さ
ctx.lineWidth = penSize;
//線のボケ具合
ctx.shadowColor = penColor;
```

---

## クリックで色を変更してみよう

```javascript
//色を変更
colors.forEach((colorli) => {
  colorli.addEventListener("mousedown", (e) => {
    colors.forEach((clr) => {
      clr.classList.remove("active");
    });
    colorli.classList.add("active");
    style = window.getComputedStyle(e.target);
    penColor = style.getPropertyValue("color");
  });
});
```
