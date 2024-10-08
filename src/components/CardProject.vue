<template>
  <main>
    <div v-for="i in 3" :key="i" class="card">
      <h3>{{ title }}</h3>
      <p>
        {{ text }}
      </p>
      <button><img src="../assets/images/arrow-1.png" /></button>
    </div>
  </main>
</template>

<script>
export default {
  data() {
    return {
      title: 'Développement Web',
      text: "Des sites rapides, responsives et optimisés pour le SEO. Que ce soit pour moderniser un site existant ou en créer un de zéro, je m'assure qu'il reflète votre identité et réponde aux besoins de vos utilisateurs."
    }
  },
  name: 'CardService'
}
</script>

<style scoped>
main {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.card {
  width: 30%;
  height: 30vh;
  background-color: var(--card-blue-color);
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;
  position: sticky;
  top: 20%;
  margin: 3% 0;
  color: var(--text-card-blue-color);
}
.card::before {
  content: '';
  background-image: url('../assets/images/stairs.png');
  background-size: cover;
  position: absolute;
  opacity: 0.5;
  top: 0px;
  right: 0px;
  bottom: 0px;
  left: 0px;
}
h3 {
  font-size: 24px;
  font-weight: bold;
  position: relative;
}

p {
  width: 70%;
  font-size: 14px;
  position: relative;
}

button {
  position: relative;
  width: 45px;
  height: 45px;
  border-radius: 50%;
  background-color: transparent;
  border: 1px solid var(--text-card-blue-color);
  cursor: pointer;
}

button:hover {
  color: aliceblue;
  rotate: -20deg;
  transition: 200ms linear all;
}

img {
  width: 80%;
}
</style>
