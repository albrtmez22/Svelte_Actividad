<script>
  import Header from './components/Header.svelte';
  import Footer from './components/Footer.svelte';
  import HeroSection from './components/HeroSection.svelte';
  import TabsSection from './components/TabsSection.svelte';
</script>

<div class="flex flex-col min-h-screen bg-gray-100">
  <Header />
  <HeroSection />
  <main class="flex-grow container mx-auto px-4 py-8">
    <TabsSection />
  </main>
  <Footer />
</div>