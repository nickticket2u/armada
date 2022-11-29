<style>
    a:visited,a:link{color:grey}
    
</style>


<script>
let email = 'shaharizal@lagendaarmada.com'

let fmail = '';
    

function loop(){
    fmail = email.substring(0,fmail.length+1);
    if(fmail.length!=email.length){
        setTimeout(loop,100);
    }
}
loop()

</script>
<div class="title is-4">

HUBUNGI KAMI

</div>

<div class="card">
    <div class="card-content">
        <div class="content">
Lagenda Armada Sdn. Bhd.<br/>
Suite 42-1, 1St Floor <br/>
Jalan Rampai Niaga 4<br/>
Rampai Business Park<br/>
53300 WP Kuala Lumpur
<br/><br/>
<b>No. Telefon : </b>603-4131 7043
<br/><br/>
<b>E-mel : {fmail}</b>
</div></div>
</div>