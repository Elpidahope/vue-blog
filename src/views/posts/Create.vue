<script setup>
</script>

<template>
  <div>
    <form @submit.prevent="addUser">
      <label for="name">Name:</label>
      <input v-model="user.name" type="text" name="name" pattern="^[^\s]*$" placeholder="* name" required title="Bitte verwenden Sie keine Leerzeichen" />
      <p></p>

      <label for="geb">Geburtstag:</label>
      <p></p>
      <input v-model="user.geb" type="text" name="geb" pattern="^[^\s]*$" placeholder="Format muss sein: 00-00-0000" required title="Format muss sein: 00-00-0000" />
      <p></p>

      <label for="ver">Verhältnis zum Main:</label>
      <p></p>
      <input v-model="user.ver" type="text" name="ver" pattern="^[^\s]*$" placeholder="Format muss sein: 00-00-0000" required />
      <p></p>

      <label for="balance">Kontostand:</label>
      <p></p>
      <input v-model="user.balance" type="number" id="balance" name="balance" pattern="^[^\s]*$" placeholder="Konto" required />
      <p></p>

      <label for="aktien">Aktiendepot:</label>
      <p></p>
      <input v-model="user.aktien" type="number" id="aktien" name="aktien" pattern="^[^\s]*$" placeholder="aktien" required />
      <p></p>

      <label for="debt">Schulden:</label>
      <p></p>
      <input v-model="user.debt" type="number" id="debt" name="debt" pattern="^[^\s]*$" placeholder="Schulden" required />
      <p></p>

      <button type="submit">Benutzer hinzufügen</button>
    </form>
  </div>
</template>
