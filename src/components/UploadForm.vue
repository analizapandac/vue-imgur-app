<template>
  <div class="dropper">
    <input type="file" @change="uploadImages($event.target.files)" multiple accept="image/*">
    <span>Drag files here!</span>
  </div>
</template>

<script>
import { mapActions } from 'vuex';

export default {
  name: 'UploadForm',
  methods: mapActions(['uploadImages'])
}
</script>

<style scoped>
  .dropper {
    height: 30vh;
    border: 2px dashed black;
    border-radius: 5px;
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
  }

  .dropper:hover {
    background-color: #eee;
  }

  input {
    width: 100%;
    height: 100%;
    position: absolute;
    opacity: 0;
  }
</style>

