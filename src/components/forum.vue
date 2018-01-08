
<template>
  <v-app light>
   <main>
     <v-content>
       <v-container>
         <v-layout row wrap align-center>
           <v-flex xs12 md4>
             <div class="text-xs-center">
               <v-avatar size="125px">
                 <img src="https://avatars0.githubusercontent.com/ananddharne" alt="">
               </v-avatar>
               <h3>Anand <span style="font-weight:bold">Dharne</span></h3>
               <h4 class="text-xs-center"> Social profiles</h4> <br>
               <v-layout justify-space-between>
                 <a href="https://github.com/ananddharne" target="_blank" class="body-2">Github</a>
                 <a href="https://www.linkedin.com/in/ananddharne/" target="_blank" class="body-2">LinkedIn</a>
                 <a href="https://www.facebook.com/anand.dharne" target="_blank" class="body-2">Facebook</a>
                 <a href="https://gitlab.com/ananddharne" target="_blank" class="body-2">Gitlab</a>
               </v-layout>
             </div>
           </v-flex>
           <v-flex xs12 md5 offset-md2>
             <div v-for="post in posts" :key="post.title">
               <v-card class="my-3" hover>
                 <v-card-media
                   class="white--text"
                   height="170px"
                   :src="post.imgUrl"
                 >
                   <v-container fill-height fluid>
                     <v-layout fill-height>
                       <v-flex xs12 align-end flexbox>
                         <span class="headline">{{ post.title }}</span>
                       </v-flex>
                     </v-layout>
                   </v-container>
                 </v-card-media>
                 <v-card-text>
                   {{ post.content }}
                 </v-card-text>
                 <v-card-actions>
                   <v-spacer></v-spacer>
                   <v-btn flat class="blue--text">Original source</v-btn>
                   <a :href="post.originalSource" target="_blank"> {{post.originalSourcetital}} </a>
                 </v-card-actions>
               </v-card>
             </div>
           </v-flex>
         </v-layout>
       </v-container>
     </v-content>
   </main>
   <v-footer class="secondary" app>
     <v-layout row wrap align-center>
       <v-flex xs12>
         <div class="white--text ml-3">
           Made with
           <v-icon class="red--text">favorite</v-icon>
           and Vue.js
         </div>
       </v-flex>
     </v-layout>
   </v-footer>
 </v-app>
 </template>

<script>
export default {
  name: 'forum',
  data () {
    return {
      title: 'Your Logo',
      posts: [
        {
          title: '7 Crypo-currencies to watch out for in 2018!',
          content: 'The crypto world is booming humungously! In my opinion, I feel this is one giant bubble paving its way to explode just like the market crash in 2008 or the fall of the dotcom revolution. However it doesnt hurt to make some money considering the bubble wont burst for another 20 years. Bitcoin seems to be the obvious choice to buy since it is the father of all crypto and too good to fall down any sooner while Etherium being the second best choice and Litecoin to follow. However, if you dont want to spend big bucks but still root for your future by investing in some interesting alt coins, take a sneak peek at this article. I bet my money on Cardano(Ada)  ',
          imgUrl: 'http://bottomstack.com/wp-content/uploads/2017/07/cryptocurrency.jpg',
          originalSourcetital: 'Crypocurrencies in 2k18!',
          originalSource: 'https://www.marketwatch.com/story/7-cryptocurrencies-to-watch-in-2018-if-youre-on-the-hunt-for-the-next-bitcoin-2017-12-12'
        },
        {
          content: 'This article really changed my life and helped me take an unconventional approach towards getting sh*it done. Almost every possible solution to stay on your goals and keep your life on track is discussed in this Reddit thread. Have been on my saved lists for the past 2 years. Thought I would share it with you guys. Please read the comments too, some of them are really helpful!',
          imgUrl: 'https://i.ytimg.com/vi/yQpjREmWOzg/maxresdefault.jpg',
          originalSourcetital: 'Get Disciplined',
          originalSource: 'https://www.reddit.com/r/getdisciplined/comments/4xwrut/advice_this_is_the_real_secret_to_successa/'
        },
        {
          content: 'The title says it all',
          imgUrl: 'https://camo.githubusercontent.com/a9730eef2d6a8e0586cde596c81e146f21171c03/68747470733a2f2f692e696d6775722e636f6d2f37767033366e682e706e67',
          originalSourcetital: 'dddd',
          originalSource: ''
        }
      ]
    }
  }
}
</script>
