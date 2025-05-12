<script>
  import { partidos } from '../data/partidos.js';
</script>

<div>
  <h2 class="text-xl font-semibold mb-4">Próximos Partidos</h2>
  <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
    {#each partidos as partido}
      <div class="border rounded-lg p-4 hover:shadow-md transition">
        <div class="flex justify-between items-center">
          <div class="font-medium">{partido.local}</div>
          <div class="text-sm text-gray-500">VS</div>
          <div class="font-medium text-right">{partido.visitante}</div>
        </div>
        <div class="text-sm text-gray-500 mt-2 text-center">{partido.fecha}</div>
      </div>
    {/each}
  </div>
</div>