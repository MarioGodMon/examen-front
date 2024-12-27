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
              <h1>Ejercicios</h1>
              <HrSat/>
              <div style="margin: 30px;" />
              <!-- svelte-ignore a11y-click-events-have-key-events -->
              <div class="container">
                  <div class="componets-container-left">
                      
                          <!-- svelte-ignore a11y-no-static-element-interactions -->
                          <div class="icon-container"on:click={() => navigate("/ejercicio1")}>
                              <i class="fa-brands fa-codepen"></i>
                              <p style="font-size: 1.4rem;">Ejercicio1</p>
                          </div>
                      <div style="margin: 20px;" />
                          <!-- svelte-ignore a11y-no-static-element-interactions -->
                          <div class="icon-container"on:click={() => navigate("/ejercicio2")}>
                              <i class="fa-brands fa-codepen"></i>
                              <p style="font-size: 1.4rem;">Ejercicio2</p>
                          </div>
                      <div style="margin: 20px;" />
                  </div>
                  <div class="componets-container-right">
                          <!-- svelte-ignore a11y-no-static-element-interactions -->
                          <div class="icon-container"on:click={() => navigate("/ejercicio3")}>
                              <i class="fa-brands fa-codepen"></i>
                              <p style="font-size: 1.4rem;">Ejercicio3</p>
                          </div>
                      <div style="margin: 20px;" />
                          <!-- svelte-ignore a11y-no-static-element-interactions -->
                          <div class="icon-container"on:click={() => navigate("/ejercicio4")}>
                              <i class="fa-brands fa-codepen"></i>
                              <p style="font-size: 1.4rem;">Ejercicio4</p>
                          </div>
                      <div style="margin: 20px;" />    
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
      height: 80%;
  }

  .container{
      display: grid;
      width: 70%;
      grid-template-columns: 1fr 1fr;
  }

  .icon-container {
      grid-column: 1;
      grid-row: 1;
      display: flex;
      justify-content: start;
      align-items: center;
      gap: 10%;
      cursor: pointer;
  }

  .icon-container i {
      color: var(--golden);
      font-size: 1.8rem;
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
