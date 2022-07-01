<h1> Macros </h1>

Here some of my go-to macros I'm using while developing themes. 

<h2>RGBA converters</h2>
Generates RGBA value for either background-color or color. You'll need:
<ul>
<li>HEX Value</li>
<li>Opacity</li>
</ul>

<strong>Usage:</strong>

background-color
<code>
{{ rgba_bg("020a10", 90) }}
</code>

will render
<code>
background-color: rgba(2, 10, 16, 0.9);
</code>

color
<code>
{{ rgba_color("020a10", 90) }}
</code>
will render
<code>
color: rgba(2, 10, 16, 0.9);
</code>


<h2>Shadows</h2>
Generates box-shadows for every major browser. You'll need
<ul>
<li>horizontal position</li>
<li>vertical position</li>
<li>blur</li>
<li>spread</li>
<li>shadow color</li>
</ul>

<strong>Usage:</strong>
<code>
{{ shadow(0, 8, 30,0, "#020a10", 30) }}
</code>

will render
<code>
-webkit-box-shadow: 0px 8px 30px 0px rgba(2, 10, 16, 0.3);
       -moz-box-shadow: 0px 8px 30px 0px rgba(2, 10, 16, 0.3);
            box-shadow: 0px 8px 30px 0px rgba(2, 10, 16, 0.3);
</code>


<h2>Transition</h2>
Generates perfect browser transitions. You'll need
<ul>
<li>Property</li>
<li>Transition time</li>
<li>Easing "animation"</li>
<li>Time format</li>
</ul>

<strong>Usage:</strong>
<code>
{{ transition("all", ".3s", "ease-in-out") }}
</code>

will render
<code>
    -webkit-transition: all .3s ease-in-out;
       -moz-transition: all .3s ease-in-out;
         -o-transition: all .3s ease-in-out;
            transition: all .3s ease-in-out;
</code>


<h2>Border radius</h2>
Generates a border-radius for every major browser technology. You'll need
<ul>
<li>Border radius</li>
<li>Format</li>
</ul>

<strong>Usage:</strong>
<code>
{{ border_radius(20, "px") }}
or
{{ border_radius("20px") }}
</code>

will generate
<code>
 -webkit-border-radius: 20px;
    -moz-border-radius: 20px;
      -o-border-radius: 20px;
         border-radius: 20px;
</code>


<h2>Linear gradient</h2>
Generates fully supported linear background gradient. You'll need
<ul>
<li>Angle</li>
<li>First color HEX value</li>
<li>First color opacity</li>
<li>First color position</li>
<li>Second color HEX value</li>
<li>Second color opacity</li>
<li>Second color position</li>
</ul>

<strong>Usage:</strong>
<code>
{{ linear_gradient("100deg", "#020a10", 100, 0, "#353b40", 100, 100) }}
</code>

will generate
<code>
background: #020a10;
background: -moz-linear-gradient(100deg, rgba(2, 10, 16, 1.0) 0%, rgba(53, 59, 64, 1.0) 100%);
background: -webkit-linear-gradient(100deg, rgba(2, 10, 16, 1.0) 0%, rgba(53, 59, 64, 1.0) 100%);
background: linear-gradient(100deg, rgba(2, 10, 16, 1.0) 0%, rgba(53, 59, 64, 1.0) 100%);
filter: progid:DXImageTransform.Microsoft.gradient(startColorstr="#020a10",endColorstr="#353b40",GradientType=1);
</code>


<h2>Radial gradient</h2>
Generates fully supported linear background gradient. You'll need
<ul>
<li>First color HEX value</li>
<li>First color opacity</li>
<li>First color position</li>
<li>Second color HEX value</li>
<li>Second color opacity</li>
<li>Second color position</li>
</ul>

<strong>Usage:</strong>
<code>
{{ radial_gradient("#020a10", 100, 0, "#353b40", 100, 100) }}
</code>

will generate
<code>
background: #020a10;
   background: -moz-radial-gradient(circle, rgba(2, 10, 16, 1.0) 0%, rgba(53, 59, 64, 1.0) 100%);
   background: -webkit-radial-gradient(circle, rgba(2, 10, 16, 1.0) 0%, rgba(53, 59, 64, 1.0) 100%);
   background: radial-gradient(circle, rgba(2, 10, 16, 1.0) 0%, rgba(53, 59, 64, 1.0) 100%);
   filter: progid:DXImageTransform.Microsoft.gradient(startColorstr="#020a10",endColorstr="#353b40",GradientType=1);
</code>

<h2>Font size generator</h2>
Generate a list of ratio related font sizes. You'll need
<ul>
<li>Default size (in most cases 16px/100%/1rem)</li>
<li>Headline font-family</li>
<li>Headline weight</li>
<li>Text font-family</li>
<li>Text weight</li>
<li>Line height</li>
<li>Size ratio (see list below)</li>

<strong>Ratio list</strong>
<table width="100%" border="0" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td>1.067</td>
      <td>Minor Second</td>
    </tr>
    <tr>
      <td>1.125</td>
      <td>Major Second</td>
    </tr>
    <tr>
      <td>1.200</td>
      <td>Minor Third</td>
    </tr>
    <tr>
      <td>1.250</td>
      <td>Major Third</td>
    </tr>
    <tr>
      <td>1.333</td>
      <td>Perfect Fourth</td>
    </tr>
    <tr>
      <td>1.414</td>
      <td>Augmented Fourth</td>
    </tr>
    <tr>
      <td>1.500</td>
      <td>Perfect Fifth</td>
    </tr>
    <tr>
      <td>1.618</td>
      <td>Golden ratio</td>
    </tr>
  </tbody>
</table>


<strong>Usage:</strong>
<code>
{{ fonts("16", "Arial, Verdana, sans-serif", 700, "Arial, Verdana, sans-serif", 400, 1.75, 1.250 ) }}
</code>

will generate
<code>
body{ line-height:1.75; }

h1,h2,h3,h4,h5,h6 {
        font-family: Arial, Verdana, sans-serif;
        font-weight: 700;
        line-height: 1.75;
}

h1{ font-size: 3.052rem; }

h2{ font-size: 2.441rem; }

h3{ font-size: 1.953rem; }

h4{ font-size: 1.563rem; }

h5{ font-size: 1.250rem; }

small, .small{ font-size: 0.80rem; }

p{
    font-family: Arial, Verdana, sans-serif;
    font-weight: 400;
    line-height: 1.75;
}
</code>

