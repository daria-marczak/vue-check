<template>
  <div>
    <Header/>
    <h1>Hello</h1>
    <h2>Soemthing</h2>
    <ul>
      <li v-for="comment in comments" class="comment" :key="comment.id">
        <p>{{comment.name}}</p>
        <p>{{comment.content}}</p>
      </li>
    </ul>
  </div>
</template>

<script>
import Header from "./components/Header.vue";

export default {
  name: "App",
  components: {
    Header
  },
  data() {
    return {
      comments: [
        {
          id: 1,
          name: "Daria",
          content:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum scelerisque eget massa sit amet elementum. Integer ut ligula auctor, lacinia ipsum nec, sollicitudin mauris. Morbi aliquam "
        },
        {
          id: 2,
          name: "Ellen",
          content:
            "Cras et rhoncus metus. Proin ullamcorper metus mauris, in volutpat velit porttitor quis. Nulla ullamcorper diam leo, sed porta justo dictum eget. Aenean nec posuere est. Vivamus molestie justo in mauris lacinia lacinia. Nunc lorem urna, dignissim eu blandit ut, condimentum at felis."
        },
        {
          id: 3,
          name: "John",
          content:
            "Nullam non massa non tellus dapibus pulvinar. Maecenas in semper erat, in accumsan velit. Vestibulum semper ipsum molestie, malesuada sapien pharetra, sodales urna. Suspendisse ac efficitur nisi, in pulvinar sapien. Mauris tristique magna vel libero iaculis porttitor."
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
h1 {
  color: #ffaabb;
}

h2 {
  font-family: "Helvetica";
}

.comment {
  background: #eee;
  padding: 20px;
  margin-bottom: 10px;
  list-style: none;

  p:first-child {
    font-weight: bold;
  }
  p:last-child {
    font-size: 2em;
  }
}
</style>
