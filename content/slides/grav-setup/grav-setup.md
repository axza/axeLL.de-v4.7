+++
authors = "admin"
categories = "opengeoedu"
date = 2020-03-06T11:21:57Z
draft = true
summary = "Mit diesen Schritten bauen Sie ein CMS nach dem OpenGeoEdu-Schema um OER-Inhalte zu veröffentlichen"
tags = ["foss", "oer", "grav", "opengeoedu"]
title = "Grav Setup"
[footer]
copyright = ""
tag = "2020-03-30T00:00:00+02:00"
twitterlink = "opengeoedu"
veranstaltung = "campustagung2020"
[slides]
highlight_style = "atom-one-dark"
parallaxbackgroundimage = ""
slidenumber = true
theme = "league"
transition = ""
transitionSpeed = ""

+++
<style>
.object-fit {
width: 300px;
height: 300px;
margin: 0em auto;
}
.object-fit img {
object-fit: cover;
width: 100%;
height: 100%;
}
</style>

<div class="object-fit">
<img src="/uploads/LOGO_open_geo_edu_RGB.png">
</div>
{{ with .Params.footer }}
<div id="oge-footer" class="footer">
<span class="element">{{ .tag }}}</span>
<span class="element">{{ .veranstaltung }}</span>
<span class="element"><a href="https://twitter.com/{{ .twitterlink }}">@{{ .twitterlink }}</a></span>
<span><a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons Lizenzvertrag" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png"></a></span>
</div>

<script type="text/javascript">
window.addEventListener("load", function() {

         revealDiv = document.querySelector("body div.reveal")
         footer = document.getElementById("oge-footer");
         revealDiv.appendChild(footer);
    
     } );

</script>

## FOSS nutzen um OER zu erstellen und zu veröffentlichen

***

# h1

***