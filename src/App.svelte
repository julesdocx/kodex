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
    let element = document.getElementById(id);
    element.classList.add('selected')
}

function handleMouseOut(id) {
  let element = document.getElementById(id);
    element.classList.remove('selected')
}
</script>

<header>
      <div class=""> 
          <div class="small-nav-circle">
              <span id="1" class="stroke"></span>
              <span id="2" class="stroke"></span>
              <span id="3" class="stroke"></span>
              <span id="4" class="stroke"></span>
              <span id="5" class="stroke"></span>
              <span id="6" class="stroke"></span>
              <span id="7" class="stroke"></span>
              <span id="8" class="stroke"></span>
          </div>
    </div>
</header>
<main>
  <div class="navigation">
      <div class="grid-1 lg-grid justify-i-c"> 
          <div class="align-center nav-circle">
              <a href="#info1" class="fade-in" on:mouseout={() => handleMouseOut(1)} on:mouseover={() => handleMouseOver(1)} on:focus={()=>{true}}><span>Project1</span></a>
              <a href="#info2" class="fade-in" on:mouseout={() => handleMouseOut(2)} on:mouseover={() => handleMouseOver(2)} on:focus={()=>{true}}><span>Project2</span></a>
              <a href="#info3" class="fade-in" on:mouseout={() => handleMouseOut(3)} on:mouseover={() => handleMouseOver(3)} on:focus={()=>{true}}><span>Project3</span></a>
              <a href="#info4" class="fade-in" on:mouseout={() => handleMouseOut(4)} on:mouseover={() => handleMouseOver(4)} on:focus={()=>{true}}><span>Project4</span></a>
              <a href="#info5" class="fade-in" on:mouseout={() => handleMouseOut(5)} on:mouseover={() => handleMouseOver(5)} on:focus={()=>{true}}><span>Project5</span></a>
              <a href="#info6" class="fade-in" on:mouseout={() => handleMouseOut(6)} on:mouseover={() => handleMouseOver(6)} on:focus={()=>{true}}><span>Project6</span></a>
              <a href="#info7" class="fade-in" on:mouseout={() => handleMouseOut(7)} on:mouseover={() => handleMouseOver(7)} on:focus={()=>{true}}><span>Project7</span></a>
              <a href="#info8" class="fade-in" on:mouseout={() => handleMouseOut(8)} on:mouseover={() => handleMouseOver(8)} on:focus={()=>{true}}><span>Project8</span></a>
          </div>
    </div>
  </div>
  
    <div class="gallery__list">
        <div id="info1" class="gallery__project fade-in">
        <div class="gallery__project-title">
          Project 1
        </div>
        <div class="gallery_project-text">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ea amet reprehenderit cum ducimus accusantium sint modi magnam earum necessitatibus quis vel delectus, facere eaque consectetur dolorem dolorum placeat autem cupiditate!
        </div>
        </div>
        <div id="info2" class="gallery__project fade-in">
        <div class="gallery__project-title">
          Project 1
        </div>
        <div class="gallery_project-text">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ea amet reprehenderit cum ducimus accusantium sint modi magnam earum necessitatibus quis vel delectus, facere eaque consectetur dolorem dolorum placeat autem cupiditate!
        </div>
        </div>
        <div id="info3" class="gallery__project fade-in">
        <div class="gallery__project-title">
          Project 1
        </div>
        <div class="gallery_project-text">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ea amet reprehenderit cum ducimus accusantium sint modi magnam earum necessitatibus quis vel delectus, facere eaque consectetur dolorem dolorum placeat autem cupiditate!
        </div>
        </div>
        <div id="info4" class="gallery__project fade-in">
        <div class="gallery__project-title">
          Project 1
        </div>
        <div class="gallery_project-text">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ea amet reprehenderit cum ducimus accusantium sint modi magnam earum necessitatibus quis vel delectus, facere eaque consectetur dolorem dolorum placeat autem cupiditate!
        </div>
        </div>
        <div id="info5" class="gallery__project fade-in">
        <div class="gallery__project-title">
          Project 1
        </div>
        <div class="gallery_project-text">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ea amet reprehenderit cum ducimus accusantium sint modi magnam earum necessitatibus quis vel delectus, facere eaque consectetur dolorem dolorum placeat autem cupiditate!
        </div>
        </div>
                <div id="info6" class="gallery__project fade-in">
        <div class="gallery__project-title">
          Project 1
        </div>
        <div class="gallery_project-text">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ea amet reprehenderit cum ducimus accusantium sint modi magnam earum necessitatibus quis vel delectus, facere eaque consectetur dolorem dolorum placeat autem cupiditate!
        </div>
        </div>
                <div id="info7" class="gallery__project fade-in">
        <div class="gallery__project-title">
          Project 1
        </div>
        <div class="gallery_project-text">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ea amet reprehenderit cum ducimus accusantium sint modi magnam earum necessitatibus quis vel delectus, facere eaque consectetur dolorem dolorum placeat autem cupiditate!
        </div>
        </div>
                <div id="info8" class="gallery__project fade-in">
        <div class="gallery__project-title">
          Project 1
        </div>
        <div class="gallery_project-text">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ea amet reprehenderit cum ducimus accusantium sint modi magnam earum necessitatibus quis vel delectus, facere eaque consectetur dolorem dolorum placeat autem cupiditate!
        </div>
        </div>
  </div>
</main>

<style>

  .gallery__list {
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


