<template>
  <div>
    <Carousel loop v-model="state.value" :autoplay="true" :autoplay-speed="10000">
      <CarouselItem>
        <Row class="layout-banner" type="flex" justify="center">
          <i-col
            span="24"
            style="text-align: center;font-size: 2rem;color: #FFFFFF;margin-bottom: 10rem"
          >
            <span style="font-family: sans-serif;font-size: 3rem;">千投量化平台</span>
            <br />
            <span style="font-size: 1.5rem">专注打造科学量化模型，让更多人享受量化果实</span>
          </i-col>
          <i-col span="5" style="text-align: center">
            <Button
              type="success"
              size="large"
              style="width: 10rem;font-size: 1.2rem"
              @click="createModel"
            >创建模型</Button>
          </i-col>
          <i-col span="5" style="text-align: center">
            <Button
              type="primary"
              size="large"
              style="width: 10rem;font-size: 1.2rem"
              @click="getMyModels"
            >我的模型</Button>
          </i-col>
        </Row>
      </CarouselItem>
      <CarouselItem>
        <Row class="layout-banner2" type="flex" justify="center">
          <i-col
            span="24"
            style="text-align: center;font-size: 2rem;color: #FFFFFF;margin-bottom: 10rem"
          >
            <span style="font-family: sans-serif;font-size: 3rem;">回测卡</span>
            <br />
            <span style="font-size: 1.5rem">单次回测不限量，智能回测量更多</span>
          </i-col>
          <i-col span="5" style="text-align: center">
            <Button
              type="primary"
              size="large"
              style="width: 10rem;font-size: 1.2rem;background: transparent;border: 1px solid #ffffff"
              @click="guide"
            >了解详情</Button>
          </i-col>
        </Row>
      </CarouselItem>
      <CarouselItem>
        <Row class="layout-banner3" type="flex" justify="center">
          <i-col
            span="24"
            style="text-align: center;font-size: 2rem;color: #FFFFFF;margin-bottom: 10rem"
          >
            <span style="font-family: sans-serif;font-size: 3rem;">注册福利</span>
            <br />
            <span style="font-size: 1.5rem">注册享好礼，智能回测天天送</span>
          </i-col>
          <i-col span="5" style="text-align: center">
            <Button
              type="error"
              size="large"
              style="width: 10rem;font-size: 1.2rem"
              @click="createModel"
            >智能回测</Button>
          </i-col>
          <i-col span="5" style="text-align: center">
            <Button size="large" style="width: 10rem;font-size: 1.2rem" @click="getMore">查看更多</Button>
          </i-col>
        </Row>
      </CarouselItem>
    </Carousel>
  </div>
</template>
<script>
import { reactive } from "@vue/composition-api";
export default {
  setup() {
    const state = reactive({
      value: 0
    });
    const createModel = () => {
      //            创建模型
      // if (this.$store.state.user.isLogin) {
      //   this.$router.push("/model");
      // } else {
      //   this.$router.push("/login");
      // }
    };
    const getMyModels = () => {
      // if (this.$store.state.user.isLogin) {
      //   this.$router.push("/model/myModel");
      // } else {
      //   this.$router.push("/login");
      // }
    };
    const guide = () => {
      this.$router.push("/help/guide");
    };
    //      查看更多智能回测
    const getMore = () => {
      this.$router.push("/help/geneticdoc");
    };
    return {
      state,
      createModel,
      getMyModels,
      guide,
      getMore
    };
  }
};
</script>
<style rel="stylesheet" scoped>
.layout-banner {
  background: url("../../assets/img/banner.png");
  background-repeat: no-repeat;
  min-height: 35rem;
  padding: 5rem 0;
}

.layout-banner2 {
  background-repeat: no-repeat;
  min-height: 35rem;
  padding: 5rem 0;
  background: url("../../assets/img/banner2.png");
}
.layout-banner3 {
  background-repeat: no-repeat;
  min-height: 35rem;
  padding: 5rem 0;
  background: url("../../assets/img/banner3.png");
}

.slogan {
  width: 30rem;
  margin: auto;
  font-size: 3rem;
  color: #ffffff;
}

.slogan p {
  text-align: center;
}

.description {
  width: 30rem;
  margin: auto;
}

hr {
  border: 5px solid;
  width: 5rem;
  margin: auto;
}
</style>
