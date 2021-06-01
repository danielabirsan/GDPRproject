<script> 
document.cookie = "session= test GDPR";
 document.cookie = "username=Daniela Birsan"; 
 document.cookie = "favorite_task=collect Data";

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
</body>
