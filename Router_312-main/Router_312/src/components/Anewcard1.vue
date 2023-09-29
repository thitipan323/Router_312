<template>
    <div class="box_all">
        <div class="col" v-for="(n, i) in gundumList" :key="n">
            <div class="card">
                <img :src="n.img" class="card-img-top" alt="Travel Destination">
                <div class="card-body">
                    <h3 class="card-title">{{ n.name }}</h3>
                    <p class="card-text">ราคา: {{ n.price }} บาท</p>
                    <h6 class="card-subtitle">*** เหลือ 3 ตัว ***</h6>
                    <button class="btn btn-primary" @click="list_local_control(n.name, n.quantity)">สั่งซื้อ</button>
                </div>
            </div>
        </div>
    </div>
</template>
<script setup>
import { ref } from 'vue';
const gundumList=ref([
{name: 'PG RX-0 UNICORN GUNDAM',  price:6800 , img:"https://da.lnwfile.com/_/da/_raw/1c/ec/xn.jpg", quantity: 0 ,
        text_box:'	Bandai® Gunpla Perfect Grade 1/60 Model Kit PG RX-0 UNICORN GUNDAM ยูนิคอร์น กันดั้ม'
}])
</script>
<style scoped>
.card {
    width: 18rem;
    margin: 20px;
    border: 1px solid #ddd;
    border-radius: 10px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}
.card-img-top {
    height: 200px;
    object-fit: cover;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
}
.card-body {
    padding: 20px;
}
.card-title {
    font-size: 1.5rem;
    margin-bottom: 10px;
}
.card-text {
    font-size: 1.2rem;
}
.card-subtitle {
    font-size: 1rem;
    color: #888;
    margin-top: 10px;
}
.btn-primary {
    background-color: #007BFF;
    border: none;
    border-radius: 5px;
    color: #fff;
}
.btn-primary:hover {
    background-color: #0056b3;
}
.box_all {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    margin: 30px auto;
}
</style>