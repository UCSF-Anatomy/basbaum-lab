---
layout: default
title: Lab Members
permalink: /people/
---
<br>

## Primary Investigator

{% assign lab_member = site.lab_members | where:"positionCode", "0groupLeader"  | first %}

<div class="labMembersContainerTop labMembersContainer">
  <div>
    {% assign imgUrlLink = "/img/lab_members/" | prepend: site.baseurl | append: lab_member.imgLink %}
    <a href="{{ imgUrlLink }}" target="_blank"><img class="labMembers" src="{{ imgUrlLink }}" /></a>
  </div>
    <br>
  <div>
    <span class="labMemberName">{{ lab_member.name }}, {{ lab_member.degree }}</span>
    <span class="labMemberPosition">{{ lab_member.position }}</span>
    <span class="labMemberEmail">{{ lab_member.email | replace:'.',' [dot] ' | replace:'@',' [at] '}}</span>
    <div class="labMemberContent">{{ lab_member.content | markdownify }}</div>
  </div>
</div>

### Administrative Support
{% assign lab_member = site.lab_members | where:"positionCode", "1admin"  | first %}

<div class="labMembersContainerTop labMembersContainer">
  <div>
    {% assign imgUrlLink = "/img/lab_members/" | prepend: site.baseurl | append: lab_member.imgLink %}
    <a href="{{ imgUrlLink }}" target="_blank"><img class="labMembers" src="{{ imgUrlLink }}" /></a>
  </div>
    <br>
  <div>
    {% assign degree = lab_member.degree | strip_newlines %}
    {% assign websiteMember = lab_member.website | strip_newlines %}
    {% if degree == "" %}
      <span class="labMemberName">{{ lab_member.name }}</span>
    {% else %}
      <span class="labMemberName">{{ lab_member.name }}, {{ degree }}</span>
    {% endif %}
    <span class="labMemberPosition">{{ lab_member.position }}</span>
    <span class="labMemberEmail">{{ lab_member.email | replace:'.',' [dot] ' | replace:'@',' [at] '}}</span>
    <div class="labMemberContent">{{ lab_member.content | markdownify }}</div>
  </div>
</div>

## Current Lab Members
<div class="grid-container">
{% for lab_member in site.lab_members %}
  {% if lab_member.positionCode == "0groupLeader" %}
    {% continue %}
  {% elsif lab_member.positionCode == "1admin" %}
    {% continue %}
  {% endif %}
  <div class="labMembersContainer">
  	<div>
      {% assign imgUrlLink = "/img/lab_members/" | prepend: site.baseurl | append: lab_member.imgLink %}
  		<a href="{{ imgUrlLink }}" target="_blank"><img class="labMembers" src="{{ imgUrlLink }}" /></a>
  	</div>
    <br>
  	<div>
      {% assign degree = lab_member.degree | strip_newlines %}
      {% assign websiteMember = lab_member.website | strip_newlines %}
      {% if degree == "" %}
  		  <span class="labMemberName">{{ lab_member.name }}</span>
      {% else %}
        <span class="labMemberName">{{ lab_member.name }}, {{ degree }}</span>
      {% endif %}
  		<span class="labMemberPosition">{{ lab_member.position }}</span>
      <span class="labMemberEmail">{{ lab_member.email | replace:'.',' [dot] ' | replace:'@',' [at] '}}</span>
      {% if websiteMember == "" %}
        <!-- <span class="labMemberWebsite"><a href="{{ websiteMember }}" target="_blank"></a></span> -->
      {% else %}
        <span class="labMemberWebsite"><a href="{{ websiteMember }}" target="_blank">{{ websiteMember }}</a></span>
      {% endif %}
  		<div class="labMemberContent">{{ lab_member.content | markdownify }}</div>
  	</div>
  </div>
{% endfor %}
</div>
<hr>

## Former Lab Members

### Postdoctoral Fellows

<div class='formerLabMembers' markdown="1">

* Ingrid Abols
* Fatima Matos
* Kate Skinner
* [Susan Hockfield](https://hockfield.mit.edu)
* Robert Presley
* Ruth Riley
* Ellyn J. Glazer
* Terrence Coderre
* Igor Mitrovic
* Lilia Cruz
* Kathleen Gogas
* Annika Malmberg
* Steven Lakos
* Daniel Menétrey
* William Martin
* Hervé Martin
* Luc Jasmin
* Catherine Abbadie
* Hee Jung Cho
* Hantao Liu
* Serge Marchand
* Liang Liu
* Helen Wang
* Dawn Detweiler
* [Bradley Taylor](https://www.anesthesiology.pitt.edu/people/bradley-k-taylor-phd)
* William Eckert
* Simona Neumann
* Andy Ahn
* Katarina Nydahl-Sanderson
* Javier Mazario
* Jerome Bonnefont
* Tetsuro Nikai
* [Gregory Scherrer](https://www.scherrerlab.com)
* Jennifer Gibbs
* Noritaki Immamachi
* [Reza Sharif Naeini](https://www.mcgill.ca/shariflab)
* Jie Zhang
* Zhonghui Guan
* Carlos Solorzano
* Alex Etlin
* Julia Kuhn
* Line Loken
* Christopher Alvaro
<!-- Current
Joao Braz
Xiaobing Yu
Jarret Weinrich
Juan Salvatierra
Andrew Crowther
Mahsa Sadeghi
Biafra Ohanonu
Soha Chaaya
Julian Motzkin 
-->

</div>

### Graduate Students

<div class='formerLabMembers' markdown="1">

* Michelle Moss
* Geoff Kwiat
* David Reichling
* Shu-Ing Chi
* Jessica Brown
* Dana Rohde
* Yu-Qing Cao
* Myriam Gastard
* Jodie Trafton
* Karla Petersen
* Robin LeWinter
* Shannon Shields
* Dan Cavanaugh
* Rochelle Urban
* Dina Juarez-Salinas
* Todd Dembo
* May Tran
* Karuna Meda
* Racheli Wercberger

<!-- Current
Cindy Liu 
-->

</div>

<!-- 
* Mollie Bernstein
* Jiao Chen
* Zhongui Guan
* Katherine Hamel
* Julia Kuhn
* Jacqueline Leff
* Sung Joong Lee
* Sofie Line Loken
* Hongju Lui
* Karuna Meda
* Paul Su
* Wulin Tan
* Racheli Wercberger
* Chris Alvaro
* Ferda Cevikbas
* Todd Dembo
* Alex Etlin
* Noemie Frezel
* Harriet Heyman
* Dina Juarez-Salinas
* Yu Shi
* Carlos Solorzano
* May Tran
* Smitha Vaman
* David Villafuerte
* Xidao Wang
 -->