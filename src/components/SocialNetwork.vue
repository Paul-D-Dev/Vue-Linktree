<template>
    <div >
        <ul class="social-list">
            <li v-for="social in socials" 
                v-bind:key="social.id"> 
                <a class="logo-wrapper" v-bind:href="social.url">
                    <img class="social-logo" :src="social.icon" :alt="social.name">
                </a>
            </li>
        </ul>
    </div>

</template>

<script lang='ts'>
import { Vue } from 'vue-class-component';

export default class SocialNetwork extends Vue{
    socials = [
        {id: 0, name:'Facebook', url:'https://www.facebook.com/DAODAVY/', icon: require('@/assets/facebook.png')},
        {id: 1, name:'Instagram', url:'https://www.instagram.com/daodavy', icon: require('@/assets/instagram.png')},
        {id: 2, name:'Twitter', url:'https://twitter.com/daodavy', icon: require('@/assets/twitter.png')},
        {id: 3, name:'Linkedin', url:'https://www.linkedin.com/company/daodavy/', icon: require('@/assets/linkedin.png')},
    ];

}
</script>

<style lang="scss">
.social-list {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    margin-top: 30px;
}
li {

    list-style: none;

    .social-logo { 
        width: 32px;
        height: 32px;
    }
}
</style>