---
title: Supporters
displaytext: null
layout: null
tab: true
order: 3
tags: okinawa
---

### List of Donors

[Donate](/donate/)ページで"Publicly list me as a supporter of OWASP Okinawa"を選択して寄付していただいた方々のリストです。

{% assign donors = site.data.ow_attributions | uniq | default: 'こちらに名前が掲載されます' %}
{% for donor in donors %}
* {{ donor | strip_html | strip }}
{% endfor %}

The OWASP Foundation is very grateful for the support by the individuals and organizations listed. However please note, the OWASP Foundation is strictly vendor neutral and does not endorse any of its supporters.  
Read more about our <a href="/www-policy/operational/donations" target="_blank" rel="noopener">Donation Policy</a>.
