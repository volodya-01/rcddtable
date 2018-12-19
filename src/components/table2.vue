<template>
    <div class="dormitoryData">
      <el-table
        ref="dormitoryTable"
        :data="dormitory"
        tooltip-effect="dark"
        stripe
        style="width: 100%">
        <el-table-column type="selection" width="45"></el-table-column>
        <el-table-column label="序号"  type="index" width="65"></el-table-column>
        <el-table-column label="人物" prop="people">
          <template slot-scope="scope">
            <div :class="scope.row.isEdit==0? 'one' :'two'"> {{ scope.row.people }}</div>
          </template>
        </el-table-column>
        <el-table-column label="关系" prop="relationship">
          <template slot-scope="scope">
            <div :class="scope.row.isEdit==0? 'one' :'two'"> {{ scope.row.relationship }}</div>
          </template>
        </el-table-column>
        <el-table-column label="初见" prop="meet">
          <template slot-scope="scope">
            <div :class="scope.row.isEdit==0? 'one' :'two'"> {{ scope.row.meet }}</div>
          </template>
        </el-table-column>
        <el-table-column label="地点" prop="place">
          <template slot-scope="scope">
            <div :class="scope.row.isEdit==0? 'one' :'two'"> {{ scope.row.place }}</div>
          </template>
        </el-table-column>
        <el-table-column label="昵称" prop="execg">
          <template slot-scope="scope">
            <div :class="scope.row.isEdit==0? 'one' :'two'"> {{ scope.row.execg }}</div>
          </template>
        </el-table-column>
        <el-table-column label="认识年限" prop="year">
          <template slot-scope="scope">
            <div :class="scope.row.isEdit==0? 'one' :'two'"> {{ scope.row.year }}</div>
          </template>
        </el-table-column>
        <el-table-column label="成名之作" prop="works">
          <template slot-scope="scope">
            <div :class="scope.row.isEdit==0? 'one' :'two'"> {{ scope.row.works }}</div>
          </template>
        </el-table-column>
      </el-table>
    </div>
</template>
<script>
 
  export default {
   name:"Table2",
    data () {
      return {
        dormitory: [{
          people: '雷森',
          relationship: '大学室友',
          meet: '2010-09-02',
          place: '图书馆',
          execg: '胖子',
          year: '8年',
          works: '海阔天空',
          isEdit: '1'
        }, {
          people: '刘利伟',
          relationship: '大学室友',
          meet: '2010-09-02',
          place: '5#633',
          execg: '老大',
          year: '8年',
          works: '勇气',
          isEdit: '1'
        }, {
          people: '李金龙',
          relationship: '大学室友',
          meet: '2010-09-02',
          place: '5#633',
          execg: '二哥',
          year: '8年',
          works: '遇见',
          isEdit: '1'
        }, {
          people: '马康',
          relationship: '大学室友',
          meet: '2010-09-02',
          place: '餐饮大厦',
          execg: '康哥',
          year: '8年',
          works: '不再联系',
          isEdit: '1'
        }, {
          people: '牛光卫',
          relationship: '大学室友',
          meet: '2010-09-02',
          place: '图书馆',
          execg: '牛牛娃',
          year: '8年',
          works: '断点',
          isEdit: '1'
        }, {
          people: '陆兆攀',
          relationship: '大学室友',
          meet: '1991-07-27',
          place: '百浪',
          execg: '帅哥',
          year: '27年',
          works: '不再犹豫',
          isEdit: '0'
        }, {
          people: '小甜',
          relationship: '亲密的人',
          meet: '2016-10-05',
          place: '小寨',
          execg: '甜甜圈',
          year: '2年',
          works: 'Forever Love',
          isEdit: '0'
        }]
      }
    }
  }
</script>
 
<style>
.one {
      background: #ff1493;
    }
    .two{
        background-color: aqua;
    }
</style>