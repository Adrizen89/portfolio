<template>
  <HeadPage />
  <main>
    <h1>
      Des créations de solutions<br />
      <span>web personnalisées</span>
    </h1>
    <p class="description">
      Plongez dans l’univers du web design sur mesure. Je vous aide à transformer vos idées en
      expériences en ligne exceptionnelles, conçues pour maximiser l'impact et l'efficacité.
    </p>
    <div class="avatar">
      <img class="img-avatar" src="../assets/images/avatar.png" />
      <p class="name-avatar"><a class="name" href="services">adb.digital</a></p>
    </div>

    <img src="../assets/images/arrow.svg" />

    <div class="scroll-parent">
      <div class="scroll-element primary">
        <img src="../assets/images/figma.png" alt="figma" />
        <img src="../assets/images/flutter.png" alt="flutter" />
        <img src="../assets/images/firebase.png" alt="firebase" />
        <img src="../assets/images/python.png" alt="python" />
      </div>
      <div class="scroll-element secondary">
        <img src="../assets/images/vuejs.png" alt="vuejs" />
        <img src="../assets/images/wordpress.png" alt="wordpress" />
        <img src="../assets/images/figma.png" alt="figma" />
        <img src="../assets/images/flutter.png" alt="flutter" />
        <img src="../assets/images/firebase.png" alt="firebase" />
      </div>
    </div>
  </main>
</template>

<script>
import HeadPage from '../components/HeadPage.vue'

export default {
  name: 'HomePage',
  components: {
    HeadPage
  }
}
</script>

<style lang="css" scoped>
main {
  padding-top: 10rem;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
  height: 100vh;
  padding: 7rem 0;
}
h1 {
  max-width: 900px;
  text-align: center;
  font-size: 3rem;
  font-weight: bold;
  color: var(--text-primary-color);
}
span {
  background: var(--primary-gradient);
  -webkit-background-clip: text;
  color: transparent;
  font-weight: bold;
}
.description {
  max-width: 900px;
  text-align: center;
  font-weight: 500;
  color: var(--text-primary-color);
}
.avatar {
  width: 20%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.img-avatar {
  object-fit: contain;
  width: 50%;
}
.name-avatar {
  display: block;

  background-color: var(--btn-primary-color);
  padding: 5px 10px;
  border-radius: 50px;
  text-align: center;
  width: 50%;
  margin: auto;
}
.name {
  text-decoration: none;
  color: white;
  font-weight: 700;
}

.scroll-parent {
  position: relative;
  width: 100%;
  height: 7vh;
  overflow-x: hidden;
}

.scroll-element {
  width: inherit;
  height: inherit;
  position: absolute;
  left: 0%;
  top: 0%;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.scroll-element img {
  width: 20%;
  height: 100%;
  margin: 0 2rem;
  object-fit: cover;
}

.primary {
  animation: primary 10s linear infinite;
}

.secondary {
  animation: secondary 10s linear infinite;
}

@keyframes primary {
  from {
    left: 0%;
  }
  to {
    left: -100%;
  }
}

@keyframes secondary {
  from {
    left: 100%;
  }
  to {
    left: 0%;
  }
}
</style>
