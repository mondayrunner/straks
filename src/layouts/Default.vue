<template>
  <div>
    <header>
      <strong>
        <g-link to="/">Bureau<span>&cap;ieuws</span></g-link>
      </strong>
      <nav class="nav">
        <g-link class="nav__link" to="/">Overzicht</g-link>
        <g-link class="nav__link" to="/about/">Over ons</g-link>
      </nav>
    </header>
    <div class="layout">
      <slot/>
    </div>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
body {
  /* font-family: -apple-system,system-ui,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,sans-serif; */
  font-family: "Avenir Next","Avenir",sans-serif;
  margin:0;
  padding:0;
  line-height: 1.5;
  background: rgb(45, 96, 190);
  /* background: linear-gradient(to left, #ffffff, #f4f7f8); W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  min-height: 100vh;
  background: linear-gradient(to right, rgb(27, 73, 160), rgb(45, 96, 190)); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  padding-bottom: 10rem;
}
p,
h2 {
  margin-bottom: 0;
}
p {
  margin-top: 0.4rem;
}
a {
  color: black;
}

a,
a:hover,
.active--exact {
  color: white;
}
.active--exact {
  color: rgb(158, 172, 185);
  text-decoration: none;
}
.layout a:hover,
a:hover {
  color: coral;
}

.layout {
  max-width: 760px;
  margin: 0 auto;
  padding: 50px 100px;
  /* border: 10px solid #111; */
  background: #fafafa;
  border-radius: 3px;
  box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);
  box-shadow: 0 3px 6px rgba(0,0,0,0.16), 0 3px 6px rgba(0,0,0,0.23);
}

.layout a {
  color: #111;
}

header {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 20px;
  height: 80px;
  background: rgb(34, 79, 161);
  padding-left: 30px;
  padding-right: 30px;
  border-bottom: 1px solid #6085ca;
  /* box-shadow: 0px 1px 5px rgb(211, 211, 211); */
}

h1,
p {
  font-size: 1rem;
  color: #222;
  padding-bottom: 4px;
  /* font-family: -apple-system,system-ui,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,sans-serif; */
}
header a {
  text-decoration: none;
}
header strong {
  text-transform: uppercase;
  font-size: 1.3rem;
}
header strong a {
  color:#fafafa !important;
}

header strong a span {
  font-weight: normal;
  color:#b7c8ff !important;
}
.nav {
  position: absolute;
  right: 20px;
  top: 30px;
  /* margin-left: auto; */
  font-size: 0.9rem;
}
.nav__link {
  margin-left: 20px;
}
</style>
