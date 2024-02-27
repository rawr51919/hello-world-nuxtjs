<template>
  <div className="hello-style">
    <!-- this is a comment -->
    <div>{{message}}</div>
    <div>from {{name}}!</div>
    <div>{{2 + 2 + 5}}</div>
  </div>
  <div style={{goodbyeStyle}}>Goodbye from {{name}}</div>
  <div className="hello-style">
    <div v-for="letter in letters" :key="letter">
      {{letter === " " ? "-" : letter}}
    </div>
  </div>
  <div>Number of letters: {{letters.length}}</div>
</template>
<script>
  export default {
    data() {
      return {
        message: 'Hello World!',
        name: 'Colton Rushton',
        letters: [],
        goodbyeStyle: {
          color: '#FF0000',
          fontSize: '30px',
          fontWeight: 'bold',
          fontFamily: 'Courier New, sans-serif'
      }
    };
  },
  mounted() {
    this.letters = this.message.split("");
  }
};
</script>
