<template>
  <div class="container">
    <div class="textcloud">
      <ul class="cloud" role="navigation" aria-label="Webdev word cloud">
        <li><a data-weight="4" href="#">HTTP</a></li>
        <li><a data-weight="2" href="#">Ember</a></li>
        <li><a data-weight="5" href="#">Sass</a></li>
        <li><a data-weight="8" href="#">HTML</a></li>
        <li><a data-weight="6" href="#">FlexBox</a></li>
        <li><a data-weight="4" href="#">API</a></li>
        <li><a data-weight="5" href="#">VueJS</a></li>
        <li><a data-weight="6" href="#">Grid</a></li>
        <li><a data-weight="3" href="#">Rest</a></li>
        <li><a data-weight="9" href="#">JavaScript</a></li>
        <li><a data-weight="3" href="#">Animation</a></li>
        <li><a data-weight="7" href="#">React</a></li>
        <li><a data-weight="8" href="#">CSS</a></li>
        <li><a data-weight="1" href="#">Cache</a></li>
        <li><a data-weight="3" href="#">Less</a></li>
      </ul>
    </div>
  </div>
</template>

<script>
  export default {

  }

</script>

<style lang="scss" scoped>
  .container {
    margin: 0 auto;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
  }

  html,
  body {
    height: 100vh;
    width: 100vw;
    margin: 0;
    padding: 0;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  ul.cloud {
    list-style: none;
    padding-left: 0;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
    line-height: 2.75rem;
    max-width: 600px;
  }

  ul.cloud a {
    /*   
  Not supported by any browser at the moment :(
  --size: attr(data-weight number); 
  */
    --size: 4;
    --color: #a33;
    color: var(--color);
    font-size: calc(var(--size) * 0.25rem + 0.5rem);
    display: block;
    padding: 0.7rem 0.5rem;
    position: relative;
    text-decoration: none;
    /* 
  For different tones of a single color
  opacity: calc((15 - (9 - var(--size))) / 15); 
  */
  }

  ul.cloud a[data-weight="1"] {
    --size: 1;
  }

  ul.cloud a[data-weight="2"] {
    --size: 2;
  }

  ul.cloud a[data-weight="3"] {
    --size: 3;
  }

  ul.cloud a[data-weight="4"] {
    --size: 4;
  }

  ul.cloud a[data-weight="5"] {
    --size: 6;
  }

  ul.cloud a[data-weight="6"] {
    --size: 8;
  }

  ul.cloud a[data-weight="7"] {
    --size: 10;
  }

  ul.cloud a[data-weight="8"] {
    --size: 13;
  }

  ul.cloud a[data-weight="9"] {
    --size: 16;
  }

  ul[data-show-value] a::after {
    content: " ("attr(data-weight) ")";
    font-size: 1rem;
  }

  ul.cloud li:nth-child(2n+1) a {
    --color: #181;
  }

  ul.cloud li:nth-child(3n+1) a {
    --color: #33a;
  }

  ul.cloud li:nth-child(4n+1) a {
    --color: #c38;
  }

  ul.cloud a:focus {
    outline: 1px dashed;
  }

  ul.cloud a::before {
    content: "";
    position: absolute;
    top: 0;
    left: 50%;
    width: 0;
    height: 100%;
    background: var(--color);
    transform: translate(-50%, 0);
    opacity: 0.15;
    transition: width 0.25s;
  }

  ul.cloud a:focus::before,
  ul.cloud a:hover::before {
    width: 100%;
  }

  @media (prefers-reduced-motion) {
    ul.cloud * {
      transition: none !important;
    }
  }

</style>
