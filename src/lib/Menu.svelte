<script>
    let logotop = '/src/assets/logotop.jpg'  
    let menuActive = false;
    let menuClass = "navbar-menu";
    const menuToggle = ()=>{
      menuActive = !menuActive;
    }
  
    $:menuClass=menuActive?"navbar-menu is-active":"navbar-menu";
</script>

<nav class="navbar  is-fixed-top" role="navigation" aria-label="main navigation">
    <div class="navbar-brand">
      <a class="navbar-item" href="/">
        <img src={logotop} width="112" height="28"/>
      </a>
  
      <a style="margin-right:10px" role="button" class="navbar-burger" aria-label="menu" on:click={menuToggle} aria-expanded="false" data-target="navbarBasicExample">
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
      </a>
    </div>
  
    <div id="navbarBasicExample" class={menuClass} >
      <div class="navbar-start">
  
        <a class="navbar-item" href="/">
            Pembangunan Terkini
          </a>


          <a class="navbar-item" href="/">
            Projek Siap Dibina
          </a>

          <a class="navbar-item" href="/">
            Pembinaan Mampu Milik
          </a>      
          
          <a class="navbar-item" href="/">
            Pembinaan Rumah Sewa
          </a>   
          
          <a class="navbar-item" href="/">
            Rakan Strategik (PEMAJU)
          </a>            

        <a class="navbar-item">
          Profil Syarikat
        </a>

        <a class="navbar-item">
           Hubungi Kami
          </a>        
  
        <!--div class="navbar-item has-dropdown is-hoverable">
          <a class="navbar-link">
            More
          </a>
  
          <div class="navbar-dropdown">
            <a class="navbar-item">
              About
            </a>
            <a class="navbar-item">
              Jobs
            </a>
            <a class="navbar-item">
              Contact
            </a>
            <hr class="navbar-divider">
            <a class="navbar-item">
              Report an issue
            </a>
          </div>
        </div>
      </div-->
  
      <!--div class="navbar-end">
        <div class="navbar-item">
          <div class="buttons">
            <a class="button is-primary">
              <strong>Sign up</strong>
            </a>
            <a class="button is-light">
              Log in
            </a>
          </div>
        </div>
      </div>
    </div-->
  </nav>