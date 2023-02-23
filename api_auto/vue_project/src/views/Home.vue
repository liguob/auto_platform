<template>
  <div class="home" style="height:100%">
    <el-container style="height:100%">
      <el-aside style="width: 200px;background: white">
        <v_menu></v_menu>
      </el-aside>
      <el-container>
        <el-header style="padding: 0 5px">
          <el-row style="margin-top: 10px;">
            <el-col :span="6" style="background-color: #42b983">
              <div class="grid-content" style="background-color: #ffe578">
                <el-button round style="float: right">实时</el-button>
              </div>

            </el-col>
            <el-col :span="6"><div class="grid-content bg-purple-dark">测试2</div></el-col>
            <el-col :span="6"><div class="grid-content bg-purple-dark">测试3</div></el-col>
            <el-col :span="6"><div class="grid-content bg-purple-dark">测试4</div></el-col>
          </el-row>
        </el-header>
        <el-main style="background: linear-gradient(to right, white, #B7CAD8, #5E7DB3);padding: 0 5px">
          <div>
            <el-card class="box-card" style="width: 20%; margin-right: 1px;float: left">
              <div slot="header" class="clearfix">
                <span>统计信息</span>
                <el-button style="float: right; padding: 3px 0" type="text">查看详情</el-button>
              </div>
              <div style="margin-bottom: 10%">项目总数: 10</div>
              <div style="margin-bottom: 10%">用例总数: 100</div>
              <div style="margin-bottom: 6px">接口总数: 500</div>
            </el-card>
            <el-card class="box-card" style="width: calc(80% - 5px);float: left">
              <div slot="header" class="clearfix">
                <span>上次用例执行情况</span>
                <el-button style="float: right; padding: 3px 0" type="text">查看详情</el-button>
              </div>
              <div>接口通过率</div>
              <el-progress :text-inside="true" :stroke-width="14" :percentage="100" status="success" style="margin-bottom: 10px"></el-progress>
              <div>用例成功率</div>
              <el-progress :text-inside="true" :stroke-width="14" :percentage="80" status="warning" style="margin-bottom: 10px"></el-progress>
              <div>执行失败</div>
              <el-progress :text-inside="true" :stroke-width="14" :percentage="50" status="exception"></el-progress>
            </el-card>
          </div>
          <div>
            <el-card class="box-card" style="float: left;margin-top: 1px;width: 60%">
            <div slot="header" class="clearfix">
                <span>个人贡献</span>
                <el-button style="float: right; padding: 3px 0" type="text">查看详情</el-button>
            </div>
            <table class="table_process">
              <thead class="header">
              <tr>
                <th>项目占比</th>
                <th>接口占比</th>
                <th>用例占比</th>
                <th>监控占比</th>
              </tr>
              </thead>
              <tbody class="table_data">
                <tr>
                  <td><el-progress type="circle" :percentage="25"></el-progress></td>
                  <td><el-progress type="circle" :percentage="100" status="success"></el-progress></td>
                  <td><el-progress type="circle" :percentage="10" status="exception"></el-progress></td>
                  <td><el-progress type="circle" :percentage="25"></el-progress></td>
                </tr>
              </tbody>
            </table>
          </el-card>
            <el-card class="box-card" style="width: calc(40% - 5px); margin-top: 1px;float: left">
              <div slot="header" class="clearfix">
                <span>待处理消息</span>
                <el-button style="float: right; padding: 3px 0" type="text">查看详情</el-button>
              </div>
              <div class="message">
                <div v-for="o in 5" :key="o" style="text-align: left; margin: 10px">
                  {{'消息 ' + o }}
                </div>
              </div>
            </el-card>
          </div>
        </el-main>
        <el-footer style="height: 150px; background: linear-gradient(to right, white, #B7CAD8, #5E7DB3)">
          <el-card class="box-card" style="width: calc(100% - 15px);height: 120px;background: linear-gradient(to right, white, #B7CAD8, #5E7DB3)">
            <div v-for="o in 4" :key="o" style="text-align: left; margin: 5px">
              {{'通知信息 ' + o }}
            </div>
          </el-card>
        </el-footer>
      </el-container>
    </el-container>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import v_menu from "@/components/menu.vue";
export default {
  name: 'home',
  components: {
    v_menu
  }
}
</script>
<style>
.el-header, .el-footer {
  text-align: center;
}
.el-col{
  border-radius: 4px;
}

.el-aside {
  background-color: #D3DCE6;
  color: #333;
  /*text-align: center;*/
}

.el-main {
  background-color: #E9EEF3;
  color: #333;
}

body > .el-container {
  margin-bottom: 40px;
}

.el-container:nth-child(5) .el-aside,
.el-container:nth-child(6) .el-aside {
  line-height: 260px;
}

.el-container:nth-child(7) .el-aside {
  line-height: 320px;
}

.text {
  font-size: 14px;
}

.item {
  margin-bottom: 15px;
}

.clearfix:before,
.clearfix:after {
  display: table;
  content: "";
}

.clearfix:after {
  clear: both
}

.box-card {
  height: 270px;
}

/*.el-card span {*/
/*  font-size: 15px;*/
/*}*/

.el-card div{
  font-size: x-small;
}
.el-card span{
  font-size: large;
}
th,td{
  text-align: center;
  width: 15%;
}
</style>
