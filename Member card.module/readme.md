<h1>Member card</h1>
<p>This module is a customizable member card with optional social media buttons.</p>

<h2>Usage</h2>
<p>Just drag&drop it into your page. Works best when there are several next to each other. I'll recommend 3-4 in each row.</p>

<h2>Options</h2>
<ul>
<li>Profile image(image): Select your profile image</li>
<li>Title(text)<sup>*</sup>: If you'd like to prepend some title like "Dr." before the name.</li>
<li>First name(text)<sup>*</sup>: Your first name</li>
<li>Last name(text)<sup>*</sup>: Your last name</li>
<li>Position(text)<sup>*</sup>: If you'd like to add a position</li>
<li>Show social follow(boolean): If you'd like to add social follow icons below the position</li>
<li>Include FontAwesome(boolean): Load FontAwesome free(solid, regular, brands).<strong>Only activate this if you don't see icons</strong></li>
<li>FontAwesome weight(choise): Choose between solid or regular weight for non brand icons(if you select eMail in a social icon setting)</li>
<li>Social networks(repeater-group):
<ul>
<li>Social Link(link): Choose between external(to a social network) or eMail URL. If you select external only brand icons will work. If you select "email" the option "FontAwesome weight" will work.</li>
<li>Social icon(text): place the name of your icon here. <i>Example:</i> for the LinkedIn icon put fa-linkedin in the field</li>
</ul>
</li>
</ul>
<hr>
<sup>*</sup>: If left blank those options won't be rendered in the source code (to minimize HTML size and preserve the look of the card)

<h2>Style options</h2>
<ul>
<li>Spacing(spacing): Define the padding and margin of the member card. <strong>Margin will be applied to top and bottom since left & right will be defined through your templte columns</strong></li>
<li>Background color(color): Background color of the card</li>
<li>Border radius(number): Set a border radius for the card. For best looks all other border radius settings(image, social icons) are calculated and be half of the set radius</li>
<li>Social styling(group):
<ul>
<li>Transition(number): The time for smoother hover transition</li>
<li>Spacing(spacing): Spacing of the icons. <strong>Margin won't work since it can destroy the look&feel</strong></li>
<li>Default(group):
<ul>
<li>Background color(color): Color of the social icon background</li>
<li>Icon color(color): Color of the FontAwesome icon</li>
</ul>
</li>
<li>Hover(group):
<ul>
<li>Background color(color): Color of the social icon background on hover</li>
<li>Icon color(color): Color of the FontAwesome icon on hover</li>
</ul>
</li>
</ul>
</li>
</ul>