<template>
  <v-container class="my-15">
    <v-row justify="center">
        <v-col lg="15" class="text-center">
            <v-subheader class="text-h4 justify-center">Portfolio</v-subheader>
            <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Soluta omnis nulla, voluptatem possimus qui ipsam?</p>
        </v-col>
        <v-col lg="12">
            <div class="text-center">
                <v-chip @click="activePortfolio = 'webapp'" :color="activePortfolio === 'webapp'? 'success': ''" class="mx-5">Web App</v-chip>
                <v-chip @click="activePortfolio = 'mobileapp'" :color="activePortfolio === 'mobileapp'? 'success': ''" class="mx-5">Mobile App</v-chip>
                <v-chip @click="activePortfolio = 'desktopapp'" :color="activePortfolio === 'desktopapp'? 'success': ''"  class="mx-5">Desktop App</v-chip>
            </div>
        </v-col>
        <slot v-if="activePortolio === 'webapp'">
            <v-col lg="3" v-for="{web, webindex} in webApps" :key="webindex">
                <v-card>
                    <v-img
                    :src="web.image"
                    class="white--text align-end"
                    gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                    height="200px"
                    >
                    <v-card-title>{{web.title}}</v-card-title>
                    </v-img>
                </v-card>
            </v-col>
        </slot>

        <slot v-if="activePortolio === 'mobileapp'">
            <v-col lg="3" v-for="{mobile, mobileindex} in mobileApps" :key="mobileindex">
                <v-card>
                    <v-img
                    :src="web.image"
                    class="white--text align-end"
                    gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                    height="200px"
                    >
                    <v-card-title>{{mobile.title}}</v-card-title>
                    </v-img>
                </v-card>
            </v-col>
        </slot>
    </v-row>
  </v-container>
</template>

<script>
export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: "Porfolio",
    data() {
        return{
            activePortfolio: 'webapp',
            webApps: [
                {title: 'Web App 1', image:'https://images.unsplash.com/photo-1488590528505-98d2b5aba04b?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8dGVjaG5vbG9neXxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=700&q=60'},
                {title: 'Web App 2', image:'https://images.unsplash.com/photo-1518770660439-4636190af475?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8dGVjaG5vbG9neXxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=700&q=60'},
                {title: 'Web App 3', image:'https://images.unsplash.com/photo-1531297484001-80022131f5a1?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8M3x8dGVjaG5vbG9neXxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=700&q=60'},
                {title: 'Web App 4', image:'https://images.unsplash.com/photo-1519389950473-47ba0277781c?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8NHx8dGVjaG5vbG9neXxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=700&q=60'},
                {title: 'Web App 5', image:'https://images.unsplash.com/photo-1580894742597-87bc8789db3d?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8NXx8dGVjaG5vbG9neXxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=700&q=60'},
                {title: 'Web App 6', image:'https://images.unsplash.com/photo-1451187580459-43490279c0fa?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Nnx8dGVjaG5vbG9neXxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=700&q=60'},
                {title: 'Web App 7', image:'https://images.unsplash.com/photo-1535223289827-42f1e9919769?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTB8fHRlY2hub2xvZ3l8ZW58MHx8MHx8&auto=format&fit=crop&w=700&q=60'},
            ],
            mobileApps: [
                {title: 'Web App 1', image:'https://images.unsplash.com/photo-1488590528505-98d2b5aba04b?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8dGVjaG5vbG9neXxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=700&q=60'},
                {title: 'Web App 2', image:'https://images.unsplash.com/photo-1518770660439-4636190af475?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8dGVjaG5vbG9neXxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=700&q=60'},
                {title: 'Web App 3', image:'https://images.unsplash.com/photo-1531297484001-80022131f5a1?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8M3x8dGVjaG5vbG9neXxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=700&q=60'},
                {title: 'Web App 4', image:'https://images.unsplash.com/photo-1519389950473-47ba0277781c?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8NHx8dGVjaG5vbG9neXxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=700&q=60'},
                {title: 'Web App 5', image:'https://images.unsplash.com/photo-1580894742597-87bc8789db3d?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8NXx8dGVjaG5vbG9neXxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=700&q=60'},
                {title: 'Web App 6', image:'https://images.unsplash.com/photo-1451187580459-43490279c0fa?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Nnx8dGVjaG5vbG9neXxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=700&q=60'},
                {title: 'Web App 7', image:'https://images.unsplash.com/photo-1535223289827-42f1e9919769?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTB8fHRlY2hub2xvZ3l8ZW58MHx8MHx8&auto=format&fit=crop&w=700&q=60'},
            ]
        }
    }

}
</script>

<style>

</style>

34:42