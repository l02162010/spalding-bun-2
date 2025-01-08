<template>
  <div class="h-full flex flex-col justify-center items-center">
    <div class="flex justify-evenly w-full">
      <div @click="lang = 'zh-TW'">
        <Vue3Lottie :animationData="fireWork" :height="200" :width="200" />
      </div>
      <div></div>
      <div class="lottie-reverse" @click="lang = 'el-GR'">
        <Vue3Lottie :animationData="fireWork" :height="200" :width="200" />
      </div>
    </div>
    <div class="flex justify-evenly w-full">
      <div @click="lang = 'eff'">
        <Vue3Lottie :animationData="fireWork" :height="200" :width="200" />
      </div>
      <div class="text-center">
        <template v-if="lang === 'eff'">
          <div>
            ㄕ ㄅㄛˊ ㄐㄩㄣ，ㄕㄥ ㄖˋ ㄎㄨㄞˋ ㄌㄜˋ！
          </div>
          <div>
            ㄊㄧㄥ ㄕㄨㄛ ㄐㄧㄣ ㄊㄧㄢ ㄕˋ ㄋㄧˇ ㄉㄜ˙ ㄉㄚˋ ㄖˋ ㄗˇ。
          </div>
          <div>
            ㄖㄣˊ ㄕㄥ ㄓㄜˋ ㄊㄧㄠˊ ㄌㄨˋ ㄕㄤˋ，ㄒㄧ ㄨㄤˋ ㄋㄧˇ ㄩㄥˇ ㄩㄢˇ ㄒㄧㄤˋ ㄎㄞ ㄍㄨㄚˋ 
            ㄧ ㄧㄤˋ ㄗㄡˇ ㄉㄜ˙ ㄕㄨㄣˋ ㄈㄥ ㄕㄨㄣˋ ㄕㄨㄟˇ，ㄒㄧㄠˋ ㄉㄜ˙ ㄅㄧˇ ㄊㄞˋ ㄧㄤˊ ㄏㄞˊ ㄘㄢˋ ㄌㄢˋ，
            ㄕㄨㄞˋ ㄉㄠˋ ㄅㄧˇ ㄨㄛˇ ㄔㄚˋ ㄧˋ ㄉㄧㄢˇ。
          </div>
        </template>
        <template v-if="lang === 'zh-TW'">
          <div>
            施博鈞，生日快樂！
          </div>
          <div>
            聽說今天是你的大日子。
          </div>
          <div>
            人生這條路上，希望你永遠像開掛一樣走得順風順水，笑得比川普開心，帥到比我差一點。
          </div>
        </template>
        <template v-if="lang === 'en-US'">
          <div>
            Happy birthday, Bo-Jun Shih!
          </div>
          <div>
            I heard that today is your big day.
          </div>
          <div>
            In this journey of life, I hope you always move forward like you're in god mode, sail through smoothly, laugh harder than Trump, and be almost as handsome as me.
          </div>
        </template>
        <template v-if="lang === 'el-GR'">
          <div>
            Χρόνια πολλά, Μπο-Τζουν Σι!
          </div>
          <div>
            Άκουσα ότι σήμερα είναι η μεγάλη σου μέρα.
          </div>
          <div>
            Στο ταξίδι της ζωής, ελπίζω να προχωράς πάντα σαν να είσαι σε god mode, να πλέεις ομαλά, να γελάς πιο πολύ και από τον Τραμπ, και να είσαι σχεδόν τόσο όμορφος όσο εγώ.
          </div>
        </template>
        <template v-if="lang === 'dongbei-CN'">
          <div>
            哎呀！施博鈞！今兒過生日啊！
          </div>
          <div>
            今天是你大喜日子啊，真是嘎嘎帶勁兒啊！
          </div>
          <div>
            人這一輩子啊，就得像你這樣，干啥啥成，走哪兒哪兒順，老天都偏向你！
          </div>
          <div>
            笑得比地主家兒的傻兒子還燦爛，帥得那叫一個唬人！就是吧，還差我那麼一丟丟，哈哈！
          </div>
        </template>
        <template v-if="lang === 'me'">
          <div>好啦！祝你比我帥啦！</div>
          <div>生日快樂啦</div>
        </template>
      </div>
      <div class="lottie-reverse" @click="lang = 'dongbei-CN'">
        <Vue3Lottie :animationData="fireWork" :height="200" :width="200" />
      </div>
    </div>
    <div class="flex justify-evenly w-full">
      <div @click="lang = 'en-US'">
        <Vue3Lottie :animationData="fireWork" :height="200" :width="200" />
      </div>
      <div></div>
      <div class="lottie-reverse" @click="lang = 'me'">
        <Vue3Lottie :animationData="fireWork" :height="200" :width="200" />
      </div>
    </div>
  </div>


</template>

<script>
import { Vue3Lottie } from 'vue3-lottie'
import fireWork from './data/fireWork.json'

export default {
  name: 'App',
  components: {
    Vue3Lottie
  },
  data() {
    return {
      fireWork,
      lang: 'eff',
    }
  },
}
</script>

<style>
@font-face {
  font-family: 'elffont';
  src: url('./assets/fonts/elffont-rock.otf') format('opentype');
  font-weight: normal;
  font-style: normal;
}

#app {
  font-family: 'elffont', sans-serif;
  font-size: 2rem;
}

.lottie-reverse {
  transform: scaleX(-1); /* 水平镜像 */
}
</style>
