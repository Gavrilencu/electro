<script>
  import logo from "$lib/img/logo.png";
  import home from "$lib/img/home.png";
  import contact from "$lib/img/contact.png";
  import services from "$lib/img/services.png";
</script>

<header class="header">
  <a href="/"> <img src={logo} alt="" class="logo" /></a>

  <nav class="nav">
    <a href="" class="list"><img src={home} alt="" class="ico" />Home</a>
    <a href="" class="list"
      ><img src={services} alt="" class="icoserv" />Services</a
    >
    <a href="" class="list"
      ><img src={contact} alt="" class="icocont" /> Contact</a
    >
    <a href="" class="list">Form</a>
  </nav>
</header>

<style>
  .icoserv {
    width: 21px;
    margin-right: 3px;
  }
  .ico {
    width: 25px;
    margin-right: 3px;
  }
  .icocont {
    width: 22px;
    margin-right: 3px;
  }
  .nav {
    display: flex;
    align-items: center;
  }
  * {
    transition: 0.5s;
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    text-decoration: none;
    color: black;
  }
  .logo {
    width: 130px;
    cursor: pointer;
  }
  .header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    background-color: rgb(255, 255, 255);
    position: fixed;
    padding-inline: 100px;
    box-shadow: 0px 0px 10px rgba(130, 130, 130, 0.651);
    height: 100px;
  }
  .list {
    margin-inline: 15px;
    color: rgb(0, 0, 0);
    display: flex;
    align-items: center;
  }
  .list:hover {
    transform: scale3d(1.1, 1.1, 0.3);
    color: rgb(93, 93, 93);
  }
</style>
