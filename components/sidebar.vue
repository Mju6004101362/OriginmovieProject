<template>
  <div class="side">
    <br /><br />
    <div class="header-icon">
      <img src="~/assets/img/logoad.png" alt="" />
    </div>
    <br />
    <br />
    <hr />
    <br />

    <ul>
      <nuxt-link to="/admin/addMovie">
        <li id="add">เพิ่มรอบหนัง</li>
      </nuxt-link>
      <nuxt-link to="/admin/cost">
        <li id="cost">สรุปการจอง</li>
      </nuxt-link>
      <nuxt-link to="/admin/searchPaid">
        <li id="paid">ค้นหารายจ่ายลูกค้า</li>
      </nuxt-link>
      <nuxt-link to="#">
        <li>ออกจากระบบ</li>
      </nuxt-link>
    </ul>
    <br />
    <hr />
  </div>
</template>

<script>
export default {}
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
  height: 60px;
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

.side ul a li {
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

.side ul a:last-child:hover li {
  background-color: rgb(252, 127, 127);
}
</style>
