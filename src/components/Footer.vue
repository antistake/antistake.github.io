<script>
import { MDBFooter, MDBContainer, MDBRow, MDBCol, MDBIcon, mdbRipple } from 'mdb-vue-ui-kit';
export default {
    components: {
        MDBFooter,
        MDBContainer,
        MDBRow,
        MDBCol,
        MDBIcon
    },
    directives: {
        mdbRipple
    }
};
</script>

<template>
    <footer>
        Join the conversation<br>
        <a href="https://github.com/primestaking">Github</a>
        <a href="https://discord.gg/tMMGgRuwA8">Discord</a>
        <a href="mailto:primestaking.info@gmail.com">Email</a>
    </footer>
</template>

<style scoped>

footer {
    display: block;
    width: 100%;
    position: absolute;
    left: 0;
    bottom: 0;
    margin: 0;
    color: rgb(233, 233, 233);
    text-align: center;
    background-color: rgb(57, 57, 57);
    padding: 20px 0px;
}

a {
    margin: 10px;
}
</style>