<template>
  <div>
    <section class="hero is-fullheight is-default is-bold">
      <div class="hero-head">
          <!-- <nav class="navbar">
              <div class="container">
                  <div class="navbar-brand">
                      <a class="navbar-item" href="../">
                      </a>
                  </div>
              </div>
          </nav> -->
      </div>
      <div class="hero-body">
          <div class="container">
              <div class="columns is-vcentered pb-6">
                  <div class="column is-8">
                      <h1 class="title mb-5">
                          Hi, I'm Jaïr.
                      </h1>
                      <h2 class="subtitle is-4">
                          I'm a Software Engineer based in the Netherlands. Currently working as Software Developer at Effect.AI.
                          <!-- In case you have doubts on how to pronounce my name, <a href="#" @click="play">here you go.</a> -->
                      </h2>
                      <br>
                  </div>
                  <!-- <div class="column is-5 is-offset-1">
                      <figure class="image is-4by3">
                          <img src="https://picsum.photos/800/600/?random" alt="Description">
                      </figure>
                  </div> -->
              </div>
          </div>
      </div>
      <div class="down-icon has-text-centered pb-2">
        <font-awesome-icon :icon="['fa', 'angle-down']" class="icon alt"/>
      </div>
    </section>
    <About/>
    <Resume/>
    <Contact class="mb-6"/>
    <footer class="footer mt-6 h py-4 has-text-centered">
      Made by me
    </footer>
  </div>
</template>

<script>
import Resume from '@/components/Resume'
import About from '@/components/About'
import Contact from '@/components/Contact'
import AOS from 'aos'
import 'aos/dist/aos.css'

export default {
  name: 'Home',
  components: {
    Resume, 
    Contact,
    About
  },
  data () {
    return {
    }
  },
  methods: {
  },
  mounted() {
    AOS.init({once: true, duration: 800 })
  },
}
</script>
<style scoped lang="scss">
footer {
  font-family: $family-mono;
      font-size: .8rem;
}
.subtitle {
  line-height: 2.7rem !important;
}
img {
  border-radius: 10px;
}
a {
  font-size: 1.5rem;
  line-height: 2.7rem;
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

.down-icon {
	transform: translatey(0px);
	animation: float 3s ease-in-out infinite;
  i {
    font-size: 1.5rem;
  }
}

@keyframes float {
	0% { 
		transform: translatey(0px);
    color: $text;
	}
	50% {
		transform: translatey(-17px);
    color: #ccc;
	}
	100% {
		transform: translatey(0px);
    color: $text;
	}
}
</style>
