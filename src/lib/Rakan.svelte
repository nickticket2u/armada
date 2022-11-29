<style>
    a:visited,a:link{color:grey}
</style>


<script>

    let projects = [
        [
        {
            "id":"1",
            "title":"BANDAR BARU SETIA AWAN PERDANA, PERAK",
            "image":"/src/assets/r1.jpg",
            "pemaju":"SETIA AWAN HOLDINGS SDN BHD",
            "jenis":"TERES 1 TINGKAT",
            "lokasi":"PERAK"
        },  
        {
            "id":"2",
            "title":"BANDAR BARU SETIA AWAN PERDANA, PERAK",
            "image":"/src/assets/r2.jpg",
            "pemaju":"SETIA AWAN HOLDINGS SDN BHD",
            "jenis":"SEMI-D 1 TINGKAT",
            "lokasi":"PERAK"
        },
        {
            "id":"3",
            "title":"TAMAN MULIA, PERAK",
            "image":"/src/assets/r3.jpg",
            "pemaju":"SETIA AWAN HOLDINGS SDN BHD",
            "jenis":"TERES 2 TINGKAT",
            "lokasi":"PERAK"
        }],
        [
        {
            "id":"4",
            "title":"BANDAR BARU SETIA AWAN PERDANA, PERAK",
            "image":"/src/assets/r4.jpg",
            "pemaju":"YNH PROPERTY BERHAD",
            "jenis":"PANGSAPURI",
            "lokasi":"PERAK"
        },
        {
            "id":"5",
            "title":"BANDAR BARU SETIA AWAN PERDANA, PERAK",
            "image":"/src/assets/r5.jpg",
            "pemaju":"IKATAN INTRA SDN BHD",
            "jenis":"BANGLO 1 TINGKAT",
            "lokasi":"KETEREH, KELANTAN"
        },
        {
            "id":"6",
            "title":"BANDAR BARU SETIA AWAN PERDANA, PERAK",
            "image":"/src/assets/r6.jpg",
            "pemaju":"IKATAN INTRA SDN BHD",
            "jenis":"SEMI-D 1 TINGKAT SETENGAH",
            "lokasi":"GUA MUSANG, KELANTAN"
        }],
        [
        {
            "id":"7",
            "title":"BANDAR BARU SETIA AWAN PERDANA, PERAK",
            "image":"/src/assets/r7.jpg",
            "pemaju":"IKATAN INTRA SDN BHD",
            "jenis":"BANGLO 1 TINGKAT",
            "lokasi":"PASIR PUTEH, KELANTAN"
        },
        {
            "id":"8",
            "title":"BANDAR BARU SETIA AWAN PERDANA, PERAK",
            "image":"/src/assets/r8.jpg",
            "pemaju":"IKATAN INTRA SDN BHD",
            "jenis":"BANGLO 1 TINGKAT",
            "lokasi":"KOTA BHARU, KELANTAN"
        },
        {
            "id":"9",
            "title":"BANDAR BARU SETIA AWAN PERDANA, PERAK",
            "image":"/src/assets/r9.jpg",
            "pemaju":"NORTH ELEGANCE PROPERTY SDN BHD",
            "jenis":"SEMI-D 1 TINGKAT",
            "lokasi":"PORT DICKSON, NEGERI SEMBILAN"
        }],
        [
        {
            "id":"10",
            "title":"BANDAR BARU SETIA AWAN PERDANA, PERAK",
            "image":"/src/assets/r10.jpg",
            "pemaju":"NORTH ELEGANCE PROPERTY SDN BHD",
            "jenis":"TERES 1 TINGKAT",
            "lokasi":"PORT DICKSON, NEGERI SEMBILAN"
        },
        {
            "id":"11",
            "title":"BANDAR BARU SETIA AWAN PERDANA, PERAK",
            "image":"/src/assets/r11.jpg",
            "pemaju":"SETIA AWAN HOLDINGS SDN BHD",
            "jenis":"TERES 1 TINGKAT",
            "lokasi":"PERAK"
        },
        {
            "id":"12",
            "title":"BANDAR BARU SETIA AWAN PERDANA, PERAK",
            "image":"/src/assets/r12.jpg",
            "pemaju":"PASIR DELIMA SDN BHD",
            "jenis":"SEMI-D 1 TINGKAT",
            "lokasi":"DUNGUN, TERENGGANU"
        }] ,
        [
        {
            "id":"13",
            "title":"BANDAR BARU SETIA AWAN PERDANA, PERAK",
            "image":"/src/assets/r13.jpg",
            "pemaju":"PASIR DELIMA SDN BHD",
            "jenis":"SEMI-D 1 TINGKAT",
            "lokasi":"BESUT, TERENGGANU"
        },
        {
            "id":"14",
            "title":"BANDAR BARU SETIA AWAN PERDANA, PERAK",
            "image":"/src/assets/r14.jpg",
            "pemaju":"PASIR DELIMA SDN BHD",
            "jenis":"TERES 1 TINGKAT",
            "lokasi":"BESUT, TERENGGANU"
        },
        {
            "id":"15",
            "title":"BANDAR BARU SETIA AWAN PERDANA, PERAK",
            "image":"/src/assets/r15.jpg",
            "pemaju":"PASIR DELIMA SDN BHD",
            "jenis":"BANGLO 1 TINGKAT",
            "lokasi":"BESUT, TERENGGANU"
        }]  ,
        [ {
            "id":"16",
            "title":"BANDAR BARU SETIA AWAN PERDANA, PERAK",
            "image":"/src/assets/r16.jpg",
            "pemaju":"IKATAN INTRA SDN BHD",
            "jenis":"TERES 1 TINGKAT",
            "lokasi":"BACHOK, KELANTAN"
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
<div class="column is-one-third ">
<div class="card">
    <div class="card-image">
      <figure class="image is-4by3">
        <img src={p.image} alt={p.title}/>
      </figure>
    </div>
    <div class="card-content">
        <div class="content"><small>
            {p.pemaju}<br/>
            {p.jenis}<br/>
            {p.lokasi}</small>
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