# Change Log
All notable changes to this project will be documented in this file.

## v1.4.6 - 18th Oct, 2015

 - Add new feature `data-<attr>` for LI el of node


## v1.4.5 - 18th Oct, 2015

 - Add new feature `columns`
 	- option `columnsTpl` - inner template for columns
 	- option of node `columns` - array of columns, contains `{ 'class' : '', 'text':'' }`
 		-- `class` - some css class of column
 		-- `text` - some html value


## v1.4.4 - 18th Oct, 2015

 - Add new Event `onAfterRender`

 
## v1.4.3 - 15th Oct, 2015
 
  - fix CSS
  
## v1.4.2 - 14th Oct, 2015
  
   - fix

 
## v1.4.0 - 14th Oct, 2015

### New Features

 - Add node menu:
 	- option `menuTpl` - inner template for menu 
 	- option `showMenu` - enable node menu 
 	- event `onNodeMenuClick` - event on click on menu button
 	 
 	![f970bb36c4](https://cloud.githubusercontent.com/assets/5524684/10469016/d7b9fa04-721b-11e5-8499-4b097607bf39.jpg)
 
 
## v1.3.2 - 13th Oct, 2015

 - fix `redraw`
 
 
## v1.3.1 - 13th Oct, 2015

### New Features

- Add Tooltips

	- Node has `def` property 

	- New option `showTip`


## v1.3.0 - 12th Oct, 2015

### New Features

- New methods `reDrawNode` and `getDomNode`

- Change public method `render` 

- New properties `nodeLiClass` and `itemTemplate`
	
- New Events `onNodeHover` and `onNodeLeave`

- Fix `buildStyleOverride`

- more fixies



## v1.2.0 - 9th May, 2015

### New Features

- Disable nodes, allow a tree node to disabled (not selectable, expandable or checkable)

	- Added node state property `disabled` to set a node initial state

	- Methods `disableAll`, `disableNode`, `enableAll`, `enableNode` and `toggleNodeDisabled` added to control state programmatically

	- Events `nodeDisabled` and `nodeEnabled`

- Checkable nodes, allows a tree node to be checked or unchecked.

	- Added node state property `checked` to set a node initial state

	- Pass option `{showCheckbox: true}` to initialize tree view with checkboxes

	- Use options `checkedIcon` and `uncheckedIcon` to configure checkbox icons

	- Methods `checkAll`, `checkNode`, `uncheckAll`, `uncheckNode` and `toggleNodeChecked` to control state programmatically

	- Events `nodeChecked` and `nodeUnchecked`

- New option + node property `selectedIcon` to support displaying different icons when a node is selected.

- New search option `{ revealResults : true | false }` which when set to true will automatically expand the tree view to reveal matching nodes

- New method `revealNode` which expands the tree view to reveal a given node

- New methods to retrieve nodes by state : `getSelected`, `getUnselected`, `getExpanded`, `getCollapsed`, `getChecked`, `getUnchecked`, `getDisabled` and `getEnabled`


### Changes
- Removed nodeIcon by default, by popular demand.  Use `{nodeIcon: 'glyphicon glyphicon-stop'}` in initial options to add a node icon.

- Search behaviour, by default search will the expand tree view and reveal results.  Alternatively pass `{revealResults:false}`

- Method collapseNode accepts new option `{ ignoreChildren: true | false }`.  The default is false, passing true will leave child nodes uncollapsed


### Bug Fixes
- Remove unnecessary render in clearSearch when called from search

- Child nodes should collapse by default on collapseNode

- Incorrect expand collapse icon displayed when nodes array is empty




## v1.1.0 - 29th March, 2015 

### New Features

- Added node state properties `expanded` and `selected` so a node's intial state can be set

- New get methods `getNode`, `getParent` and `getSiblings` for retrieving nodes and their immediate relations

- New select methods `selectNode`, `unselectNode` and `toggleNodeSelected`

- Adding `nodeUnselected` event

- New global option `multiSelect` which allows multiple nodes to hold the selected state, default is false

- New expand collapse methods `expandAll`, `collapseAll`, `expandNode`, `collapseNode` and `toggleNodeExpanded`

- Adding events `nodeExpanded` and `nodeCollapsed`

- New methods `search` and `clearSearch` which allow you to query the tree view for nodes based on a `text` value

- Adding events `searchComplete` and `searchCleared`

- New global options `highlightSearchResults`, `searchResultColor` and `searchResultBackColor` for configuring how search results are displayed




## v1.0.2 - 6th February, 2015

### Changes
- jQuery dependency version updated in Bower

### Bug Fixes
- Events not unbound when re-initialised

- CSS selectors too general, affecting other page elements
