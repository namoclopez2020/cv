<template>
    <div>
        <div class="container-fluid">
            <div :class="'row theme-bg-'+[theme]+'-600'">
                <div :class="'col-12 col-sm-12 col-md-5 col-lg-4 col-xl-3 col-xxl-3 theme-bg-'+[theme]+'-800 p-2'">
                    <picture-profile class="pt-2"/>
                    <name/>
                    
                </div>
                <div :class="'col-12 col-sm-12 col-md-7 col-lg-8 col-xl-9 col-xxl-9 theme-'+[theme]+'-100 p-2'">
                    <iam/>
                   
                </div>
                <div :class="'col-12 col-sm-12 col-md-12 col-lg-12 col-xl-12 col-xxl-12 theme-'+[theme]+'-100 p-2'">
                   
                </div>
            </div>
        </div>
    </div>
</template>

<script>

import iam from './Iam'
import name from './Name'
import PictureProfile from './Picture'


export default {
    name: 'Dashboard',
    components: {
        // Colors,
       
        iam,
        name,
        PictureProfile
       
    },
    methods: {
        resizeTextarea (event) {
            event.target.style.height = (event.target.scrollHeight) + 'px'
        },
    },
};
</script>