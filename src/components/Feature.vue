<script setup>
import { BeakerIcon, CurrencyDollarIcon, LibraryIcon, ServerIcon } from '@heroicons/vue/solid';
import KusamaIcon from "../assets/kusama.svg"

const features = [
    {
        icon: ServerIcon,
        color: 'rgb(74, 150, 216)',
        description: "Dedicated servers with an enterprise-grade hardware & monitoring setup provides secure & reliable validation"
    },
    {
        icon: CurrencyDollarIcon,
        color: 'rgb(255, 200, 71)',
        description: "Automatic payouts each era to maximise returns from compounding"
    },
    {
        icon: LibraryIcon,
        color: 'rgb(10, 190, 31)',
        description: "Run by active community members & participates in on-chain governance"
    },
]

</script>

<template>
    <div class="features">
        <div v-for="feature in features" :key="feature.name" class="feature">
            <div class="icon-line">
                <div class="hr-line"></div>
                    <component :is="feature.icon" aria-hidden="true" :style="{ color: feature.color }"/>
                <div class="hr-line"></div>
            </div>
            <p class="text">{{ feature.description }}</p>
        </div>
    </div>
</template>

<style scoped>

.hr-line {
    width: 100%;
    position: relative;
    margin: 10px;
    margin-bottom: 50px;
    border-bottom: 1px solid;
    display: inline;
}

.icon-line {
    display: flex;
}

svg {
    width: 100px;
    height: 100px;
    position: relative;
    color: rgb(10, 190, 31);
}


.text {
    margin: 10px;
    margin-top: -10px;
    width: 280px;
}

.features {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}

.feature {
    margin-left: 10px;
    margin-right: 10px;
}
</style>
