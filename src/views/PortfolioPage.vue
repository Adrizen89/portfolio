<template>
  <main>
    <h2>Mon Portfolio</h2>

    <p>
      Adrien, développeur web expérimenté, fusionne technologie et stratégie digitale. Spécialiste
      en création de sites performants et optimisés pour le SEO, son expertise, forgée dans le monde
      professionnel, sublime vos projets en alliant créativité et efficacité pour des résultats
      visibles et mesurables.
    </p>
    <div class="animation-img">
      <div class="img"></div>
      <div></div>
    </div>
    <button class="btn-port">
      <span class="content-btn">Voir mon Portfolio</span>
    </button>
  </main>
</template>

<script>
export default {
  name: 'PortfolioPage'
}
</script>

<style scoped>
main {
  min-height: 100vh;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 5rem;
  align-items: center;
}
h2 {
  text-align: center;
  font-weight: bold;
  font-size: 2.5rem;
  color: var(--primary-color);
}
p {
  width: 900px;
  text-align: center;
  color: var(--primary-color);
  font-weight: 500;
}
.img {
  width: 900px;
  height: 50vh;
  background-color: green;
}
.btn-port {
  cursor: pointer;
  position: relative;
  white-space: nowrap;
}
.btn-port::before,
.btn-port::after {
  position: absolute;
  width: 100%;
  top: 100%;
  left: 0;
  pointer-events: none;
}
.btn-port::before {
  content: '';
}
.btn-port {
  width: 15%;
  border: none;
  padding: 0.7rem 1rem;
  background-color: var(--border-color);
  border-radius: 50px;
  color: var(--background-color);
  cursor: pointer;
  font-family: 'Raleway', sans-serif;
}

.btn-port::after {
  content: url('../assets/images/arrow-btn.png');
  top: 35%;
  background: none;
  transform: translate3d(150%, 0, 0);
  transition: transform 0.3s cubic-bezier(0.5, 0.5, 0.3, 1);
}
.btn-port:hover::after {
  transform: translate3d(0, 0, 0);
}

.btn-port span {
  display: inline-block;
  transition: transform 0.3s cubic-bezier(0.5, 0.5, 0.3, 1);
  font-weight: 600;
  font-size: 0.9rem;
}

.btn-port:hover span {
  transform: translate3d(-150%, 0, 0);
}
.btn-port {
  overflow: hidden;
}
</style>
