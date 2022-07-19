<template>
  <div class="Notif">
    <div class="parent_notif_button">
      <button class="button_to_notif" @click="NotifPush">
        Recevoir Notification
      </button>
    </div>
  </div>
</template>

<script setup>
const NotifPush = function () {
  Notification.requestPermission()
    .then(function (result) {
      if (result === "granted") {
        console.log(result);
      }
      const img = "https://cdn-icons-png.flaticon.com/800/7207/7207402.png";
      const text = "Coucou ! Votre commance est en cours de preparation.";
      const notification = new Notification("Commande Reçu !", {
        body: text,
        icon: img,
      });
      notification.addEventListener("click", function () {
        alert("YES");
      });
    })
    .catch(function (result) {
      console.log(result);
    });
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
.Notif {
  height: 100vh;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.parent_notif_button {
  height: 5rem;
  width: 15rem;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 0.5rem;
  box-shadow: #c1c1ff 0px 8px 24px;
}
.button_to_notif {
  border: 1px solid #c1c1ff;
  padding: 0.5rem 1rem;
  cursor: pointer;
  border-radius: 0.5rem;
  transition: 0.1s linear;
  font-family: Monospace;
}
.button_to_notif:hover {
  background-color: #bcbcbc;
}
</style>
