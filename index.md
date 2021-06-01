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
 <input id="nameField" type="text" class="form-control"
 placeholder="Nume Prenume">
 <button class="btn btn-success custom" type="button" id="saveBtn"
         onclick="setNameData(()">Save</button>
 
 Nume prenume: " 
 <b>
  <span id="nameCookie"></span>
 <br>
</body>
