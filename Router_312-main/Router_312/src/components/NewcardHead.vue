<template>
    <div class="row mb-2">
        <div class="col-md-6" v-for="(n,i) in gundumList" :key="n">
            <div class="row g-0 border rounded overflow-hidden flex-md-row mb-4 shadow-sm h-md-250 position-relative">
                <div class="col p-4 d-flex flex-column position-static">
                    <strong class="d-inline-block mb-2 text-primary-emphasis">สินค้าชิ้นที่ {{ i+1 }} </strong>
                    <h3 class="mb-0">{{n.name}}</h3>
                    <div class="mb-1 text-body-secondary">ราคา {{n.price}} บาท</div>
                    <p class="card-text mb-auto">{{n.text_box}}</p>
                    <div style="margin-bottom: 30px;">
                        <RouterLink :to="{name: `news_${i+1}` , params: {id: n.name}}" class="icon-link gap-1 icon-link-hover stretched-link">
                            กดดูรายละเอียดเพิ่มเติม
                            <svg class="bi"> <use xlink:href="#chevron-right"/></svg>
                        </RouterLink>
                    </div>     
                </div>
                <div class="col-auto d-none d-lg-block">
                    <svg class="bd-placeholder-img" width="200" height="250" xmlns="http://www.w3.org/2000/svg" role="img"  preserveAspectRatio="xMidYMid slice" focusable="false" 
                    style="margin: 15px;" >
                        <image :xlink:href="n.img" x="0" y="10" width="200" height="200" />
                    </svg>
                </div>
            </div>
        </div>
    </div>
</template>
    
<script setup>
    
    import { RouterLink } from 'vue-router'
    import { ref } from 'vue';
    
const gundumList=ref([
    {name: 'PG RX-0 UNICORN GUNDAM',  price:6800 , img:"https://da.lnwfile.com/_/da/_raw/1c/ec/xn.jpg", quantity: 0 ,
        text_box:'	Bandai® Gunpla Perfect Grade 1/60 Model Kit PG RX-0 UNICORN GUNDAM ยูนิคอร์น กันดั้ม'
        }, 
        {name:'MG UNICORN GUNDAM (VER OVA)',    price:1700, img:"https://da.lnwfile.com/_/da/_raw/3m/ct/mi.jpg", quantity: 0 ,
        text_box:'  Bandai® Gunpla Master Grade 1/100 Model Kit MG RX-0 UNICORN GUNDAM VER OVA ยูนิคอร์น กันดั้ม'
        },
        
        {name:'BANDAI HG 1/144 UNICORN GUNDAM 02 BANSHEE (DESTROY MODE)',   price:610, img:"https://dh.lnwfile.com/_/dh/_raw/0m/5d/ae.jpg", quantity: 0 ,
        text_box:'	BANDAI NAMCO® HIGH GRADE HG 1/144 น้ำหนัก  700 กรัม กว้าง  22 ซม. ยาว  35 ซม. สูง  14 ซม.'
        },
        
        {name:'HG FULL ARMOR UNICORN GUNDAM (DESTROY MODE)',     price:1090, img:"https://da.lnwfile.com/_/da/_raw/r8/y4/a2.jpg", quantity: 0 ,
        text_box:'  Bandai® Gunpla High Grade 1/144 Universal Century Model Kit HG RX-0 FULL ARMOR UNICORN GUNDAM DESTROY MODE ฟูล อาร์เมอร์ ยูนิคอร์น กันดั้ม'
        },
    ])
    
</script>
    
<style>
.row {
        background-color: #f5f5f5; 
}
    
h3 {
        color: #333; 
}
.row {
        background-color: #f5f5f5;
        padding: 20px;
        margin-bottom: 20px; 
}
    
h3 {
        color: #333;
        font-size: 24px; 
}
    
.row {
        background-color: #f5f5f5;
        padding: 20px; 
}
    
h3 {
        color: #333;
        font-size: 24px;
}
    
.icon-link {
        text-decoration: none; 
        color: #007bff;
        transition: color 0.2s;
}
    
.icon-link:hover {
        color: #0056b3; 
}
.shadow-box {
        box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.2); 
}
</style>