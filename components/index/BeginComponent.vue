<template>

    <div class="container">
        <div class="begin d-flex flex-row justify-content-around align-items-center">
            <div class="begin-header">
                <h1>Let’s simply begin with rentiz.</h1>
            </div>
            <div class="begin-text">
                <p>Neque, vestibulum sed varius magna et at. Eu, adipiscing morbi augue justo. Nibh laoreet volutpat
                    quis velit. Blandit aliquam donec sed morbi congue eget lorem viverra porta id lobortis.
                </p>
                <LinksLinkComponent class="indexlink" :text="text" :path="path"/>
            </div>
        </div>
    </div>

</template>

<script>

export default {
    name: "BeginComponent",
    data(){
        return{
            text:'Get Started',
            path:'/signin'
        }
    }
}
</script>

<style lang="scss" scoped>
</style>