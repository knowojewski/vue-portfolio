<template>
    <div class="nav-container">
        <div class="nav-wrapper">
            <nav class="navigation">
                <ul class="links main-links">
                    <NavigationLink 
                    v-for="link in mainLinks" 
                    :key="link.pageName" 
                    :linkProp="link"
                    />
                </ul>

                <ul class="links socials-links">
                    <NavigationLink 
                    v-for="link in socialsLinks" 
                    :key="link.pageName" 
                    :linkProp="link"
                    />
                </ul>
            </nav>
        </div>
    </div>
</template>

<script>
import { Vue, Component } from 'vue-property-decorator';
import NavigationLink from './NavigationLink';

@Component({
    components: {
        NavigationLink
    }
})
export default class NavigationMain extends Vue {
    mainLinks = [
        {
            pageType: 'router',
            pageRoute: '/',
            pageName: 'Home',
            pageIcon: 'ic:round-home' 
        },
        {
            pageType: 'router',
            pageRoute: '/about',
            pageName: 'About',
            pageIcon: 'ic:baseline-3p' 
        },
        {
            pageType: 'router',
            pageRoute: '/stack',
            pageName: 'Stack',
            pageIcon: 'ic:baseline-3p' 
        },
        {
            pageType: 'router',
            pageRoute: '/works',
            pageName: 'Works',
            pageIcon: 'ic:outline-web' 
        },
        {
            pageType: 'router',
            pageRoute: '/contact',
            pageName: 'Mail',
            pageIcon: 'ic:baseline-email' 
        }
    ]

    socialsLinks = [
        {
            pageType: 'socials',
            pageRoute: 'https://www.facebook.com',
            pageName: 'Facebook',
            pageIcon: 'bi:facebook' 
        },
        {
            pageType: 'socials',
            pageRoute: 'https://www.github.com',
            pageName: 'About',
            pageIcon: 'ic:baseline-3p' 
        },
        {
            pageType: 'socials',
            pageRoute: 'https://www.linkedin.com',
            pageName: 'Stack',
            pageIcon: 'ic:baseline-3p' 
        }
    ]
}
</script>

<style>

</style>