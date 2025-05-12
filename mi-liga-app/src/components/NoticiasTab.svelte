<script>
  import { noticias } from '../data/noticias.js';
</script>

<div>
  <h2 class="text-xl font-semibold mb-4">Últimas Noticias</h2>
  <div class="space-y-4">
    {#each noticias as noticia}
      <div class="border-b pb-4 last:border-b-0">
        <h3 class="font-medium text-lg">{noticia.titulo}</h3>
        <p class="text-sm text-gray-500">{noticia.fecha}</p>
      </div>
    {/each}
  </div>
</div>