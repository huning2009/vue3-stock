<template>
  <Row type="flex" justify="center" style="padding: 1rem 20rem;background-color: #333;">
    <i-col :xs="5" :sm="5" :lg="4">
      <div class="f-title">关于</div>
      <ul>
        <li>
          <router-link to="/help/about" target="_blank">关于我们</router-link>
        </li>
        <li>
          <router-link to="/help/companystate" target="_blank">公司声明</router-link>
        </li>
      </ul>
    </i-col>
    <i-col :xs="5" :sm="5" :lg="4">
      <div class="f-title">帮助中心</div>
      <ul>
        <li>
          <router-link to="/help/question" target="_blank">常见问题</router-link>
        </li>
        <li>
          <router-link to="/help/guide" target="_blank">新手指南</router-link>
        </li>
      </ul>
    </i-col>
    <i-col :xs="14" :sm="14" :lg="4">
      <Row type="flex" justify="start">
        <i-col span="10">
          <div class="f-title">关注我们</div>
          <img style="width: 5rem;height: 5rem" src="../../assets/img/public.jpg" alt="千投量化公众号" />
          <p style="color: #fff">微信公众号</p>
        </i-col>
        <i-col span="10">
          <div class="f-title">加入我们</div>
          <img style="width: 5rem;height: 5rem" src="../../assets/img/hitqtqq.jpg" alt="千投量化QQ群" />
          <p style="color: #fff;">QQ群号(643033887)</p>
        </i-col>
      </Row>
    </i-col>
    <i-col
      :xs="24"
      :sm="24"
      :lg="16"
      style="border-top: 1px solid #fff;color:#797a8d;font-size: 0.875rem;padding:.5rem 0;margin-top: 1rem"
    >
      <span>&copy;2016-2017 **************.com 版权所有</span>
      <a href="https://baidu.com" target="_blank">鲁************号</a>
      <span style="float:right;color: #fff">*****************有限公司</span>
    </i-col>
  </Row>
</template>
<script>
// import {BASE_API_URL} from '../api/api'
export default {
  data() {
    return {
      //        publicSrc: BASE_API_URL + '/img/public.jpg',
      //        qqSrc: BASE_API_URL + '/img/hitqtqq.jpg'
    };
  }
};
</script>
<style rel="stylesheet" scoped>
.f-title {
  font-size: 1rem;
  color: #fff;
  margin-bottom: 0.5rem;
}

a {
  font-size: 0.875rem;
  color: #797a8d;
}

a:hover {
  color: #fff;
}

ul li {
  margin-bottom: 0.5rem;
}
</style>
