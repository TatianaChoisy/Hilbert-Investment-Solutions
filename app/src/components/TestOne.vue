<template>
  <div class="TestOne">
    <h1>Tech Test 1</h1>
    <input type="file" @change="onFileSelected">
    <button @click="onUpload">Upload</button>
  </div>
</template>

<script>

import axios from 'axios'

export default {
  name: 'Test One',
  data () {
  return {
    selectedFile: null
  }
},
  methods: {
    onFileSelected(event) {
    this.selectedFile = event.target.files[0]
        },
    onUpload() {
      const fd = new FormData();
      fd.append('image', this.selectedFile, this.selectedFile.name)
      axios.post('https://drive.google.com/drive/folders/1ndCOzEiDqWlFDJnNn3simz6pYOirLmOl', fd, {
      onUploadProgress: uploadEvent => {
        console.log('Upload Progress:' + Math.round(uploadEvent.loaded / uploadEvent.total * 100) + '%')
        }
    })

  }
}
}



</script>

<style>

.TestOne {

height: 200px;

}

</style>
