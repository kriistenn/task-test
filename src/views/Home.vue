<template>
  <div class="container">
    <div class="items-list">
      <div v-for="item in items" :key="item.name" @click="selectItem(item)" class="item-card">
        <span>Name: {{ item.name }}</span>
        <span>Value: {{ item.value }}</span>
      </div>
    </div>
    <div class="item-form__container" v-if="selectedItem">
      <div class="item-form">
        <h2>{{ selectedItem.name }}</h2>
        <div class="item-form--input">
          <label>Value:</label>
          <input type="text" v-model="selectedItem.value" class="item-form__input-field"/>
        </div>
        <button @click="saveChanges" class="item-form__button">Save</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomePage',
  data() {
    return {
      items: [
        {name: 'foo1', value: 'bar1'},
        {name: 'foo2', value: 'bar2'},
        {name: 'foo3', value: 'bar3'},
        {name: 'foo4', value: 'bar4'},
        {name: 'foo5', value: 'bar5'},
        {name: 'foo6', value: 'bar6'},
        {name: 'foo7', value: 'bar7'},
        {name: 'foo8', value: 'bar8'},
        {name: 'foo9', value: 'bar9'},
        {name: 'foo10', value: 'bar10'},
        {name: 'foo11', value: 'bar11'},
        {name: 'foo12', value: 'bar12'},
        {name: 'foo13', value: 'bar13'},
        {name: 'foo14', value: 'bar14'},
        {name: 'foo15', value: 'bar15'},
        {name: 'foo16', value: 'bar16'},
        {name: 'foo17', value: 'bar17'},
        {name: 'foo18', value: 'bar18'},
        {name: 'foo19', value: 'bar19'},
        {name: 'foo20', value: 'bar20'},
        {name: 'foo21', value: 'bar21'},
        {name: 'foo22', value: 'bar22'},
        {name: 'foo23', value: 'bar23'},
        {name: 'foo24', value: 'bar24'},
        {name: 'foo25', value: 'bar25'},
        {name: 'foo26', value: 'bar26'},
        {name: 'foo27', value: 'bar27'},
        {name: 'foo28', value: 'bar28'},
        {name: 'foo29', value: 'bar29'},
        {name: 'foo30', value: 'bar30'},
        {name: 'foo31', value: 'bar31'},
      ],
      selectedItem: null,
    };
  },
  methods: {
    selectItem(item) {
      this.selectedItem = item;
    },
    saveChanges() {

      this.selectedItem = null;
    },
  },
};
</script>

<style scoped>
.container {
  display: flex;
  justify-content: space-between;
  margin: 20px;
}

.items-list {
  width: 30%;
  display: flex;
  gap: 18px;
  flex-direction: column;
  overflow-y: scroll;
  max-height: 100vh;
  padding: 30px;
}

.item-form__container {
  width: 60%;
}

.item-form {
  background: #fff;
  box-shadow: 0px 4px 16px 1px rgba(51, 44, 56, 0.3);
  border-radius: 10px;
  padding: 14px;
}

h2 {
  margin-top: 0;
}

.item-form__input-field {
  width: 100%;
  padding: 5px;
  margin-bottom: 10px;
}

.item-form__input-field[type=text] {
  width: 100%;
  padding: 12px 20px;
  margin: 8px 0;
  box-sizing: border-box;
}

.item-form__button {
  padding: 5px 10px;
  background-color: #007bff;
  color: #fff;
  border: none;
  cursor: pointer;
  font-size: 24px;
  border-radius: 4px
}

.item-card {
  display: flex;
  flex-direction: column;
  background: #fff;
  box-shadow: 0px 4px 16px 1px rgba(51, 44, 56, 0.3);
  border-radius: 10px;
  transition: box-shadow 0.3s ease-in-out;
  padding: 14px;
  cursor: pointer;
}

.item-form--input {
  display: flex;
  align-items: center;
  gap: 12px;
}
</style>
