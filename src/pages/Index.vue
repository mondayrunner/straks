<template>
  <Layout>
    <article v-for="edge in $page.newsItems.edges" :key="edge.node.id">
      <h2><a v-bind:href="edge.node.url" target="_new">{{ edge.node.title }}</a>&nbsp;<small v-if="edge.node.company">&mdash; {{ edge.node.company.name }}</small></h2>
      <p>{{ edge.node.content }}</p>

      <p class="link" v-if="edge.node.url"><a v-bind:href="edge.node.url" target="_new">{{ edge.node.url }}</a> &rarr;</p>
    </article>
  </Layout>
</template>

<page-query>
query {
  newsItems: allStrapiNewsItems {
    edges {
      node {
        id
        title
        content
        url
        company {
          name
        }
      }
    }
  }
}
</page-query>


<script>
export default {
  metaInfo: {
    title: 'Nieuwsoverzicht'
  }
}
</script>

<style>
article {
  position: relative;
  padding-left: 1rem;
  padding-bottom: 1rem;
  margin-bottom: 1rem;
  border-bottom: 1px dotted #ddd;
  /* border-left: 3px solid #ddd; */
}

article::after {
  position: absolute;
  top: 14px;
  left: 2px;
  border-left: 8px solid #ddd;
  border-top: 4px solid transparent;
  border-bottom: 4px solid transparent;
  /* border-right: 10px solid transparent; */
  /* border-top: 10px solid transparent; */
  width: 0;
  height: 0;
  content: "";
  display: block;
}

h2 {
  font-size: 1.5rem;
}

h2 small {
  color:slategray;
}

h2 a {
  text-decoration: none;
}

h2 a:hover {
  background:#e4f0fa;
}


p.link {
  text-align: right;
  font-size: 0.8rem;
}
p.link a {
  color: rgb(164, 170, 175);
}
</style>
