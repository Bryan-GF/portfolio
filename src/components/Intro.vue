<template>
  <div class="Intro">
    <div class='introBody'>
        <h1>Hey there!</h1>
        <p>I'm Bryan Garcia-Felix, the full stack developer you might want to hire. Welcome to my <span class="portfolio">portfolio!</span></p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Intro',
  props: {
    
  },
  data() {
    return {
      //State
    }
  },
  mounted () {
      
  },
  beforeDestroy () {
    
  },
  methods: {
    
  }
}
</script>

<style lang="less">

.Intro {
  padding: 0 1.5rem 4rem 1.5rem;
  
}

.introBody {
  margin-top: 5rem;
    h1 {
        color: #ED202E;
        font-size: 2.5rem;
        font-weight: bold;
    }
    p {
        font-size: 2.2rem;
        .portfolio {
            color: #ED202E;
            font-weight: bold;
        }
    }
    margin-bottom: 3.5rem;
}

.introButton {
    button {
        background: white;
        border: 5px solid  #ED202E;
        box-shadow: 0 6px 10px 0 lightgray;
        color: #ED202E;
        font-size: 1.2rem;
        font-weight: bold;
        padding: 1rem 1rem;
        outline: none;

        &:hover {
            cursor: pointer;
            box-shadow: 0 6px 10px 0 #ED202E;
        }
    }
}

@media screen and (min-width: 600px) {
    .Intro {
      padding: 0 4rem 4rem 4rem;
      height: 30vh;
    }
    .introBody {
      margin-top: 5rem;
    }
}

@media screen and (min-width: 765px) {
    .Intro {
      padding: 5rem 15vw 2rem 15vw;
      height: 70vh;
    }
    .introBody {
      margin-top:3rem;
      h1 {
        font-size:3.5rem;
      }
      p {
        font-size: 3.5rem;
      }
    }
}

@media screen and (min-width: 1200px) {
  .introBody {
      margin-top:8rem;
  }
}

</style>