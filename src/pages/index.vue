<template>
    <div>
        <h1>What's the Date Today?</h1>
        <div class="today">
            <div class="currentDate">현재날짜 : {{ now }}</div>
            <div class="currentTime">현재시간 : {{ date }}</div>
        </div>
    </div>
</template>

<script>
    export default {
        setup(){
            const moment = require('moment'); // moment 모듈불러오기
            const now = moment().format('YYYY-MM-DD'); //오늘
            const date= moment().format('HH : MM : ss');
            
            function update(){
                setInterval(()=>{
                    date, 1000
                });
            }
            update();
            return{
                now , date, update
            }
        }
    }
</script>

<style>
*{margin: 0; padding: 0; box-sizing: 0;}
h1{color: mediumaquamarine; margin-top: 150px !important;}
.today{background: #f5f5f5; border-radius: 5px; width: 500px; margin: 0 auto; padding: 20px; color: mediumaquamarine; font-weight: bold; text-align: center; display: flex; align-items: center; justify-content: space-around;}
.currentDate, .currentTime{color: #666;}
</style>