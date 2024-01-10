<template>
    <div
    class="max-w-sm rounded overflow-hidden shadow-lg cursor-pointer"
    :class="{ 'border-2 border-blue-500': active }"
    @click="play(track)">
            <div class="w-full h-1/2">
                <img class="w-full h-full" :src="`/storage/${track.image}`" />
            </div>
            <div style="height: 120px;" class="px-6 py-4">
                <div class="font-bold text-xl mb-2">
                    {{ track.title }}
                </div>
                <small class="text-gray-700 text-base">
                    {{ track.artist }}
                </small>
            </div>
        <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded w-8/12" 
        style="margin-left: 50%; transform: translateX(-50%); margin-top: ;"
        @click="play()">Play</button>
    </div>
</template>

<script>
    export default {
        emits: ['played'],
        props: {
            track: Object,
            active: {
                type: Boolean,
                default: false,
            },
        },
        methods: {
            play() {
                this.$emit('played', this.track);
            },
        },
    };
</script>