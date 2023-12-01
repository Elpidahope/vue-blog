<template>
  <div>
    <h1>Finanzen</h1>
    <div v-for="user in users" :key="user.id">
      <!--<p>Benutzer: {{ user.name }}</p>
      <p>Kontostand: {{ user.balance }}</p>-->

      <!-- VCard für jeden Benutzer -->
      <VCard class="mx-auto" max-width="280" :title="user.name" :subtitle="`${user.name} on 2023-11-15, 05:15`">
        <VDivider />
        <VCardText>
          Kontostand: {{ user.balance }} <p></p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod.
        </VCardText>
        <form @submit.prevent="withdrawMoney(user.id)">
          <label for="amount">Betrag zum Abbuchen:</label>
          <input type="number" v-model="withdrawAmount" id="amount" />
          <button type="submit">Abheben</button>
        </form>
      </VCard>

      <!-- Formular zum Abbuchen -->


      <br /><br />
    </div>
    <div>
      <form @submit.prevent="abbuchen">
        <label for="amount">Betrag zum Abbuchen:</label>
        <input type="number" v-model="withdrawAmount" id="amount" />
        <button type="submit">Abheben</button>
      </form>
    </div>
  </div>
</template>

<script>
import userData from "./users.json";

export default {
  data() {
    return {
      users: userData,
      withdrawAmount: 0,
    };
  },
  methods: {
    withdrawMoney(userId) {
      // Finde den Benutzer mit der angegebenen ID
      const user = this.users.find((u) => u.id === userId);

      // Setze den Abbuchungsbetrag zurück
      this.withdrawAmount = 0;
    },
  },
};
</script>
<script setup>
</script>
<script setup>
</script>
<script setup>
</script>
<script setup>
</script>
<script setup>
</script>