<script>
  import gsap from 'gsap';
	import { onMount } from 'svelte';

	let colour = 'red';

  let galleryElements = document.getElementsByClassName('gallery__project');
  setTimeout(() => {
    Array.from(galleryElements).forEach((elem) => {
      elem.addEventListener('click', () => {
        const classList = Array.from(elem.classList)
        if (classList.includes('gallery__project--expanded')) {
          elem.classList.remove('gallery__project--expanded');
        } else {
          elem.classList.add('gallery__project--expanded');
        }
      })
    });
  }, 100);

function handleMouseOver(id) {
    let elements = document.querySelectorAll('.i' + id);
    elements.forEach((elem) => {
      elem.classList.add('selected')
    })
}

function handleMouseOut(id) {
  let elements = document.querySelectorAll('.i' + id);
  elements.forEach((elem) => {
    elem.classList.remove('selected')
  })
}
</script>

<header>
      <div class=""> 
          <div class="small-nav-circle">
              <span class="i1 stroke"></span>
              <span class="i2 stroke"></span>
              <span class="i3 stroke"></span>
              <span class="i4 stroke"></span>
              <span class="i5 stroke"></span>
              <span class="i6 stroke"></span>
              <span class="i7 stroke"></span>
              <span class="i8 stroke"></span>
          </div>
          <div class="header-title__container">
              <p class="i1 header-title">Kodexmafia</p>
              <p class="i2 header-title">Cornelis</p>
              <p class="i3 header-title">Navgul</p>
              <p class="i4 header-title">Tomstacks</p>
              <p class="i5 header-title">Seelisaughust</p>
              <p class="i6 header-title">Edgelord</p>
              <p class="i7 header-title">Paulusencornelis</p>
              <p class="i8 header-title">Clit</p>
          </div>
    </div>
</header>
<main>
  <div class="navigation">
      <div class="grid-1 lg-grid justify-i-c"> 
          <div class="align-center nav-circle">
              <a href="#info1" class="fade-in" on:mouseout={() => handleMouseOut(1)} on:mouseover={() => handleMouseOver(1)} on:focus={()=>{true}}><span>Kodexmafia</span></a>
              <a href="#info2" class="fade-in" on:mouseout={() => handleMouseOut(2)} on:mouseover={() => handleMouseOver(2)} on:focus={()=>{true}}><span>Cornelis</span></a>
              <a href="#info3" class="fade-in" on:mouseout={() => handleMouseOut(3)} on:mouseover={() => handleMouseOver(3)} on:focus={()=>{true}}><span>Navgul</span></a>
              <a href="#info4" class="fade-in" on:mouseout={() => handleMouseOut(4)} on:mouseover={() => handleMouseOver(4)} on:focus={()=>{true}}><span>Tomstacks</span></a>
              <a href="#info5" class="fade-in" on:mouseout={() => handleMouseOut(5)} on:mouseover={() => handleMouseOver(5)} on:focus={()=>{true}}><span>Seelisaughust</span></a>
              <a href="#info6" class="fade-in" on:mouseout={() => handleMouseOut(6)} on:mouseover={() => handleMouseOver(6)} on:focus={()=>{true}}><span>Edgelord</span></a>
              <a href="#info7" class="fade-in" on:mouseout={() => handleMouseOut(7)} on:mouseover={() => handleMouseOver(7)} on:focus={()=>{true}}><span>Paulusencornelis</span></a>
              <a href="#info8" class="fade-in" on:mouseout={() => handleMouseOut(8)} on:mouseover={() => handleMouseOver(8)} on:focus={()=>{true}}><span>Clit</span></a>
          </div>
    </div>
  </div>
  
    <div class="gallery__list">
        <div id="info1" class="gallery__project fade-in">
        <div class="gallery__project-title">
          Kodexmafia
        </div>
        <div class="gallery_project-text">
          Gathering of digital boobssexmaniacs based in Brussels, Belgium. Making trash digital art, mostly using Photoshop.
          They have a specific client base, consisting of soundcloud trappers and producers.
        </div>
        </div>
        <div id="info2" class="gallery__project fade-in">
        <div class="gallery__project-title">
          Cornelis
        </div>
        <div class="gallery_project-text">
          The very best at making wonderfull music and not showing it to anyone. If you would like to hear some of his beatifull audio works you should beg him for a private link. Again his music really rules over all other music that exists.
        </div>
        </div>
        <div id="info3" class="gallery__project fade-in">
        <div class="gallery__project-title">
          Navgul
        </div>
        <div class="gallery_project-text">
          Not every music is good and neither is Navgul's music. Producing is just a way to chew on time for him. Sadly he stopped making music in 2021, realising he had better hopes of product descency in the visualarts.
        </div>
        </div>
        <div id="info4" class="gallery__project fade-in">
        <div class="gallery__project-title">
          Tomstacks
        </div>
        <div class="gallery_project-text">
          The most motivating person on earth. You see him ...  you are motivated. Besides slaying the architecture game and being international, he also is an underrated soundcloud vocalist.
        </div>
        </div>
        <div id="info5" class="gallery__project fade-in">
        <div class="gallery__project-title">
          Seelisaughust
        </div>
        <div class="gallery_project-text">
          Known as a quantity based writer, thinker, and playwriter. He informs his consumers about a combination of absurd and important views. He has a website, posts regularly on Medium and tries to keep up with crazy content on Instagram.
        </div>
        </div>
                <div id="info6" class="gallery__project fade-in">
        <div class="gallery__project-title">
          Edgelord
        </div>
        <div class="gallery_project-text">
          Edgelord is an established soundcloud artist focusing on ...
        </div>
        </div>
                <div id="info7" class="gallery__project fade-in">
        <div class="gallery__project-title">
          Paulus and Cornelis
        </div>
        <div class="gallery_project-text">
          Coming soon...
        </div>
        </div>
        <div id="info8" class="gallery__project fade-in">
        <div class="gallery__project-title">
          C-lit
        </div>
        <div class="gallery_project-text">
          Also an established musician
        </div>
        </div>
  </div>
</main>

<style>

  .gallery__list {
    color: black;
    margin-top: 45vh;
    display: grid;
    grid-template-columns: repeat(3, 300px);
    grid-auto-rows: 5rem;
    grid-gap: 16px;
    grid-auto-flow: dense;
    transition: 0.1s ease-in;
  }
  .gallery__project {
    text-align: left;
    grid-column: span 3;
    grid-row: span 3;
    transition: 0.1s ease-in;
    display: grid;
    grid-template-columns: minmax(150px, 25%) 1fr;
    gap: 12px;
  }
  .gallery__project:hover {
    position: relative;
    border-radius: 50%;
  }
  .gallery__project-text {
    max-width: 50%;
  }


</style>


