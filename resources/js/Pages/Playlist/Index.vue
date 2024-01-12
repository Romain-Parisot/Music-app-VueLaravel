<template>
    <MusicLayout>
        <template #title> Playlists </template>

        <template #action>
            <Link
                :href="route('playlists.create')"
                class="bg-green-500 hover:bg-green-600 text-white rounded-md px-3 py-2 text-sm font-medium"
            >
                Créer une playlist
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
};
</script>

<style></style>
