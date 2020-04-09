<template>
  <section class="content">
    <div id="section-3312541" klickart-edit-component-info="">
      <link rel="stylesheet" href="//static-public.klickpages.com.br/tmp/zip/1162/styles/main.css?v=1552592704">
      <section
        class="counter template-cris bottom"
        style="background-attachment: fixed;"
        data-klickart-delay-options="{&quot;enabled&quot;:false,&quot;selectedType&quot;:&quot;default&quot;,&quot;time&quot;:&quot;&quot;,&quot;dateTime&quot;:&quot;2019-09-25T16:47:57.543Z&quot;,&quot;timezone&quot;:&quot;-03:00&quot;,&quot;redirect&quot;:false,&quot;url&quot;:&quot;&quot;}"
      >
        <div
          class="component-bg"
          style="background-color: rgb(0, 0, 0);"
          klickart-edit-background-mask-visible="true"
        />
        <div class="container">
          <h3 class="title" style="color: rgb(255, 255, 255);">
            <b class="medium-b">O tempo está acabando!</b>
            <div>
              <font class="klickart-fontSize" style="font-size: 28px;">
                Se a acaba el tempo!
              </font><b
                class="medium-b"
              ><br></b>
            </div>
            <div>
              <font class="klickart-fontSize" style="font-size: 30px;">
                <i class="medium-i"><font
                  class="klickart-fontSize"
                  style="font-size: 29px;"
                >The time is ending!</font></i>
              </font>
            </div>
            <div><b class="medium-b"><font class="klickart-fontSize" style="font-size: 30px;"><br></font></b></div>
          </h3>
          <div class="description Medium Medium-rich" style="color: rgb(255, 255, 255); font-size: 24px;">
            Você vai ficar
            de fora?
            <div>
              <div>
                <font class="klickart-fontSize" style="font-size: 18px;">
                  Te vas quedar fuera?
                </font><br>
              </div>
              <div>
                <font class="klickart-fontSize" style="font-size: 18px;">
                  <i class="medium-i">You will be left
                    out?</i><br>
                </font>
              </div>
            </div>
          </div>
          <div
            class="countdown timer"
          >
            <countdown date="2019-11-18 23:59:59" />
            <div class="item days" style="background-attachment: scroll; background-color: rgb(255, 119, 16);">
              <div class="num" data-timer-replace="%D">
                {{ remaining.days }}
              </div>
              <div class="name Medium Medium-rich">
                dias
              </div>
            </div>
            <div class="item" style="background-attachment: scroll; background-color: rgb(255, 119, 16);">
              <div class="num" data-timer-replace="%H" style="color: rgb(255, 255, 255);">
                {{ remaining.hours }}
              </div>
              <div class="name">
                Horas
              </div>
            </div>
            <div class="item" style="background-attachment: scroll; background-color: rgb(255, 119, 16);">
              <div class="num" data-timer-replace="%M" style="color: rgb(255, 255, 255);">
                {{ remaining.minutes }}
              </div>
              <div class="name">
                Minutos
              </div>
            </div>
            <div class="item" style="background-color: rgb(255, 119, 16);">
              <div class="num" style="color: rgb(255, 255, 255);">
                {{ remaining.seconds }}
              </div>
              <div class="name">
                Segundos
              </div>
            </div>
          </div>
          <div
            style="display: none;"
            class="form-content"
            data-klickart-delay-options="{&quot;enabled&quot;:false,&quot;selectedType&quot;:&quot;default&quot;,&quot;time&quot;:&quot;&quot;,&quot;dateTime&quot;:&quot;2019-09-25T16:47:57.557Z&quot;,&quot;timezone&quot;:&quot;-03:00&quot;,&quot;redirect&quot;:false,&quot;url&quot;:&quot;&quot;}"
          >
            <a
              id="klickart-linkud2nvi7q8b800"
              class="general-button success modal-trigger"
              href="#"
              klickart-edit-not-highlight=""
              klickart-edit-link-type="default"
              klickart-edit-link-href-klickbox="#"
              klickart-edit-link-href-faq-question="#"
              style="background-attachment: scroll;"
            ><span><b
              class="medium-b"
            >GARANTIR MEU LUGAR AGORA MESMO!</b></span></a>
          </div>
        </div>
      </section>
    </div>
  </section>
</template>

<script>
import moment from 'moment'
export default {
  name: 'TimeRunningOut',
  props: {
    until: {
      type: String,
      default: 'April 13, 2020 23:59:59'
    },
    expiredText: { default: 'Now Expired' }
  },
  data () {
    return { now: new Date() }
  },
  computed: {
    finished () {
      return this.remaining.total <= 0
    },
    remaining () {
      const remaining = moment.duration(Date.parse(this.until) - this.now)
      if (remaining <= 0) { this.$emit('finished') }
      return {
        total: remaining,
        days: remaining.days(),
        hours: remaining.hours(),
        minutes: remaining.minutes(),
        seconds: remaining.seconds()
      }
    }
  },
  created () {
    this.refreshEverySecond()
  },
  methods: {
    refreshEverySecond () {
      // eslint-disable-next-line no-return-assign
      const interval = setInterval(() => this.now = new Date(), 1000)
      this.$on('finished', () => clearInterval(interval))
    }
  }
}
</script>

<style scoped>
  .content {
    background-color: #2c2f39;
  }
</style>
