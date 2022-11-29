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
  

        <div class="navbar-item has-dropdown is-hidden-mobile is-hoverable">
          <a class="navbar-link" >
            Projek
          </a>
            <div class="navbar-dropdown">
            <a class="navbar-item" href="/?page=1">
              Pembangunan Terkini
            </a>
            <a class="navbar-item" href="/?page=2">
              Projek Siap Dibina
            </a>
            <a class="navbar-item" href="/?page=3">
              Pembinaan Mampu Milik
            </a>
            <a class="navbar-item" href="/?page=4">
              Pembinaan Rumah Sewa
            </a>
          </div>
        </div>


        <a class="navbar-item is-hidden-tablet" href="/?page=1">
          Pembangunan Terkini
        </a>
        <a class="navbar-item is-hidden-tablet" href="/?page=2">
          Projek Siap Dibina
        </a>
        <a class="navbar-item is-hidden-tablet" href="/?page=3">
          Pembinaan Mampu Milik
        </a>
        <a class="navbar-item is-hidden-tablet" href="/?page=4">
          Pembinaan Rumah Sewa
        </a>
       
          
          <a class="navbar-item" href="/?page=5">
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