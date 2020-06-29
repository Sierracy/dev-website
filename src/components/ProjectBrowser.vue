<template>
    
    <v-container class="ma-20">
        <!-- <div class="disabled"> </div> -->
        <v-row class="ma-0 pa-0">
            <v-col class="ma-0 pa-0" v-for="project in projects" :key="project.name" cols="12" xs="12" sm="6" md="4">
                <v-hover v-slot:default="{ hover }">
                    <v-card flat tile height="100%" class="ma-0 pa-0 {'on-hover' : hover}">                  
                        <v-img height="400px" :src="project.src">
                            <v-expand-transition hide-on-leave="true">
                                <div
                                    v-if="hover"
                                    class="d-flex transition-fast-in-fast-out grey darken-2 v-card--reveal display-3 white--text"
                                    style="height: 100%;"
                                >
                                    <div class="d-block">
                                    {{project.name}}
                                    </div>
                                    <div>
                                    <v-btn tile color="white" class="d-block">View Project</v-btn>
                                    </div>
                                </div>
                            </v-expand-transition>
                        </v-img>
                    </v-card>
                </v-hover>
            </v-col>
        </v-row>
    </v-container>
    
</template>
<script>
export default {
    name: 'ProjectBrowser',
    data: function() {
        return {
            projects: [
                {name: 'test1', flex: 4, src: 'https://source.unsplash.com/random?sig=1'}, 
                {name: 'test2', flex: 4, src: 'https://source.unsplash.com/random?sig=2'}, 
                {name: 'test3', flex: 4, src: 'https://source.unsplash.com/random?sig=3'}, 
                {name: 'test4', flex: 4, src: 'https://source.unsplash.com/random?sig=4'}, 
                {name: 'test5', flex: 4, src: 'https://source.unsplash.com/random?sig=5'}, 
                {name: 'test6', flex: 4, src: 'https://source.unsplash.com/random?sig=6'}
            ]

        }
    }
}
</script>
<style>

    .disabled{
        position: absolute;
        width: 100%;
        height: 100%;
        background-color: rgba(0,0,0,0.5);
        
        
        
        cursor: pointer;
        z-index: 2;
    }

    .v-card--reveal {
    align-items: center;
    bottom: 0;
    justify-content: center;
    opacity: .75;
    position: absolute;
    width: 100%;
    }

    
</style>