<template>
  <nav>
    <img src="../assets//images/logo.svg" />

    <ul>
      <li class="content__item">
        <a class="link link--leda" href="#" data-text="Accueil"><span>Accueil</span></a>
      </li>
      <li class="content__item">
        <a class="link link--leda" href="#" data-text="Portfolio"><span>Portfolio</span></a>
      </li>
      <li class="content__item">
        <a class="link link--leda" href="#" data-text="À propos"><span>À propos</span></a>
      </li>
      <li class="content__item">
        <a class="link link--leda" href="#" data-text="Contact"><span>Contact</span></a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'HeadPage'
}
</script>

<style scoped>
a {
  text-decoration: none;
  color: var(--text-primary-color);
}
li {
  list-style: none;
}
nav {
  display: flex;
  justify-content: space-between;
  padding: 0 5%;
  background: transparent;
  -webkit-backdrop-filter: blur(8px);
  backdrop-filter: blur(8px);
  align-items: center;
  width: 100%;
  position: fixed;
}
ul {
  display: flex;
  justify-content: space-around;

  width: 40%;
}
.content__item {
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  position: relative;
}
.content__item::before {
  position: absolute;
  top: 0;
  left: 0;
}
.link {
  cursor: pointer;
  position: relative;
  white-space: nowrap;
}
.link::before,
.link::after {
  position: absolute;
  width: 100%;
  height: 1px;
  background: currentColor;
  top: 100%;
  left: 0;
  pointer-events: none;
}
.link::before {
  content: '';
}
a:hover {
  outline: none;
}
.link--leda {
  overflow: hidden;
  line-height: 2;
}

.link--leda::before {
  height: 2px;
  top: calc(100% - 5px);
  transform-origin: 100% 50%;
  transform: scale3d(0, 1, 1);
  transition: transform 0.3s cubic-bezier(0.5, 0.5, 0.3, 1);
}

.link--leda:hover::before {
  transform-origin: 0% 50%;
  transform: scale3d(1, 1, 1);
}

.link--leda::after {
  content: attr(data-text);
  height: 100%;
  top: 0;
  background: none;
  transform-origin: 100% 50%;
  transform: translate3d(150%, 0, 0);
  transition: transform 0.3s cubic-bezier(0.5, 0.5, 0.3, 1);
}

.link--leda:hover::after {
  transform: translate3d(0, 0, 0);
}

.link--leda span {
  display: inline-block;
  transition: transform 0.3s cubic-bezier(0.5, 0.5, 0.3, 1);
}

.link--leda:hover span {
  transform: translate3d(-150%, 0, 0);
}
</style>
