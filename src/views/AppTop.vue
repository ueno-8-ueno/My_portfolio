<script setup lang="ts">
import Skills from '../components/Skills.vue';
import Profile from '../components/Profile.vue';
import Works from '../components/Works.vue';
import Footer from '../components/Footer.vue';
</script>

<template>
  <main class="main-bg">
    <div class="main-visual">
      <div class="main-visual-content">
        <p class="main-visual-text">ペンギンが大好きなエンジニアのポートフォリオ</p>
      </div>
    </div>

    <div class="section-box">
      <h1 class="section-title">Profile</h1>
      <Profile></Profile>
    </div>

    <div class="section-box">
      <h2 class="section-title">Skills</h2>
      <Skills></Skills>
    </div>

    <div class="section-box">
      <h2 class="section-title">Works</h2>
      <Works></Works>
    </div>

  </main>
  <Footer></Footer>
</template>

<style>
.main-visual{
  width: 100%;
  height: 300px;
  background-image: url("/images/penguin.png");
  background-size: cover;
  background-position: center;
}
.main-visual-content{
  width: 40%;
  height: 300px;
  background-color: rgba(0,0,0,0.5);
  text-align: center;
  padding-top: 105px;
}
.main-visual-text{
  color: white;
  font-family: serif;
}

.main-bg{
  background-color:rgb(236, 255, 249) ;
}

.section-box{
  margin-top: 80px;
}

.section-title{
  border-bottom: 8px solid #dbdbdb;
  text-align: center;
  line-height: 0.6;
  font-family:"Bradley Hand", Courier;
  font-size: 60px;
  margin: 10px auto;
  width: 40%;
}
</style>