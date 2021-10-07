<template>
  <section>
    <nav>
      <nuxt-link to="/">Inspirational Quotes</nuxt-link>
    </nav>
    <main>
      <div>
        <h2>फक्त जिंकणाराच नाही तर कुठं हरावं हे कळणारा सुद्धा महान असतो!</h2>
        <img 
          width="80%"
          src="/splash.jpg" 
          alt="Inspirational Quotes">
          <br>
        <nuxt-link to="/quotes" class="quoteBtn">प्रेरणादायी सुविचार</nuxt-link>
      </div>
    </main>
  </section>
</template>

<script>

export default {
  head() {
    return {
      title: 'Best Motivational Quotes',
      meta: [
        { name: "description", content: "अपयश हे जणू माणसाच्या जीवनालाच चीकटलेले आहे. मात्र अपयशाविणा यशाची चव देखील चाखता येत नाही"  },
        { name: "shortcut icon", content: "❤️"  },
        { name: "twitter:card", content: "summary_large_image" },
        { name: "twitter:site", content: "@marathideveloper" },
        { name: "twitter:title", content: "Motivational Quotes" },
        { name: "twitter:description", content: "मात्र अपयशाविणा यशाची चव देखील चाखता येत नाही." },
        { name: "twitter:creator", content: "@marathideveloper" },
        { name: "twitter:image", content: "social image" },
        { property: "og:title", content: "Best Motivational Quotes"  },
        { property: "og:type", content: "website"  },
        { property: "og:url", content: "http://marathideveloper.in"  },
        { property: "og:image", content: "social image"  },
        { property: "og:image:secure_url", content: "social image"  },
        { property: "og:description", content: "Best Motivational Quotes"  }, 
        { property: "og:site_name", content: "Best Motivational Quotes"  },
      ],
      link: [
        { rel: "shorcut icon", href: "http://marathideveloper/favicon.png" }
      ]
    }
  }
}
</script>

<style>
  nav {
    position: fixed;
    top: 0;
    right: 0;
    left: 0;
    height: 56px;
    background: rgb(64 19 19);
    box-shadow: 0 1px 3px pink;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  nav a {
    color: white;
    text-decoration: none;
    font-size: 1.5em;
    font-weight: lighter;
  }

  main {
    margin-top: 56px;
    min-height: calc(100vh - 56px);
    display: flex;
    align-items: center;
  }

  main div {
    margin: 0 auto;
    flex-basis: 90%;
    text-align: center;
  }

  main div h1 {
    font-size: 3em;
    font-weight: lighter;
    text-align: center;
    margin: 20px 0;
  }

  main div img {
    border-radius: 10px;
    box-shadow: 1px 1px 3px rgba(0, 0, 0, 0.3);
  }

  main div .quoteBtn {
    background:  rgb(255, 51, 51);
    border: 0;
    padding: 1.2em;
    color: white;
    font-size: 1.3em;
    text-decoration: none;
    margin-top: 20px;
    border-radius: 10px;
    box-shadow: 1px 1px 3px rgba(0, 0, 0, 0.3);
    transition: all 100ms ease-in-out;
  }

  @media screen and (min-width: 768px) {
    main div img {
      width: 50%;
    }
  }
</style>
