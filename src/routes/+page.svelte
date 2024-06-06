<script type="module">
  import StatusBar from './components/statusBar.svelte'
  import Notify from './components/notify.svelte'

  let notifyMessage = ''

  async function getMessage() {
    notifyMessage = await new Promise((resolve) => {
      setTimeout(() => {
        resolve('I love you, baby!')
      }, 1000)
    })
  }

  getMessage()
</script>

<svelte:head>
  <title>mobile sumilator</title>
</svelte:head>

<div
  class="text-white h-screen w-screen rounded-2xl bg-gradient-to-b from-cyan-500 to-blue-500"
>
  {#if notifyMessage}
    <Notify />
  {/if}
</div>
