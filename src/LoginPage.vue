<script setup>
import { ref } from 'vue'
const username = ref('') // 用户名
</script>
<template>
  <div id="container">
    <div id="panel-background"></div>
    <div id="panel-title" class="text-common-style">系统登录</div>
    <div id="panel-username-input">
      <span class="input-label text-common-style">用户名</span>
      <input class="input-content" type="text" name="username" v-model="username" />
      <div class="close-button">
        <img class="close-button-img" src="/src/assets/img/close.png" />
      </div>
    </div>
  </div>
</template>

<style scoped>
/* 根容器，全屏，背景图是本地图片，保持宽高比并至少覆盖父容器空间 */
#container {
  width: 100%;
  height: 100%;
  position: relative;
  background-image: url('/src/assets/img/login_bg.png');
  background-size: cover;
}
/* 登录框，居中，因为施加了遮罩式模糊，所以与它的内容是平行的而非上下级的，避免影响内容 */
#panel-background {
  width: 60%;
  height: 60%;
  border: 1px solid white;
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  backdrop-filter: blur(3px); /* 遮罩式模糊效果 */
}
/* 文字通用样式 */
.text-common-style {
  letter-spacing: 0.5rem;
  color: white;
}
/* 登录框标题 */
#panel-title {
  position: absolute;
  top: 25%;
  left: 50%;
  transform: translateX(-50%);
  font-size: 2rem;
}
/* 输入项-用户名 */
#panel-username-input {
  position: absolute;
  top: 40%;
  left: 50%;
  transform: translateX(-50%);
}
/* 输入项标题 */
.input-label {
}
/* 输入项内容 */
.input-content {
  background-color: transparent;
  border: 1px white solid;
  border-radius: 5px;
  outline: none;
  color: white;
  padding: 10px;
}
/* 输入项内容（有焦点）*/
.input-content:focus {
  background-color: rgba(255, 255, 255, 0.15);
}
/* 删除按钮 */
.close-button {
  position: absolute;
  top: 50%;
  right: 10px;
  transform: translateY(-50%);
  width: 20px;
  height: 20px;
  border: 1px white solid;
}
/* 删除按钮中的图片 */
.close-button-img {
  width: 10px;
  height: 10px;
  top: 50%;
  left: 50%;
  position: absolute;
  transform: translate(-50%, -50%);
  filter: invert(100%); /* 反转颜色，黑色变白色*/
}
</style>
