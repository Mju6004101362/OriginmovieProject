<template>
<div class="side" v-if="authenticatedUser">
    <div class="header-icon">
        <img src="~/assets/img/logoad.png" alt="" />
    </div>
    <hr />
    <ul>
        <nuxt-link to="/admin/addMovie">
            <li id="add">เพิ่มรอบหนัง</li>
        </nuxt-link>
        <nuxt-link to="/admin/cost">
            <li id="cost">สรุปการจอง</li>
        </nuxt-link>
        <nuxt-link to="/admin/searchPaid">
            <li id="paid">ชำระเงิน</li>
        </nuxt-link>
        <li @click="logout()">ออกจากระบบ</li>
    </ul>
    <br />
    <hr />
</div>
</template>

<script>
import firebase from "firebase"
export default {
    data() {
        return {
            authenticatedUser: null
        }
    },
    created() {
        firebase.auth().onAuthStateChanged(user => (this.authenticatedUser = user))
    },
    methods: {
        logout() {
            if (confirm('คุณต้องการออกจากระบบใช่หรือไม่?')) {
                firebase.auth().signOut()
                location.href = "/login"
            }
        }
    }
}
</script>

<style scoped>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.side {
    width: 250px;
    min-height: 100vh;
    background-color: rgb(255, 218, 6);
    -webkit-box-shadow: 4px 0px 5px 0px rgba(20, 34, 230, 0.2);
    -moz-box-shadow: 4px 0px 5px 0px rgba(45, 24, 238, 0.2);
    box-shadow: 4px 0px 5px 0px rgba(10, 14, 216, 0.2);
    position: fixed;
}

.side .header-icon {
    height: 150px;
    display: flex;
    justify-content: center;
    align-items: center;
}

.side .header-icon img {
    width: 190px;
    height: 140px;
}

.side ul a {
    text-decoration: none;
    color: #000;
}

.side ul li {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 0 16px;
    height: 60px;
    cursor: pointer;
    transition: 0.3s;
}

.side ul a:hover li {
    background-color: rgb(225, 225, 225);
}

.side ul a:focus li {
    background-color: rgb(190, 190, 190);
}

.side ul li:hover {
    background-color: rgb(252, 127, 127);
}
</style>
