# Snippets

For useful widgets and beautiful styling only some additional html does the trick. Below, there are custom snippets ready-to-use in your EN template. Just copy a snippet of your choice, select "HTML" in the EN editor and paste it there. Once you've pasted the snippet you may change back to "normal" to continue editing. Save and see the magic happen!

## copy boxes above the form fields

Everything that comes before the actual form fields in the right column (including the info toggle and the counter) needs to be wrapped in a div like this:

```html
<div class="above-form">
  content
</div>
```

This way your content gets the right colors, e.g. a white background instead of a grey one.

### background info

```html
<a class="info-toggle">More info</a>

<div id="background-info" class="background-info-hidden">
  <h2>Background info</h2>
  <p>more more more info</p>
</div>
```

The `.info-toggle` element enables the "show more info" logic. A click on the toggle shows the element with the id `#background-info` and hides the toggle.

### progress bar

```html
<div class="pgbar-thermometer" data-target="250" data-start="0" data-service="EaEmailAOTarget">
  <div class="t_body">
    <div class="t_level">&nbsp;</div>
  </div>
  <span class="t_current">0</span> people have taken action
</div>
```

Change the value of data-target according to your needs. Change data-start to add an initial value for the progress bar, e.g. offline supporters. Use data-service="NetDonor" on donation pages. If the data-attributes are missing, the default values shown above will be used instead.

## copy boxes below the form fields

Everything that comes below the actual form fields needs this wrapper:

```html
<div class="below-form">
  your content
</div>
```

This wraper is especially important because it not only sets the right colors but also ensures that the content appears below the submit button!

### disclaimer

To get a disclaimer text with the right styles, wrap it in a div of its own. Assuming the disclaimer is placed below the submit button, it looks like this:

```html
<div class="below-form">
  <div class="disclaimer">
    disclaimer text
  </div>
</div>
```

## thank you page

Since there are no form fields on the thank you page, all the right column content should get this wrapper:

```html
<div class="no-form">
  your content
</div>
```

## share links

These are social share buttons for Facebook, Twitter and e-mail-sharing:

```html
<div class="no-form">
  <ul class="share-links">

    <li class="facebook"><a class="button" href="https://www.facebook.com/sharer.php?u={{urlencoded url}}" title="Share this via Facebook!" target="_blank" data-share="facebook"><i></i><span>Facebook</span></a></li>

    <li class="twitter"><a class="button" href="http://twitter.com/share?text={{urlencoded share text}}&url={{urlencoded url}}" title="Share this via Twitter!" target="_blank" data-share="twitter"><i></i><span>Twitter</span></a></li>

    <li class="email last"><a class="button" href="{{EN email share url}}" title="Share this via E-Mail!" target="_blank" data-share="email"><i></i><span>E-Mail</span></a></li>

  </ul>
</div>
```

Make sure to replace the {{placeholder parts}} with the real urls and share texts! The name between <span>name</span> is what's displayed on the button itself, the title pops up when hovering over the botton.

## submission tracking

Place this snippet on the thankyou page to track submissions (it's hidden so it doesn't matter if it is inside a wrapper or not):

```html
    <input type="hidden" name="track-submission" value="1">
```
