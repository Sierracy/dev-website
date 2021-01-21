<template>
    <nav>
        <v-app-bar app fixed class="hidden-sm-and-down">
            <v-toolbar-title> 
                Sierra N. Ellison
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn text v-for="(item, index) in navLinks" :key="index">{{item.title}}</v-btn>
           
        </v-app-bar>
        <v-app-bar app fixed class="hidden-md-and-up">
            <v-spacer></v-spacer>
            <div class="text center">
            <v-menu offset-y>
                <template v-slot:activator="{ on, attrs }">
                    <v-app-bar-nav-icon class="hidden-md-and-up"
                    v-bind="attrs"
                    v-on="on">
                    </v-app-bar-nav-icon>
                </template>
                <v-list>
                    <v-list-item v-for="(item, index) in navLinks" :key="index">
                        <v-list-item-title>{{item.title}}</v-list-item-title>
                    </v-list-item>
                </v-list>
            </v-menu>
            </div>
            <v-spacer></v-spacer>
        </v-app-bar>
        
    </nav>
</template>
<script>
export default {
    name: 'Navbar',
    data: function(){
        return {
            navLinks: [
                {title: 'About'},
                {title: 'Projects'},
                {title: 'Blog'},
                {title: 'Contact'}
            ]
        }
    }
}
</script>