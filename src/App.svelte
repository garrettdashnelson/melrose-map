<script>
  import './bulma-imports.scss'
  export let name;

  let section = 'home';

</script>


<style lang="scss">

:global(html) {
  height: 100%;
}

:global(body) {
  min-height: 100%;
  background: linear-gradient(330deg, #775311f0, #0f572df0), url('map-background-excerpt.jpg');
  background-attachment: fixed;
}

.main-title {
  font-weight: 400;
  font-size: 2.6rem;
  text-shadow: 2px 2px 0 rgba(238, 255, 0, 0.329);
  & strong {
    font-weight: 600;
  }
}

.button.is-link.is-outlined:hover {
  box-shadow: 3px 3px 0 rgba(238, 255, 0, 0.329);
}
</style>


<section class="section">
  <div class="container">
    <h1 class="title main-title">The <strong>biking, hiking, and walking</strong> map of <strong>Melrose, Massachusetts</strong></h1>
  </div>

  {#if section==='home'}
  <div class="container mt-5">
    <div class="columns">
      <div class="column is-half">
        <h3 class="is-size-4 is-italic">Printed map</h3>
        <a href="https://www.dropbox.com/s/mm2cf9sofipsum0/melrose-export.pdf?dl=1" class="button is-link is-outlined my-2">Full map, PDF, folding size (24 in x 36 in)</a><br>
        <a href="" class="button is-link is-outlined my-2">Simple map, PDF, letter size (8½ in x 11 in)</a><br>
        <a href="" class="button is-link is-outlined my-2">Buy a full size map for $5.00</a><br>
    </div>
      <div class="column is-half">
        <h3 class="is-size-4 is-italic">Interactive map</h3>
        <a href="" class="button is-link is-outlined my-2" on:click={function(){ section='webmap'; }}>Visit the web map</a><br>
        <button class="button is-link is-outlined my-2" on:click={function(){ section='itineraries'; }}>Melrose itineraries</button><br>
      </div>

    </div>

    <div class="columns">
      <div class="column is-half">
        <h3 class="is-size-4 is-italic">Created by</h3>
        <ul>
          <li><a href="https://pedbikemelrose.org">Melrose Pedestrian & Bicyclist Committee</a></li>
          <li><a href="http://people.matinic.us/garrett">Garrett Dash Nelson</a></li>
        </ul>
      </div>
      <div class="column is-half">
        <h3 class="is-size-4 is-italic">Sponsors</h3>
        <ul>
          <li>Someone</li>
          <li>Someone</li>
          <li>Someone</li>
        </ul>
      </div>
    </div>
    
  </div>
  {:else if section==='webmap'}
    <div class="container mt-5">
      blah
    </div>

  {:else if section==='itineraries'}
    <div class="container mt-5">
      
      <h2 class="title is-size-2">Itineraries</h2>
      <div class="columns">
        <div class="column is-half">
          <h3 class="is-size-4 is-italic">Historic walks</h3>
          <ul>
            <li>The Village</li>
          </ul>
        </div>

        <div class="column is-half">
          <h3 class="is-size-4 is-italic">Hikes with views</h3>
          <ul>
            <li>Highlands to High Rock</li>
          </ul>
        </div>

      </div>
    </div>
  {/if}
  
</section>
