  // mounted () {
  //   axios.all([
  //     axios.get('https://gbfs.urbansharing.com/oslobysykkel.no/station_status.json'),
  //     axios.get('https://gbfs.urbansharing.com/oslobysykkel.no/station_information.json')
  //     ])
  //     .then(axios.spread(function (stations, data) {
  //     let bySykkel = data.stations(data.stations);
  //     this.setState({ stations: bySykkel })
  //   }))
  //   .then(response => (this.setState({ stations: response.stations})))
  //   // .then(response => (this.stations = response.data.data.stations))
  //   .catch(error => console.log(error));
  // }

  // mounted () {
  //   axios
  //     .get('https://gbfs.urbansharing.com/oslobysykkel.no/station_information.json')
  //     .then(response => (this.stations = response.data.data.stations))
  // }

  // mounted () {
  // function getStationName() {
  //   return axios.get('https://gbfs.urbansharing.com/oslobysykkel.no/station_information.json');
  // }
  // function getBikesAvailable() {
  //   return axios.get('https://gbfs.urbansharing.com/oslobysykkel.no/station_status.json');
  // }

  // axios.all([getStationName(), getBikesAvailable()])
  //   .then(axios.spread(function (, station_status) {
  //     Response => (this.station_information = respnse.data.data.stations)
  //   } ));
  // }

  // mounted () {
  //   axios
  //     .get('https://gbfs.urbansharing.com/oslobysykkel.no/station_information.json')
  //     .then((response) => {
  //       return axios.get('https://gbfs.urbansharing.com/oslobysykkel.no/station_status.json');
  //     })
  // }