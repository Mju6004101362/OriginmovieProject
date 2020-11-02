<template>
<div class="box">
    <div style="margin:8px 0">
        <h2 style="text-align:center">Log in</h2>
    </div>
    <p>Username</p>
    <input type="text" v-model="email">
    <p>Password</p>
    <input type="password" v-model="password">
    <div style="display:flex;justify-content:flex-end;padding-top:12px">
        <button @click="login()">Login</button>
    </div>

</div>
</template>

<script>
import firebase from "firebase"
import auth from "@/plugins/firebaseConfig.js"
export default {
    layout: 'login',
    data() {
        return {
            email: '',
            password: '',
        }
    },
    methods: {
        login() {
            firebase.auth().signInWithEmailAndPassword(this.email, this.password).then(Response => {
                    location.href = "/admin/addMovie"
                })
                .catch((error) => {
                    // Handle Errors here.
                    var errorCode = error.code;
                    var errorMessage = error.message;
                    alert('Username หรือ Password ไม่ถูกต้อง')
                    console.log('wrong username / password')
                });

        }
    }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Prompt:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Prompt', sans-serif;
}

.box {
    width: 300px;
    height: 300px;
    background-color: #fff;
    border-radius: 4px;
    padding: 16px;
    -webkit-box-shadow: 0px 0px 5px 0px rgba(0, 0, 0, 0.2);
    -moz-box-shadow: 0px 0px 5px 0px rgba(0, 0, 0, 0.2);
    box-shadow: 0px 0px 5px 0px rgba(0, 0, 0, 0.2);
}

.box input {
    margin: 8px 0;
    padding: 0 12px;
    width: 100%;
    height: 40px;
    border: 1px solid #d39e00;
    border-radius: 4px;
    font-size: 16px;
}

.box button {
    width: 80px;
    height: 40px;
    border: none;
    border-radius: 4px;
    background-color: #ecb100;
    transition: 0.3s;
    cursor: pointer;
}

.box button:hover {
    background-color: #e0a800;
}
</style>
