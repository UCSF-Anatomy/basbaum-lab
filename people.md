---
layout: default
title: Lab Members
permalink: /people/
---
<br>

## Primary Investigator

{% assign lab_member = site.lab_members | where:"positionCode", "0groupLeader"  | first %}

<div class="labMembersContainerTop">
  <div>
    <a href="{{ lab_member.imgLink }}" target="_blank"><img class="labMembers" src="{{ lab_member.imgLink }}" /></a>
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

<div class="labMembersContainerTop">
  <div>
    <a href="{{ lab_member.imgLink }}" target="_blank"><img class="labMembers" src="{{ lab_member.imgLink }}" /></a>
  </div>
    <br>
  <div>
    <span class="labMemberName">{{ lab_member.name }}, {{ lab_member.degree }}</span>
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
  		<a href="{{ lab_member.imgLink }}" target="_blank"><img class="labMembers" src="{{ lab_member.imgLink }}" /></a>
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

### Former Lab Members
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