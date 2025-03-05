# Registraion-form
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="initial-scale=1.0, maximum-scale=1.0, user-scalable=1">
<title>Home</title>
<style media="screen">
*,*:after,*:before{
-webkit-box-sizing: border-box;
-moz-box-sizing: border-box;
-ms-box-sizing: border-box;
box-sizing: border-box;
}
body{
font-family: arial;
font-size: 16px;
margin: 0;
background: #068abc;
color: #000;
display: flex;
min-height: 100vh;
justify-content: space-around;
align-items: center;
}

.form_box{
width: 450px;
background:#ffffff;
padding: 30px;
border-radius: 7px;
box-shadow: 0 0 20px rgba(0,0,0,0.2);
}
h1{
  text-align: center;
  margin-top: 0;
  margin-bottom: 50px;
}
.input-row{margin-bottom: 13px; position: relative;}
.form_box input:not([type="submit"]),
.form_box textarea,
.form_box select{
font-family: arial;
width: 100%;
margin: 0 0 3px;
padding: 13px 15px;
font-size: 20px;
color: #000;
border-radius: 5px;
background: #d3d1d1;
border: 1px solid transparent
}
*::-webkit-input-placeholder {
opacity: 1;
color: inherit;
}
.form_box textarea{ height: 100px; resize: none; }

.form_box input[type="submit"]{
padding: 10px 50px;
font-size: 20px;
cursor: pointer;
border-radius: 5px;
border:0;
color: #fff ;
background: #00668d;
margin: 0 auto;
display: block;
}
.form_box input[type="submit"]:hover{ background: #000; }

.error{
display: block;
font-weight: 700;
font-size: 14px;
color: red;
display: none;
}

</style>
</head>
<body>
<div class="container">
  <form name="custom_form" id="customForm" onsubmit="return FormValidation()" action="valid.html">
    <div class="form_box">
      <h1>Registration Form</h1>
      <div class="input-row">
        <input type="text" name="name" placeholder="Name*">
        <span class="error">Please Enter Your Name</span>
      </div>
      <div class="input-row">
        <input type="text" name="email" placeholder="Email*">
        <span class="error">Please Enter Your Email</span>
      </div>
      <div class="input-row">
        <input type="text" name="phone" placeholder="Phone*">
        <span class="error">Please Enter Your Phone</span>
      </div>
      <div class="input-row">
        <select name="subject">
          <option value="">Subject*</option>
          <option value="Design">Web Designer</option>
          <option value="Develpment">Frontend Developer</option>
          <option value="Marketing">Backend Developer</option>
        </select>
        <span class="error">Please Enter Your Subject</span>
      </div>
      <div class="input-row">
        <input placeholder="Message*" name="message">
        <span class="error">Please Enter Your Message</span>
      </div>
      <input type="submit" value="Submit" name="">
    </div>
  </form>
</div>
<script>
function FormValidation(){
//alert("Alert")
var name=document.custom_form.name;
var email=document.custom_form.email;
var phone=document.custom_form.phone;
var subject=document.custom_form.subject;
var message=document.custom_form.message;
var conditions=document.custom_form.conditions;

if (name.value == "") {
   name.nextElementSibling.style.display = "block";
   name.style.border = "1px solid #f00";
   return false
}else{
  name.nextElementSibling.style.display = "none";
  name.style.border = "1px solid transparent";
}
if (!email.value.match(/^([\w-\.]+@([\w-]+\.)+[\w-]{2,4})?$/) || email.value == "") {
   email.nextElementSibling.style.display = "block";
   email.style.border = "1px solid #f00";
   return false
}else{
  email.nextElementSibling.style.display = "none";
  email.style.border = "1px solid transparent";
}
if (!phone.value.match( /^\(?([5-9]{1})\)?([0-9]{9})$/) || phone.value == "") {
   phone.nextElementSibling.style.display = "block";
   phone.style.border = "1px solid #f00";
   return false
}else{
  phone.nextElementSibling.style.display = "none";
  phone.style.border = "1px solid transparent";
}
if (subject.value == "") {
   subject.nextElementSibling.style.display = "block";
   subject.style.border = "1px solid #f00";
   return false
}else{
  subject.nextElementSibling.style.display = "none";
  subject.style.border = "1px solid transparent";
}
if (message.value == "") {
   message.nextElementSibling.style.display = "block";
   message.style.border = "1px solid #f00";
   return false
}else{
  message.nextElementSibling.style.display = "none";
  message.style.border = "1px solid transparent";
}
}

</script>
</body>
</html>
