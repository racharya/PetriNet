<template>
  <div class="navbar navbar-default navbar-fixed-top">
    <div class="container-fluid">
    <h1>Petri Net</h1>
    <div class="btn-group navbar-btn">
        <button class="btn btn-secondary btn-sm" id="place-button" v-on:click=addPlace()>
          <span class="glyphicon glyphicon-plus"></span> Place
        </button>
        <button class="btn btn-secondary btn-sm" id="transition-button">
          <span class="glyphicon glyphicon-plus"></span> Transition
        </button>
        <button class="btn btn-secondary btn-sm" id="transition-button">
          <span class="glyphicon glyphicon-plus"></span> + Tokens
        </button>
        <button class="btn btn-secondary btn-sm" id="transition-button">
          <span class="glyphicon glyphicon-plus"></span> - Tokens
        </button>
        <button class="btn btn-secondary btn-sm" id="remove-button">
          <span class="glyphicon glyphicon-remove"></span> Remove
        </button>
        <button class="btn btn-secondary btn-sm" id="clear-button">
          <span class="glyphicon glyphicon-remove-circle"></span> Clear
        </button>
        <button class="btn btn-secondary btn-sm" id="run-button">
          <span class="glyphicon glyphicon-remove-circle"></span> Run
        </button>
        <button class="btn btn-secondary btn-sm" id="stop-button">
          <span class="glyphicon glyphicon-remove-circle"></span> Stop
        </button>
        <button class="btn btn-secondary btn-sm" id="new-button">
          <span class="glyphicon glyphicon-remove-circle"></span> New
        </button>
        <button class="btn btn-secondary btn-sm" id="save-button">
          <span class="glyphicon glyphicon-remove-circle"></span> Save
        </button>
        <button class="btn btn-secondary btn-sm" id="restore-button">
          <span class="glyphicon glyphicon-remove-circle"></span> Restore
        </button>
        <button class="btn btn-secondary btn-sm" id="open-button">
          <span class="glyphicon glyphicon-remove-circle"></span> Open
        </button>
        <button class="btn btn-secondary btn-sm" id="download-button">
          <span class="glyphicon glyphicon-remove-circle"></span> Download
        </button>
  <div class="btn-group" role="group">
    <button id="btnGroupDrop1" type="button" class="btn btn-secondary dropdown-toggle" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
      Examples
    </button>
    <div class="dropdown-menu" aria-labelledby="btnGroupDrop1">
      <a class="dropdown-item" href="#">Water</a>
      <a class="dropdown-item" href="#">Vending Machine</a>
      <a class="dropdown-item" href="#">Dining Philosophers</a>
      <a class="dropdown-item" href="#">Communication Protocol</a>
      <a class="dropdown-item" href="#">Readers-Writers</a>
    </div>
  </div>
  </div>
</div>
  <svg class='container-fluid'>  
    <circle v-if="addPlaceBtnClicked" cx="50" cy="50" r="40" stroke="orange" stroke-width="5" fill="blue"></circle>
    <text v-if="addPlaceBtnClicked" x="50" y="100" stroke="#0000" stroke-width="2px" dy=".3em">P{{numberOfClicks}}</text>
  </svg>
</div>
</template>

<script>
export default {
  name: "PetriNetMain",
  props: {
    msg: String
  },
  data() {
    return {
      numberOfClicks: 0,
      addPlaceBtnClicked: false
    };
  },
  methods: {
    addPlace() {
      this.addPlaceBtnClicked = true;
      this.numberOfClicks++;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container-fluid {
  display: block;
}

.btn-primary {
  border: 1px solid black;
}
#run-button,
#stop-button {
  background-color: red;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
