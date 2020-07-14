<template>
    <div class="box">
        <div class="menu-list">
        <div class="total" :class="{active:item.id === sel}" v-for="item in tabs" :key="item.id" @click="select(item)">
            <b>{{ item.label }}</b>
        </div>
        </div>
        <div class="text">
        <div class="all" v-show="sel === 1">
          <div class="m-yer">
            <h2>2020年5月</h2>
            <div class="u-day">
              <span>日</span>
              <span>一</span>
              <span>二</span>
              <span>三</span>
              <span>四</span>
              <span>五</span>
              <span>六</span>
            </div>
            <div class="data">
              <span>6</span>
              <span>7</span>
              <span class="active">8</span>
              <span>9</span>
              <span>10</span>
              <span>11</span>
              <span>12</span>
            </div>
          </div>
          <div class="m-lei">
              <div class="u-pro">
                <div><span>11:00</span><i> </i></div>
                <div><span>12:00</span><i> </i></div>
                <div><span>13:00</span><i> </i></div>
                <div><span>14:00</span><i> </i></div>
                <div><span>15:00</span><i> </i></div>
              </div>
          </div>
        </div>
        <div class="all" v-show="sel === 2">222</div>
        <div class="all" v-show="sel === 3">333</div>
        </div>
    </div>
</template>
<script>
export default {
    data () {
        return {
        yxf:4,
        wxz:5,
        ywg:1,
        sel:1,
        tabs: [
            {label: '日视图',num:0, id: 1},
            {label: '周视图',num: 0, id: 2},
            {label: '月视图',num: 0, id: 3},
        ]
        }
    }
}
</script>

<style>
  .box{
    height: 48px;
  }
  .equi_container {
      display: flex;
      flex-direction: column;
  }
  .menu-list {
      display: flex;
      box-shadow: 0px 1px 0px 0px rgba(0,0,0,0.05), 0px 1px 0px 0px rgba(0,0,0,0.05) inset;
  }
  .total{
      flex: 1;
      height: 48px;
      line-height: 48px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      /*height: 100%;*/
      /*line-height: 0.44rem;*/
      background:#ffffff;
      color: #666666;;
      font-size: 14px;
      text-align:center;
      float:left;
     
  }
  .total.active{
    background: #ffa800;
    color: #444444;
  }
  .text{
      flex: 1;
  }
  .m-yer{
    width: 375px;
    height: 139px;
    background: #ffffff;
    border-radius: 0px 0px 12px 12px;
    margin-bottom: 11px;
    box-shadow: 0px 6px 10px 0px rgba(131,134,163,0.12); 
  }
.m-yer h2{
    height: 22px;
    font-size: 16px;
    font-family: PingFangSC, PingFangSC-Semibold;
    font-weight: 600;
    color: #366cb3;
    padding: 11px 0 11px 20px;
    margin: 0;
    line-height: 22px;
}
.u-day,.data{
  margin-bottom: 13px;
  display: flex;
}
.u-day span{
  font-size: 14px;
  text-align: center;
  flex: 1;
  color: #366cb3;
}
.data span{
  color: #444444;
  font-size: 14px;
  text-align: center;
  line-height: 38px;
  flex: 1;
}
.data span.active{
  width: 38px;
  height: 38px;
  display: block;
  float: left;
  background: #366cb3;
  border-radius: 10px;
}
.u-pro{
  margin-bottom: 30px;
}
.u-pro div{
  width: 100%;
  height: 30px;
  line-height: 30px;
  margin-bottom: 30px;
}
.u-pro div span{
  font-size: 12px;
  font-weight: 400;
  color: #999999;
  float: left;
  margin: 0 13px 0 17px;
}
.u-pro div i{
  width: 301px;
  height: 1px;
  margin-top: 15px;
  float: left;
  background: #f1eff2;
}
</style>