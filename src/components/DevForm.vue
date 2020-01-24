<template>
    <form>
        <div class="input-block">
            <label for="github_username">Usuário do GitHub</label>
            <input type="text" required
                name="github_username" 
                id="github_username"
            />
        </div>

        <div class="input-block">
            <label for="github_username">Tecnologias</label>
            <input type="text" required
                name="techs" 
                id="techs"
            />
        </div>

        <div class="input-group">
            <div class="input-block">
                <label for="latitude">Latitude</label>
                <input type="text" required
                    name="latitude" 
                    id="latitude"
                />
            </div>

            <div class="input-block">
                <label for="longitude">Longitude</label>
                <input type="text" required
                    name="longitude" 
                    id="longitude"
                />
            </div>
        </div>

        <button type="submit"> Salvar </button>
    </form>
</template>

<script>
export default {
    name: 'DevForm'
}
</script>