<template>
    <header>
        <v-app-bar app color="green" dark>
            <v-app-bar-title>
                <router-link to="/" class="header">
                    Ueno's Portfolio
                </router-link>
            </v-app-bar-title>
            <p class="version">updated 2024/1/12</p>
        </v-app-bar>
    </header>
</template>

<style scoped>
.header {
  text-decoration: none;
  color: inherit;
  font-size: 30px;
  margin-left: 2%;
}

.version{
    text-align: right;
    padding-right: 2%;
}
</style>