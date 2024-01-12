<template>
    <MusicLayout>
        <template #title> Playlists: {{ playlist.title }} </template>

        <template #action>
            <Link
                :href="route('playlists.index')"
                class="bg-blue-500 hover:bg-blue-600 text-white rounded-md px-3 py-2 text-sm font-medium"
            >
                Retour
            </Link>
        </template>

        <template #content> </template>
    </MusicLayout>
</template>

<script>
import MusicLayout from "@/Layouts/MusicLayout.vue";
export default {
    components: {
        MusicLayout,
    },
    props: {
        playlist: Object,
    },
};
</script>

<style></style>
