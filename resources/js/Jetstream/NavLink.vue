<template>
    <inertia-link :href="href" :class="classes">
        <slot></slot>
    </inertia-link>
</template>

<script>
    export default {
        props: ['href', 'active'],

        computed: {
            classes() {
                return this.active
                            ? 'bg-gray-100 text-gray-900 group rounded-md py-2 px-2 flex items-center text-sm font-medium'
                            : 'text-gray-600 hover:bg-gray-50 hover:text-gray-900 group rounded-md py-2 px-2 flex items-center text-sm font-medium'
            }
        }
    }
</script>
