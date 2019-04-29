<script>
import fontawesome from "@fortawesome/fontawesome";
import brands from "@fortawesome/fontawesome-free-brands";
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';

fontawesome.library.add(brands);

export default {
  name: 'Contact',
  props: {
    
  },
  components: {
      FontAwesomeIcon
  },
  data() {
    return {
      
    }
  },
  mounted () {

  },
  beforeDestroy () {
    
  },
  methods: {

  },
  computed: {
  }
}
</script>

<template>
  <div class='Contact'>
    <div class='contactWrapper'>
        <h1>Let's Connect</h1>
        <p>Have any lingering thoughts or questions about me or my work? Feel free to contact me at...</p>
        <span>briangfelix@gmail.com</span>
        <div class='contactIcons'>
            <a target='_blank' href='https://github.com/Bryan-GF'>
                <font-awesome-icon :icon="['fab', 'github']"/>
            </a>
            <a target='_blank' href='https://www.linkedin.com/in/bryan-garciafelix/'>
                <font-awesome-icon :icon="['fab', 'linkedin']"/>
            </a>
        </div>
    </div>
  </div>
</template>



<style lang="less">

    .Contact {
        padding: 2rem 1rem 4rem 1rem; 
        margin-left: 8%;
        margin-right: 8%;  
        h1 {
            color: #ED202E;
            font-size: 2.5rem;
            font-weight: bold;
        }
        p {
            font-size: 1.5rem;
            font-weight: 600;
            line-height: 2.4rem;
        }

        span {
            font-size: 1.2rem;
            font-weight: 600;
            border-bottom: 5px solid #f7717a;
            &:hover {
                border-bottom: 5px solid #ED202E;
                cursor: pointer;
            }
        }
        .contactIcons {
            margin-top: 50px;
            svg {
                height: 50px;
                width: 50px;
                margin-right: 30px;
                color: #212121 !important;
                &:hover {
                    cursor: pointer;
                    color: black !important;
                }
            }
        }
    }



@media screen and (min-width: 765px) {
    .Contact {
      padding: 2rem 10vw 4rem 10vw;
      h1 {
          font-size: 2.8rem;
      }
      p {
          font-size: 1.6rem;
      }
      span {
        font-size: 1.4rem;
      }
        .contactIcons {
                svg {
                    height: 60px;
                    width: 60px;
                }
        }
    }
}

@media screen and (min-width: 1050px) {
    .Contact {
      h1 {
          font-size: 3.5rem;
      }
      p {
          font-size: 1.9rem;
      }
      span {
        font-size: 1.6rem;
      }
        .contactIcons {
            svg {
                height: 65px;
                width: 65px;
            }
        }
    }
}


</style>