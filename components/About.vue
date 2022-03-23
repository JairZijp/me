<template>
  <section class="section mt-6 mb-6">
    <div class="container is-widescreen mt-6 mb-6">
      <div class="columns mt-6">
        <div class="column is-4 has-text-centered pr-6" data-aos="fade-right">
          <figure class="image">
            <img src="../assets/img/me.jpg" alt="me">
          </figure>
        </div>
        <div class="column is-three-fifths ml-6" data-aos="fade-left">
          <h2 class="title is-1 mb-5 mt-5 ml-6">About Me</h2>
          <p class="is-5 pl-6">
            My path in software development started in 2015 when I specialized mostly in the front end development of websites.
            As I went on, I developed a more complete skill set inlcuding back end and mobile development. 
            More recently I have started to work with blockchains to build decentralized applications.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>
<style scoped lang="scss">
section {
  padding-bottom: 6rem;
}
p {
  font-size: 1.5rem;
  line-height: 2.7rem;
}
img {
  border-radius: 10px;
  width: 40rem;
  height: auto;
  display: block;
  object-fit: cover;
}

figure {
  &:hover {
    img {
      top: -.7rem;
      left: -.7rem;
    }
    &:after {
      top: 1.3rem;
      left: 1.3rem;
    }
  }
  
  &:after {
    border-radius: 10px;
    content:'';
    position: absolute;
    width: 100%;
    height: 100%;
    z-index: -1;
    transition: .3s ease;
  }

  img {
    transition: .3s ease;
  }
  
  &:after {
    background: $secondary;
    top: 1rem;
    left: 1rem;
  }
}
@media screen and (max-width: $tablet) {
  .pl-6 {
    padding-left: 0 !important;
  }
  div.ml-6 {
    margin-left: 0 !important;
  }
  p {
    font-size: 1.3rem;
    line-height: 2.4rem;
  }
  .mt-6 {
    margin-top: 1rem !important;
  }
  .mb-6 {
    margin-bottom: 0 !important;
  }
  .is-two-fifths {
    margin-bottom: 1.5rem;
  }
}
</style>