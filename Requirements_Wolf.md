---
layout: default
title: Wolf Requirements
---

<html>
<title>W3.CSS</title>
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css">
<body>


<div class="w3-bar w3-red">
  <button class="w3-bar-item w3-button" onclick="openCity('CalloftheWild')">Call of the Wild</button>
  <button class="w3-bar-item w3-button" onclick="openCity('CouncilFire')">Council Fire</button>
  <button class="w3-bar-item w3-button" onclick="openCity('DutyToGodFootsteps')">Duty To God Footsteps</button>
  <button class="w3-bar-item w3-button" onclick="openCity('HowlingAtTheMoon')">Howling At The Moon</button>
  <button class="w3-bar-item w3-button" onclick="openCity('PawsOnThePath')">Paws On The Path</button>
  <button class="w3-bar-item w3-button" onclick="openCity('RunningWithThePack')">Running With The Pack</button>
</div>

<div id="CalloftheWild" class="w3-container city">
{% capture my_include %}{% include_relative _WolfAdventures/CalloftheWild.md %}{% endcapture %}
{{ my_include | markdownify }}
</div>

<div id="CouncilFire" class="w3-container city" style="display:none">
{% capture my_include %}{% include_relative _WolfAdventures/CouncilFire.md %}{% endcapture %}
{{ my_include | markdownify }}
</div>

<div id="DutyToGodFootsteps" class="w3-container city" style="display:none">
{% capture my_include %}{% include_relative _WolfAdventures/DutyToGodFootsteps.md %}{% endcapture %}
{{ my_include | markdownify }}
</div>

<div id="HowlingAtTheMoon" class="w3-container city" style="display:none">
{% capture my_include %}{% include_relative _WolfAdventures/HowlingAtTheMoon.md %}{% endcapture %}
{{ my_include | markdownify }}
</div>

<div id="PawsOnThePath" class="w3-container city" style="display:none">
{% capture my_include %}{% include_relative _WolfAdventures/PawsOnThePath.md %}{% endcapture %}
{{ my_include | markdownify }}
</div>

<div id="RunningWithThePack" class="w3-container city" style="display:none">
{% capture my_include %}{% include_relative _WolfAdventures/RunningWithThePack.md %}{% endcapture %}
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
