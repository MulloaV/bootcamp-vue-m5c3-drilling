<template>
    <div class="container">
        <h1>Juegos Favoritos</h1>
        <b-list-group>
            <ul class="list-group">
                <li class="list-group-item" v-for="(game, index) in games" :key="index">
                    <span> {{ game }} </span>
                    <button class="btn btn-small btn-danger" @click="$emit('delete-game', index)">Eliminar</button>
                </li>
            </ul>

        </b-list-group>

    </div>
</template>

<script>
export default {
  props: {
    games: {
      type: Array,
      required: true
    }
  },
  emits: ['delete-game']
}
</script>

<style scoped>
.btn-small {
    margin-left: 10px;
    padding: 5px 10px;
    font-size: 12px;
    line-height: 1.5;
    border-radius: 3px;
    margin-bottom: 5px;
    align-items: end;
}
</style>
