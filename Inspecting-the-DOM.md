Inspecting the [DOM](https://developer.mozilla.org/en-US/docs/DOM) of a web page is possible with the **[[Inspector]]** and **3D View** tools.

#### Selecting a node

Once the **Inspector** tool is open and you mouse over the page, a dashed outline will highlight the current DOM node you're hovering over. Clicking will lock that DOM node for further inspection:

[[images/highlighter.png]]

#### Navigating with Markup View

The markup view shows you the current DOM tree in HTML markup. It highlights the currently selected node in grey. Navigate to other nodes by clicking or using the arrow keys:

[[images/markup-view.png|width=600px]]

#### Breadcrumbs
The breadcrumbs are a list of nodes in the hierarchy of the currently selected node, displayed along the top of the markup view. Navigate to a node by clicking or using the arrow keys. Navigate to a sibling node by pulling down the context menu on the breadcrumb.

[[images/breadcrumbs.png|width=650px]]

You can navigate the entire DOM tree from either the markup view or the breadcrumbs.

#### Node Search
Use the node search to the right of the breadcrumbs to quickly find nodes that match a selector. Entering a selector will highlight the first node that matches that selector. Pressing `Enter` will navigate to the next node that matches.

[[images/node-search.png|width=650px]]

#### 3D View

Navigate with a 3D view of the DOM with the 3D View tool ([[images/3d-view-icon.png]] button on the devtools window):

[[images/3d-view.png|width=700px]]


## Editing the DOM

You can edit DOM nodes extensively in the markup view. Double click or press `Enter` on any node to edit it. Change the tag name, edit attribute names and values, add attributes, and change the values of text nodes:

[[images/markup-editing.png]]

### Node menu
Right-click a node in the markup view and breadcrumbs to open the node menu. Use this menu to delete the node, copy its HTML content, and lock pseudo-classes like :hover:

[[images/node-menu.png|400px]]


[Next: Editing Styles](Editing Styles)

