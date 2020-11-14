<template>
  <main>
    <template>
      <div class="container-fluid">
        <div class="container">
          <div class="top-banner">
            <div class="left-part"></div>
            <div class="right-part"></div>
          </div>
          <div class="wwm-info">
            <div class="heading">
              <h3>working with me</h3>
            </div>
            <div class="text">
              <p>
                We help companies to lead the pack. With innovative product
                design that solves real problems that people have. Explore our
                methods and approach.
              </p>
            </div>
          </div>

          <div class="center-banner"></div>

          <div class="fpvd-info">
            <div class="for-people">
              <div class="heading">
                <h4>for people</h4>
              </div>
              <div class="text">
                <p>
                  We design products for people. Product that make a real
                  improvement for the user in terms of safety, performance,
                  health or living conditions. Products that people will love.
                </p>

                <p>
                  We will help you to put the user's interests first all the
                  time.
                </p>
              </div>
            </div>
            <div class="vision-driven">
              <div class="heading">
                <h4>vision driven</h4>
              </div>
              <div class="text">
                <p>
                  We believe that good product design is based on vision and
                  strategy, not on democratic decision making. Easy consensus is
                  the enemy of great product design.
                </p>

                <p>
                  You hired us because we do something ou cannot. We will not
                  overload you with choice, but we will help to make good
                  decision.
                </p>
              </div>
            </div>
            <div class="action-area">
              <div class="heading"></div>
              <div class="text">
                <div class="action-button">want to talk?</div>
              </div>
            </div>
          </div>
          <div class="bottom-banner">
            <div class="gallery-images">
              <div class="top-gallery">
                <img src="/images/ahsaeed/DSCN1382.jpg" height="150px" alt="" />
                <img
                  src="/images/ahsaeed/Anita_Strozzi.jpg"
                  height="150px"
                  alt=""
                />
              </div>
              <div class="bottom-gallery">
                <img
                  src="/images/ahsaeed/Bier_Strozzi.jpg"
                  height="150px"
                  alt=""
                />
                <img src="/images/ahsaeed/DSCN1364.jpg" height="150px" alt="" />
              </div>
            </div>
            <div class="right-part"></div>
          </div>
          <div class="empty-banner"></div>
        </div>
      </div>
    </template>

    <script>
      export default {
        name: "newpage"
      };
    </script>

    <style scoped>
      .top-banner {
        display: flex;
        justify-content: flex-start;
        margin-top: 20px;
      }

      .top-banner .left-part {
        width: 60%;
        height: 300px;
        background: url("/images/ahsaeed/black_foldet.jpg") no-repeat left
          center;
        background-size: cover;
      }

      .top-banner .right-part {
        width: 40%;
        height: 300px;
        background: url("/images/ahsaeed/MCS_III_Auto_A4_Vitrine.jpg") no-repeat
          left center;
        background-size: cover;
      }

      .wwm-info {
        display: flex;
        justify-content: flex-start;
        margin-top: 20px;
      }

      .heading {
        width: 60%;
        display: flex;
        align-items: center;
        justify-content: center;
      }

      .heading h3 {
        text-align: center;
      }

      .text {
        width: 40%;
        display: flex;
        justify-content: flex-start;
      }

      .center-banner {
        margin-top: 20px;
        display: flex;
        justify-content: flex-start;
        height: 250px;
        background: url("/images/ahsaeed/banner-three.png") no-repeat left
          center;
        background-size: cover;
      }

      .fpvd-info .for-people,
      .fpvd-info .vision-driven,
      .fpvd-info .action-area {
        display: flex;
        justify-content: flex-start;
        margin-top: 20px;
      }

      .for-people .text,
      .vision-driven .text {
        display: flex;
        flex-direction: column;
      }

      .action-area .action-button {
        padding: 10px 20px;
        border: 2px solid black;
        border-radius: 2px;
        cursor: pointer;
      }

      .bottom-banner {
        margin-top: 20px;
        display: flex;
        justify-content: flex-start;
        height: 300px;
      }

      .bottom-banner .gallery-images {
        height: 150px;
        width: 40%;
      }

      .gallery-images .top-gallery {
        display: flex;
        justify-content: flex-start;
      }

      .gallery-images .bottom-gallery {
        display: flex;
        justify-content: flex-start;
      }

      .gallery-images img {
        height: 150px;
        width: 50%;
      }

      .bottom-banner .right-part {
        width: 60%;
        background: url("/images/ahsaeed/bue-e-slide.png") no-repeat left center;
        background-size: cover;
      }

      .empty-banner {
        margin: 20px 0;
        height: 60px;
        background-color: darkgray;
      }
    </style>
  </main>
</template>

<script>
import { mapState } from "vuex";
import IconBase from "~/components/IconBase.vue";
import IconMapPin from "~/components/IconMapPin.vue";

export default {
  components: {
    IconBase,
    IconMapPin
  },
  computed: mapState(["page", "users", "places"])
};
</script>

<style>
.mapboxgl-missing-css {
  display: none;
}
</style>

<style lang="scss" scoped>
main {
  padding-top: 20px;
  border-top: 1px solid #ddd;
  margin-top: 120px;
}

.places {
  img {
    float: left;
    margin: 0 15px 15px 0;
  }
  p {
    margin-top: 10px;
  }
  .location {
    padding: 10px 0;
  }
}

hr {
  border-top: 1px solid #ddd;
  border-bottom: none;
  margin-top: 15px;
}

.mapcontain {
  width: 35%;
  float: right;
  height: 400px;
  p {
    margin: 10px 0;
  }
  img {
    width: 100%;
  }
}

@media screen and (max-width: 600px) {
  .mapcontain {
    width: 100%;
    margin: 10px 0;
  }
}
</style>
