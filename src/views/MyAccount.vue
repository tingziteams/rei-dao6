<template>
  <v-container class="myAccount stake_background">
     <div class="header-title">
      <h1>My Account</h1>
      <div class="title-detailed">Details about your account, balances, and voting</div>
    </div>
    <v-row>
      <v-col>
          <MyAccountBalance></MyAccountBalance>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <MyAccountCrude></MyAccountCrude>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <MyAccountNFT></MyAccountNFT>
      </v-col>
    </v-row>
  </v-container>
</template>
<script>
import MyAccountBalance from '../components/MyAccountBalance';
import MyAccountCrude from '../components/MyAccountCrude';
import MyAccountNFT from '../components/MyAccountNFT';
import { mapGetters } from 'vuex';
// import MyAccountProposals from '../components/MyAccountProposals';

export default {
  components:{
    MyAccountBalance,
    MyAccountCrude,
    MyAccountNFT
  },
  data() {
    return {
  
    };
  },
  computed: {
    ...mapGetters({
      connection: 'connection',
    })
  },
};
</script>

<style scoped lang="scss">
.header-title{
  margin: 1.5rem 0;
    .title-detailed{
      font-size: 14px;
      color: #868E9E;
    }
}
.myAccount{
  padding-left:40px;
  padding-right:40px;
}
@media screen and (max-width: 900px) {
  .myAccount{
    padding-left:20px;
    padding-right:20px;
  }
}
</style>
