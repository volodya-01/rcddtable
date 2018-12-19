<template>
  <div class="hello">
    <table cellspacing="0">
    <thead>
      <tr>
        <td>水厂名称</td>
        <td>出厂压力</td>
        <td>出厂流量</td>
        <td>清水池水位</td>
        <td class="fonttext"> 1#</td>
        <td class="fonttext">2#</td>
        <td class="fonttext">3#</td>
        <td class="fonttext">4#</td>
        <td class="fonttext">5#</td>
        <td class="fonttext">6#</td>
        <td class="fonttext">7#</td>
        <td class="fonttext">8#</td>
      </tr>
    </thead>
    <tbody id="tby">
      <tr v-for="(item,index) in stu" :key="index.id">
        <td><span> {{item.name}}</span></td>
        <td><span>{{item.p}}</span></td>
        <td><span>{{item.w}}</span> </td>
        <td><span>{{item.q}}</span> </td>
        <td><span class="box" :class="item.t1==0? 'one' :(item.t1==1? 'two' :(item.t1==2? 'three' :''))" >{{item.r1}}</span></td>
        <td><span class="box" :class="item.t2==0? 'one' :(item.t2==1? 'two' :(item.t2==2? 'three' :''))">{{item.r2}}</span></td>
        <td><span class="box" :class="item.t3==0? 'one' :(item.t3==1? 'two' :(item.t3==2? 'three' :''))" >{{item.r3}}</span></td>
        <td><span class="box" :class="item.t4==0? 'one' :(item.t4==1? 'two' :(item.t4==2? 'three' :''))">{{item.r4}}</span></td>
        <td><span class="box" :class="item.t5==0? 'one' :(item.t5==1? 'two' :(item.t5==2? 'three' :''))">{{item.r5}}</span></td>
        <td><span class="box" :class="item.t6==0? 'one' :(item.t6==1? 'two' :(item.t6==2? 'three' :''))">{{item.r6}}</span></td>
        <td><span class="box" :class="item.t7==0? 'one' :(item.t7==1? 'two' :(item.t7==2? 'three' :''))">{{item.r7}}</span></td>
        <td><span class="box" :class="item.t8==0? 'one' :(item.t8==1? 'two' :(item.t8==2? 'three' :''))">{{item.r8}}</span></td>
      </tr>
    </tbody>
  </table>
  <div class="table">
    <Table/>
     <!-- <Table2/> -->
  </div>
  </div>
</template>
<script>
import Table from "@/components/table";
/* import Table2 from "@/components/table2"; */
export default {
  name: "HelloWorld",
  components: {
    Table,
    /* Table2 */
  },
  data() {
    return {
      stu: [
        {
          t1: 2,
          t2: 0,
          t3: 1,
          t4: 0,
          t5: 1,
          /*   t6:1,
            t7:0,
            t8:1, */
          name: "笔架山水厂",
          p: 20,
          w: 88,
          q: 4656,
          r1: "",
          r2: 2133,
          r3: null,
          r4: 3332,
          r5: 1234
          /*  r6: 2133,
             r7: 1446,
             r8: 3332, */
        },
        {
          t1:"1",
          t2: 1,
          t3: 0,
          t4: 2,
          t5: 0,
          /*   t6:1,
            t7:0,
            t8:1, */
          name: "大涌北水厂",
          p: 45,
          w: 98,
          q: 4656,
          r1: 1234,
          r2: 2133,
          r3: 1446,
          /* r4: 3332, */
          r5: 1234
          /*  r6: 2133,
             r7: 1446,
             r8: 3332, */
        },
        {
          t1: 0,
          t2: 2,
          t3: 1,
          t4: 0,
          t5: 1,
          t6: 1,
          t7: 1,
          t8: 1,
          name: "大涌南水厂",
          p: 20,
          w: 66,
          q: 4656,
          r1: 1234,
          /*  r2: 2133, */
          r3: 1446,
          r4: 3332,
          r5: 1234,
          r6: 2133,
          r7: 1446,
          r8: 3332
        },
        {
          t1: 0,
          t2: 1,
          t3: 1,
          t4: 0,
          t5: 2,
          t6: 2,
          t7: 0,
          t8: 1,
          name: "东湖水厂",
          p: 20,
          w: 88,
          q: 4656,
          r1: 1234,
          r2: 2133,
          r3: 1446,
          r4: 3332,
          /* r5: 1234,
            r6: 2133, */
          r7: 1446,
          r8: 3332
        },
        {
          t1: 1,
          t2: 1,
          t3: 0,
          t4: 0,
          t5: 1,
          t6: 2,
          t7: 2,
          t8: 2,
          name: "梅林",
          p: 45,
          w: 98,
          q: 4656,
          r1: 1234,
          r2: 2133,
          r3: 1446,
          r4: 3332,
          r5: 1234
          /* r6: 2133,
            r7: 1446,
            r8: 3332 */
        },
        {
          t1: 1,
          t2: 1,
          t3: 1,
          t4: 0,
          t5: 0,
          t6: 1,
          /*  t7:0,
            t8:1, */
          name: "南山水厂",
          p: 20,
          w: 66,
          q: 4656,
          r1: 1234,
          r2: 2133,
          r3: 1446,
          r4: 3332,
          r5: 1234,
          r6: 2133
          /*  r7: 1446,
             r8: 3332, */
        }
      ]
    };
  }
};
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
  .hello{
    width: 1260px;
   /*  background-image: url('../assets/img/深水_日常调度_背景_17.png'); */
  }
table,
tr,
td,
th {
  padding: 0;
  margin: 0;
}
table {
  width:65%;
  background: #56667d;
  /* opacity: 0.6; */
   background-image: url('../assets/img/深水_日常调度_背景_17.png');
}
table tr {
  line-height: 30px;
}
table th,
table td {
  font-size: 10px;
  text-align: start;
  padding-left: 10px;
  color: #fff;

}
tbody tr:nth-child(odd) {
  background: #101927;
}
.box {
  display: inline-block;
  width: 42px;
  height: 15px;
  line-height: 14px;
  text-align: center;
}
.te {
  background-color: aqua;
}
.fonttext {
  text-align: center;
  padding-right: 6px;
}
.one {
  padding: 3px 6px;
  margin-top: 5px;
  margin-bottom: -5px;
  border: 1px #1a212b solid;
  border-radius: 5px;
  background-color: #abe931;
}
.two {
  padding: 3px 6px;
  margin-top: 5px;
  margin-bottom: -5px;
  border: 1px #1a212b solid;
  border-radius: 5px;
  background-color: red;
  /*  background-image: url('../assets/img/斜纹_红.png'); */
}
.three {
  background-color: #56667d;
  padding: 3px 6px;
  margin-top: 5px;
  margin-bottom: -5px;
  border: 1px #1a212b solid;
  border-radius: 5px;
}
.table {
  margin-top: 30px;
}
</style>
