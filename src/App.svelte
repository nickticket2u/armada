<script>
  import svelteLogo from './assets/svelte.svg'
  import Menu from './lib/Menu.svelte'
  import Projects from './lib/Projects.svelte'
  import Rakan from './lib/Rakan.svelte'
  import Siap from './lib/Siap.svelte'
  import Mampu from './lib/Mampu.svelte'
  import Hubung from './lib/Hubung.svelte'
  import Sewa from './lib/Sewa.svelte'
  import Footer from './lib/Footer.svelte'
  import Counter from './lib/Counter.svelte';

  let page = getParameterByName('page');

</script>
<Menu/>  
<div style="margin-top:50px">
{#if page=='1'}
<Projects/>
{/if}
{#if page=='2'}
<Siap/>
{/if}
{#if page=='3'}
<Mampu/>
{/if}
{#if page=='4'}
<Sewa/>
{/if}
{#if page=='5'}
<Rakan/>
{/if}
{#if page=='7'}
<Hubung/>
{/if}

</div>
<div><br/><br/>©️ Lagenda Armada Sdn. Bhd. (No. Pendaftaran 1398236-A) {#if (new Date()).getFullYear()>2022}2022-{/if}{(new Date()).getFullYear()}</div>