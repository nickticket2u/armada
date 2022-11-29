<style>
    a:visited,a:link{color:grey}
    
</style>


<script>
let email = 'shaharizal@lagendaarmada.com'

let fmail = 'wwwwwwwwww@lagendaarmada.com';
String.prototype.replaceAt = function(index, replacement) {
    return this.substring(0, index) + replacement + this.substring(index + replacement.length);
}
let i = 0;
function loop(){
    fmail = fmail.replaceAt(i,email.charAt(i))
    i++;
    if(i<10){
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
<b>No. Telefon : </b><br/>603-4131 7043
<br/><br/>
<b>E-mel :</b><br/>
{fmail}
</div></div>
</div>