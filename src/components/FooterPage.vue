<template>
  <div class="footer">
    <img src="../assets//images/logo.svg" />
    <div class="nav-bar">
      <nav class="nav-portfolio">
        <ul>
          <li><a class="a-title" href="#">Mon Portfolio</a></li>
          <li><a href="#">Gestion des consommations</a></li>
          <li><a href="#">Sport Decision</a></li>
          <li><a href="#">Metals Prices</a></li>
        </ul>
      </nav>
      <nav class="nav-about">
        <ul>
          <li><a class="a-title" href="#">À propos</a></li>
          <li><a href="#">Mentions légales</a></li>
          <li><a href="#">Politique de confidentialité</a></li>
          <li><a href="#">Me contacter</a></li>
        </ul>
      </nav>
      <nav class="nav-rs">
        <ul>
          <li><a class="a-title" href="#">Mes réseaux</a></li>
          <li><a href="#">Explorez davantage avec mes réseaux sociaux !</a></li>
          <li>
            <div>
              <img src="" />
              <img src="" />
              <img src="" />
            </div>
          </li>
        </ul>
      </nav>
    </div>
  </div>
</template>

<script>
export default {
  name: 'FooterPage'
}
</script>

<style scoped>
a {
  text-decoration: none;
  color: var(--primary-color);
}
li {
  list-style: none;
}
.footer {
  width: 100%;
  height: 20vh;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 5rem;
}
.nav-bar {
  display: flex;
  gap: 3rem;
}
.a-title {
  font-weight: bold;
  font-size: 1.1rem;
}
</style>
