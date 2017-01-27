# HTML code standards
This document outlines the rules for writing HTML documents and fragments across all of our codebases.

## General rules
We write HTML5 markup, following XHTML standards for readability.
General rules for all HTML documents are:
 - HTML documents should use HTML5 doctype - `<!DOCTYPE html>`
 - Indent using 2 spaces
 - Tags and attributes should be lowercase (`<p class="intro">` not `<P CLASS="intro"`)
 - Use double quotes for attribute values
 - Close all elements - either a closeing tag (`<p>...</p>`) or self-closing (`<img src="jeff.jpg" />`)

 ## Template tags

 Template tags such as those found in Django templates should be indented as if they were nested HTML tags:
 ```
 <!--GOOD-->
 {% if people %}
   <ul>
     {% for people as person %}
       <li>{{ person.name }}</li>
     {% endfor %}
   </ul>
 {% endif %}

 <!--BAD-->
 {% if people %}
 <ul>
 {% for people as person %}
   <li>{{ person.name }}</li>
 {% endfor %}
 </ul>
 {% endif %}

 <!--BAD-->
 {% if people %}
 <ul>
   {% for people as person %}
   <li>{{ person.name }}</li>
   {% endfor %}
 </ul>
 {% endif %}
 ```
