<template>
    <li class="link-box">
        <router-link v-if="linkProp.pageType === 'router'" :to="linkProp.pageRoute" class="link">
            <span class="iconify" data-inline="false" :data-icon="linkProp.pageIcon"></span>
            <span class="link-text">{{ linkProp.pageName}} </span>
        </router-link>
        <a v-else-if="linkProp.pageType === 'socials'" :href="linkProp.pageRoute" class="link">
            <span class="iconify" data-inline="false" :data-icon="linkProp.pageIcon"></span>
            <span class="link-text">{{ linkProp.pageName}} </span>
        </a>
    </li>
</template>

<script>
import { Vue, Component, Prop } from 'vue-property-decorator';

@Component
export default class NavigationLink extends Vue {
    @Prop(Object) linkProp;
}
</script>

<style>

</style>