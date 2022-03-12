<template>
  <div class="home">
    <div id="ebook-id"></div>
  </div>
</template>

<script>
import Epub from 'epubjs'
global.epub = Epub
export default {
  name: 'Home',
  mounted () {
    this.book = new Epub('/2014_Book_Self-ReportedPopulationHealthA.epub')
    this.book.renderTo('ebook-id', {
      width: window.innerWidth,
      height: window.innerHeight
    }).display()
  }
}
</script>
