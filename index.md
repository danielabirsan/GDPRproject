<script> 
 function alertCookie() 
 { 
 alert(document.cookie);
 } 
 function checkCookie() {
  var username = getCookie("username");
  if (username != "") {
   alert("Welcome again " + username);
  } else {
    username = prompt("Please enter your name:", "");
    if (username != "" && username != null) {
      setCookie("username", username, 365);
    }
  }
}
 </script> 
 
 
 <body>
 Nota de informare
 <input id="nameField" type="text" class="form-control " placeholder="Nume Prenume">
 <button class="btn btn-success custom" type="button" id="saveBtn" onclick="setNameData()">Save</button>
 <Br></Br>
 <input id="browserField" type="text" class="form-control " placeholder="Browser">
 <span id="nameCookie"></span>
 <button class="btn btn-success custom" type="button" id="saveBtn2" onclick="setBrowser()">Save</button>
<br><br><br>
Cookies Data<br>
 Nume prenume: <b><span id="nameCookie"></span></b><br>
	Browser: <b><span id="browserCookie"></span></b><br>
	OS: <b><span id="detectOS"></span></b><br>

