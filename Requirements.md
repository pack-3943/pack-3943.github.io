---
layout: page
title: Requirements
permalink: Requirements
---

<html>
<title>W3.CSS</title>
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css">
<body>


<div class="w3-bar w3-orange">
  <button class="w3-bar-item w3-button" onclick="openCity('Games Tigers Play')">Games Tigers Play</button>
  <button class="w3-bar-item w3-button" onclick="openCity('Team Tiger')">Team Tiger</button>
  <button class="w3-bar-item w3-button" onclick="openCity('Tiger Bites')">Tiger Bites</button>
  <button class="w3-bar-item w3-button" onclick="openCity('Tiger Circles')">Tiger Circles</button>
  <button class="w3-bar-item w3-button" onclick="openCity('Tigers In The Wild')">Tigers In The Wild</button>
  <button class="w3-bar-item w3-button" onclick="openCity('My Tiger Jungle')">My Tiger Jungle</button>
</div>

<div id="Games Tigers Play" class="w3-container city">
{% capture my_include %}{% include_relative _Adventures/Games_Tigers_Play.md %}{% endcapture %}
{{ my_include | markdownify }}
</div>

<div id="Team Tiger" class="w3-container city" style="display:none">
{% capture my_include %}{% include_relative _Adventures/Team_Tiger.md %}{% endcapture %}
{{ my_include | markdownify }}
</div>

<div id="Tiger Bites" class="w3-container city" style="display:none">
{% capture my_include %}{% include_relative _Adventures/Tiger_Bites.md %}{% endcapture %}
{{ my_include | markdownify }}
</div>

<div id="Tiger Circles" class="w3-container city" style="display:none">
{% capture my_include %}{% include_relative _Adventures/Tiger_Circles_Duty_To_God.md %}{% endcapture %}
{{ my_include | markdownify }}
</div>

<div id="Tigers In The Wild" class="w3-container city" style="display:none">
{% capture my_include %}{% include_relative _Adventures/Tigers_In_Wild.md %}{% endcapture %}
{{ my_include | markdownify }}
</div>
<div id="My Tiger Jungle" class="w3-container city" style="display:none">
{% capture my_include %}{% include_relative _Adventures/My_Tiger_Jungle.md %}{% endcapture %}
{{ my_include | markdownify }}
</div>


<script>
function openCity(cityName) {
  var i;
  var x = document.getElementsByClassName("city");
  for (i = 0; i < x.length; i++) {
    x[i].style.display = "none";  
  }
  document.getElementById(cityName).style.display = "block";  
}
</script>

</body>
</html>
