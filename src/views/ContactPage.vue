<template>
  <main>
    <div class="card">
      <h3>Vous un Projet ?</h3>
      <p>
        Prêt à donner vie à votre vision ? Contactez-moi dès aujourd'hui et commençons à travailler
        sur votre prochain projet. Envoyez-moi un message pour discuter de vos besoins et commencer
        à collaborer dès maintenant !
      </p>
      <button class="btn-contact">
        <span class="content-btn">Me contacter</span>
      </button>
    </div>
  </main>
</template>

<script>
export default {
  name: 'ContactPage'
}
</script>

<style scoped>
.card {
  width: 900px;
  height: 50vh;
  background-color: #fff;
  margin: 10rem auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 3rem;
  border-radius: 10px;
}
h3 {
  font-size: 32px;
  background: var(--primary-gradient);
  -webkit-background-clip: text;
  color: transparent;
  font-weight: bold;
}
p {
  width: 70%;
  text-align: center;
}
.btn-contact {
  cursor: pointer;
  position: relative;
  white-space: nowrap;
}
.btn-contact::before,
.btn-contact::after {
  position: absolute;
  width: 100%;
  top: 100%;
  left: 0;
  pointer-events: none;
}
.btn-contact::before {
  content: '';
}
.btn-contact {
  width: 15%;
  border: none;
  padding: 0.7rem 1rem;
  background-color: var(--border-color);
  border-radius: 50px;
  color: var(--background-color);
  cursor: pointer;
  font-family: 'Raleway', sans-serif;
}

.btn-contact::after {
  content: url('../assets/images/arrow-btn.png');
  top: 35%;
  background: none;
  transform: translate3d(150%, 0, 0);
  transition: transform 0.3s cubic-bezier(0.5, 0.5, 0.3, 1);
}
.btn-contact:hover::after {
  transform: translate3d(0, 0, 0);
}

.btn-contact span {
  display: inline-block;
  transition: transform 0.3s cubic-bezier(0.5, 0.5, 0.3, 1);
  font-weight: 600;
  font-size: 0.9rem;
}

.btn-contact:hover span {
  transform: translate3d(-150%, 0, 0);
}
.btn-contact {
  overflow: hidden;
}
</style>
