# Instagram-Followers
Bu yerda Instagram obunachi kopaytirsa boladi
<!DOCTYPE html><html lang="uz">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>IG Dashboard</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f1f5f9;
      color: #111;
    }.login-box, .dashboard {
  max-width: 400px;
  margin: 100px auto;
  background: white;
  padding: 25px;
  border-radius: 12px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}

h2 {
  text-align: center;
}

input {
  width: 100%;
  padding: 10px;
  margin: 10px 0;
  border-radius: 6px;
  border: 1px solid #ccc;
}

button {
  width: 100%;
  padding: 10px;
  background: #2563eb;
  color: white;
  border: none;
  border-radius: 6px;
  cursor: pointer;
  font-size: 16px;
}

button:hover {
  background: #1d4ed8;
}

.error {
  color: red;
  text-align: center;
}

.dashboard {
  display: none;
  max-width: 800px;
}

.card {
  background: #f8fafc;
  padding: 15px;
  border-radius: 10px;
  margin: 10px 0;
  box-shadow: 0 2px 6px rgba(0,0,0,0.08);
}

  </style>
</head>
<body><!-- LOGIN --><div class="login-box" id="loginBox">
  <h2>Login</h2>
  <input type="text" id="username" placeholder="Username">
  <input type="password" id="password" placeholder="Password">
  <button onclick="login()">Kirish</button>
  <p class="error" id="error"></p>
</div><!-- DASHBOARD --><div class="dashboard" id="dashboard">
  <h2>Instagram Dashboard</h2>  <div class="card">
    <h3>Profil Ma’lumotlari</h3>
    <p>Username: <b id="userDisplay"></b></p>
  </div>  <div class="card">
    <h3>Reja</h3>
    <ul>
      <li>📸 Kuniga 1 post</li>
      <li>⏰ Story har 3 soatda</li>
      <li>#️⃣ Hashtag ishlatish</li>
      <li>💬 Komment yozish</li>
    </ul>
  </div>  <div class="card">
    <h3>Maqsad</h3>
    <p>🎯 1 oyda 5K follower</p>
  </div><button onclick="logout()">Chiqish</button>

</div><script>
  // Test login ma'lumotlari
  const correctUser = "almaz";
  const correctPass = "12345";

  function login() {
    const user = document.getElementById("username").value;
    const pass = document.getElementById("password").value;
    const error = document.getElementById("error");

    if (user === correctUser && pass === correctPass) {
      document.getElementById("loginBox").style.display = "none";
      document.getElementById("dashboard").style.display = "block";
      document.getElementById("userDisplay").innerText = user;
    } else {
      error.innerText = "Login yoki parol noto‘g‘ri";
    }
  }

  function logout() {
    document.getElementById("dashboard").style.display = "none";
    document.getElementById("loginBox").style.display = "block";
    document.getElementById("username").value = "";
    document.getElementById("password").value = "";
    document.getElementById("error").innerText = "";
  }
</script></body>
</html>
