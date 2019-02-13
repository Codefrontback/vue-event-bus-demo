<template>
    <div>
        <nav>
            <div class="container">
                <div class="nav-wrapper">
                    <ul class="right">
                        <li>
                            <a href="https://www.google.com" target="_blank" class="github"><i class="fa fa-github"></i></a>
                        </li>
                    </ul>
                </div>
            </div>
        </nav>
        <Home></Home>
        <br>

        <h5>Listening Component</h5>
        <Listener></Listener>
        <footer class="page-footer">
            <div class="footer-copyright">
                <div class="container">
                    <span>&copy; 2018</span>&nbsp;<a href="https://artixun.com" target="_blank" style="color:white;text-decoration:none">Artixun Softwares.</a>
                </div>
            </div>
        </footer>
    </div>
</template>

<script>

    import Home from './components/HomeComponent.vue'
    import Listener from './components/ListenerComponent.vue'

    export default {
        name: 'app',
        components: {
            Home,
            Listener
        }
    }
</script>

<style scoped>
    /*.fade-enter-active, .fade-leave-active {*/
    /*transition: opacity .5s*/
    /*}*/
    /*.fade-enter, .fade-leave-active {*/
    /*opacity: 0*/
    /*}*/

    .fade-enter-active,
    .fade-leave-active {
        transition-duration: 0.2s;
        transition-property: opacity;
        transition-timing-function: ease;
    }

    .fade-enter,
    .fade-leave-active {
        opacity: 0
    }

    .container{
        padding:0px;
    }
    #nav-mobile a:hover{
        text-decoration: none !important;
        color:white;
    }
    #nav-mobile a:focus{
        text-decoration: none !important;
        color:white;
        background-color:rgba(0,0,0,0.1);
    }

    .page-footer{
        padding-top:0px;
        position:fixed;
        bottom:0;
        width:100%;
        z-index: 1;
    }
    .github
    {
        font-size:25px;
    }

    .github:hover{
        color:white;
    }

    .github:focus{
        color:white;
    }
    h5{
        text-align: center;
    }
</style>
