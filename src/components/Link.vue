<template>

    <ul class="link__btn-wrapper">
        <li class="link__btn"
            v-for="link in links" 
            :key="link.id">
                <a :href="link.url">{{link.name}}</a>
        </li>
    </ul>
  
</template>

<script>
import {Vue} from 'vue-class-component';

export default class Link extends Vue {
    links = [
        { id: 1, name:'Notre site', url:"https://daodavy.com"},
        { id: 2, name:'Mon super site', url:"https://daodavy.com" }
        ];
}
</script>

<style lang="scss">

$color : salmon;
$bg-color: #3D3B3C;

.link__btn {
    display: flex;
    width: 100%;
    min-height: 60px;
    background-color: $color;
    border:2px solid $color;
    transition: all 0.1s ease-in-out;
    overflow: hidden;
    
    &:not(:first-of-type) {
        margin-top: 20px;
    }
    &:hover {
        background-color: transparent;
        a {
            color : $color;
        }
    }

    a {
        width: 100%;
        padding: 10px;
        display: flex;
        justify-content: center;
        align-self: center;
        color: $bg-color;
    }
}
</style>