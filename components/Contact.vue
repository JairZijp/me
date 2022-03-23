<template>
  <section class="section mb-6" data-aos="fade-right">
    <div class="container mb-6">
      <div class="columns mb-6">
        <div class="column is-three-fifths is-offset-one-fifth has-text-centered mt-6 mb-6">
          <h2 class="has-text-centered title is-1 mb-5">Get In Touch</h2>
          <p class="is-5 pb-3">
            Whether you have a question or just want to say hi, you can contact me via <a target="_blank" href="mailto: jairzijp123@gmail.com">email</a> or on <a target="_blank" href="#">LinkedIn</a>.
          </p>
          <div class="mt-5 icons is-flex">
            <a target="_blank" href="https://github.com/JairZijp">
              <font-awesome-icon :icon="['fab', 'github']" class="icon alt"/>
            </a>
            <a href="https://www.linkedin.com/in/ja%C3%AFr-zijp-424657104/" target="_blank">
              <font-awesome-icon :icon="['fab', 'linkedin-in']" class="icon alt"/>
            </a>
            <a href="mailto: jairzijp123@gmail.com" target="_blank">
              <font-awesome-icon :icon="['fa', 'envelope']" class="icon alt"/>
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<style scoped lang="scss">
p, a {
  font-size: 1.5rem;
  line-height: 2.7rem;
}

a {
  display: inline-block;
  position: relative;
  &:before {  
    transform: scaleX(0);
    transform-origin: top right;
  }
  &:hover {
    color: $secondary;
  }
  
  &:hover::before {
    transform: scaleX(1);
    transform-origin: top left;
  }
  
  &:before {
    content: " ";
    display: block;
    position: absolute;
    right: 0; bottom: 5px; left: 0;
    top: auto;
    height: 3px;
    background: $secondary;
    z-index: -1;
    transition: transform .3s ease;
  }
}

.icons {
  justify-content: center;
  svg {
    width: 35px;
    height: 35px;
    padding: 0 18px;
  }
  a {
    display: block;
    color: $text;
    transition: .3s ease;
    &:before {
     display: none;
    }
    &:hover {
      margin-top: -5px;
    }
  }
}
</style>