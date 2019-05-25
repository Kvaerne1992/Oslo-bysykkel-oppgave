<template>
  <div>
    <div class="one">
      <div class="two">
        <div 
          v-for="stations in stations" 
          :key='stations.id'
          class="stations">
          <p>Stasjon: {{stations.name}} </p>
          <p>Antall plasser: {{stations.capacity}} </p>
        </div>
      </div>
      <div class="two">
        <div
          v-for="stationInformation in stationInformation"
          :key='stationInformation.id'
          class="stations">
          <p>Tilgjengelige sykler: {{stationInformation.num_bikes_available}} </p>
          <p>Ledige plasser: {{stationInformation.num_docks_available}} </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'CardList',
  data () {
    return {
      stations: null,
      data: null,
      stationInformation: null
    };
  },
  mounted() {
    axios
      .get("https://gbfs.urbansharing.com/oslobysykkel.no/station_information.json")
      .then(response => (this.stations = response.data.data.stations));

    axios
      .get("https://gbfs.urbansharing.com/oslobysykkel.no/station_status.json")
      .then(response => (this.stationInformation = response.data.data.stations));
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

  h1 {
    display: block;
    margin: 0 auto;
    text-align: center;
  }

  .one {
  display: flex;
  flex-direction: row;
  }

  .two {
    display: flex;
    flex-direction: column;
  }

  .stations {
    display: inline-display;
    width: 250px;
    height: 100px;
    margin-left: 0px;
    margin-bottom: 10px;
    padding: 16px;
    text-align: center;
    box-shadow: 2px 2px 0px 4px #BFBFBF;
  }

</style>


<!-- { "station_id": "787", "name": "Kirkegata 15", "address": "Kirkegata 15, Oslo", "lat": 59.91015615055511, "lon": 10.743456971511705, "capacity": 12 } -->