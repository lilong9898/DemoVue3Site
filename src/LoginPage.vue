<template>
  <div id="container">
    <div id="panel-background"></div>
    <div id="panel-content">系统登录</div>
  </div>
</template>

<style scoped>
/* 根容器，全屏，背景图是本地图片，保持宽高比并至少覆盖父容器空间 */
#container {
  width: 100%;
  height: 100%;
  position: relative;
  background-image: url("/src/assets/img/login_bg.png");
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
/* 登录框标题 */
#panel-content {
  position: absolute;
  top: 25%;
  left: 50%;
  transform: translateX(-50%);
  letter-spacing: 1rem;
  font-size: 2rem;
  color: white;
}
</style>
