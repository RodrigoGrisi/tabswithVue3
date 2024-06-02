<template>
  <div class="Container">
    <div class="news">
      <img
        class="news-cover"
        src="https://images.pexels.com/photos/830891/pexels-photo-830891.jpeg?auto=compress&cs=tinysrgb&dpr=2&w=500"
        alt="News Cover"
      />
      <div>
        <h1>News Title</h1>
        <p>
          This is the content of the news article. It provides detailed
          information about the topic.
        </p>
      </div>
    </div>
  </div>
</template>
<script>
</script>

<style scoped>
.Container {
  max-width: 100%;
  background-color: rgb(148, 140, 155);
  margin: 20px;
  border-radius: 8px;
}

.news {
  display: flex;
  width: 100%;
}

.Container .news img {
  object-fit: cover;
  width: 180px;
  border-radius: 8px;
  margin: 10px;
}
</style>
