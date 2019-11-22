
<template>
  <div class="form" id="form">
    <h2>Meld je aan om jouw kunst tentoon te stellen en/of te verkopen.</h2>
    <p>Bij deelname wordt er verwacht dat jouw kunst uiterlijk 27 November klaar staat.</p>
    <form id="inschrijving" method="post">
      <input required type="text" placeholder="Naam" name="voornaam" />
      <input required type="text" placeholder="Achternaam" name="achternaam" />
      <input required type="email" placeholder="Email" name="email" />
      <input required type="text" placeholder="Aantal kunstwerken" name="aantalkunstwerken" />
      <p>Wanneer kom jij jouw kunstwerk(en) brengen?</p>

      <input required type="date" placeholder="datum" name="date" />
      <input required type="text" placeholder="Wat wil je tentoonstellen/verkopen?" name="tentoonstellen" />
      <button>Meld mij aan</button>
    </form>
  </div>
</template>
<script>
import $ from "jquery";
export default {
  mounted() {
    emailjs.init("user_i1nBwT1JtVORHfNE9pch0");
    var myform = $("form#inschrijving");
    myform.submit(function(event) {
      event.preventDefault();

      // Change to your service ID, or keep using the default service
      var service_id = "default_service";
      var template_id = "inschrijfformulier";

      myform.find("button").text("verzenden...");
      emailjs.sendForm(service_id, template_id, myform[0]).then(
        function() {
          alert("verzonden!");
          $('input').val('')

          myform.find("button").text("verzonden!");
        },
        function(err) {
          alert("Send email failed!\r\n Response:\n " + JSON.stringify(err));
          myform.find("button").text("probeer opnieuw");
        }
      );
      return false;
    });
  }
};
</script>
<style scoped>
h2 {
  text-transform: uppercase;
  width: calc(100% - 50px);
  max-width: 500px;
  margin: 0 auto;
  text-align: left;
  box-sizing: border-box;
  margin-bottom: 20px;
  /* background: green; */
}
p {
  width: calc(100% - 50px);
  max-width: 500px;
  margin: 0 auto;
  text-align: left;
  margin-bottom: 20px;
}
form p {
  margin-left: 0;
  margin-top: 10px;
  margin-bottom: 0px;
}
button {
  height: 50px;
  min-width: 150px;
  background: #3792d9;
  color: white;
  border: none;
  font-weight: bolder;
  float: left;
  margin-top: 30px;
  text-transform: uppercase;
}
.form {
  min-height: 100vh;
  background: black;
  position: relative;
  width: 100%;
  color: white;
  padding-top: 100px;
}

form {
  width: calc(100% - 50px);
  max-width: 500px;
  box-sizing: border-box;
  /* background: purple; */
  margin: 0 auto;
}
input {
  height: 40px;
  width: 100%;
  box-sizing: border-box;
  background: black;
  border: none;
  color: white;
  border-bottom: 1px solid white;
  margin-bottom: 20px;
  /* border-radius: 10px; */
}
input[type="date"] {
  color: white;
  border-radius: 0px !important;

}
input::placeholder {
  color: white;
}
</style>