<template>
  <Layout>

    <div class="container">
      <div class="journal-hero">
        <h1 class="journal-header">
          “ The things that we love tell us who we are.” 
        </h1>
        <p>- Saint Thomas Aquinas</p>
      </div>
    </div>

    <g-link 
      :to="item.node.path"
      v-for="item in $page.posts.edges" 
      :key="item.node.id"
      class="journal-post"
    >
      <div class="container journal">
        <h2 class="journal-title">{{ item.node.title }}</h2>
        <p class="journal-excerpt">{{ item.node.excerpt }}</p>
      </div>
    </g-link>
      
  </Layout>
</template>

<page-query>
query Journal {
	posts: allJournalPost {
    edges {
      node {
        id
        path
        title
        excerpt
      }
    }
  }
}
</page-query>

<script>
export default {
}
</script>

<style scoped>

body {
  background-color: var(--color-base-1);
  }

.container.journal {
  max-width: 720px;
}
.journal-hero {
  padding: 4rem 0;
  color: var(--color-contrast);
}
.journal-header {
  font-family: 'Pirata One', cursive;
  font-size: 6rem;
  font-weight: 400;
  padding: 0;
  margin: 0;
}
.journal-hero p {
  font-size: 0.875rem;
  font-weight: 700;
  text-align: right;
  color: var(--color-contrast-50);
}
.journal-post {
  display: block;
  padding: 2rem 0;
  text-decoration: none;
  transition: background 0.5s ease;
}
.journal-post > * {
  transition: transform 0.5s ease;
}
.journal-post:hover {
  background-color: var(--color-base-3);
}
.journal-post:hover > * {
  transform: translateX(4rem);
}
.journal-post h1,
.journal-post h2 {
  margin: 0;
  padding: 0;
}
.journal-title {
  font-family: 'Pirata One', cursive;
  font-weight: 400;
  font-size: 3rem;
  color: var(--color-contrast-1);
}
.journal-excerpt {
  color: var(--color-contrast-1);
  font-weight: 400;
}

@media (min-width: 560px) {
  .journal-post {
    padding: 3rem 0;
  }
}

@media (min-width: 860px) {
  .journal-post {
    padding: 5rem 0;
  }
}
</style>
