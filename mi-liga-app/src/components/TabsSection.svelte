<script>
  import ClasificacionTab from './ClasificacionTab.svelte';
  import PartidosTab from './PartidosTab.svelte';
  import NoticiasTab from './NoticiasTab.svelte';
  
  let activeTab = 'clasificacion';
  
  function setActiveTab(tab) {
    activeTab = tab;
  }
</script>

<div class="flex border-b border-gray-200 mb-6">
  <button 
    class="px-4 py-2 font-medium {activeTab === 'clasificacion' ? 'text-blue-600 border-b-2 border-blue-600' : 'text-gray-500 hover:text-blue-500'}"
    on:click={() => setActiveTab('clasificacion')}
  >
    Clasificación
  </button>
  <button 
    class="px-4 py-2 font-medium {activeTab === 'partidos' ? 'text-blue-600 border-b-2 border-blue-600' : 'text-gray-500 hover:text-blue-500'}"
    on:click={() => setActiveTab('partidos')}
  >
    Próximos Partidos
  </button>
  <button 
    class="px-4 py-2 font-medium {activeTab === 'noticias' ? 'text-blue-600 border-b-2 border-blue-600' : 'text-gray-500 hover:text-blue-500'}"
    on:click={() => setActiveTab('noticias')}
  >
    Noticias
  </button>
</div>

<div class="bg-white rounded-lg shadow-md p-6">
  {#if activeTab === 'clasificacion'}
    <ClasificacionTab />
  {:else if activeTab === 'partidos'}
    <PartidosTab />
  {:else if activeTab === 'noticias'}
    <NoticiasTab />
  {/if}
</div>