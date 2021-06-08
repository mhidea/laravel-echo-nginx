<template>
  <div class="container">
    <div class="row justify-content-center">
      <div class="col-md-8">
        <div class="card">
          <div class="card-header">Example Component</div>

          <div class="card-body">I'm an example component.</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    console.log("DOMAIN:  Component mounted.");
    window.EchoDomain.private("App.Models.User.1").listen(".test", (e) => {
      console.log("DOMAIN:  ++++++++++++++");
      console.log(e);
    });
    window.EchoDomain.channel("public").listen(".test", (e) => {
      console.log("DOMAIN:  ---------------");
      console.log(e);
    });
  },
};
</script>
