<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login Page</title>
     <link rel="stylesheet" href="login.css">
    

</head>
<body>
    <div class="container">
        <h2>Login</h2>
        
        <div class="welcome">
           
                <h3>Welcome to the Future.</h3><br>
                <p>Your gateway to innovation and seamless connectivity. Access cutting-edge technology and smart solutions. Log in to enter the next level of high-tech performance.</p>
            </div>
            <form id="userForm" onsubmit="return validateForm()" action="index.html">
                            <div class="left">
            <div class="form-group">
            
                <label for="username" id="user1">Email</label>
                <input type="text" id="email" name="email">
                <span id="emailError" class="error" color="red"></span>

            </div>
            <div class="form-group">
                <label for="password">Password</label>
                <input type="password" id="password" name="password">
                <span id="passwordError" class="error" ></span>

            </div>
            <button class="btn" type="submit">submit</button>
        </form>
        <div class="login-section">
            Don't have an account?   <a href="signup.html" style="color: #fff; text-decoration: underline;"> Sign up</a>
        </div>
    </div>
    </div>
    <script>
        function validateForm() {
           
            const email = document.getElementById("email").value.trim();
            const password = document.getElementById("password").value.trim();

            let valid = true;

            const emailPattern = /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/;
            if (!emailPattern.test(email)) {
                document.getElementById("emailError").innerHTML = "Please enter a valid email address.";
                valid = false;
                return valid;
            }

            if (password.length <= 7) {
                document.getElementById("passwordError").innerHTML = "Please enter a valid password grater then 8 letter.";
                valid = false;
                return valid;
            }

            if (valid) {
                document.getElementById("result").innerHTML = "Form submitted successfully!";
            } else {
                document.getElementById("result").innerHTML = "Please correct the errors above.";
            }
            return valid;
        }
    </script>
    
</body>
</html>
