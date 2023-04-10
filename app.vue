<template>
  <main>
    <ContentList path="/blog" v-slot="{ list }">
      <div v-for="post in list" :key="post._path">
        <NuxtLink :to="`/blog/${post.slug}`">
          <h2>{{ post.title }}</h2>
          <p>{{ post.description }}</p>
        </NuxtLink>
      </div>
    </ContentList>
  </main>
</template>
