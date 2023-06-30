<script setup lang="ts">
</script>

<template>
    <v-container>
        <div class="works-area">

            <!--成果物1-->
            <v-card class="work overflow-y-auto">
                <v-card-text>関数電卓</v-card-text>
                <v-divider class="mx-4 mb-5"></v-divider>
                    <v-row>
                        <img src="../assets/work1.png" width="150" class="work-img">
                        <ul class="work-text">
                            <li>[技術] JavaScript, HTML, CSS</li>
                            <li>初めてまともに作成した成果物</li>
                            <li>四則演算の他に様々な計算が可能</li>
                            <li><a href="https://ueno-8-ueno.github.io/scientific_calculator/">こちらからサイトに飛べます</a></li>
                        </ul>
                    </v-row>
            </v-card>
            
            <!--成果物2-->
            <v-card class="work overflow-y-auto">
                <v-card-text>Shelfie</v-card-text>
                <v-divider class="mx-4 mb-5"></v-divider>
                    <v-row>
                        <img src="../assets/work2.png" width="150" class="work-img">
                        <ul class="work-text">
                            <li>[技術] Vue.js, FastAPI, etc...</li>
                            <li>KC3Hack 2023で開発したWebアプリ</li>
                            <li>書籍管理が可能</li>
                            <li>主にフロントエンド(Vue.js)を担当した</li>
                        </ul>
                    </v-row>
            </v-card>

            <!--成果物3-->
            <v-card class="work overflow-y-auto">
                <v-card-text>ポートフォリオ</v-card-text>
                <v-divider class="mx-4 mb-5"></v-divider>
                    <v-row>
                        <img src="../assets/work3.png" width="150" class="work-img">
                        <ul class="work-text">
                            <li>[技術] Vue.js, Vuetify</li>
                            <li>本ポートフォリオサイト</li>
                            <li>github-pagesを用いたのでデプロイが楽</li>
                            <li>UIデザインに力を入れた(頑張った)</li>
                        </ul>
                    </v-row>
            </v-card>

        </div>
    </v-container>
</template>

<style>
.works-area{
    background-color: rgba(0,0,0,0.1);
    width: 100%;
    padding: 20px;
    margin-bottom: 50px;
    border-radius: 5px;
}

.work{
    width: 70%;
    padding: 10px;
    margin-right: 5%;
    margin-bottom: 20px;
}
.work:nth-child(even){
    margin-right: 0%;
    margin-left: auto;
}

.work-img{
    margin: 5px;
    padding: 10px;
}

.work-text{
    margin-left: 10px;
    font-family: serif;
}

@media(max-width:600px){
    .works-area{
        width: 100%;
    }
    .work{
        width: 100%;
        margin: 20px auto;
    }

    .work-img{
        margin: 0 auto;
    }

    .work-text{
        margin: 10px auto;
    }
}
</style>