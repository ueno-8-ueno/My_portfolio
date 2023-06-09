<script setup lang="ts">
import {ref} from "vue";
import type { Language, Framework } from "@/interfaces";

/* 言語エリア(ここに追加) */
const languageListInit = new Map<number, Language>();
languageListInit.set(1, {
    level: 3,
    name: "JavaScript",
    about: "2022年4月にハローワールド. 主にフロントエンドで使用している.",
    level_color: "level-3",
    dialog: false,
});

languageListInit.set(2, {
    level: 2,
    name: "TypeScript",
    about: "2023年2月にハローワールド. 主にVue.jsで使用している.",
    level_color: "level-2",
    dialog: false,
});

languageListInit.set(3, {
    level: 3,
    name: "Java",
    about: "2022年4月にハローワールド. 大学の実習でオブジェクト指向を学んだ.",
    level_color: "level-3",
    dialog: false,
});

languageListInit.set(4, {
    level: 1,
    name: "Python",
    about: "2020年4月にハローワールド. 高校2年生からほとんど触っていない.",
    level_color: "level-1",
    dialog: false,
});

languageListInit.set(5, {
    level: 3,
    name: "Ruby",
    about: "2023年5月にハローワールド. paizaラーニングにて学んだ.",
    level_color: "level-3",
    dialog: false,
});

const languageList = ref(languageListInit);



/* フレームワークエリア(ここに追加) */
const frameworkListInit = new Map<number, Framework>();

frameworkListInit.set(1, {
    level: 4,
    name: "Vue.js",
    about: "2023年2月にハローワールド. フロントエンドで使用している. ハッカソンイベントにて初めて使用した.",
    level_color: "level-4",
    dialog: false,
});

frameworkListInit.set(2, {
    level: 2,
    name: "Vuetify",
    about: "2023年2月にハローワールド. Vue.jsと共に学び始めたcssフレームワーク.",
    level_color: "level-2",
    dialog: false,
});

frameworkListInit.set(3, {
    level: 1,
    name: "FastAPI",
    about: "2023年2月にハローワールド. バックエンドで使用するが, ほとんど触っていない.",
    level_color: "level-1",
    dialog: false,
});

frameworkListInit.set(4, {
    level: 2,
    name: "Ruby on Rails",
    about: "2023年6月にハローワールド. 主にバックエンドで使用している.",
    level_color: "level-2",
    dialog: false,
});

const frameworkList = ref(frameworkListInit);
</script>

<template>
    <v-container>
        <v-card class="skills-level">
            <v-table class="skills-level-table">
                <thead>
                    <th class="level-1">Lv.1</th>
                    <th class="level-2">Lv.2</th>
                    <th class="level-3">Lv.3</th>
                    <th class="level-4">Lv.4</th>
                </thead>
                <tr>
                    <td>if, for文が扱えるレベル.<br>もしくはしばらく触っていない.</td>
                    <td>リファレンス本などがあれば利用できるレベル.</td>
                    <td>リファレンスをほとんど参照せずとも<br>任意の処理が記述できるレベル.</td>
                    <td>問題なく日常的に利用できるレベル.<br>成果物の作成経験がある.</td>
                </tr>
            </v-table>
        </v-card>

        <v-card class="languages">
            <p class="skills-kinds">Languages</p>
            <v-row dense>
                <v-col v-for="[id, languageItem] in languageList" :key="id">
                    <!--ここから-->
                    <img v-if="languageItem.name=='JavaScript'" src="../assets/JavaScript.png" height="80" width="80" @click="languageItem.dialog = true" class="hover_anim">
                    <img v-else-if="languageItem.name=='TypeScript'" src="../assets/TypeScript.png" height="80" width="80" @click="languageItem.dialog = true" class="hover_anim">
                    <img v-else-if="languageItem.name=='Java'" src="../assets/Java.png" height="80" width="60" @click="languageItem.dialog = true" class="hover_anim">
                    <img v-else-if="languageItem.name=='Python'" src="../assets/Python.png" height="80" width="80" @click="languageItem.dialog = true" class="hover_anim">
                    <img v-else-if="languageItem.name=='Ruby'" src="../assets/Ruby.png" height="80" width="80" @click="languageItem.dialog = true" class="hover_anim">
                    <!--ここまでを編集(画像)-->

                    <p>{{languageItem.name}}</p>
                    <p :class="languageItem.level_color">Lv.{{ languageItem.level }}</p>

                    <!--以下, ダイアログエリア-->
                    <v-dialog v-model="languageItem.dialog" max-width="500">
                        <v-card>
                        <v-row no-gutters>
                            <v-col cols="12">
                                <v-card color="#E0F2F1" elevation="5">
                                    <v-card-title class="dialig-title">
                                        <h2>{{ languageItem.name }}</h2>
                                    </v-card-title>
                                    <v-divider class="mx-4 mb-1"></v-divider>
                                    
                                    <div class="d-flex flex-no-wrap justify-space-between">
                                        <div class="me-auto">
                                            <v-card-text><h4>Lv.{{ languageItem.level }}</h4></v-card-text>
                                            <v-card-text>{{ languageItem.about }}</v-card-text>
                                        </div>
                                    </div>
                                </v-card>
                            </v-col>
                        </v-row>
                    </v-card>
                    </v-dialog>
                    <!--ダイアログ終了-->
                </v-col>
            </v-row>
        </v-card>

        <v-card class="frameworks">
            <p class="skills-kinds">Frameworks</p>
            <v-row dense>
                <v-col v-for="[id, frameworkItem] in frameworkList" :key="id">
                    <!--ここから-->
                    <img v-if="frameworkItem.name=='Vue.js'" src="../assets/Vue.png" height="80" width="80" @click="frameworkItem.dialog = true" class="hover_anim">
                    <img v-else-if="frameworkItem.name=='Vuetify'" src="../assets/Vuetify.png" height="80" width="80" @click="frameworkItem.dialog = true" class="hover_anim">
                    <img v-else-if="frameworkItem.name=='FastAPI'" src="../assets/FastAPI.svg" height="80" width="80" @click="frameworkItem.dialog = true" class="hover_anim">
                    <img v-else-if="frameworkItem.name=='Ruby on Rails'" src="../assets/Rails.png" height="80" width="100" @click="frameworkItem.dialog = true" class="hover_anim">
                    <!--ここまでを編集(画像)-->

                    <p>{{frameworkItem.name}}</p>
                    <p :class="frameworkItem.level_color">Lv.{{ frameworkItem.level }}</p>

                    <!--以下, ダイアログエリア-->
                    <v-dialog v-model="frameworkItem.dialog" max-width="500">
                        <v-card>
                        <v-row no-gutters>
                            <v-col cols="12">
                                <v-card color="#E0F2F1" elevation="5">
                                    <v-card-title class="dialig-title">
                                        <h2>{{ frameworkItem.name }}</h2>
                                    </v-card-title>
                                    <v-divider class="mx-4 mb-1"></v-divider>
                                    
                                    <div class="d-flex flex-no-wrap justify-space-between">
                                        <div class="me-auto">
                                            <v-card-text><h4>Lv.{{ frameworkItem.level }}</h4></v-card-text>
                                            <v-card-text>{{ frameworkItem.about }}</v-card-text>
                                        </div>
                                    </div>
                                </v-card>
                            </v-col>
                        </v-row>
                    </v-card>
                    </v-dialog>
                    <!--ダイアログ終了-->
                </v-col>
            </v-row>
        </v-card>
    </v-container>
</template>

<style>
.skills-title{
    font-size: 50px;
    background-color: rgb(104, 179, 255);
    width: 250px;
    text-align: center;
    border: 5px solid #12747b;
    border-radius: 10px;
    margin: 0 auto; /*中央揃え */
}
.skills-level{
    border-radius: 5px;
    width: 100%;
    margin: 0 auto;
}
.skills-level thead{
    background-color: #12747b;
    color: white;
}
.skills-level td{
    font-family: serif;
    padding: 3px;
    text-align: center;
}
.skills-level td:nth-child(odd){
    background: rgb(238, 238, 238);
}

.skills-kinds{
    font-size: 30px;
}

.languages{
    text-align: center;
    background-color: aliceblue;
    border-radius: 10px;
    margin: 20px;
}
.languages > p{
    text-decoration:underline;
    padding-bottom: 10px;
}
.frameworks{
    text-align: center;
    background-color: aliceblue;
    border-radius: 10px;
    margin: 20px;
}
.frameworks > p{
    text-decoration:underline;
    padding-bottom: 10px;
}
.level-1{
    color:white;
    background-color: #D4ADFC;
}
.level-2{
    color:white;
    background-color: #5C469C;
}
.level-3{
    color:white;
    background-color: #1D267D;
}
.level-4{
    color:white;
    background-color: #0C134F;
}

.hover_anim {
  transition-duration: 0.3s;
}

.hover_anim:hover {
  transform: scale(1.1);
}

.dialig-title{
    text-align: center;
}
</style>