# katharo
<h1>Hero slider</h1>
<p>A hero slider build upon <a href="https://swiperjs.com/">SwiperJS</a>.<p>

<h2>Usage</h2>
<p>Simply drag&drop it into your template or page. This module can be used multiple times on a page if you want to. But consider the notes</p>

<h2>Options</h2>
Slider Configuration(group): These settings will be applied to the whole module
<ul>
<li>Show arrows(boolean): Enable this to show clickable arrows left&right of each slide</li>
<li>Show pagination(boolean): Enable this to show a pagination(dots) at the bottom of each slide</li>
<li>Keyboard control(boolean): Enable this if you want to give the visitor the ability to navigate through the slides by keyboard arrows</li>
</ul>

Slides(repeater group): Set your individual slides here
<ul>
<li>Background style(choice): Select if you want a color or image as background for the single slide.</li>
<li>Background image(image): Select a background image for this slide. <strong>Only visible if you select "image" as background style.</strong></li>
<li>Background color(color): Set a background color for this slide. <strong>Only visible if you select "color" as background style.</strong></li>
<li>Top line(text): Enter some text above the headline.</li>
<li>Top line color(color): Select the color for the top line.</li>
<li>Headline(text): The main headline.</li>
<li>Headline size(choice): Select the H-tag size of the headline.</li>
<li>Headline color(color): Select the color of the headline.</li>
<li>Content(rich-text): Place your content here.</li>
<li>Add button(boolean): Enables Button option

  <ul>
<li>CSS class(text): Enter your button class(es) here.</li>
<li>URL(link): Select from your pages, enter an URL or an email adress.</li>
<li>Label(text): Give your button a label.</li>
</ul>
</li>
</ul>

<ul>Styles
<li>Spacing(padding): Set padding for all slides. <strong>Margin is disabled</strong></li>
<li>Highlight color(color): Set a highlight color for arrows and active pagination dot</li>
<li>Pagination color(color): Set the color for inactive pagination dot(s).</li>
<li>Arrow size(number): Set the size of arrows.</li>
</ul>