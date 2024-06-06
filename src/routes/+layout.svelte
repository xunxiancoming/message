<script>
  import '../app.css'
  import StatusBar from './components/statusBar.svelte'
</script>

<div
  class="text-white h-screen w-screen rounded-2xl bg-gradient-to-b from-cyan-500 to-blue-500"
>
  <StatusBar />
  <slot />
</div>
