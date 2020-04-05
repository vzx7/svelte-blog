<script>
  /**
   * Метод для открытия мобильного меню
   * @param {object} evt
   **/
  const handleBurgerClick = evt => {
    evt.currentTarget.classList.toggle("is-active");
    navMenu.classList.toggle("is-active");
  };

  /**
   * Метод для клика мо меню
   * @param {object} evt
   **/
  const handleMenuClick = evt => {
    const menuList = document.getElementsByClassName("navbar-item");
    if (menuList) {
      for (let x = 0; x < menuList.length; x++) {
        menuList.item(x).classList.remove("is-active");
      }
    }
    evt.currentTarget.classList.add("is-active");
  };
</script>

<style lang="scss">
  $color: red;

  h1 {
    color: $color;
  }
</style>

<nav class="navbar is-primary">
  <div class="container">
    <div class="navbar-brand">
      <a href="" class="navbar-item" style="font-weight: bold">
        Приход Екатеринбурга
      </a>
      <span
        data-target="navMenu"
        class="navbar-burger burger"
        on:click={handleBurgerClick}>
        <span />
        <span />
        <span />
      </span>
    </div>
  </div>
  <div id="navMenu" class="navbar-menu">
    <div class="navbar-end">
      <a href="#" class="navbar-item is-active" on:click={handleMenuClick}>
        Home
      </a>
      <a href="#" class="navbar-item" on:click={handleMenuClick}>About</a>
      <a href="#" class="navbar-item" on:click={handleMenuClick}>Evente</a>
      <a href="#" class="navbar-item" on:click={handleMenuClick}>Other</a>
      <a href="#" class="navbar-item" on:click={handleMenuClick}>All</a>
    </div>
  </div>
</nav>

<section>
  <div class="columns">
    <div class="column">First column</div>
    <div class="column">Second column</div>
    <div class="column">Third column</div>
  </div>
</section>
<footer class="footer has-text-centered">
  <div class="container">
    <div class="columns">
      <div class="column is-8-desktop is-offset-2-desktop">
        <p>
          <strong class="has-text-weight-semibold">
            <a href="https://www.npmjs.com/package/bulma-start">
              bulma-start@0.0.3
            </a>
          </strong>
        </p>
        <p>
          <small>
            Source code licensed
            <a href="http://opensource.org/licenses/mit-license.php">MIT</a>
          </small>
        </p>
        <p style="margin-top: 1rem;">
          <a href="http://bulma.io">
            <img
              src="made-with-bulma.png"
              alt="Made with Bulma"
              width="128"
              height="24" />
          </a>
        </p>
      </div>
    </div>
  </div>
</footer>
