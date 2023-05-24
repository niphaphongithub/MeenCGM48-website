<template>
    <div>
    <HelloWorld />
    <CardSCMeeen imageSrc="https://scontent.fbkk13-3.fna.fbcdn.net/v/t39.30808-6/346485754_9247852471951770_3133583966902416245_n.jpg?_nc_cat=110&ccb=1-7&_nc_sid=730e14&_nc_eui2=AeELJ8-MSdzEqmaSQfONvCJHBh-pLeZXP5cGH6kt5lc_lynTmnrgwWe_rNu29wJYAjaHRYk9IttxNSxYvlG0H-eB&_nc_ohc=8GtnB9G4oi8AX9hUoYm&_nc_ht=scontent.fbkk13-3.fna&oh=00_AfDh9tNkK5kuM5AmPyMxFabYKlvo6_C0Lk7_p2LmmLfjuw&oe=6471CEE8">
    </CardSCMeeen>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import CardSCMeeen from './components/Card.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    CardSCMeeen
  }
}
</script>

<style>
/* body{
  text-align: center;
  align-items: center;
} */
</style>
