<script>
export default {
  data() {
    return {
      underText: 0,
      imgLinks: [
        {
          link: "../../public/img/buy-comics-digital-comics.png",
          url: '#',
          text: "DIGITAL COMICS"
        },
        {
          link: "../../public/img/buy-comics-merchandise.png",
          url: '#',
          text: "DC MERCHANDISE"
        },
        {
          link: "../../public/img/buy-comics-subscriptions.png",
          url: '#',
          text: "SUBSCRIPTION"
        },
        {
          link: "../../public/img/buy-comics-shop-locator.png",
          url: '#',
          text: "COMIC SHOP LOCATOR"
        },
        {
          link: "../../public/img/buy-dc-power-visa.svg",
          url: '#',
          text: "DC POWER VISA"
        },  
      ],
      infoLinks: [
        {
          text: "DC COMICS",
          url: "#",
          underLink: [
            {
              text: "Character",
              url: "#",
            },
            {
              text: "Comics",
              url: "#",
            },
            {
              text: "Movies",
              url: "#",
            },
            {
              text: "TV",
              url: "#",
            },
            {
              text: "Games",
              url: "#",
            },
            {
              text: "Videos",
              url: "#",
            },
            {
              text: "News",
              url: "#",
            },
          ],
        },
        {
          text: "SHOP",
          url: "#",
          underLink: [
            {
              text: "Shop DC",
              url: "#",
            },
            {
              text: "Shop DC Collectibles",
              url: "#",
            },
          ],
        },
        {
          text: "DC",
          url: "#",
          underLink: [
            {
              text: "Terms Of Use",
              url: "#",
            },
            {
              text: "Privacy policy (New)",
              url: "#",
            },
            {
              text: "Ad Choices",
              url: "#",
            },
            {
              text: "Advertising",
              url: "#",
            },
            {
              text: "Jobs",
              url: "#",
            },
            {
              text: "Subscriptions",
              url: "#",
            },
            {
              text: "Talent Workshops",
              url: "#",
            },
            {
              text: "CPSC Certificates",
              url: "#",
            },
            {
              text: "Ratings",
              url: "#",
            },
            {
              text: "Shop Help",
              url: "#",
            },
            {
              text: "Contact Us",
              url: "#",
            },
          ],
        },
        {
          text: "SITES",
          url: "#",
          underLink: [
            {
              link: "DC",
              url: "#",
            },
            {
              text: "Mad Magazine",
              url: "#",
            },
            {
              text: "DC Kids",
              url: "#",
            },
            {
              text: "DC Universe",
              url: "#",
            },
            {
              text: "DC Power Visa",
              url: "#",
            },
          ],
        },
      ],
      socialLinks: [
        {
          link: "../../public/img/footer-facebook.png",
          url: '#',
        },
        {
          link: "../../public/img/footer-twitter.png",
          url: '#',
          
        },
        {
          link: "../../public/img/footer-youtube.png",
          url: '#',
          
        },
        {
          link: "../../public/img/footer-pinterest.png",
          url: '#',
          
        },
        {
          link: "../../public/img/footer-periscope.png",
          url: '#',
        }
      ]
    };
  },
 
};
</script>

   
<template>

  <!-- first section -->
  <section class="img-section">
    <div  v-for="img in imgLinks">
      <a :href="img.url">
        <div>
          <img :src="img.link" alt="img">
        </div>
        <div>
          <p>{{ img.text }}</p>
        </div>
      </a>
    </div>
  </section>

  <!-- second section -->
  <section class="info-section">
    <!-- <img src="../../public/img/dc-logo-bg.png" alt=""> -->
    <ul>
      <li v-for="link in infoLinks">
        <a class="title-link"  :href="link.url">{{ link.text }}</a>
          <li> 
            <a class="under-link">{{ link.underLink[underText].text }}</a>
          </li>
      </li>
    </ul>
  </section>

  <!-- third section -->
  <section class="social-section">
    <div>
      <button>SIGN-UP NOW</button>
    </div>
    <div>
      <ul>
        <li><a href="#">FOLLOW US</a></li>
        <li v-for="img in socialLinks">
          <a :href="img.url">
            <img :src="img.link" alt="social">
          </a>
      </li>
      </ul>
    </div>
  </section>
</template>


<style lang="scss" scoped>

// first section  
.img-section{
  width: 100%;
  height: 200px;
  background-color: #0082f9;
  display: flex;
  justify-content: center;
  align-items: center;
    a{
      text-decoration: none;
      color: white;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 0 1.5rem;
      img {
        width: 60px;
      }
      p {padding: 1rem;
      }
    }
}

// second section
.info-section{
  background-image: url(../../public/img/footer-bg.jpg);
  background-size: cover;
  width: 100%;
  height: 500px;
  a {
    text-decoration: none;
  }
.title-link{
  color: white; 
}

.under-link{
  color: gray;
}

  
}

// third section

.social-section {
  width: 100%;
  height: 100px;
  background-color: #303030;
  display: flex;
  justify-content: space-around;
  align-items: center;
  button {
    color: white;
    background-color: #303030;
    padding: 0.8rem 1rem;
    border: 3px solid #0b78ec;
  }
  ul {
    list-style-type: none;
    display: flex;
    justify-content: center;
    align-items: center;
    li {
      padding: 0 1rem;
      a {
        text-decoration: none;
        color: #0b78ec;
      }
    }
  }
}
</style>
