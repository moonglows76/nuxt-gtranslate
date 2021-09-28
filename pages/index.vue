<template>
  <div class="container">
    <p>東京</p>
    <p>おはようございます</p>
    <p>こんにちは</p>
    <p>おやすみなさい</p>
    <a href="#" @click="doGTranslate" data-lang="/ja/ja" title="Japanese" class="gflag nturl" style="background-position:-700px -100px;"><img src="https://gtranslate.net/flags/blank.png" height="32" width="32" alt="Japanese" /></a>
    <a href="#" @click="doGTranslate" data-lang="/ja/zh-CN" title="Chinese (Simplified)" class="gflag nturl" style="background-position:-300px -0px;"><img src="https://gtranslate.net/flags/blank.png" height="32" width="32" alt="Chinese (Simplified)" /></a>
    <a href="#" @click="doGTranslate" data-lang="/ja/en" title="English" class="gflag nturl" style="background-position:-0px -0px;"><img src="https://gtranslate.net/flags/blank.png" height="32" width="32" alt="English" /></a>
    <a href="#" @click="doGTranslate" data-lang="/ja/ko" title="Korean" class="gflag nturl" style="background-position:-0px -200px;"><img src="https://gtranslate.net/flags/blank.png" height="32" width="32" alt="Korean" /></a>


    <div id="google_translate_element"></div>
  </div>
</template>

<script>
export default {
  methods: {
    doGTranslate(e) {
      e.preventDefault()
      const lang = e.currentTarget.getAttribute('data-lang')
      this.$cookies.set('googtrans', lang)
      location.reload()
    },
  },
}
</script>


<style type="text/css">
a.gflag {vertical-align:middle;font-size:32px;padding:1px 0;background-repeat:no-repeat;background-image:url(//gtranslate.net/flags/32.png);}
a.gflag img {border:0;}
a.gflag:hover {background-image:url(//gtranslate.net/flags/32a.png);}
#goog-gt-tt {display:none !important;}
.goog-te-banner-frame {display:none !important;}
.goog-te-menu-value:hover {text-decoration:none !important;}
body {top:0 !important;}
#google_translate_element {display:none!important;}
</style>
