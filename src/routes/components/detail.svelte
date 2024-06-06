<script>
  /**
   * @type {{id:string,message:string}[]}
   */
  let messages = [
    { id: new Date().toTimeString(), message: 'I love you, baby!' }
  ]

  let msg = ''

  function sendMsg() {
    if(!msg) return
    messages = [...messages, { id: new Date().toTimeString(), message: msg }]
    msg = ''
  }
</script>

<div>
  {#each messages as { message }}
    <div class="flex my-6">
      <div
        class="w-12 h-12 rounded-full bg-gray-800 flex justify-center items-center font-bold"
      >
        K
      </div>
      <div class="bg-slate-50 text-black p-2 ml-2 rounded">{message}</div>
    </div>
  {/each}
  <input
    bind:value={msg}
    type="text"
    class="w-full rounded h-10 text-black px-2"
    placeholder="text here"
  />
  <button
    type="button"
    on:click={sendMsg}
    class="bg-white w-full h-8 text-black inline-flex justify-center items-center rounded mt-2"
    >send</button
  >
  <a class="w-full mt-10 block text-center" href="/">go back</a>
</div>
