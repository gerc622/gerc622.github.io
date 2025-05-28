<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>哇！你来啦 - 登录</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #e6f2ff;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .login-box {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
            text-align: center;
            width: 300px;
        }
        h1 {
            color: #ff85a2;
            margin-bottom: 20px;
        }
        input {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ddd;
            border-radius: 5px;
            box-sizing: border-box;
        }
        button {
            background-color:#4a90e2;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            width: 100%;
            font-size: 16px;
        }
        button:hover {
            background-color: #4a90e2;
        }
        .error {
            color: red;
            margin-top: 10px;
            font-size: 14px;
        }
    </style>
</head>
<body>
    <div class="login-box">
        <h1> 哇！你来啦</h1>
        <p>请输入用户名和密码：</p>
        
        <input type="text" id="username" placeholder="用户名" required>
        <input type="password" id="password" placeholder="密码" required>
        <button onclick="checkLogin()">哇！你来啦</button>
        
        <p id="error" class="error"></p>
    </div>

    <script>
        function checkLogin() {
            const username = document.getElementById("username").value;
            const password = document.getElementById("password").value;
            const errorElement = document.getElementById("error");

            if (username === "gerc" && password === "123gerc，。") {
                // 登录成功，跳转到主页面（如 home.html）
                window.location.href = "home.html";
            } else {
                errorElement.textContent = "公主殿下再试一次吧";
            }
        }
    </script>
</body>
</html>
