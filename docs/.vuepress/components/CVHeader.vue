<template>
<div class="cv-header">
    <div>
        <h1>张建亚</h1>
    </div>
    <div class="container">
        <div class="item">
            <h4>Java 开发</h4>
        </div>
        <div class="item">
            <h4>北京，朝阳</h4>
        </div>
        <div class="item">
            <a href="mailto:codeworm@outlook.com">codeworm@outlook.com</a>
        </div>
        <div class="item">
            <a href="https://github.com/ZJianYa">github.com/ZJianYa</a>
        </div>
    </div>
</div>
</template>

<style lang="stylus" scoped>
.cv-header
    margin-bottom 1.5em

.container
    display: flex
    padding-bottom: 1em /* Padding bottom for mobile */
    border-bottom: 3px solid #cccccc
    flex-wrap: wrap

h1
  margin: 0

h4, a
  font-size: 130%
  margin: 0.2em 0 0 0
  padding: 0 0 0.2em 0
  font-weight: 600
  line-height: 1
  display block
//   margin-block-start: 1.33em
//   margin-block-end: 1.33em;


.item
  flex: 1
  min-width: 100%

@media (min-width: 768px)
  .cv-header
      margin-bottom 2.5em

  .item
    margin-bottom: 0.25em
    min-width: 50%
  

  .container
    margin-bottom: 2em /* Margin bottom for tablet+ */
    padding-bottom: 0
  

@media print
  .container
    margin-bottom: .5em /* Margin bottom for tablet+ */
    padding-bottom: .4rem
    display: block
    border-bottom: 2px solid #cccccc
    :not(:first-child)
      padding-left: 2em

  .item
    display: inline

  h4, a
    display inline
    font-size: 95%
    margin: 0.1em 0 0 0
    padding: 0 0 0.1em 0
  
  .cv-header
    margin-bottom 1rem
</style>

