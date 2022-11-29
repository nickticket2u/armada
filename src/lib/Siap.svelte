<style>
    a:visited,a:link{color:grey}
</style>


<script>

    let projects = [
        [
        {
            "id":"1",
            "title":"PERUMAHAN SETINGKAT DI JALAN SAKAWI,JALAN KEBUN SELANGOR",
            "image":"/src/assets/s1.jpg",
            "jenis":"SATU TINGKAT",
        },  
        {
            "id":"2",
            "title":"JALAN KEBUN SELANGOR",
            "image":"/src/assets/s2.jpg",
            "jenis":"DUA TINGKAT",
        },
        {
            "id":"3",
            "title":"PERUMAHAN SETINGKAT DI JALAN SAKAWI,JALAN KEBUN SELANGOR",
            "image":"/src/assets/s3.jpg"
        }],
        [
        {
            "id":"4",
            "title":"PERUMAHAN SETINGKAT BANGALOW,BUKIT CANGGANG,SELANGOR",
            "image":"/src/assets/s4.jpg"    ,
            "image2":"/src/assets/s5.jpg"                    
        }
    ]                                                                                                  
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
    PEMBANGUNAN YANG DIURUSKAN OLEH LAGENDA ARMADA SDN BHD
</p>
{#if selected==null}


{#each projects as pp,index2}
<div class="columns">
{#each pp as p,index}
<div class="column is-one-third">
<div class="card" >

    <div class="card-image">
      <figure class="image ">
        <img src={p.image} alt={p.title}/>
      </figure>
      {#if p.image2 !=null}
      <figure class="image ">
        <img src={p.image2} alt={p.title}/>
      </figure>      
      {/if}
    </div>
    <div class="card-content">
        <div class="content">
            {p.title}<br/>
            {#if p.jenis != null}
            JENIS {p.jenis}
            {/if}
        </div>
      </div>    
</div>
</div>
{/each}
</div>
{/each}
{/if}