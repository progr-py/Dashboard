<template >
  <div id="a">


    <div class="container">
      <aside :style="{display: isActive }">
        <div class="top">
            <div class="logo">
                <img src="./assets/logo.png" alt="" />
                <h2>Kha <span class="danger">Wal</span></h2>
            </div>
            <div class="close" id="close-btn" @click="active">
                <i class="uil uil-multiply"></i>
            </div>
        </div>
        <div class="side-bar">
            <a href="#" class="active" @click="active">
                <i class="uil uil-th"></i>
                <h3>Dashboard</h3>
            </a>
            <a href="#">
                <i class="uil uil-user"></i>
                <h3>Customers</h3>
            </a>
            <a href="#">
                <i class="uil uil-file-copy-alt"></i>
                <h3>Orders</h3>
            </a>
            <a href="#">
                <i class="uil uil-analysis"></i>
                <h3>Analytics</h3>
            </a>
            <a href="#">
                <i class="uil uil-envelope-alt"></i>
                <h3>Messages</h3>
                <span class="message-count">12</span>
            </a>
            <a href="#">
                <i class="uil uil-file-check-alt"></i>
                <h3>Products</h3>
            </a>
            <a href="#">
                <i class="uil uil-exclamation-octagon"></i>
                <h3>Reports</h3>
            </a>
            <a href="#">
                <i class="uil uil-setting"></i>
                <h3>Settings</h3>
            </a>
            <a href="#">
                <i class="uil uil-plus"></i>
                <h3>Add Products</h3>
            </a>
            <a href="#">
                <i class="uil uil-sign-out-alt"></i>
                <h3>Logout</h3>
            </a>
        </div>
    </aside>
      <main-bar ></main-bar>
      <div class="rigth">
        <div class="top">
          <button id="menu-btn" @click="active">
            <i class="uil uil-bars"></i>
          </button>
          <div class="theme-toggler" @click="changeTheme()">

            <i class="uil uil-sun " :class="darkTheme ? null : 'active' "></i>
            <i class="uil uil-moon" :class="darkTheme ? 'active' : null"></i>
          </div>
          <div class="profile">
            <div class="info">
              <p>Hey, <b>Khaled</b></p>
              <small class="text-muted">Admin</small>
            </div>
            <div class="profile-photo">
              <img src="./assets/profile-1.jpg" alt="" />
            </div>
          </div>
        </div>
        <div class="recent-updates">
          <h2>Recent Updates</h2>
          <div class="updates">
            <!--  -->
            <div class="update" v-for=" update in updates ">
              <div class="profile-photo">
                <img :src="update.src" alt="">
              </div>
              <div class="message">
                <p>
                  <b>{{update.username}}</b> {{update.notification}}
                </p>
                <small class="text-muted">{{update.time}}</small>
              </div>
            </div>
            <!--  -->
          </div>
        </div>
        <div class="sales-analytics">
          <h2>Sales Analytics</h2>
          <div class="item online">
            <div class="icon">
              <i class="uil uil-shopping-cart"></i>
            </div>
            <div class="rigth">
              <h3>Online Orders</h3>
              <small class="text-muted">Last 24 Hours</small>
            </div>
            <h5 class="success">+39%</h5>
            <h3>3849</h3>
          </div>
          <div class="item offline">
            <div class="icon">
              <i class="uil uil-shop"></i>
            </div>
            <div class="rigth">
              <h3>Ofline Orders</h3>
              <small class="text-muted">Last 24 Hours</small>
            </div>
            <h5 class="danger">-19%</h5>
            <h3>1200</h3>
          </div>
          <div class="item customers">
            <div class="icon">
              <i class="uil uil-shopping-cart"></i>
            </div>
            <div class="rigth">
              <h3>Online Orders</h3>
              <small class="text-muted">Last 24 Hours</small>
            </div>
            <h5 class="success">+39%</h5>
            <h3>3849</h3>
          </div>
          <div class="item add-product">
            <div>
              <i class="uil uil-plus"></i>
              <h3>Add product</h3>
            </div>
          </div>
        </div>
      </div>

    </div>
  </div>
</template>

<script>


import main from './components/main.vue'

export default {
  components: {
    'main-bar': main,
  },
  data() {
    return {
      isActive: null,
      darkTheme:false,
      updates:[{
  "username": "Feodor",
  "notification": "SM55 W524 5607 186N FIKU RU9M OLD",
  "src": "https://robohash.org/velitmodianimi.png?size=50x50&set=set1",
  "time": "12:05 PM"
}, {
  "username": "Camala",
  "notification": "IS28 8337 3134 7751 7478 8205 79",
  "src": "https://robohash.org/etnihilmolestias.png?size=50x50&set=set1",
  "time": "7:04 AM"
}, {
  "username": "Ole",
  "notification": "PS42 BOHJ INPJ IJNM 0L82 R43W EIYR 7",
  "src": "https://robohash.org/estquodconsectetur.png?size=50x50&set=set1",
  "time": "12:48 PM"
}, {
  "username": "Berna",
  "notification": "FO84 2327 2050 4010 05",
  "src": "https://robohash.org/doloribussedvoluptatem.png?size=50x50&set=set1",
  "time": "7:35 PM"
}, {
  "username": "Davide",
  "notification": "LI56 5196 6WU6 Q34E JO79 T",
  "src": "https://robohash.org/delectusnostrumblanditiis.png?size=50x50&set=set1",
  "time": "11:46 PM"
}]
    };
  },  methods: {
         active() {
            if (this.isActive == 'block') {
                this.isActive = 'none'
            } else {
                this.isActive = 'block'
            }
        }, changeTheme() {
      if (this.darkTheme == false) {
        document.body.classList.toggle('dark-theme-var')
        this.darkTheme = true;
      } else {
        document.body.classList.toggle('dark-theme-var')
        this.darkTheme = false;
      }
    },

    }
};

</script>
<style>

</style>
