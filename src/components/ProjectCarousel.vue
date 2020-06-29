<template>
    <v-container>
        <v-carousel cycle touch>
            <v-carousel-item>
                <v-card>
                <v-img src="../assets/light.jpg"/>
                </v-card>
            </v-carousel-item>
            <v-carousel-item>
                <v-card>
                <v-img src="../assets/defocused.jpg"/>
                </v-card>
            </v-carousel-item>

        </v-carousel>
    </v-container>
</template>
<script>
export default {
    name: 'ProjectCarousel'
}
</script>