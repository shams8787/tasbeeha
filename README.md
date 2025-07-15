# tasbeeha
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <title>تسبيحة الزهراء عليها السلام</title>
  <style>
    body { font-family: 'Arial'; background: #f5f5f5; text-align: center; padding: 40px; direction: rtl; }
    h1 { color: #4b0082; }
    button { font-size: 20px; margin: 10px; padding: 15px 25px; border-radius: 10px; border: none; background-color: #dcdcdc; }
    .counter { font-size: 18px; margin-top: 5px; }
  </style>
</head>
<body>

<h1>تسبيحة الزهراء (عليها السلام)</h1>

<div>
  <button onclick="increment('akbar', 34)">الله أكبر</button>
  <div class="counter" id="akbar-count">0 / 34</div>

  <button onclick="increment('hamd', 33)">الحمد لله</button>
  <div class="counter" id="hamd-count">0 / 33</div>

  <button onclick="increment('subhan', 33)">سبحان الله</button>
  <div class="counter" id="subhan-count">0 / 33</div>
</div>

<button onclick="reset()">إعادة التسبيح 🔄</button>

<script>
  let counts = { akbar: 0, hamd: 0, subhan: 0 };

  function increment(type, max) {
    if (counts[type] < max) {
      counts[type]++;
      document.getElementById(`${type}-count`).textContent = `${counts[type]} / ${max}`;
    }
  }

  function reset() {
    counts = { akbar: 0, hamd: 0, subhan: 0 };
    document.getElementById('akbar-count').textContent = "0 / 34";
    document.getElementById('hamd-count').textContent = "0 / 33";
    document.getElementById('subhan-count').textContent = "0 / 33";
  }
</script>

</body>
</html>
