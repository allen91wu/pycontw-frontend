<template>
    <div class="two-col-layout">
        <div class="left-col">
            <slot></slot>
        </div>
        <div class="right-col">
            <slot name="right-col"></slot>
        </div>
    </div>
</template>

<script>
export default {
    name: 'TwoColWrapper',
}
</script>

<style lang="postcss" scpoed>
@media (min-width: 1024px) {
    .two-col-layout {
        @apply gap-6;
        grid-template-columns: 1fr 5fr;
    }
}
.two-col-layout {
    @apply grid my-4;
}
.left-col {
    @apply justify-self-start mb-2 text-primary-500;
    font-size: 20px;
    @media (min-width: 1024px) {
        font-size: 24px;
    }
}
.right-col {
    @apply leading-4 lg:leading-6 my-auto;
    font-size: 16px;
    line-height: 28px;
    @media (min-width: 1024px) {
        font-size: 18px;
    }
}
</style>
