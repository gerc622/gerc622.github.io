<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>公主殿下的秘密花园 - 登录</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #e6f2ff; /* 浅蓝色背景 */
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
            color: #4a90e2; /* 蓝色标题 */
            margin-bottom: 20px;
        }
        input {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #cce0ff; /* 浅蓝色边框 */
            border-radius: 5px;
            box-sizing: border-box;
            background-color: #f5f9ff; /* 输入框浅蓝背景 */
        }
        button {
            background-color: #4a90e2; /* 蓝色按钮 */
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            width: 100%;
            font-size: 16px;
            transition: background-color 0.3s;
        }
        button:hover {
            background-color: #3a7bc8; /* 深蓝色悬停效果 */
        }
        .error {
            color: #ff6b6b; /* 错误提示红色 */
            margin-top: 10px;
            font-size: 14px;
        }
    </style>
</head>
<body>
    <div class="login-box">
        <h1> 公主殿下的秘密花园</h1>
        <p>请输入用户名和密码：</p>
        
        <input type="text" id="username" placeholder="用户名" required>
        <input type="password" id="password" placeholder="密码" required>
        <button onclick="checkLogin()">进入秘密花园</button>
        
        <p id="error" class="error"></p>
    </div>

    <script>
        function checkLogin() {
            const username = document.getElementById("username").value;
            const password = document.getElementById("password").value;
            const errorElement = document.getElementById("error");

            if (username === "Gerc" && password === "123gerc") {
                window.location.href = "home.html";
            } else {
                errorElement.textContent = " 用户名或密码错误！";
            }
        }
    </script>
</body>
</html>

