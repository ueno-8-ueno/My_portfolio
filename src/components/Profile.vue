<template>
    <v-container>
        <div class="profile-area">
            <img
                src="/images/icon.png"
                height="250"
                width="250"
                class="icon"
            >
            <v-card class="introduction">
                <h2>Introduction</h2>
                <v-table>
                    <thead>
                        <th>属性</th>
                        <th>内容</th>
                    </thead>
                    <tr>
                        <td>名前:</td>
                        <td>上野 颯大 (うえの そうた)</td>
                    </tr>
                    <tr>
                        <td>大学:</td>
                        <td>近畿大学 情報学部 情報学科 2年</td>
                    </tr>
                    <tr>
                        <td>所属団体:</td>
                        <td>KINDAI Info-Tech HUB (役員就任:2023年〜)</td>
                    </tr>
                    <tr>
                        <td>趣味:</td>
                        <td>ギター, バンド練習, DTM, etc...</td>
                    </tr>
                    <tr>
                        <td>所有資格等:</td>
                        <td>基本情報技術者, 応用情報技術者, 第二種電気工事士</td>
                    </tr>
                    <tr>
                        <td>好きな動物:</td>
                        <td>ペンギン</td>
                    </tr>
                </v-table>
            </v-card>
        </div>
    </v-container>
</template>

<style>
.profile-area{
    display: flex;
    justify-content: center;
}

.icon{
    border-radius: 50px;
    border: 2px solid;
    margin: 20px;
}
.introduction {
    font-family: serif;
    width: 800px;
    margin: 10px
}
.introduction h2{
    padding-left: 10px;
}

.introduction thead{
    background-color: #12747b;
    color: white;
    
}
.introduction td{
    padding: 3px;
}
.v-table td {
    background: white;
}
.v-table tr:nth-child(odd) td {
    background: rgb(243, 243, 243);
}

/* レスポンシブ対応 */
@media(max-width:600px){
    .profile-area{
        display: block;
        width: 100%;
        margin: 0 auto;
    }

    .icon{
        display: block;
        margin: 20px auto;
    }

    .introduction {
        width: 100%;
    }
}
</style>