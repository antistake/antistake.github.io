<script setup>
const kusama = {
    img: {
        src: 'kusama.svg',
        alt: 'Kusama logo'
    },
    keys: ['DwQx7moAfebiPXDq1kc3oTvByyBWhjFoyXY6fu5xvucTEB6']
}

const polkadot = {
    img: {
        src: 'polkadot.svg',
        alt: 'Polkadot logo'
    },
    keys: ['DwQx7moAfebiPXDq1kc3oTvByyBWhjFoyXY6fu5xvucTEB6']
}

function copyKey(event) {
    const key = event.target.textContent;
    console.log(key);
    navigator.clipboard.writeText(key);
    const confirmElement = document.getElementById(key)
        .animate(
            [ { opacity: 0 }, { opacity: 1 } ],
            {
                fill: 'forwards',
                easing: 'steps(4, end)',
                duration: 50
            });
}
</script>

<template>
    <div class="networks">

        <div class="network">
            <img :src="kusama.img.src" :alt="kusama.img.alt" class="logo" />
            <h3>Kusama Validator</h3>
            <div v-for="key in kusama.keys" :key="key">
                <div class="key" @click="copyKey">
                    <p>{{key}}</p>
                </div>
                <p class="copy-confirmation" :id="key">Copied!</p>
            </div>
        </div>
        <div class="network">
            <img :src="polkadot.img.src" :alt="polkadot.img.alt" class="logo" />
            <h3>Polkadot Validator</h3>
            <p>Coming Soon!</p>
        </div>
    </div>
</template>

<style scoped>




h3 {
    margin-top: 3px;
}

.copy-confirmation {
    opacity: 0;
    margin: 0;
}

.logo {
    height: 3em;
}

.key {
    max-width: 80vw;
    background: #e3e3e3;
    display: inline-block;
    border-radius: 20px;
}
.key > * {
    margin: 10px;
    text-overflow: ellipsis;
    white-space: nowrap;
    overflow: hidden;
}

.networks {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    margin-bottom: 5em;
}

.network {
    margin: 20px;
    margin-left: auto;
    margin-right: auto;
}

</style>
