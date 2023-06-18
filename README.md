# お絵かきアプリ作成してみよう

![完成をQRで確認しよう](./images/QR.png)

## 完成のリンク

[完成へのリンク](https://tec-yoshi-taka.github.io/js-paint-finish/)
<br><br>

---

## 資料

[資料へのリンク](https://drive.google.com/file/d/1VRlSrcz8XDlrfgTHXIzb0Xhz4_bze7aO/view?usp=sharing)

---

## Javascript のコードの部分はこちらを参照してください。

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

## ペンの色と太さを変数に代入してみよう

```javascript
//ペンの色と太さを変数に代入してみよう
let penColor = "rgb(255,0,0)";
let penSize = 2;
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

---

## さらにペンを増やす（HTML）

```HTML
<!-- 好きなの色を増やそう -->
<li id="other"><i class="fas fa-fill-drip"></i></li>
```

## さらにペンを増やす（CSS）

```css
#color li#other {
  background-color: お好きな色;
}
#color li#other.active,
#color li#other:hover {
  color: お好きな色;
  background-color: #fff;
}
```

---
