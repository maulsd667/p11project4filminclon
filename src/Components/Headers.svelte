<script>
    import Logo from "./logo.svelte";
    import Link from "./Link.svelte";
    import lupa from "../assets/Lupa.png"
    
</script>

<header>
   <Logo />
    <nav>
       <Link text= "inicio" />
       <Link text= "peliculas" />
       <Link text= "series" />
       <Link text= "coleccion" />
       <Link text= "kids" />
       <Link text= "Mas" />

      </nav>
      <div class="flex-grown-1"></div>
      <button id="btn-sub">SUSCRIBETE</button>
      <button id="btn-login">INICIAR SESIÓN</button>
      <img src={lupa} alt="Icono de búsqueda"/>

    </header>


<style>
   header{
      display: flex;
      justify-content: flex-start;
      align-items: center;
      margin: 20px 40px;
      gap: 20px;
      background-color: black;
   }
   .flex-grown-1{
      flex-grow: 1 !important;
   }
   #btn-sub{
      background-color: #02ffa1;
      border: none;
   }   
   #btn-login{
      color: white;
      background-color: transparent;
      border: 2px solid #fff;

   }
   #btn-login:hover{
      border-color: #6f6f81;
   }
   #btn-login:active{
      background-color: #6f6f81;
   }
</style>

