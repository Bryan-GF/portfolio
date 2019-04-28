<template>
  <div class="Projects">
    <h1>Projects</h1>
    <div class='projectContainer'>
      <div class='cardContainer'>
        <div class='projectHeader right'>
          <h2>Erudition</h2>
        </div>
        <div class='projectImage'>
          <img alt="Erudition screenshot" src="../assets/Erudition.jpg">
        </div>
        <div class='projectInfo'>
          <p>Learning made Social. Erudition is an app for people to find, store, share, and discuss online learning resource.</p>
          <div class='projectButtons'>
            <a target='_blank' href='https://learned-app.now.sh/'>
              <button>Website</button>
            </a>
            <a target='_blank' href='https://github.com/labs11-learned-1/labs11-learned1-FE'>
              <button>Github</button>
            </a>
          </div>
        </div>
      </div>
      <div class='cardContainer'>
        <div class='projectHeader left'>
          <h2>Jotter</h2>
        </div>
        <div class='projectImage'>
          <img alt="Jotter screenshot" src="../assets/Jotter.png">
        </div>
        <div class='projectInfo'>
          <p>Jotter is an app where users can create, store, and manage all their notes.</p>
          <div class='projectButtons'>
            <a target='_blank' href='https://trusting-lichterman-9aca74.netlify.com/'>
              <button>Website</button>
            </a>
            <a target='_blank' href='https://github.com/Bryan-GF/front-end-project-week'>
              <button>Github</button>
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Projects',
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
  .Projects {
    padding: 0 1rem 3rem 1rem;
    background: rgba(0,0,0,0.05);

    h1 {
        color: black;
        font-size: 2.5rem;
        font-weight: bold;
        padding-top: 90px;
        padding-bottom: 10px;
        margin: 0;
        border-bottom: 8px solid #ED202E;
        max-width: 500px;
        color: #212121;
    }

    .projectContainer {
      margin-top: 100px;
      

      .cardContainer {
        display: flex;
        align-items: center;
        border-radius: 10px;
        flex-direction: column;
        padding-top: 2rem;
        padding-bottom: 2rem;
        overflow:hidden;
        background: white;
        margin-bottom: 90px;
        
        .projectHeader{
          padding-bottom: 2rem;
          width: 100%;
          display: flex;
          flex-wrap: wrap;
          justify-content: center;

          h2 {
            margin: 0;
            font-size: 2.3rem;
            width: 100%;
          }
          
        }

        .right {
          h2 {
            text-align: end;
            padding-right: 30px;
          } 
        }

        .left {
          h2 {
            text-align: start;
            padding-left: 30px;
          } 
        }

        .projectImage {
          width: 90%;
          img {
            width: 100%;
            border-top: 6px solid #ED202E;
            border-bottom: 6px solid #ED202E;
          }
        }

        .projectInfo {
          display: flex;
          justify-content: center;
          flex-wrap: wrap;
          padding-top: 1rem;
          p {
           width: 90%; 
           font-size: 1.1rem;
           text-align: center;
          }
          .projectButtons {
            margin-top: 1rem;

            a {
              margin: 1rem 1rem;
            }

            button {
              background: white;
              border: none;            
              outline: none;              
              padding: 1rem 1rem;
              font-size: 1.5rem;
              font-weight: 600;
              width: 130px;
              background: #ED202E;
              color: white;
              &:hover {
                  cursor: pointer;
                  background: #f7717a;
              }
            }
          }
        }
      }     
    }
  }

</style>