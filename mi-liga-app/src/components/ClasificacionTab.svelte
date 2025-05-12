<script>
  import { equipos } from '../data/equipos.js';
</script>

<div>
  <h2 class="text-xl font-semibold mb-4">Clasificación Actual</h2>
  <div class="overflow-x-auto">
    <table class="min-w-full divide-y divide-gray-200">
      <thead class="bg-gray-50">
        <tr>
          <th class="px-3 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">Pos</th>
          <th class="px-3 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">Equipo</th>
          <th class="px-3 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">PTS</th>
          <th class="px-3 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">PJ</th>
          <th class="px-3 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">PG</th>
          <th class="px-3 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">PE</th>
          <th class="px-3 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">PP</th>
          <th class="px-3 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">GF</th>
          <th class="px-3 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">GC</th>
        </tr>
      </thead>
      <tbody class="bg-white divide-y divide-gray-200">
        {#each equipos as equipo}
          <tr class={equipo.posicion <= 4 ? 'bg-blue-50' : ''}>
            <td class="px-3 py-4 whitespace-nowrap text-sm font-medium text-gray-900">{equipo.posicion}</td>
            <td class="px-3 py-4 whitespace-nowrap text-sm font-medium text-gray-900">{equipo.nombre}</td>
            <td class="px-3 py-4 whitespace-nowrap text-sm text-gray-500">{equipo.puntos}</td>
            <td class="px-3 py-4 whitespace-nowrap text-sm text-gray-500">{equipo.jugados}</td>
            <td class="px-3 py-4 whitespace-nowrap text-sm text-gray-500">{equipo.ganados}</td>
            <td class="px-3 py-4 whitespace-nowrap text-sm text-gray-500">{equipo.empatados}</td>
            <td class="px-3 py-4 whitespace-nowrap text-sm text-gray-500">{equipo.perdidos}</td>
            <td class="px-3 py-4 whitespace-nowrap text-sm text-gray-500">{equipo.golesFavor}</td>
            <td class="px-3 py-4 whitespace-nowrap text-sm text-gray-500">{equipo.golesContra}</td>
          </tr>
        {/each}
      </tbody>
    </table>
  </div>
  <div class="mt-4 text-sm text-gray-500">
    <div class="inline-block w-4 h-4 bg-blue-50 mr-2"></div>
    <span>Clasificación a Champions League</span>
  </div>
</div>