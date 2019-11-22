<template>
  <nav>
    <div class="balk"></div>
    <ul>
      <li>
        <div class="logo"></div>
      </li>
      <div class="social">
        <a href="https://www.facebook.com/events/999112710423265/">
          <span>
            <div
              class="icon"
              style="background: url('https://cdn.discordapp.com/attachments/628330179428614147/633447038268211200/facebook-logo.png') center center no-repeat;color: black;background-size: contain;"
            ></div>
          </span>
        </a>

        <a href="https://www.instagram.com/kunstigrotterdam">
          <span>
            <div
              class="icon"
              style="background: url('https://cdn.discordapp.com/attachments/628330179428614147/647107916591136808/instagram.png') center center no-repeat;color: black;background-size: contain;"
            ></div>
          </span>
        </a>
        <a href="mailto:kunstigrotterdam@hotmail.com">
          <span>
            <div
              class="icon"
              style="background: url('https://cdn.discordapp.com/attachments/628330179428614147/647108196577837090/email.png') center center no-repeat;color: black;background-size: contain;"
            ></div>
          </span>
        </a>
      </div>
    </ul>

    <!-- <button>BUtY TICKETS</button> -->
  </nav>
</template>
<script>
import $ from "jquery";
export default {
  mounted() {
    // $(document).scroll(function() {
    //   var $nav = $("nav");
    //   $nav.toggleClass("scrolled", $(this).scrollTop() > $nav.height());
    // });
  }
};
</script>
<style scoped>
.balk {
  height: 10px;
  background: black;
  width: 100%;
  position: absolute;
}
.social span {
  display: inline-block;
  margin: 5px;
  padding-top: 3px;
  box-sizing: border-box;
  margin-top: 20px;
  height: 30px;
  width: 30px;
  background: black;
  border-radius: 50%;
}
.social {
  height: 100px;
  width: 120px;
  /* background: black; */
  position: absolute;
  right: 20px;
  top: 0px;
  text-align: center;
}
.icon {
  height: 13px;
  display: inline-block;
  margin: 5px;

  width: 13px;
  filter: invert(100%);
  background: yellow;
}
nav {
  height: 80px;
  width: 100%;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 1;
  transition: all 0.3s ease;
  display: flex;
}
.scrolled {
  background: white;
  color: black;
}
.logo {
  height: 100px;
  margin-top: 10px;
  width: 100px;
  background: url("https://cdn.discordapp.com/attachments/569465743180169220/647079675771879434/kunstig_logo.jpg")
    no-repeat center center;
  background-size: cover;
}
ul {
  padding: 0 0 0 50px;
  box-sizing: border-box;
  margin: 0;
  height: 100%;
  flex: 1;

  /* background: green; */
}
button {
  height: 60px;
  width: 150px;
  /* border-radius: 5px; */
  border: none;
  font-weight: bolder;
  background: black;
  color: white;
  margin: 10px;
  margin-top: 40px;
  margin-right: 40px;
  font-size: 15px;
  outline: none;
  text-transform: uppercase;
}
li {
  display: block;
  height: 100%;
  text-transform: uppercase;
  min-width: 100px;
  color: white;

  font-weight: bolder;
  line-height: 80px;
  float: left;
  /* background: blue; */
  margin-left: 5px;
}
@media only screen and (max-width: 600px) {
  ul {
    padding: 0 0 0 20px;
  }
  li {
    width: 100px;
  }
}
</style>
