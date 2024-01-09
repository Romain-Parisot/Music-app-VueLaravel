<template>
    <MusicLayout>
        <template #title>
            Créer une musique
        </template>
        <template #action>
            <Link :href="route('tracks.index')" class="bg-blue-500">
                Retour
            </Link> 
        </template>
        <template #content>
            <form>
                <div class="mb-3">
                    <label class="block text-gray-700 text-sm font-bold mb-2" for="title">
                        Titre
                    </label>
                    <input
                        id="title"
                        v-model="form.title"
                        class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline border-red-500"
                        :class="{ 'border-red-500': form.errors.title }"
                        type="text"
                        placeholder="Title"
                    >
                    <p class="text-red-500 text-xs italic">{{ form.errors.title }}</p>
                </div>
                <div class="mb-3">
                    <label class="block text-gray-700 text-sm font-bold mb-2" for="artist">
                        Artiste
                    </label>
                    <input
                        id="artist"
                        v-model="form.artist"
                        class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline border-red-500"
                        :class="{ 'border-red-500': form.errors.artist }"
                        type="text"
                        placeholder="Nom de l'artiste"
                    >
                    <p class="text-red-500 text-xs italic">{{ form.errors.artist }}</p>
                </div>
                <div class="mb-3">
                    <label class="block text-gray-700 text-sm font-bold mb-2" for="album">
                        Album
                    </label>
                    <input
                        id="album"
                        v-model="form.album"
                        class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline border-red-500"
                        :class="{ 'border-red-500': form.errors.album }"
                        type="text"
                        placeholder="Nom de l'album"
                    >
                    <p class="text-red-500 text-xs italic">{{ form.errors.album }}</p>
                </div>
                <div class="mb-3">
                    <label class="block text-gray-700 text-sm font-bold mb-2" for="image">
                        Image
                    </label>
                    <input
                        id="image"
                        v-on="form.image"
                        class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline border-red-500"
                        :class="{ 'border-red-500': form.errors.image }"
                        type="file"
                        placeholder="Image"
                    >
                    <p class="text-red-500 text-xs italic">{{ form.errors.image }}</p>
                </div>
                <div class="mb-3">
                    <label class="block text-gray-700 text-sm font-bold mb-2" for="music">
                        Musique
                    </label>
                    <input
                        id="music"
                        v-on="form.music"
                        class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline border-red-500"
                        :class="{ 'border-red-500': form.errors.music }"
                        type="file"
                        placeholder="Musique"
                    >
                    <p class="text-red-500 text-xs italic">{{ form.errors.music }}</p>
                </div>
                <div class="mb-3">
                    <label class="block text-gray-700 text-sm font-bold mb-2" for="display">
                        Afficher
                    </label>
                    <input
                        id="display"
                        v-model="form.display"
                        class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline border-red-500"
                        :class="{ 'border-red-500': form.errors.display }"
                        type="checkbox"
                        placeholder="Afficher"
                    >
                    <p class="text-red-500 text-xs italic">{{ form.errors.display }}</p>
                </div>
                {{ form }}
            </form>
        </template>
    </MusicLayout>
</template>

<script>
import MusicLayout from '@/Layouts/MusicLayout.vue';

    export default {
    components: { MusicLayout },
    data() {
        return {
            test: 'test',
            form: this.$inertia.form({
                title: '',
                artist: '',
                album: '',
                image: null,
                music: null,
                display: true,
            }),
        };
    },
}
</script>