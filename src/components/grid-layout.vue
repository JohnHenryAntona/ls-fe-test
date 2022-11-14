<template>
  <main class="default-page">
    <h1>Experienced & Multi-Talented</h1>
    <div class="divider"></div>
    <p class="description">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam tortor
      leo, porttitor vel dictum at, aliquam et augue. Duis vel molestie risus,
      ut lobortis felis.
    </p>
    <div class="card-container">
      <div class="card-items">
        <div v-for="index in 8" :key="index" class="card-item">
          <div class="card-header">
            <span class="header-icon">
              <img src="../assets/images/info.png" alt="" />
            </span>
          </div>
          <div class="card-body">
            <div class="body-title">BLOCK</div>
            <div class="body-content">
              <span class="content">
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
                <p>Ut vestibulum eros nisi, eu sagit-tis nisl feugiat quis.</p>
              </span>
            </div>
            <div class="actions" v-on:click="handleToggle">
              <span class="toggle"></span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: "GridLayout",
  props: {},
  methods: {
    handleToggle(event) {
      var contentWrapperElement =
        event.currentTarget.previousElementSibling.firstChild;
      // Toggle active class on hidden <p> tags
      contentWrapperElement.childNodes.forEach(function (item) {
        item.classList.toggle("active");
      });
      // Toggle active class on toggle button
      event.currentTarget.firstChild.classList.toggle("active");
    },
  },
};
</script>
