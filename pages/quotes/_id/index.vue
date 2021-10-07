<template>
  <div id="quoteCard">
    <h1>{{ quote.author }}</h1>
    <hr>
    <p>{{ quote.body }}</p>
  </div>
</template>
<script>
export default {
  computed: {
    quotes() {
      return [{
    id: '1',
    body: 'Quote of the day.',
    author: 'John Snow'
  },
   {
    id: '2',
    body: '“You must be the change you wish to see in the world.”',
    author: 'Mahatma Gandhi'
  },
  {
    id: '3',
    body: 'Success is a relative term. More success, more relatives.”',
    author: 'V.P.Kale'
  }, {
    id: '4',
    body: '“पुस्तकांच्या सहवासात शांत आयुष्य वेचण्यासारखा दुसरा आनंद नाही.”',
    author: 'Mahatma Gandhi'
  }, {
    id: '5',
    body: 'महत्व वेगाला नाही तर आपण त्या वेगाने कोणत्या दिशेला चाललोय याला असत.',
    author: 'Unknown'
  }, {
    id: '6',
    body: ' आयुष्य मगरीसारखं जगायचं जेव्हा perfect झडप मारायची असेल तेव्हाच हालचाल करायची. ',
    author: 'Unknown'
  },
  {
    id: '7',
    body: 'एक वेळेस दहा काम करण्यापेक्षा दहा वेळेस एकच काम करा यश नक्कीच तुमच्या हातात येईल.',
    author: 'Unknown'
  },
  {
    id: '8',
    body: 'कधी कधी हक्क मागून मिळत नाहीत, ते मिळवावे लागतात...',
    author: 'Mahatma Gandhi'
  }, {
    id: '9',
    body: 'जर भविष्यात राजासारखे जगायाचे असेल तर आज संयम हा खुप कडवट असतो पण त्याच फळ फार गोड असते..',
    author: 'Mahatma Gandhi'
  },
  {
    id: '10',
    body: '"Life is trying things to see if they work."',
    author: 'Ray Bradbury'
  }
]
    },
    quote() {
      const param = this.$route.params.id
      const quote = this.quotes[this.quotes.findIndex(x => x.id.toString() === param)];
      return quote
    }
  },
  head() {
    return {
      title: 'Best Motivational Quotes',
      meta: [
        { name: "description", content: this.quote.body + ' - ' + this.quote.author },
        { name: "shortcut icon", content: "❤️"  },
        { name: "twitter:card", content: "summary_large_image" },
        { name: "twitter:site", content: "@marathideveloper" },
        { name: "twitter:title", content: "Best Motivational Quotes" },
        { name: "twitter:description", content: this.quote.body + ' - ' + this.quote.author },
        { name: "twitter:creator", content: "@marathideveloper" },
        { name: "twitter:image", content: "http://marathideveloper/social.jpg" },
        { property: "og:title", content: this.quote.body  },
        { property: "og:type", content: "website"  },
        { property: "og:url", content: "http://marathideveloper/"+this.quote.id  },
        { property: "og:image", content: "http://marathideveloper/social.jpg"  },
        { property: "og:image:secure_url", content: "http://marathideveloper/social.jpg"  },
        { property: "og:description", content: this.quote.body + ' - ' + this.quote.author  }, 
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
#quoteCard {
    width: 70%;
    border: 0.5px solid #eb6d13;
    box-shadow: -1px 2px 15px 3px rgb(225 30 30 / 83%);
    padding: 1.5em;
    margin: 1.5em auto;
    margin-top: 200px;
}
</style>
