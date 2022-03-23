<template>
  <section>
    <div class="container has-text-centered" data-aos="fade-left">
      <h2 class="title is-1 mt-5 mb-6">Resume</h2>
      <div class="columns mt-2">
        <div class="column is-three-fifths is-offset-one-fifth">
          <div class="tabs-wrapper">
            <div class="tabs">
              <ul>
                <li @click="tab = 'effect'" :class="{ 'is-active': tab === 'effect'}"><a>Effect.AI</a></li>
                <li @click="tab = 'emr'" :class="{ 'is-active': tab === 'emr'}"><a>EatMyRide</a></li>
                <li @click="tab = 'gemba'" :class="{ 'is-active': tab === 'gemba'}"><a>Gemba IOT</a></li>
                <li @click="tab = 'fbi'" :class="{ 'is-active': tab === 'fbi'}"><a>FBI Design</a></li>
              </ul>
            </div>
            <div class="content-wrap pl-5">
              <div id="pictures" class="tab-content" :class="{ 'is-active': tab === 'effect'}">
                <h3 class="title mb-1 is-5">Software Developer - Effect.AI</h3>
                <span class="date">February 2021 - Present</span>
                <p>Currently Software Developer @Effect.AI. Building the new version of decentralized microtasking platform Effect Force.</p>
                <div class="tags mt-4">
                  <span class="tag is-primary is-light">VueJS</span>
                  <span class="tag is-primary is-light">NodeJS</span>
                  <span class="tag is-primary is-light">SQL</span>
                  <span class="tag is-primary is-light">Python</span>
                  <span class="tag is-primary is-light">Blockchain Development</span>
                  <span class="tag is-primary is-light">HTML</span>
                  <span class="tag is-primary is-light">SASS/CSS</span>
                </div>
              </div>
              <div id="music" class="tab-content" :class="{ 'is-active': tab === 'emr'}">
                <h3 class="title mb-1 is-5">Mobile Developer - EatMyRide</h3>
                <span class="date">August 2020 - February 2021</span>
                <p>Mobile Developer @EatMyRide. Worked on the EatMyRide mobile application.</p>
                <div class="tags mt-4">
                  <span class="tag is-primary is-light">React Native</span>
                  <span class="tag is-primary is-light">SQL</span>
                  <span class="tag is-primary is-light">HTML</span>
                  <span class="tag is-primary is-light">SASS/CSS</span>
                </div>
              </div>
              <div id="videos" class="tab-content" :class="{ 'is-active': tab === 'gemba'}">
                <h3 class="title mb-1 is-5">Mobile Developer - Gemba IOT</h3>
                <span class="date">February 2019 - June 2019</span>
                <p>Mobile Developer @Gemba IOT. Building cross platform mobile apps. Also worked on NodeJS backends. </p>
                <div class="tags mt-4">
                  <span class="tag is-primary is-light">Javascript</span>
                  <span class="tag is-primary is-light">SQL</span>
                  <span class="tag is-primary is-light">NodeJS</span>
                  <span class="tag is-primary is-light">HTML</span>
                  <span class="tag is-primary is-light">SASS/CSS</span>
                </div>
              </div>
              <div id="documents" class="tab-content" :class="{ 'is-active': tab === 'fbi'}">
                <h3 class="title mb-1 is-5">Web Developer - FBI Design</h3>
                <span class="date">February 2016 - August 2020</span>
                <p>Web Developer @FBI Design developing websites and platforms for businesses big & small</p>
                <div class="tags mt-4">
                  <span class="tag is-primary is-light">PHP</span>
                  <span class="tag is-primary is-light">Javascript</span>
                  <span class="tag is-primary is-light">SQL</span>
                  <span class="tag is-primary is-light">Wordpress</span>
                  <span class="tag is-primary is-light">SASS/CSS</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: 'Home',
  data () {
    return {
      tab: 'effect'
    }
  },
}
</script>
<style scoped lang="scss">
.tabs-wrapper {
  display: flex;
}

.tabs {
  flex-grow: 2;
  min-width: 25%;
  margin-right: 30px;
  
  ul {
    display: block;
    text-align: left;
    border-bottom-color: transparent !important;
    
    li {
      display: block;
      transition: transform .3s ease;
      a {
        transition: border .3s ease;
        display: block;
        border-bottom-color: transparent !important;
        border-right: 2px solid #dbdbdb;
        transform-origin: top right;
      }
      &.is-active {
        a {
          border-right-color: $secondary;
        }
      }
    }
  }
}

.content-wrap {
  text-align: left;
  .tab-content {
    padding-top: 12px;
    display: none;
    animation: fadeInLeft .5s;
    
    &.is-active {
      display: block;
    }
    p {
      font-size: 1rem;
    }
    .date {
      font-family: $family-mono;
      font-size: 1rem;
      display: block;
      margin-bottom: 20px;
    }
  }
}


//Keyframes
@-webkit-keyframes fadeInLeft {
    from {
        -webkit-transform: translate3d(-20px, 0, 0);
        transform: translate3d(-20px, 0, 0);
        opacity: 0;
    }

    to {
        -webkit-transform: translate3d(0, 0, 0);
        transform: translate3d(0, 0, 0);
        opacity: 1;
    }
}

@keyframes fadeInLeft {
    from {
        -webkit-transform: translate3d(-20px, 0, 0);
        transform: translate3d(-20px, 0, 0);
        opacity: 0;
    }

    to {
        -webkit-transform: translate3d(0, 0, 0);
        transform: translate3d(0, 0, 0);
        opacity: 1;
    }
}

.fadeInLeft {
    opacity: 0;
    -webkit-animation-name: fadeInLeft;
    animation-name: fadeInLeft;
}

@media screen and (max-width: $tablet) {
  .tabs-wrapper {
    flex-direction: column;
  }
  .tabs {
    display: none;
  }
  .content-wrap {
    .tab-content {
      display: block !important;
      padding: 2rem 1rem;
      border-bottom: 1px solid #eee;
    }
  }
  .title {
    margin-bottom: 2rem !important;
  }
} 
</style>