<template>
  <footer class="footer">
    <div class="container-fluid">
      <ul class="nav">
        <li class="nav-item">
          <a class="nav-link" href="http://www.creative-tim.com">
            Feito por Fabio, Luis, Luciano e Matheus
          </a>
        </li>
      </ul>
      <div class="copyright">
        © {{year}} Hosteado <i class="tim-icons icon-laptop"></i> by
        <a href="https://www.binarcode.com" target="_blank">Thandera Solutions</a>&nbsp;
      </div>
    </div>
  </footer>
</template>
<script>
  export default {
    data() {
      return {
        year: new Date().getFullYear()
      }
    }
  };
</script>
<style>
</style>
