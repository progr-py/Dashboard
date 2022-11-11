<template>
      <div class="rigth">
        <div class="top">
          <button id="menu-btn" @click="active">
            <i class="uil uil-bars"></i>
          </button>
          <div class="theme-toggler" @click="changeTheme()">

            <i class="uil uil-sun " :class="darkTheme ? null : 'active'"></i>
            <i class="uil uil-moon" :class="darkTheme ? 'active' : null"></i>
          </div>
          <div class="profile">
            <div class="info">
              <p>Hey, <b>Khaled</b></p>
              <small class="text-muted">Admin</small>
            </div>
            <div class="profile-photo">
              <img src="../assets/profile-1.jpg" alt="" />
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
</template>
<script>
export default{
    data() {
        return {
            darkTheme: false,
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

        }
    },
    methods: {
    changeTheme() {
      if (this.darkTheme == false) {
        document.body.classList.toggle('dark-theme-var')
        this.darkTheme = true;
      } else {
        document.body.classList.toggle('dark-theme-var')
        this.darkTheme = false;
      }
    },
  getImage(imagePath) {
    return require(imagePath);
  }

  }

}
</script>