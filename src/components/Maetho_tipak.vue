<template>
  <div class="col" v-for="(n) in travellist" :key="n">
    <div class="name">
      <h3>{{ n.name }}</h3>
    </div>
    <div class="tipark">
      <!-- <RouterLink to="/meatho_tipak"></RouterLink> / -->
      <RouterLink class="nav-btn" to="/meatho_tiew">ที่พัก / สถานที่เที่ยว</RouterLink>
    </div>
  </div>
  <h3>ที่พัก</h3>
    <div class="col" v-for="(stay, index) in stayy" :key="index">
      <div class="name">
        <div class="name">
        <img :src="stay.img" style="width: 80%;" alt="รูปภาพ 1">
        <br>
        <br>
        <img :src="stayimg2" style="width: 80%;" alt="">
        <br><br>
        <h4>{{ stay.name }}</h4>
      </div>
      <div class="tipark">
        <p>{{ stay.text_box }}</p>
        <p>สถานที่ : {{ stay.Location }}</p>
        <p>เบอร์ติดต่อ : {{ stay.phone }}</p>
        <p>ราคา :{{ stay.Price }}</p>
        <p>Facebook : <a :href="stay.link">{{ stay.Facebook }}</a></p>
        <p>พิกัด : <a :href="stay.place">{{ stay.place }}</a></p>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const travellist=ref([
{name: 'ดอยแม่โถ', img:"https://www.reviewchiangmai.com/wp-content/uploads/2022/06/doi-mae-tho-1536x1024.jpg", quantity: 0 ,
text_box:'เดินทางโดยสวัสดิภาพ'
}])

const stayy=ref([
{name:'แม่โถแคมป์ปิ้ง ' , 
  img: "https://www.paiduaykan.com/travel/wp-content/uploads/2022/11/35-.jpg",
  img2:"https://th.bing.com/th/id/OIP.srAJVcagsDUnsOZ0sOrlHgHaFj?pid=ImgDet&rs=1",
  text_box:'แม่โถแคมป์ปิ้ง เป็นที่พักเพียงแห่งเดียวในดอยแม่โถ เป็นที่พักในรูปแบบเต้นท์  โลเคชั่นดีมาก ตั้งอยู่บนภูเขามองเห็นวิวได้ 360 องศา แต่เส้นทางจากปากทางถนนใหญ่มายังที่พักจะแคบนิดนึงและเป็นทางดิน ถ้าช่วงฝนตกถนนลื่นรถเก๋ง หรือรถโหลดต่ำไม่แนะนำให้ขึ้นมาค่ะ ใช้บริการรถของที่พักมารับส่งจะดีกว่า '  ,
  Location:'-',
  phone:' 093-6144803',
  Price:'เต้นท์มีทั้งหมด 6 หลัง ราคาหลังละ 2290 บาท พักได้ 2 ท่าน ราคารวมรถนำเที่ยวทุ่งหญ้าสะวันนา และอาหารเช้าข้าวต้ม  ราคาจะแตกต่างกันตามฤดูที่เข้าพัก',
  link: 'https://www.facebook.com/maethocamping/',
  Facebook:'แม่โถแคมป์ปิ้ง Maetho Camping',
  place:'https://goo.gl/maps/gio21befGYXF8j9y8',
},
])

</script>

<style>
.card-img-top{
height: 100%;
padding: 25px;
}

.box_all{
justify-content: center;
align-items: center;
margin-left: 30%;
text-align: center
}
.nav-btn{
  text-decoration: none;
}
</style>
