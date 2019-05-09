<template>
  <div class="Projects">
    <h1>Projects</h1>
    <div class='projectContainer'>
      <div class='cardContainer rightContainer'>
        <div class='projectHeader right'>
          <h2>Erudition</h2>
        </div>
        <div class='projectContent rightContent'> 
          <div class='projectImage'>
            <img alt="Erudition screenshot" src="../assets/Erudition.jpg">
          </div>
          <div class='projectInfo'>
            <div class='projectStack'>
              <span>ReactJS</span>
              <span>NextJS</span>
              <span>Firebase</span>
              <span>Algolia</span>
              <span>Webpack</span>
              <span>MaterialUI</span>
            </div>
            <p>Learning made Social. Erudition is an app for people to find, store, share, and discuss online learning resource.</p>
            <div class='projectButtons'>
              <a class='leftTag' target='_blank' href='https://learned-app.now.sh/'>
                <button>Website</button>
              </a>
              <a class='rightTag' target='_blank' href='https://github.com/labs11-learned-1/labs11-learned1-FE'>
                <button>GitHub</button>
              </a>
            </div>
          </div>
        </div>
      </div>
      <div class='cardContainer leftContainer'>
        <div class='projectHeader left'>
          <h2>Jotter</h2>
        </div>
        <div class='projectContent leftContent'> 
          <div class='projectImage'>
            <img alt="Jotter screenshot" src="../assets/Jotter.png">
          </div>
          <div class='projectInfo'>
            <div class='projectStack'>
              <span>ReactJS</span>
              <span>Redux</span>
              <span>ExpressJS</span>
              <span>PostgreSQL</span>
              <span>Bcrypt</span>
              <span>CSS</span>
            </div>
            <p>Jotter is an app where users can create, store, and manage all their notes.</p>
            <div class='projectButtons'>
              <a class='leftTag' target='_blank' href='https://trusting-lichterman-9aca74.netlify.com/'>
                <button>Website</button>
              </a>
              <a target='_blank' href='https://github.com/Bryan-GF/Front-End-Notes' class='rightTag' >
                <button>GitHub</button>
              </a>
            </div>
          </div>
        </div>
      </div>
      <div class='cardContainer leftContainer'>
        <div class='projectHeader left'>
          <h2>Treasure Hunt</h2>
        </div>
        <div class='projectContent leftContent'> 
          <div class='projectImage'>
            <img alt="Treasure Hunt screenshot" src="../assets/treasurehunt.png">
          </div>
          <div class='projectInfo'>
            <div class='projectStack'>
              <span>ReactJS</span>
              <span>CSS</span>
              <span>Alogirthm Heavy</span>
            </div>
            <p>Treasure Hunt is a dungeon crawler-esque game. Watch the world build itself around you as you discover new rooms. Find treasure and sell it at the shop and build a fortune. What you do on your adventure is your decision.</p>
            <div class='projectButtons'>
              <a class='leftTag' target='_blank' href='https://condescending-shaw-7f2791.netlify.com/'>
                <button>Website</button>
              </a>
              <a target='_blank' href='https://github.com/Bryan-GF/Lambda-Treasure-Hunt' class='rightTag' >
                <button>GitHub</button>
              </a>
            </div>
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
              padding-left: 30px;
            }
            
          }

          
          
        .projectContent {
          display: flex;
          align-items: center;
          flex-direction: column;
          

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
            padding: 1rem 1rem 0 1rem;

            .projectStack {
              display: flex;
              flex-wrap: wrap;
              justify-content: center;
              span {
                border: 3px solid #ED202E;
                padding: .3rem;
                border-radius: 6px;
                font-weight: bold;
                margin: .2rem;
              }
            }
            p {
            width: 90%; 
            font-size: 1.1rem;
            text-align: center;
            }
            .projectButtons {
              margin-top: 1rem;

              a.leftTag {
                margin-left: none;
                margin-right: 1rem;
              }
              
              a.rightTag {
                margin-right: none;
                margin-left: 1rem;
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
  }

@media screen and (min-width: 600px) {
  .Projects {
    padding: 0 3rem 3rem 3rem;
  }
}

@media screen and (min-width: 765px) {
  .Projects {
    .projectContainer {
      .projectInfo {
        p {
          font-size: 1.3rem;
        }
      }

    }
    
  }
}
@media screen and (min-width: 975px) {
  .Projects {
    padding: 0 2rem 3rem 2rem;
    h1 {
      font-size: 3.5rem;
    }
    .projectContainer {
      .cardContainer {
        
        .projectHeader{
          h2 {
            font-size: 2.7rem;
          } 
        }
        
        .rightContent {
          flex-direction: row;
        }
        .leftContent {
          flex-direction: row;
        }
        .projectContent {
          display: flex;      
          .projectImage {
            width: 55%;
            padding: 0 1rem;
            img {
              width: 90%;
              display: block;
              margin: 0 auto;
            }
          }
          .projectInfo {
            width: 45%;
            padding: 0 0 0 0;
            p {
              font-size: 1.4rem;
              padding: 1vw 0;
            }
          }
        }
        
      }
    }
    
  }
}

@media screen and (min-width: 1300px) {
  .Projects {
    .projectContainer {
      width: 80%;
      margin: 0 auto;
      margin-top: 6rem;
    }
    
  }
}



</style>