<template>
  <header class="header-content header__padding">
    <h2>
      BLOND EXTREME
    </h2>
    <h3>O melhor e mais completo curso de loiros do mundo!</h3>
    <h4>El mejor y mas completo curso de rubios del mundo!</h4>
    <h5>The best and most complete blond course in the world!</h5>
    <div class="video">
      <div class="vimeo-formatter">
        <iframe
          src="https://player.vimeo.com/video/371866574"
          width="640"
          height="360"
          frameborder="0"
          allow="autoplay; fullscreen"
          allowfullscreen
        />
      </div>
      <script src="https://player.vimeo.com/api/player.js" />
    </div>
    <div class="align__button">
      <button type="button" class="sales__button" @click="redirectSales">
        <strong style="font-size: 2rem; color: #F5F5F5">Sim quero garantir minha vaga!</strong>
        <br>
        <strong style="font-size: 1.75rem; color: #F5F5F5">Si, quiero assegurar mi lugar!</strong>
        <br>
        <strong style="font-size: 1.5rem; color: #F5F5F5">Yes, I guarantee my course now!</strong>
      </button>
    </div>

    <div class="img-horizontal">
      <img alt="boleto" src="~/assets/img/creditcard/08.png">
      <img alt="american-express" src="~/assets/img/creditcard/american-express-logo-icon-png_44625.png">
      <img alt="diners" src="~/assets/img/creditcard/diners2.png">
      <img alt="hiper" src="~/assets/img/creditcard/hiper.png">
      <img alt="hipercard" src="~/assets/img/creditcard/hipercard.png">
      <img alt="mastercard" src="~/assets/img/creditcard/mastercard-25-675722.png">
      <img alt="visa" src="~/assets/img/creditcard/visa.png">
    </div>

    <p>Um conteúdo super especial por apenas R$ 297,00 em até 12 x R$ 28,94</p>
    <p class="p__espanhol">
      Un contenido super especial por sólo R$ 297,00 hasta 12 x R$ 28,94
    </p>
    <p class="p__english">
      Payment Methods: Super special content for only $ 297,00 up to 12 x $ 28,94
    </p>
  </header>
</template>

<script>
export default {

  name: 'Header',
  methods: {
    redirectSales () {
      window.location = 'https://pay.hotmart.com/R11503126C'
    }
  }
}

</script>

<style scoped>
  .header-content {
    background-color: black;
    color: #ffbb0e;
    font-family: inherit;
    z-index: -1;
    width: 100%;
    height: 100%;
  }

  h2 {
    font-size: 2.25rem;
    text-align: center;
    padding: 1.5rem 0;
    font-weight: bold;
  }

  h3 {
    font-size: 2.25rem;
    text-align: center;
  }

  h4 {
    font-size: 1.75rem;
    text-align: center;
  }

  h5 {
    font-size: 1.5rem;
    text-align: center;
  }

  p {
    font-size: 2rem;
    text-align: center;
  }

  img {
    height: 50px;
    width: 50px;
    margin: 1rem;
  }

  iframe {
    height: 480px;
  }

  .p__espanhol{
    font-size: 1.75rem;
    text-align: center;
  }

  .p__english{
    font-size: 1.5rem;
    text-align: center;
  }

  .img-horizontal {
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    margin: 1rem;
  }

  .vimeo-formatter {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    flex-wrap: nowrap;
  }

  .sales__button {
    padding: 1.25rem 2.5rem;
    font-family: open sans, sans-serif;
    color: white;
    background-color: #ff7710;
    border-radius: 5px 5px 5px 5px;
    border: 2px ridge #ff7710;
  }

  .align__button {
    display: flex;
    justify-content: center;
  }

  .header__padding {
    padding: 3rem 0;
  }

  @media screen and (max-width: 600px) {
    .video {
      margin-bottom: 1rem;
      width: 100%;
      height: 100%;
    }

    iframe {
      width: 100%;
      height: 100%;
    }

    button {
      width: 100%;
      height: 100%;
    }
  }
</style>
