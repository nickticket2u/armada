<style>
    a:visited,a:link{color:grey}
</style>


<script>

    let projects = [
        [
        {
            "id":"0",
            "title":"BANDAR BARU SETIA AWAN PERDANA, PERAK",
            "image":"/src/assets/p1.jpg",
            "pemaju":"SETIA AWAN HOLDINGS SDN BHD",
            "jenis":"TERES 1 TINGKAT",
            "lokasi":"PERAK"
        },  
        {
            "id":"1",
            "title":"BANDAR BARU SETIA AWAN PERDANA, PERAK",
            "image":"/src/assets/p1.jpg",
            "pemaju":"SETIA AWAN HOLDINGS SDN BHD",
            "jenis":"TERES 1 TINGKAT",
            "lokasi":"PERAK"
        },
        {
            "id":"2",
            "title":"BANDAR BARU SETIA AWAN PERDANA, PERAK",
            "image":"/src/assets/p1.jpg",
            "pemaju":"SETIA AWAN HOLDINGS SDN BHD",
            "jenis":"TERES 1 TINGKAT",
            "lokasi":"PERAK"
        }],
        [
        {
            "id":"3",
            "title":"BANDAR BARU SETIA AWAN PERDANA, PERAK",
            "image":"/src/assets/p1.jpg",
            "pemaju":"SETIA AWAN HOLDINGS SDN BHD",
            "jenis":"TERES 1 TINGKAT",
            "lokasi":"PERAK"
        },
        {
            "id":"4",
            "title":"BANDAR BARU SETIA AWAN PERDANA, PERAK",
            "image":"/src/assets/p1.jpg",
            "pemaju":"SETIA AWAN HOLDINGS SDN BHD",
            "jenis":"TERES 1 TINGKAT",
            "lokasi":"PERAK"
        },
        {
            "id":"5",
            "title":"BANDAR BARU SETIA AWAN PERDANA, PERAK",
            "image":"/src/assets/p1.jpg",
            "pemaju":"SETIA AWAN HOLDINGS SDN BHD",
            "jenis":"TERES 1 TINGKAT",
            "lokasi":"PERAK"
        }],
        [
        {
            "id":"3",
            "title":"BANDAR BARU SETIA AWAN PERDANA, PERAK",
            "image":"/src/assets/p1.jpg",
            "pemaju":"SETIA AWAN HOLDINGS SDN BHD",
            "jenis":"TERES 1 TINGKAT",
            "lokasi":"PERAK"
        },
        {
            "id":"4",
            "title":"BANDAR BARU SETIA AWAN PERDANA, PERAK",
            "image":"/src/assets/p1.jpg",
            "pemaju":"SETIA AWAN HOLDINGS SDN BHD",
            "jenis":"TERES 1 TINGKAT",
            "lokasi":"PERAK"
        },
        {
            "id":"5",
            "title":"BANDAR BARU SETIA AWAN PERDANA, PERAK",
            "image":"/src/assets/p1.jpg",
            "pemaju":"SETIA AWAN HOLDINGS SDN BHD",
            "jenis":"TERES 1 TINGKAT",
            "lokasi":"PERAK"
        }]                                                                                                  
    ]

    let selected = null;
    const more = (sender)=>{
        selected = sender;
        console.log(sender.title);
    }

    let queryid = window.getParameterByName('id');
    if(queryid!=null && queryid!=''){
        for(let i = 0 ; i < projects.length;i++){
            if(projects[i].id == queryid){
                selected = projects[i];
            }
        }
    }

</script>
<p class="title is-4">
    PEMBANGUNAN YANG DIURUSKAN OLEH KOPERASI HARTANAH ANGGUN BERHAD
</p>
{#if selected==null}


{#each projects as pp,index2}
<div class="columns">
{#each pp as p,index}
<div class="column">
<div class="card">
    <header class="card-header">
        <p class="card-header-title">
            {p.title}
          </p>
    </header>
    <div class="card-image">
      <figure class="image is-4by3">
        <img src={p.image} alt={p.title}/>
      </figure>
    </div>
    <div class="card-content">
        <div class="content">
            {p.jenis}
        </div>
      </div>    
</div>
</div>
{/each}
</div>
{/each}
{/if}

{#if selected!=null}

    <div class="section" style="background-color:white;">
        <a href="#" on:click={()=>{selected=null;}}>⬅️Kembali</a><br/>
    <p class="title is-4">{selected.title}</p>
    <div class="columns">
        <div class="column is-half">
            <img src={selected.image} alt={selected.title}/>
        </div>
        <div class="column is-half">
            Lorem Ipsum
        </div>        
    </div>
   
    <div>
        <div class="columns">
            <div class="column is-three-fifths">
                {@html selected.location.replace(/\n\n/gi,'<br/><br/>')}
            </div>
            <div class="column is-two-fifths">
                <img src={selected.image2} alt={selected.title}/>
            </div>            
        </div>
        
    </div>
    <a href="#" on:click={()=>{selected=null;}}>⬅️Kembali</a>
    </div>

{/if}