<script>
  import { gifts } from "./data.json"
  import giftSVG from "./assets/icons/gift.svg"
  import santaClausSVG from "./assets/icons/santa-claus.svg"
</script>

<svelte:head>
  <link
    href="https://fonts.googleapis.com/css2?family=Caveat:wght@700&display=swap"
    rel="stylesheet"
  />
</svelte:head>
<main>
  <article>
    <header>
      <img src={santaClausSVG} alt="Papa Noel icon" />
      <h1>Regalos</h1>
    </header>

    <ul>
      {#each gifts as gift}
        <li>
          <img src={giftSVG} alt="Gift icon" />{gift}
        </li>
      {/each}
    </ul>
  </article>
</main>

<style>
  article {
    font-size: 2rem;
    padding: 4rem;
    border-radius: 0.8rem;
    background-color: red;
    display: flex;
    justify-content: flex-start;
    align-items: center;
    flex-direction: column;
    max-height: 50rem;
    gap: 3rem;
    color: #fff;
    width: 75%;
    box-shadow: 0px 0px 10px 1px #00000055;
  }

  header {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: row;
    gap: 0.8rem;
  }

  header h1 {
    font-family: "Caveat", cursive;
  }

  img {
    width: 5rem;
    height: 5rem;
  }

  ul {
    display: flex;
    flex-direction: column;
    gap: 2rem;
    align-items: flex-start;
  }

  li {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 0.8rem;
  }
</style>
