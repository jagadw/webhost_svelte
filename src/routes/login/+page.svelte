<script>
</script>
    <div class="container">
        <div class="login">
            <h1>Log In</h1>
            <input type="email" placeholder="Masukan alamat email">
            <br><br>
            <input type="password" placeholder="Masukan password">
            <br><br><br>
            <div class="option">
                <input type="submit" value="Login">
                <small>Belum punya akun? <a href="./register/">Register</a></small>    
            </div>
        </div>
    </div>
<style>
    .container {
        height: 100vh;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .login {
        padding: 5vw;
        border: solid black 1px;
    }
    .option {
        justify-content: space-between;
    }
</style>