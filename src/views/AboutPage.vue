<template>
  <main>
    <h2>Je suis Adrien,<br /><span class="content-h">Développeur Fullstack</span></h2>

    <p>
      Adrien, développeur web expérimenté, fusionne technologie et stratégie digitale. Spécialiste
      en création de sites performants et optimisés pour le SEO, son expertise, forgée dans le monde
      professionnel, sublime vos projets en alliant créativité et efficacité pour des résultats
      visibles et mesurables.
    </p>
    <button class="btn-about">
      <span class="content-btn">À propos de mois</span>
    </button>
  </main>
</template>

<script>
export default {
  name: 'AboutPage'
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
  font-size: 3rem;
  color: var(--primary-color);
}
.content-h {
  background: var(--primary-gradient);
  -webkit-background-clip: text;
  color: transparent;
  font-weight: bold;
}
p {
  width: 900px;
  text-align: center;
  font-weight: 500;
  color: var(--primary-color);
}
.btn-about {
  cursor: pointer;
  position: relative;
  white-space: nowrap;
}
.btn-about::before,
.btn-about::after {
  position: absolute;
  width: 100%;
  top: 100%;
  left: 0;
  pointer-events: none;
}
.btn-about::before {
  content: '';
}
.btn-about {
  width: 15%;
  border: none;
  padding: 0.7rem 1rem;
  background-color: var(--border-color);
  border-radius: 50px;
  color: var(--background-color);
  cursor: pointer;
  font-family: 'Raleway', sans-serif;
}

.btn-about::after {
  content: url('../assets/images/arrow-btn.png');
  top: 35%;
  background: none;
  transform: translate3d(150%, 0, 0);
  transition: transform 0.3s cubic-bezier(0.5, 0.5, 0.3, 1);
}
.btn-about:hover::after {
  transform: translate3d(0, 0, 0);
}

.btn-about span {
  display: inline-block;
  transition: transform 0.3s cubic-bezier(0.5, 0.5, 0.3, 1);
  font-weight: 600;
  font-size: 0.9rem;
}

.btn-about:hover span {
  transform: translate3d(-150%, 0, 0);
}
.btn-about {
  overflow: hidden;
}
</style>
