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
  background: #fafafa;
  background: linear-gradient(to right, #fafafa, #f8f8f8); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  min-height: 100vh;
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
  padding-left: 20px;
  padding-right: 20px;
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
  background: rgb(45, 96, 190);
  background: linear-gradient(to right, rgb(27, 73, 160), rgb(45, 96, 190)); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  padding-left: 30px;
  padding-right: 30px;
  border-bottom: 1px solid #f1f1f1;
  box-shadow: 0px 1px 5px rgb(211, 211, 211);
}

h1,
P {
  font-family: -apple-system,system-ui,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,sans-serif;
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
