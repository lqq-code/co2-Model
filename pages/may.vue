<template>
  <div class="may_contanier">
    <!-- <div id="may-item">
      <img src="../assets/images/may1.png" class="img-may1" />
      <img src="../assets/images/may1.png" class="img-may1" />
    </div> -->
    <div class="may-item">
      <el-image :src="require('@/assets/images/may1.png')" class="img-may "></el-image>
      <el-image :src="require('@/assets/images/may2.png')" class="img-may may-right"> </el-image>
    </div>
    <div class="may-item">
      <el-image :src="require('@/assets/images/may3.png')" class="img-may"> </el-image>
      <el-image :src="require('@/assets/images/may4.png')" class="img-may may-right"> </el-image>
    </div>
    <div class="may-item">
      <el-image :src="require('@/assets/images/may5.png')" class="img-may"> </el-image>
      <el-image :src="require('@/assets/images/may6.png')" class="img-may may-right"> </el-image>
    </div>
    <div class="may-item">
      <el-image :src="require('@/assets/images/may7.png')" class="img-may"> </el-image>
      <div class="img-may may-right"></div>
    </div>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      drawer: false
    }
  },
  computed: {},
  methods: {}
}
</script>
<style scope>
.may_contanier {
  width: 100%;
  height: 100%;
}
.may-item {
  display: flex;
  margin-top: 60px;
}
.img-may {
  width: 50%;
  margin-left: 4%;
}
.may-right {
  margin-right: 4%;
}
</style>
