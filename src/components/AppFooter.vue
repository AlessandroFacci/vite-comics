<script>
export default {
  data() {
    return {
      underText: 0,
      imgLinks: [
        "../../public/img/buy-comics-digital-comics.png",
        "../../public/img/buy-comics-merchandise.png",
        "../../public/img/buy-comics-subscriptions.png",
        "../../public/img/buy-comics-shop-locator.png",
        "../../public/img/buy-dc-power-visa.svg",
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
          url: '#'
        },
        {
          link: "../../public/img/footer-twitter.png",
          url: '#'
        },
        {
          link: "../../public/img/footer-youtube.png",
          url: '#'
        },
        {
          link: "../../public/img/footer-pinterest.png",
          url: '#'
        },
        {
          link: "../../public/img/footer-periscope.png",
          url: '#'
        }
      ]
    };
  },
 
};
</script>
<template>
  <section>
    <img :src="imgLinks[0]" alt="img">
  </section>
  <section class="info-link">
    <!-- <img src="../../public/img/dc-logo-bg.png" alt=""> -->
    <ul>
      <li v-for="link in infoLinks">
        <a :href="link.url">{{ link.text }}</a>
          <li> 
            <a>{{ link.underLink[underText].text }}</a>
          </li>
      </li>
    </ul>
  </section>
  <section>
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
img{
  background-color: black;
}
.info-link{
  background-image: url(../../public/img/footer-bg.jpg);
  
}
 
</style>
