<template>
  <div>
    <div class="box">
      <div class="text">
        <!-- 头像区域 -->
        <img class="avatar"
             src="../assets/avatar.jpg"
             alt="" />
        <!-- 介绍区域 -->
        <h1>阿贤哦</h1>
        <h2>👨‍🎨 👨‍💻 🙋‍♂️</h2>
        <p>前端实习生 / 热爱生活 / 游戏小菜鸡</p>
        <div class="line"></div>
        <h3>“总有比游戏更有意义的东西出现”</h3>
      </div>
      <!-- 盒子区域 -->
      <div class="cards">
        <a-card hoverable
                class="aCard cards1"
                @click="goBlog">
          <div class="cardText">
            <h2>博客 Blog</h2> <br />
            <p class="fontSite">✏️ 随便写写</p>
          </div>
          <span class="icon">
            <!-- 📖 -->
            <a-icon type="book" />
          </span>
        </a-card>
        <div class="cardauto">
          <router-link to="/project">
            <a-card hoverable
                    class="aCard cards2">
              <div class="cardText">
                <h2 style="color: black;">项目 Project</h2> <br />
                <p class="fontSite"
                   style="color: black;">📦 发现新大陆</p>
              </div>
              <span class="icon">
                <!-- 🗃️ -->
                <a-icon type="dropbox"
                        style="color: black;" />
              </span>
            </a-card>
          </router-link>
        </div>
        <div class="cardauto">
          <router-link to="/resume">
            <a-card hoverable
                    class="aCard cards3">
              <div class="cardText">
                <h2 style="color: black;">简历 Resume</h2> <br />
                <p class="fontSite"
                   style="color: black">📑 我的简历</p>
              </div>
              <span class="icon">
                <!-- 📄 -->
                <a-icon type="profile"
                        style="color: black" />
              </span>
            </a-card>
          </router-link>
        </div>
      </div>
    </div>
    <footer>
      <p>©2021 | <a href="https://beian.miit.gov.cn/"
           target="_block">蒙ICP备20002340号-2</a></p>
      <p>@Axian</p>
    </footer>
  </div>

</template>

<script>
export default {
  methods: {
    goBlog () {
      this.$router.push('/blog')
    }
  }
}
</script>

<style long="scss" scoped>
.box {
  /* position: relative;
  left: 50%; */
  /* width: 440px;
  margin: 0 auto; */
  margin: 80px 0;
  padding-top: 10px;
}
.avatar {
  margin: 0 auto;
  display: block;
  /* margin-left: 50%;
  transform: translate(-50%, 0); */
  width: 120px;
  border-radius: 50%;
}

.aCard {
  position: relative;
  display: block;
  margin: 40px auto;
  width: 380px;
  height: 120px;
  border-radius: 20px;
  color: white;
}
.aCard .cardText {
  width: 200px;
}
.aCard p {
  display: inline-block;
  font-size: 16px;
}
.aCard h2 {
  display: inline-block;
}

.aCard .icon {
  position: absolute;
  top: 37px;
  left: 295px;
  font-size: 35px;
}
.cards1 {
  background-color: #24292e;
}
.cards2 {
  background-color: #2f93f7;
}
.cards3 {
  background-color: #50d850;
}
h2 {
  color: white;
}
.text {
  margin: 0 auto;
  /* width: 400px;
  height: 400px; */
  /* background-color: teal; */
}
.text h1 {
  font-size: 20px;
  margin: 15px;
  text-align: center;
  font-weight: 700 !important;
}
.text h2 {
  font-size: 20px;
  margin-top: 0.219074rem;
  text-align: center;
}
.text p {
  margin: 30px;
  text-align: center;
  font-size: 17px;
  font-weight: 500;
}
.text .line {
  margin: 60px auto;
  width: 100px;
  border: 2px solid #0070f3;
}
.text h3 {
  text-align: center;
  font-size: 18px;
  font-weight: 700;
}
footer {
  height: 100px;
  padding-top: 20px;
  margin-bottom: 20px;
  /* background-color: white; */
  color: black;
  font-size: 15px;
}

footer p a {
  color: black;
}

footer p {
  margin: 0;
  text-align: center;
  color: black;
}
</style>
