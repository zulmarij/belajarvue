<template>
  <div class="profile">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-lg-6">
          <div class="card border-0">
            <div class="row g-0">
              <div class="col-md-4 align-self-center">
                <img src="../assets/zulmarij.png" class="img-fluid user-pic" alt="zulmarij">
              </div>
              <div class="col-md-8">
                <div class="card-body text-start">
                  <h5 class="card-title">{{ firstName }} {{ lastName }}</h5>
                  <p class="card-text">{{ desc }}</p>
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

import 'bootstrap/dist/css/bootstrap.css'

export default {
  name: 'Profile',
  data() {
    return {
      firstName: 'Zul',
      lastName: 'Marij',
      desc: 'This is a wider card with supporting text below as a natural lead-in to additional content. This content is a little bit longer'
    }
  },
  components: {

  }
}
</script>

<style scoped>
  .user-pic {
    border-radius: 200%;
    height: 100px;
    width: 100px;
  }
</style>
