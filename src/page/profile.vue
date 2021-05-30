<template>
  <div class="container text-center" style="text-align: center">
    <h1>Profile</h1>
    <img src="@/assets/profile_img.jpg" width="200" />
    <p><b>Name: </b> {{ Name }}</p>
    <p><b>Nickname: </b> {{ Nickname }}</p>
    <p><b>Date of Birth: </b> {{ DOB }}</p>
    <p><b>Height: </b> {{ Height }} cm. <b>Weight: </b> {{ Weight }} kg</p>
    <p><b>Hobby: </b> {{ Hobby }}</p>
    <p><b>Skills: </b> {{ Skill }}</p>
    <br />
    <br />
    <div id="contact">
      <button v-on:click="contact()">
        Contact
        <router-link :to="{ name: 'contact' }"></router-link>
      </button>
      <p>Click button above to contact</p>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    Name: "Tawan Wareeboot",
    Nickname: "TLE",
    DOB: "15 Oct 1995",
    Height: "181",
    Weight: "69",
    Hobby: "Gaming, Watching (Movies, TV Series, Anime, ETC)",
    Skill: `C#, JAVA, SQL, 
            HTML/PHP, VB.NET, Basic Network Configuration(Cisco), 
            Network Design, R Language`,
  }),
  methods: {
    contact() {
      this.$router.push("/contact");
    },
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