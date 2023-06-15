# お絵かきアプリ作成してみよう

![完成をQRで確認しよう](./images/QR.png)

## 完成のリンク

[完成イメージへのリンク](https://tec-yoshi-taka.github.io/js-paint-finish/)
<br><br>

---

# Javascript のコードの部分はこちらを参照してください。

---

## 色を増やしてみよう

```HTML
<li id="green"><i class="fas fa-fill-drip"></i></li>
<li id="yellow"><i class="fas fa-fill-drip"></i></li>
<li id="black"><i class="fas fa-fill-drip"></i></li>
```

#### 今が 13 時の場合

![アラートの表示](./img/alert.png)
<br>

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
