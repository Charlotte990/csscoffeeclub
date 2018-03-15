
<template>
  <div class="main-grid">
    <header>
      <h1>C H A R L O T T E</h1>
    </header>
    <aside>
      <div class="sidebar-content">
        <button class="button"><a href="/">Home</a></button>
      </div>
      <div class="sidebar-content">
        <button class="button"><a href="portfolio">Portfolio</a></button>
      </div>
      <div class="sidebar-content">
        <button class="button"><a href="contact">Contact</a></button>
      </div>
    </aside>
    <main>
      <div class="main-bits">
        Content:
        <nuxt/>
      </div>
    </main>
    <footer>
      <div class="footer-content">
        <p>Footer content</p>
      </div>
    </footer>
  </div>
</template>

<script>

</script>

<style>
html, body {
  min-height: 100%;
  margin: 0;
  padding: 0;
}

.main-grid {
  min-height: 100vh;
  display: grid;
  grid-template-rows: 1fr 0.5fr 3fr 0.25fr;
  grid-template-columns: 1fr;
  grid-template-areas:  "heading"
                        "sidebar"
                        "content"
                        "footer";
}

header {
  grid-area: heading;
  background-color: #b47fa5;
}
h1 {
  padding-left: 10px;
  color:#f9ebf5;
}
main {
  grid-area: content;
  background-color: #f9ebf5;
}
.main-bits {
  padding-left: 10px;
  padding-top: 10px;
}
aside {
  grid-area: sidebar;
  background-color: #ca8fba;
  display: grid;
  grid-template-rows: 1fr;
  grid-template-columns: 1fr 1fr 1fr;
  text-align: center;
}
.sidebar-content {
  align-self:center;
}
footer {
  grid-area: footer;
  background-color: #b47fa5;
}
.footer-content {
  display: grid;
  align-self: center;
  padding-left: 10px;
  color: #f9ebf5;
}

.button {
  background-color: transparent;
  border: none;
  text-decoration: none;
  font-size: 14px;
  cursor: pointer;
}
.button:hover {
  border: 2px solid #704f67;
}
.button:focus {
  border: 2px solid #704f67;
}

@media only screen and (min-width: 800px)  {
    .main-grid {

        grid-template-columns: 200px auto;
        grid-template-rows: 0.5fr 1fr 1fr 1fr 0.25fr;
        grid-template-areas:
        "heading   heading"
        "sidebar  content"
        "sidebar content"
        "sidebar  content"
        "footer   footer";
    }
    aside {
      grid-template-columns: 1fr;
      grid-template-rows: 1fr 1fr 1fr;
    }
}
</style>
