<template>
    <v-footer app>
        <v-row wrap justify-center>  
            <v-spacer></v-spacer>
            <button onclick="window.location.href='http://www.linkedin.com';">
                <i class="fab fa-linkedin fa-2x ma-5"></i>
            </button>
            <button onclick="window.location.href='http://www.github.com';"> 
                <i class="fab fa-github fa-2x ma-5"></i> 
            </button>
            <button onclick="window.location.href='mailto:ellisosi@mail.gvsu.edu';">
            <i class="far fa-envelope fa-2x ma-5"></i>
            </button>
            <v-spacer></v-spacer>
        </v-row>
    </v-footer >
</template>
<script>
export default {
    name: 'Contact'
}
</script>