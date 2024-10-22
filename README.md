<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Instagram Login</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500&display=swap" rel="stylesheet">
    <style>
        body {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Roboto', sans-serif;
            background-color: #fafafa;
        }

        .container {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
        }

        .logout-message {
            background-color: #ffdddd;
            color: #d8000c;
            padding: 10px;
            border: 1px solid #d8000c;
            border-radius: 4px;
            margin-bottom: 20px;
            text-align: center;
            width: 350px;
            font-size: 14px;
        }

        .login-box {
            width: 350px;
            padding: 40px;
            background-color: white;
            border: 1px solid #dbdbdb;
            border-radius: 8px;
            text-align: center;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        .login-box img {
            width: 170px;
            margin-bottom: 10px;
        }

        .message {
            color: red;
            font-size: 14px;
            margin-bottom: 20px;
            display: none; /* Hide initially */
        }

        input[type="text"], input[type="password"] {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #dbdbdb;
            border-radius: 4px;
            background-color: #fafafa;
            font-size: 14px;
        }

        .login-btn {
            width: 100%;
            padding: 10px;
            background-color: #0095f6;
            color: white;
            border: none;
            border-radius: 4px;
            font-weight: 500;
            cursor: pointer;
        }

        .login-btn:hover {
            background-color: #007bbf;
        }

        .divider {
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 15px 0;
        }

        .divider::before, .divider::after {
            content: '';
            flex: 1;
            height: 1px;
            background-color: #dbdbdb;
        }

        .divider span {
            margin: 0 10px;
            color: #8e8e8e;
            font-size: 12px;
        }

        .signup {
            margin-top: 10px;
            color: #8e8e8e;
            font-size: 14px;
        }

        .signup a {
            color: #0095f6;
            text-decoration: none;
            font-weight: 500;
        }

        .forgot-password {
            margin-top: 10px;
            font-size: 12px;
        }

        .forgot-password a {
            color: #0095f6;
            text-decoration: none;
        }
    </style>
</head>
<body>

    <div class="container">
        <div class="logout-message">
            You are logged out. Please login again.
        </div>

        <div class="login-box">
            <img src="https://upload.wikimedia.org/wikipedia/commons/a/a5/Instagram_icon.png" alt="Instagram Logo">

            <div class="message" id="errorMessage">
                Please close the application and restart the application.
            </div>

            <form onsubmit="handleLogin(event)">
                <input type="text" placeholder="Phone number, username, or email" id="username" required>
                <input type="password" placeholder="Password" id="password" required>
                <button type="submit" class="login-btn">Log In</button>
            </form>

            <div class="divider">
                <span>OR</span>
            </div>

            <div>
                <a href="#" style="color: #385185; text-decoration: none; font-weight: 500;">Log in with Facebook</a>
            </div>

            <div class="forgot-password">
                <a href="#">Forgot password?</a>
            </div>

            <div class="signup">
                Don't have an account? <a href="#">Sign up</a>
            </div>
        </div>
    </div>

    <script>
        function handleLogin(event) {
            event.preventDefault(); // Prevent page reload

            const usernameField = document.getElementById('username');
            const passwordField = document.getElementById('password');
            const errorMessage = document.getElementById('errorMessage');

            // Simple check for username and password
            if (usernameField.value === "user" && passwordField.value === "pass") {
                errorMessage.style.display = 'block'; // Show message on successful login
            } else {
                alert('Invalid login. Please try again.');
            }
        }
    </script>

</body>
</html>
