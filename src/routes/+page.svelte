<script>
  let image;

  $: if (image) {
    console.log(image);
    
    for (const imgData of image) {
      console.log(`${imgData.name} has size ${imgData.size} and type ${imgData.type}`)
    }
  }
</script>

<style>
  .view {
    width: '100vw';
    height: '100vh';
    display: 'flex';
    flex-direction: 'column';
    justify-content: 'center';
    align-items: 'flex-start';
  }

  h1 {
    font-size: 3rem;
    text-align: center;
  }
</style>

<div class="view">
  <h1>Vector Image Search</h1>
  <label for="image-upload">Upload an image</label>
  <input 
    type="file" 
    id="image-upload" 
    accept="image/*" 
    bind:files={image}
  />
</div>


