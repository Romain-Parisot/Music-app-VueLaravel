<template>
    <MusicLayout>
        <template #title> Créer une playlist </template>

        <template #action>
            <Link
                :href="route('playlists.index')"
                class="bg-green-500 hover:bg-green-600 text-white rounded-md px-3 py-2 text-sm font-medium"
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
};
</script>

<style></style>
