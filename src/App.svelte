<script lang="ts">
  import { Route, Router, navigate } from "svelte-routing";
    import HrSat from "./lib/components/HrSat.svelte";
    import Ejercicio1 from "./lib/ejercicios/Ejercicio1.svelte";
    import Ejercicio2 from "./lib/ejercicios/Ejercicio2.svelte";
    import Ejercicio3 from "./lib/ejercicios/Ejercicio3.svelte";
    import Ejercicio4 from "./lib/ejercicios/Ejercicio4.svelte";
</script>

<main>
  <div class="wrapper">
      <Router>
          <Route path="/">
              <!-- svelte-ignore element_invalid_self_closing_tag -->
              <div style="margin: 10px;" />
              <h1 style="font-size: 4rem; color: var(--golden)">Ejercicios</h1>
              <HrSat/>
              <div style="margin: 30px;" />
              <!-- svelte-ignore a11y-click-events-have-key-events -->
              <div class="container">
                    <!-- svelte-ignore a11y-no-static-element-interactions -->
                    <div class="icon-container"on:click={() => navigate("/ejercicio1")}>
                        <i class="fa-solid fa-file-signature"></i>
                        <p style="font-size: 3rem;">Ejercicio 1</p>
                    </div>
                    <!-- svelte-ignore a11y-no-static-element-interactions -->
                    <div class="icon-container"on:click={() => navigate("/ejercicio2")}>
                        <i class="fa-solid fa-file-signature"></i>
                        <p style="font-size: 3rem;">Ejercicio 2</p>
                    </div>
                </div>
                <div class="container">
                        <!-- svelte-ignore a11y-no-static-element-interactions -->
                    <div class="icon-container"on:click={() => navigate("/ejercicio3")}>
                        <i class="fa-solid fa-file-signature"></i>
                        <p style="font-size: 3rem;">Ejercicio 3</p>
                    </div>
                        <!-- svelte-ignore a11y-no-static-element-interactions -->
                    <div class="icon-container"on:click={() => navigate("/ejercicio4")}>
                        <i class="fa-solid fa-file-signature"></i>
                        <p style="font-size: 3rem;">Ejercicio 4</p>
                    </div>
                </div>
          </Route>
          <Route path="/ejercicio1">
              <!-- Ejemplos de Tooltips -->
              <Ejercicio1 />
          </Route>
          <Route path="/ejercicio2">
              <!-- Ejemplos de los botones -->
              <Ejercicio2 />
          </Route>
          <Route path="/ejercicio3">
              <!-- Ejemplos de los checkboxes -->
              <Ejercicio3 />
          </Route>
          <Route path="/ejercicio4">
              <!-- Ejemplos de los input -->
              <Ejercicio4 />
          </Route>
      </Router>
      <!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
      <!-- svelte-ignore a11y-click-events-have-key-events -->
      <!-- svelte-ignore element_invalid_self_closing_tag -->
      <div style="margin: 20px;" />
  </div>
</main>

<style>
  :global(*, html, body) {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
  }
  main {
      width: 100%;
      height: 100vh;
      padding: 20px;
      background-color: rgb(228, 228, 228);
  }

  .wrapper {
      display: flex;
      flex-direction: column;
      border-radius: 10px;
      padding: 10px;
      background-color: #fff;
      align-items: center;
      height: 100%;
  }

  .container{
      display: grid;
      grid-template-columns: 1fr 1fr;
      width: 70%;
      height: 100%;
      padding: 0px 10px;
      align-items: center;
      justify-content: center;
      color: var(--soft-red);
  }

  .icon-container {
    border-radius: 10%;
    grid-row: 1;
    display: flex;
    justify-content: start;
    align-items: center;
    gap: 10%;
    cursor: pointer;
    padding: 10px;
    height: 100%;
  }

  .icon-container:hover{
    background-color: rgba(237, 236, 236, 0.574);
}

  .icon-container i {
      color: var(--golden);
      font-size: 3rem;
  }

  @media (max-width: 950px) {
      .icon-container i {
          font-size: var(--p-responsive);
      }
  }
  @media (max-width: 800px) {
      .icon-container {
          display: none;
      }
  }
</style>
