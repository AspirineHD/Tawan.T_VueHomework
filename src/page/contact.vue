<template>
  <div class="container text-center" style="text-align: center">
    <h1>Contact</h1>
    <p><b>E-Mail: </b> {{ Email }}</p>
    <p><b>Phone: </b> {{ Phone }}</p>
    <p><b>Address: </b> {{ Address }}</p>
    <br />
    <div id="contact">
      <button v-on:click="profile()">
        Profile
        <router-link :to="{ name: 'profile' }"></router-link>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    Email: "wa.tawan_st@tni.ac.th",
    Phone: "088-231-2197",
    Address:
      "No. 76, 39Suksabai Apartment, Pattanakarn 39, Suanlung, Bangkok 10250",
  }),
  methods: {
    profile() {
      this.$router.push("/");
    },
    // mFace() {
    //   this.$router.push("https://www.facebook.com/yuyu1337");
    // },
  },
};
</script>

<style scoped>
h1 {
  font-size: 2em;
  text-align: center;
  font-family: "Roboto";
}

p {
  font-size: 18px;
  font-family: "Calibri";
}
</style>