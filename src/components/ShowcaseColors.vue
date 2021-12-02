<template>
    <div>
        <!-- Color Scope -->
        <section 
        v-for="color in colors" 
        :key="color"
        class="color-block"
        >
            <!-- Shade Scope -->
            <div 
            v-for="shade in shades" 
            :key="shade"
            class="shade-block"
            :style= "{'background-color': 'hsla(var(--def-color-'+ color +'),'+ shade +'%)', }">

                {{ shade }}
                <span>{{ color }}</span>

            </div>
            <!-- End Shade Scope -->
        </section>
        <!-- End Color Scope -->
    </div>
</template>

<script>
    export default {
        data() {
            return {
                colors: ["accent","neutral","link"],
                shades: [10,20,30,40,50,60,70,80,90,95,100]
            }
        },
    }
</script>

<style scoped>
.color-block {
    display: flex;
}
.shade-block {
    flex: 1 1;
    display: flex;
    flex-direction: column;
}

</style>