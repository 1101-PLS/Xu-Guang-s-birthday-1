# Xu-Guang-s-birthday-1
<!DOCTYPE html>
<html lang="zh-CN">
<head>
  <meta charset="UTF-8">
  <title>XGbirthday</title>
  <style>
    body { font-family: sans-serif; text-align: center; padding: 50px; }
    .hidden { display: none; }
    img { max-width: 80%; height: auto; margin-bottom: 20px; }
    input[type="text"] { padding: 5px; font-size: 16px; }
    button { padding: 10px 20px; font-size: 16px; cursor: pointer; }
    .arrow { font-size: 40px; cursor: pointer; }
  </style>
</head>
<body>
  <!-- Page 1 -->
  <div id="page1">
    <img src="XGbirthday.png" alt="XGbirthday">
    <br>
    <button onclick="showTranslation()">翻译</button>
  </div>

  <!-- Page 2 -->
  <div id="page2" class="hidden">
    <img src="XGXGbirthday-translation.png" alt="XGXGbirthday-translation">
    <div class="arrow" onclick="showPasswordPage()">⬇️</div>
  </div>

  <!-- Page 3 -->
  <div id="page3" class="hidden">
    <p>请输入四位数密码：</p>
    <input type="text" id="password" placeholder="0712">
    <button onclick="checkPassword()">确认</button>
    <p id="error" style="color:red;"></p>
  </div>

  <!-- Page 4 -->
  <div id="page4" class="hidden">
    <h2>🎉生日快乐！🎂</h2>
    <img src="celebration.png" alt="Celebration">
  </div>

  <script>
    function showTranslation() {
      document.getElementById('page1').classList.add('hidden');
      document.getElementById('page2').classList.remove('hidden');
    }

    function showPasswordPage() {
      document.getElementById('page2').classList.add('hidden');
      document.getElementById('page3').classList.remove('hidden');
    }

    function checkPassword() {
      const pwd = document.getElementById('password').value.trim();
      const error = document.getElementById('error');
      if (pwd === "0712") {
        document.getElementById('page3').classList.add('hidden');
        document.getElementById('page4').classList.remove('hidden');
      } else {
        error.textContent = "啊嘞？再想想……提示“生日”";
      }
    }
  </script>
</body>
</html>
