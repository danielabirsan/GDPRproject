<body>
<input id="nameField" type="text" class="form-control " placeholder="Nume si Prenume">
<button class="btn btn-success custom" type="button" id="saveBtn" onclick="setNameData()">Save</button>
<br>	

<input id="browserField" type="text" class="form-control " placeholder="Browser">
<button class="btn btn-success custom" type="button" id="saveBtn2" onclick="setBrowser()">Save</button>
<br><br>

Nume si Prenume: <b><span id="nameCookie"></span></b><br>
Browser:<b><span id="browserCookie"></span></b><br>
OS:<b><span id="detectOS"></span></b><br>

<hr>
<div style="text-align:center; font-family:'Arial Black';"> Notă de informare privind prelucrarea datelor cu caracter personal </div>
<br>

<p>Universitatea Tehnică din Cluj-Napoca aplică începând cu 25 mai 2018 Regulamentul General al Uniunii Europene nr. 679/2016 privind protecția datelor cu caracter personal și libera circulație a acestora, modificată și completată și fundamentul Legii nr. 506/2004 privind protecția datelor cu caracter personal și protecția vieții private în comunicații electronic. Astfel Universitatea Tehnica din Cluj-Napoca, Masterul e-Activități are obligația de a administra în condiții de siguranță și numai în scopurile specificate datele personale pe care ni le furnizați despre dumneavoastră. </p>
<p>Vă notificăm faptul că datorită temeiului legal aplicabil în România și a relației contractuale în care vă aflați cu Universitatea Tehnică din Cluj-Napoca, Masterul e-Activități și stagiul de mobilitate Erasmus în UK, aceasta procesează pe perioada relațiilor contractuale datele cu caracter personal furnizate de dumneavoastră în scopul gestionării statutului de student în cadrul UTCN și gestionarea comunicării între UTCN și Universitatea din UK pentru transferul dumneavoastră la Universitatea din UK, pentru înregistrarea rezultatelor dumneavoastră obținute după parcurgerea stagiului de mobilitate Erasmus în scopul promovării. </p>
<p>Dumneavoastră sunteți obligat/ă să furnizați datele necesare în identificarea dumneavoastră în calitate de student al Universității Tehnice din Cluj-Napoca iar refuzul dumneavoastră determină imposibilitatea efectuării stagiului de mobilitate Erasmus prin sfârșitul sau anularea acestuia. Dacă în timpul stagiului nu mai doriți prelucrarea datelor cu caracter personal, rezultatele obținute nu vor mai putea fi colectate și va duce la nerecunoașterea acestuia din punct de vedere educațional.</p> 
<p>Datele cu caracter personal sunt utilizate de către operator și comunicate Universității Tehnice Cluj-Napoca, Master e-Activități, responsabililor pentru stagiul de mobilitate Erasmus din cadrul universității, Universitatea din UK și ambasada UK care eliberează documentele necesare deplasării studentului în UK. </p> 
<p>Conform Legii nr. 677/2001, beneficiați de dreptul de acces, de intervenție asupra datelor, dreptul de a nu fi supus unei decizii individuale și dreptul de a vă adresa justiției. Totodată, aveți dreptul să vă opuneți prelucrării datelor personale care vă privesc şi să solicitați ștergerea datelor*. Pentru exercitarea acestor drepturi, vă puteți adresa cu o cerere scrisă, datată și semnată la departamentul PDP al Universității Tehnice din Cluj Napoca. De asemenea, vă este recunoscut dreptul de a vă adresa justiției.</p> 
<p>Dacă unele din datele despre dumneavoastră sunt incorecte, vă rugăm să ne informați cât mai curând posibil.</p> 


<br><br>
<a target="blank" href="https://didatec-my.sharepoint.com/:w:/r/personal/birsan_da_daniela_utcluj_didatec_ro/Documents/GDPR/BirsanDaniela_NotaImformare.docx?d=w1e77f07dc5d6447589635821f9908136&csf=1&web=1&e=vFQKnk">
	<button class="btn btn-warning">Analiza DPIA</button>
</a>
</body>

<script> 

	function setNameData(){
		let element = document.getElementById('nameField');
		document.cookie = "data="+element.value;
		let btn1 = document.getElementById('saveBtn');
		document.getElementById('nameCookie').innerHTML=element.value;
	}

	function setBrowser(){
		let element = document.getElementById('browserField');
		document.cookie = "data="+element.value;
		let btn2 = document.getElementById('saveBtn2');
		document.getElementById('browserCookie').innerHTML=element.value;
	}	

	var OSName = "Unknown";
	if (window.navigator.userAgent.indexOf("Windows NT 10.0")!= -1) OSName="Windows 10";
	if (window.navigator.userAgent.indexOf("Windows NT 6.2") != -1) OSName="Windows 8";
	if (window.navigator.userAgent.indexOf("Windows NT 6.1") != -1) OSName="Windows 7";
	if (window.navigator.userAgent.indexOf("Mac")            != -1) OSName="Mac/iOS";
	if (window.navigator.userAgent.indexOf("X11")            != -1) OSName="UNIX";
	if (window.navigator.userAgent.indexOf("Linux")          != -1) OSName="Linux";
	document.cookie = "operating-system="+OSName;
	document.getElementById('detectOS').innerHTML=OSName;
</script>
