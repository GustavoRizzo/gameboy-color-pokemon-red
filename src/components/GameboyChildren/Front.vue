<template>
<div>
    <div v-if="showFront" class="box">
        <div class="shell">
            <div class="front-screen-indent">
                <div class="on-circle"></div>
                <div class="front-screen-container">
                    <img class="screen" src="#" />
                </div>
            </div>
            <div class="d-pad-container">
                <div class="d-pad-horizontal"></div>
                <div class="d-pad-vertical"></div>
            </div>
            <div class="button-a">
            </div>
            <div class="button-b"></div>
            <div class="start"></div>
            <div class="select"></div>
        </div>
    </div>
</div>
</template>

<script>
export default {
    name: 'Front',
    data() {
        return {
            showFront: false
        }
    },
    mounted() {
        this.$root.$on('messege_cartrige_in', () => {
            console.log("Front: ok, entendido");
            this.showFront = true;
        });
    }
}
</script>
