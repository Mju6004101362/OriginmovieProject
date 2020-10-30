<template>
<div class="container">
    <div class="nowPlaying">
        <div class="box">
            <div class="header">
                <h2>ติดต่อเรา</h2>
            </div>
            <h3>ลักษณะโรงหนัง</h3>
            <div>“ออริจิน ซีนีเพล็กซ์”  เป็นโรงภาพยนตร์ขนาดเล็กประกอบด้วยโรงภาพยนตร์จำนวน 3 โรงวันละ 3 เวลาอัพเดทหนัง 9 เรื่อง
             มุ่งเน้นการให้บริการลูกค้าในทุกระดับชั้นและมีโรงภาพยนตร์ที่ทันสมัย
             </div>
             <h3>โรงภาพยนตร์ที่ 1 และ 2</h3>
             <div> เป็นแบบธรรมดาแต่ละโรงมี 30 ที่นั่ง ราคาที่นั่งเริ่มต้น 120 บาทต่อที่นั่งตามประเภทหนัง</div>
            <center> <img src="~/assets/img/Theater.jpg" style="width:500px; height:300px;" alt=""> </center>
            <hr/>
            <h3>โรงภาพยนตร์ที่ 3 </h3>
            <div>เป็นแบบ3D/4DX ระบบ3D จะเป็นหนัง 3 มิติ ส่วนระบบ4DX คือโรงภาพยนตร์ที่ถูกติดตั้ง
            เอฟเฟคพิเศษเพิ่มเข้าไปได้แก่ เก้าอี้ที่เคลื่อนไหวได้รอบทิศทาง แถมยังสั่นหลัง สกิตขาได้อีก ทั้งน้ำ กลิ่น ลม
             และพายุฝนก็มี ยังไม่หมดยังมี ฟ้าฝ่า(ไฟแฟลช) ฟองสบู่และพีคสุดคือหิมะ</div>
             <div>มี 30 ที่นั่ง ราคาที่นั่งเริ่มต้น 220 บาทต่อที่นั่งตามประเภทหนัง</div>

            <center><img src="~/assets/img/4DX.jpg" style="width:500px; height:500px;" alt=""></center>
            <br>
            <center><img src="~/assets/img/3D.jpg" style="width:500px; height:500px;" alt=""></center>

            <h4>ข้อมูลการติดต่อ</h4>
         <div> <img src="~/assets/img/gmail.png" alt="" style="width:50px; height:50px grid-template-columns:40 px auto;" >: pennapafern101@gmail.com</div>
         <div> <img src="~/assets/img/telephone.png" alt="" style="width:50px; height:50px grid-template-columns:40 px auto;">: 0631140335</div>
         <div> <img src="~/assets/img/facebook.png" alt="" style="width:50px; height:50px grid-template-columns:40 px auto;">
            <a href="https://www.facebook.com/fernly.fernz.9/">https://www.facebook.com/fernly.fernz.9/</a> </div>
        </div>
 </div>
</div>
</template>

<script>
import firebase from "firebase";
import {
    db
} from '@/plugins/firebaseConfig.js'
export default {
    layout: 'main',
    data(){
        return{
            movielist: '',
            date : ''
        }
    },

}
</script>

<style scoped>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.container {
    width: 1000px;
    margin: auto;
}

.container .nowPlaying {
    padding: 32px 0;

}

.container .nowPlaying .box {
    width: 100%;
    min-height: 700px;
    border-radius: 4px;
    background-color: #fff;
    padding: 0 16px 16px 16px;
}

.container .nowPlaying .box .header {
    padding: 16px 0;
}

.container .nowPlaying .box .header h2 {
    color: #d39e00;
}

.container .nowPlaying .box hr {
    width: 100%;
    margin-bottom: 32px;
    border: 1px solid gainsboro;
}

.container .nowPlaying .box .grid {
    display: grid;
    grid-template-columns: 25% 25% 25% 25%;

}

.container .nowPlaying .box .grid .card .padd {
    width: 185px;
    height: 420px;
    margin: auto;
}

.container .nowPlaying .box .grid .card img {
    width: 185px;
    height: 275px;
    border-radius: 4px;
    object-fit: cover;
}

.container .nowPlaying .box .grid .btn-box{
  margin-bottom:8px;
  position: relative;
}

.container .nowPlaying .box .grid .btn-box img{
  width: 30px;
  height: 30px;
  position: absolute;
  top: 0;
  right: 50px;
}

.container .nowPlaying .box .grid .btn-box button {
    width: 185px;
    height: 30px;
    background-color: #FFC40E;
    border: none;
    border-radius: 4px;
    padding-right: 20px;
    cursor: pointer;
    transition: 0.3s;
}

.container .nowPlaying .box .grid .btn-box button:hover{
  background-color: #f3b90c;
}

.container .nowPlaying .box .grid .text {
    line-height: 30px;
}

.container .nowPlaying .box .grid .card h4 {
    font-weight: 500;
}


</style>
