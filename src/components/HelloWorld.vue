<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
<!--    <embed src="../assets/devResume.pdf" type="pdf">-->
    <PDFJSViewer :path="`${path}`" :fileName="`${name}`"/>
  </div>
</template>

<script>
import PDFJSViewer from "@/components/PDFJSViewer";
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  components: {
    PDFJSViewer
  },
  data() {
    return {
      name: 'devResume.pdf', //change which pdf file loads
      path: 'lib/pdfjs-2.3.200-dist/web/' //path of the PDF.js viewer.html
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
