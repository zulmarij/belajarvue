<template>
  <div id="app">
    <div class="container">
      <div class="row header mb-5 p-3">
        <div class="col-lg-12">
          <h2 class="m-0">What I do Today?</h2>
        </div>
      </div>
      <div class="row content">
        <div class="col-lg-12">
          <div class="pekerjaan-rumah">
            <div class="row">
              <div v-for="tugasSaya in tugas" v-bind:key="tugasSaya.id" class="col-lg-12 text-start mb-4 tugas">
                <div class="form-check">
                  <ItemTugas v-bind:tugasSaya="tugasSaya"/>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

import 'bootstrap/dist/css/bootstrap.css';
import ItemTugas from './components/ItemTugas.vue';

export default {
  name: 'App',
  data() {
    return {
      tugas: [
        { 
          id: 1,
          namaTugas: 'Nguli Website',
          isDone: false
        },
        { 
          id: 2,
          namaTugas: 'Telan Udara',
          isDone: false
        },
        { 
          id: 3,
          namaTugas: 'Push up Mata',
          isDone: false
        },
        { 
          id: 4,
          namaTugas: 'Olahraga Baring 8 Jam',
          isDone: false
        }
      ]
    }
  },
  components: {
    ItemTugas
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.header {
  background: #1abc9c;
}
.item-completed {
  color: #1abc9c;
}
</style>
