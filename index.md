---
layout: page
title: 登录身份验证
---

<style>
.login-container {
  max-width: 380px;
  margin: 4em auto 2em auto;
  padding: 2em 2em 1em 2em;
  background: #f8f8fb;
  border-radius: 12px;
  box-shadow: 0 4px 24px rgba(0,0,0,0.09);
}
.login-container h2 {
  text-align: center;
  margin-bottom: 1.5em;
  color: #2d3a4b;
}
.login-form label {
  display: block;
  margin-bottom: 0.5em;
  color: #444;
}
.login-form input[type="text"],
.login-form input[type="password"] {
  width: 100%;
  padding: 0.7em;
  margin-bottom: 1.2em;
  border: 1px solid #ccc;
  border-radius: 6px;
  font-size: 1em;
}
.login-form button {
  width: 100%;
  padding: 0.8em;
  background: #4b8bf4;
  color: #fff;
  border: none;
  border-radius: 6px;
  font-size: 1.1em;
  cursor: pointer;
  margin-bottom: 1em;
  transition: background 0.2s;
}
.login-form button:hover {
  background: #3466c2;
}
.login-hint {
  text-align: center;
  color: #888;
  font-size: 0.98em;
  margin-top: 1em;
}
@media (max-width: 500px) {
  .login-container {
    padding: 1em 0.5em;
  }
}
</style>

<div class="login-container">
  <h2>STEM教育辅助系统登录</h2>
  <form class="login-form" id="loginForm" onsubmit="return false;">
    <label for="username">用户名</label>
    <input type="text" id="username" name="username" placeholder="请输入用户名" autocomplete="off" required>

    <label for="password">密码</label>
    <input type="password" id="password" name="password" placeholder="请输入密码" required>

    <button type="submit" id="loginBtn">登录</button>
  </form>
  <div class="login-hint" id="loginHint">
    <p>本页面为身份验证流程演示，无实际登录功能。</p>
    <p>如需访问更多内容，请联系管理员。</p>
  </div>
</div>

<script>
  document.getElementById('loginForm').addEventListener('submit', function() {
    var user = document.getElementById('username').value.trim();
    var pwd = document.getElementById('password').value;
    var hint = document.getElementById('loginHint');
    if(user === 'mingyou' && pwd === '123456') {
      window.location.href = '/indexxx/';
    } else {
      hint.innerHTML = '<p style="color:#c00;">用户名或密码错误，请重试。</p>';
    }
  });
</script>



