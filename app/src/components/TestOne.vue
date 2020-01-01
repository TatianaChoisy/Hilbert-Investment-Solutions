<template>
  <div class="TestOne">
    <h1 class="principal-title">Tech Test 1</h1>
    <h2 class="title-test-one" v-for="item of items" :key="item.id">Item: {{item.id}} <br> Description: {{item.descr}} <br><h6 id="state">Status: FILE NOT UPLOADED<br></h6>  <input type="file" @change="onFileSelected" @click="this.value=null"/></h2>
    <!-- <input v-for="item of items" :key="item.id" type="file" @change="onFileSelected"/> -->
    <!-- <button v-for="item of items" :key="item.id" @click="onUpload">Upload </button> -->
  </div>
</template>

<script>

import axios from 'axios'

export default {
  name: 'Test One',
  data () {
  return {
    selectedFile: null,
    items: [
  {
    "id": 1,
    "descr": "A photograph representing the Automotive category"
  },
  {
    "id": 2,
    "descr": "A photograph representing the Baby Products category"
  },
  {
    "id": 3,
    "descr": "A photograph representing the Beauty category"
  },
  {
    "id": 4,
    "descr": "A photograph representing the Books category"
  },
  {
    "id": 5,
    "descr": "A photograph representing the Business, Industry and Science category"
  },
  {
    "id": 6,
    "descr": "A photograph representing the CDs and Vinyl category"
  },
  {
    "id": 7,
    "descr": "A photograph representing the Clothing category"
  },
  {
    "id": 8,
    "descr": "A photograph representing the Computer and Accessories category"
  },
  {
    "id": 9,
    "descr": "A photograph representing the DIY and Tools category"
  },
  {
    "id": 10,
    "descr": "A photograph representing the DVD and Blu-ray category"
  }
    ]
  }
},
  methods: {
    onFileSelected(event) {
    this.selectedFile = event.target.files[0]
    document.getElementById("state").textContent="Status: UPLOADED";
        },
    onUpload() {
      const fd = new FormData();
      fd.append('image', this.selectedFile, this.selectedFile.name)
      axios.post('https://drive.google.com/drive/folders/1ndCOzEiDqWlFDJnNn3simz6pYOirLmOl', fd, {
      onUploadProgress: uploadEvent => {
        console.log('Upload Progress:' + Math.round(uploadEvent.loaded / uploadEvent.total * 100) + '%')
        }
    })
  },
}

}

</script>

<style>

.TestOne {
height: 100%;

}

.principal-title {
    margin: 50px;
    font-family: "Montserrat", sans-serif;
}

.title-test-one {
  font-family: "Helvetica";
  font-weight: 300;
  margin: 50px;
} 

</style>
