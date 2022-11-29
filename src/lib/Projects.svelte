<style>
    a:visited,a:link{color:grey}
</style>


<script>

    let projects = [[
        {
            "id":"0",
            "title":"TAMAN DELIMA SAUJANA, TEMERLOH, PAHANG",
            "image":"/src/assets/p1.jpg",
            "image2":"/src/assets/l1.jpg",
            "location":`Pahang adalah negeri terbesar di Semenanjung Malaysia.
Hampir dua per tiga dari negeri ini masih diselubungi oleh hutan
hujan tropika yang menghijau, menjadikannya wilayah yang
indah dan subur dan sebagai perbendaharaan hidupan liar
sebagai tempat menarik di Pahang.

Ada banyak tempat menarik negeri Pahang yang boleh diterokai.
Antaranya ialah di Temerloh. Temerloh adalah sebuah bandar di
tengah-tengah negeri Pahang, yang terletak di persimpangan
antara Sungai Semantan dan Sungai Pahang. Temerloh
merupakan bandar Kedua terbesar dari segi pembangunan di
Pahang selepas Kuantan. Bandar ini bermula daripada aktiviti
perdagangan yang wujud sejak dahulu kerana daripada lokasinya
yang strategik. Jadi, amat sesuai untu mendirikan tapak
perumahan. Selain faktor kawasan yang stategik, factor
kemudahan jugak amat penting. Antara kemudahan yang
terdapat di Temerloh ialah Hospital, Sekolah, Bank, dan lain-lain.
`
        },
        {
            "id":"1",
            "title":"TAMAN TEROH ANGGUN, KARAK",
            "image":"/src/assets/p2.jpg",
            "image2":"/src/assets/l2.jpg",
            "location":`Karak juga merupakan kawasan yang sangat strategik untuk
didirikan tapak perumahan kerana kawasannya tidak jauh
dengan Ibu Negara iaitu Kuala Lumpur. Karak merupakan
bandar kecil di Pahang, Malaysia.

Ia dikenali sebagai Bandar Persinggahan untuk perjalanan
melalui Lebuhraya Karak dan Lebuhraya Pantai Timur dari Kuala
Lumpur ke Kuantan. Terdapat sebuah lebuhraya penyambung
di bandar ini untuk ke selatan iaitu Lebuhraya Karak Selatan`
        },  
        {
            "id":"2",
            "title":"KALUMPANG,HULU SELANGOR, SELANGOR",
            "image":"/src/assets/p3.jpg",
            "image2":"/src/assets/l3.jpg",
            "location":`Kalumpang merupakan salah satu mukim yang terdapat dalam
daerah Hulu Selangor. Pekan Kalumpang terletak di tepi jalan raya
antara Kuala Lumpur - Ipoh pada batu 46, dimana kedudukan yang 
sangat strategik untuk didirikan taman perumahan. 
Di sini juga terdapat beberapa kampung dan taman perumahan. 

Selain itu, Kalumpang juga mempunyai tarikan pelancongan. Antara 
salah satu tarikan pelancongan yang banyak terdapat di Kalumpang
ialah alam semulajadi. Kecantikan alam semulajadinya sangat
mengasyikkan dan pasti menggamit ramai pengunjung yang 
cintakan kedamaian. 

Oleh yang demikian, pembinaan perumahan yang berdekatan
dengan tarikan pelancongan amat sesuai sekali`
        }                                                                      
    ]]

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

{#if selected==null}
{#each projects as pp,index2}
<div class="columns">
{#each pp as p, index}
<div class="column">
<div class="card" on:click={()=>{more(p)}} style="margin-bottom:10px;margin-top:10px;" ontouchcancel="o()" ontouchend="o()" ontouchstart="o(this)" onmouseover="o(this)" onmouseout="o()">
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
            <a href="#a2">Lihat ➡️</a>
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