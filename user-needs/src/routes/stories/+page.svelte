<script>
    import Story from '../../components/layout/story.svelte';
  </script>
  

<header>

    <div class="heading">
        <a href="/stories"><img src="/icons/back-button-2.svg" alt="backbutton"></a>
        <h1>All stories</h1>
    </div>

    <input type="text" placeholder="Search for stories">

    <ul class="nav-ul">
        <li>
            <details>
                <summary>Animal</summary>Animal
            </details>
        </li>
        <li>
            <details>
                <summary>Season</summary>Summer
            </details>
        </li>
        <li>
            <details>
                <summary>Language</summary>English
            </details>
        </li>
        <li>
            <details>
                <summary>Sorting</summary>Length
            </details>
        </li>
    </ul>
</header>


  <main>
    <section>
      <Story />
    </section>
  </main>
  
  <img src="/nyan-cat-tilted2.svg" class="nyan-1" alt="nyan-cat">
  <img src="/nyan-cat-tilted.svg" class="nyan-2" alt="nyan-cat">
  

  <style>
.heading{
    display: flex;
    justify-content: space-between;
    align-items: center;
    justify-content: center;
    margin-bottom: 1.5rem;

    a{
        align-self: self-start;
        margin-right: auto;
    }
    h1{
        margin-right: auto;
        color: white;
        font-size: 1.3rem;
    }
}
header {
    position: fixed;
    z-index: 10;
    width: 100%; 
    height: 10vh; 
}
input{
    width: 100%;
    padding: .5rem;
    margin-bottom: .75rem;
}
.nav-ul{
    display: grid;
    color: white;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    gap: .5rem;
    list-style-type: none;
}
.nav-ul > li{
    background-color: #9264F4;
    font-size: 1em;
    padding: .2rem .3rem;
    border-radius: 5px;
}
details > summary{
    list-style-type: '>';
}


  /* Algemene reset en stijlregels */
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Poppins, sans-serif;
  }
  
  html, body {
    max-width: 100%;
    overflow-x: hidden;
  }
  
  :root {
    --card-margin: 4vw;
    --card-top-offset: 0.4em;
    background-image: linear-gradient(#471871, #142151);
  }

.nyan-1{
    height: 20rem;
    width: 20rem;
    position: fixed;
    top: 50%;
    animation: scrollOut linear forwards;
    animation-timeline: scroll();
}

.nyan-2{
    height: 20rem;
    width: 30rem;
    position: fixed;
    top: 10%;
    animation: scrollOut2 linear forwards;
    animation-timeline: scroll();
}

@keyframes scrollOut {
  from {
    transform: translateX(-200vw) translateY(50%);
  }
  to {
    transform: translateX(100vw) translateY(-40%);
  }
}
@keyframes scrollOut2 {
  from {
    transform: translateX(100vw) translateY(70%);
  }
  to {
    transform: translateX(-130vw) translateY(-50%);
  }
}

  
  /* Main layout */
  main {
    height: 190vh;
    transform: translateY(25vh);
  }
  
  section {
    width: 90vw;
    margin: 0 auto;
  }
  
  /* Responsive heights */
  @media (min-width: 1280px) {
    main {
      height: 187vh;
    }
  }
  

  </style>
  