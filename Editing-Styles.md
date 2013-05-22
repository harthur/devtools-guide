View and edit CSS with the **[[Inspector]]** and **Style Editor** tools.

### Viewing CSS rules for an element

View all the CSS rules that apply to an element by inspecting the node and checking out the **Rules** section in the Inspector sidebar:

[[images/rule-view.png|width=450px]]

#### :hover and pseudo-class styles

Fake `:hover`, `:active`, and `:focus` [pseudo-classes](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes) on an element with the node menu:

[[images/pseudo-class.png]]

### Computed Style

View the computed style of the node by checking out the **Computed** tab in the Inspector. These show the final computed values for the node's style properties.

[[images/computed.png|width=450px]]

### Box Model - Dimensions, Padding, Margin

Use the **Box Model** sidebar tab to see a visual diagram of the node's computed `width`, `height`, `margin`, `border`, and `padding`:

[[images/box-model.png|width=450px]]

### Fonts

See all the fonts used in the selected node in the **Fonts**. These are the exact fonts used by your system, so they'll differ based on which platform you're on:

[[images/fonts.png|width=320px]]

## Stylesheets

Any of the style sheet links in the **Rules** or **Computed** view will take you to the **Style Editor** tool. The Style Editor lists the style sheets in the document, including imported sheets, and lets you edit them:

[[images/style-editor.png|width=740px]]

### Saving Stylesheets

After making changes, save the stylesheet back to your local disk. Clicking **Save** will open a filepicker dialog, or will save back to disk immediately if you're editing from a file:// url or have saved it already in the same session.

### CSS Preprocessors

The Style Editor doesn't support source maps or CSS preprocessors (SASS, Less) right now, but should in the future.

## CSS Errors

Any CSS warnings or parsing errors can be found in the **Console**.

[Next: Debugging Javascript](Debugging JavaScript)
