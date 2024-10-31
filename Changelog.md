## Version 2.21.5.0

### Changes

* Some optimizations for the measure tool arrows display.
* Random material Id tool: Added UI, added an option to set a random id for each selected editable poly object

### New

* Replicator: A dialog to change settings has been added. New settings include toggles for keeping properties of the original nodes, like layer, material, and linking.

### Fixes

* Installer: When deselecting the "extras" component during the installation, a waring will raise after starting 3ds Max, indicating that some components are missing.

## Version 2.21.0.0

### Changes

* Measure dimension tools
  * Changed the way that text labels are displayed, for readability: Now the background is ON by default, has more margin around the text legend and the color can be configured.
  * Added options:
    * "Offset from origin" setting, to render the dimension lines away from the measure points. This can be found on the "Set units"dialog.
    * "Arrowheads angle": Now you can control the aperture angle for the arrowheads. This can be found on the "Set units"dialog.
    * "Extension line length": The extension lines at the measure points can now be customized. This can be found on the "Set units"dialog.
    * Added an option in the history dialog to turn on/off arrowheads.
    * Option in the configuration dialog to globally turn on/off arrowheads.
* Several optimizations done to the graphic functions that displays visual information and gizmos.
  * All the text labels that shows measurements, like distances and angles are now rendered with a background.
* Angle between edges: The tool is now interactive, allowing to change the edges selection and the active object. When turning off the tool, if you have changed the current object selection, it will ask if you want to change the object instead of deactivate the tool.

### Known issues

The color of the text labels backgrounds (besides the measure distance tools) that can be changed in the configuration dialog will be blended with the current wireframe color. A workaround is unchecking the random colors option (in the color picker) setting a default light gray color, and using a dark color for the texts background (via de config. dialog).

### Fixes

* Fixed a problem with normal gamma correct tool: Error triggered if V-ray or Corona render are not installed.

## Version 2.20.3.0

### Fixes

* Installer:
  * Install directory always falls back to %APPDATA%
  * Error message after uninstall/reinstall.

## Version 2.20.2.0

### Fixes

* MacroScripts failing to find scripts

## Version 2.20.0.0

### New

* Added support for 3ds max 2025

### Fixes

* Position tools: The objects were positioned in an unexpected order.
* Code optimization, faster startup.
* Fixed a problem that caused a crash when an invalid license was used.

### Changes

* Reorganized the menu.
* Removed support for versions prior to 3ds max 2018. This was done to streamline the development.
* Changed the files structure and install directory. Now the plugin content is installed in the ApplicationPlugins folder instead of the main 3ds max installation, following the recent guidelines for plugin developers.

## Version 2.10.5.0

### Fixes

* camera manager: fixed FOV parameter
* explode/merge: fixed problem with non editable-ploy objects
* modifiers presets: fixed problem that crashed the tool when adding a modifier to a group
* measure tools: fixed a problem that caused the tool to end after the first measure

## Version 2.10.4.0

### Fixes

* reDimension tool: fixed undo.

## Version 2.10.3.0

### Fixes

* critical fix for reDimension tool.

## Version 2.10.2.0

### Fixes

* critical fix for reDimension tool.

## Version 2.10.1.0

### Fixes

* critical fix for 1D align tool.

## Version 2.10.0.0

### New

* Vertices ALign: Align the selected vertices. 1- Select a set of vertices or edges. 2- Click an origin point and an end point, to define a straight line to which to align the vertices. Only works with Editable Polys
* Modifiers Presets: new tool to store presets for modifiers.
* refGuides: Compute line guides intersection. If you move the guides, delete the intersection points, or just forgot to enable the setting to create them, and needs the intersection points, use this action.
* Select with same material: A more convenient quick way to select objects sharing the same material.

### Fixes

* Color clipboard: color swatches were shown with alpha values.
* Mirror tool: the UI dialog background was transparent uin 3ds Max 2024.
* Eyedropper gbuffer function was broken
* reference rotation: angle tracking was inverted, incorrect angle tracking in certain situations.
* refGuide - polar mode: angle tracking was inverted, misplaced text labels.
* Distribute tool: wrong positioning of objects
* refGuides delete tool: The filters to remove only one type of object were not working properly.

### Changes

* Added some missing icons
* Optimizations in Eyedropper tool
* Some general code-maintenance adn optimizations

## Version 2.9.8.1

### Fixes

* Missing icons
* Small UI fixes
* Camera Manager: Fixed a bug causing the tool to crash then the cameras list was updated after deleting the active camera.

## Version 2.9.8.0

### New

* Angle between two edges
  * Select two edges in an Editable poly or mesh object.
  * Turn on the tool to show the angle between these two edges. Check the button again to change the object or to disable the tool.

### Changes

* Angle between two faces: The tool have been improved to work with any geometry type. Also, it no longer needs an object to be selected for it to work.
* intersection points tool have been improved to show each placed line at the same time.
* Some minor optimizations

### Fixes

* Line guide UI dialog was displayed with a transparent background. Added radio buttons for options that were placed in a context menu.
* The tooltips for the line guide unit display tools were swapped.
* Fixed non functional quick access UI floaters.
* Stamp Tool: fixed a problem with the tool crashing at start.

## Version 2.9.7.1

### Fixes

* Detailer:
  * Error "no .count property in obj" when only one base object is selected
  * Optimizations
* Error in scale lock switch

## Version 2.9.7.0

### New

* Edge Length tool:
  Change edge length. Works Only with Editable Poly objects.
    1. Select the Editable Poly object and start the tool.
    2. Select a set of edges you want to modify and select a reference vertex for each edge, it will be used as a base point to set the direction of the operation.
      If no vertex is selected the tool will use the first one that finds.
    3. Options: Max, minimum, and average length, custom value.
* Measure distance: added an option to draw the dimension line with arrowheads

### Fixes

* History Dialog: Fixed a crash related to the UI
* Replicator group mode toggle was not working properly
* Array Polar UI scaling broke the angle pick dial

### Changes

* Dimension object creation: updated and simplified the dimension object reposition UI dialog.
* Viewport Composition Guides: Use right-click in the add guide buttons to clean the guides
* Stamp tool moved to "extras"
* Code quality changes

## Version 2.9.6.0

### New

* 3ds Max 2024 support.
* Dimension tool improvements: Dimension objects
  * Expanded the customization:
    * Now it is possible to change the arrow heads style. Available styles are: Arrow, Triangle, Circle, Ticks.
    * You can set an offset parameter to move the line away from the points.
    * Added extension lines to better mark the start and end of the dimension line
    * New "Solid rendering" option creates an outlined spline with a extrude modifier applied. Lines thickness and extrude value can be controlled
    * After starting the tool, a new dialog to align the dimension and flip the text

### Fixes

* Some small fixes and optimizations
* Isolate layer tool will fail and hang 3ds max if the layer has child layers.
* Removed unnecessary script calls from the ribbon ui that were filling the log file.

## Version 2.9.5.2

### New

* Random swap transforms: randomly exchange the position-rotation-scale between a selection of objects.
  
### Changes

* Added a submenu for the Lock flag tools that where removed from the ribbon panel. This is now an optional feature installed with the "Extras"
* Added an icon for tools that were missing it.
* Re-arranged some tools. Integrated a few extra scripts from the freebies: Normal maps gamma adjust.
* Updated face ID tools, integrated "random ID set" in the floater dialog.
* Added a shortcut to a quick reference guide that contains a list of the available tools, and a short description of how to use them.

### Fixes

* Fixed a problem with the "mirror tool" that caused the UI dialog to be transparent
* Small usability fix for the "stamp tool": changing settings in the UI are now properly disabled when the tool is running.
* Some internal changes and minor UI fixes.

## Version 2.9.5.1

### New

* 1D array:
  * Press SHIFT when launching the tool to clone the source at the segments middle.
  * The clones will be aligned to the reference line direction. please note that the orientation will depend on the source object pivot.

### Enhancements

* Undocumented feature of "Reference rotation": If you hold CTRL key when performing the last step (rotation) the tool will rotate an instance of the object instead.
* Divide distance: the points will be aligned to follow the reference line direction.

### Fixes

* Fixed a problem with the "Pivot from 3 points" option when the tool is used directly from the shortcut.
* Improved some of the pivot tools to work with multiple selected objects at once.
* Some quality and performance improvements.

## Version 2.9.5.0

### New

* Tool to measure the angle between two polygons faces.
* Accumulative dimension Measure. Useful to visualize the length of a non linear path, or to get the perimeter of a shape.

### Enhancements

* Improved refRotation tool.
* General optimizations.

### Fixes

* Material Replacer tool was not working
* Fixed the configuration, some settings where not saved

### Fixes

* Mirror tool:
  * Fixed inverted rotation
  * Fixed clone mode not deactivating
  * Added a cancel button.
* ref Rotate: fix for inverted rotation result
* ref Scale: rewritten to be more reliable. In previous versions, the tool will fail if the reference vectors where perpendicular.
* cameraManager: Unlocked the rollout height. In displays with a resolution of 1080p some buttons where cropped
* Pivot tools:
  * Fixed Working Pivot to Pivot button
  * Added a tooltip for the "Pivot to Face" to express more clearly that only works with editable polys.
* infoTool: Fixed swapped dimension labels.

### New

* Added an option to disable Bounding box snap auto activation in certain tools.
* ref Rotate: If you press CTRL on the last step, the rotation is performed over a copy of the reference object.

## Version 2.9.4.3

### Fixes

* Mirror tool:
  * Fixed inverted rotation
  * Fixed clone mode not deactivating
  * Added a cancel button.
* ref Rotate: fix for inverted rotation result
* ref Scale: rewritten to be more reliable. In previous versions, the tool will fail if the reference vectors where perpendicular.
* cameraManager: Unlocked the rollout height. In displays with a resolution of 1080p some buttons where cropped
* Pivot tools:
  * Fixed Working Pivot to Pivot button
  * Added a tooltip for the "Pivot to Face" to express more clearly that only works with editable polys.
* infoTool: Fixed swapped dimension labels.

### New

* Added an option to disable Bounding box snap auto activation in certain tools.
* ref Rotate: If you press CTRL on the last step, the rotation is performed over a copy of the reference object.

## Version 2.9.4.2

### New

* Reference move tool (User requested): Move tool that uses two (origin and destination) reference points.
* Swap position tool (User requested): Select a collection of objects (will follow the selection pick order) and cycle their transform from one to the next.

### Fixes

* Fixed critical functionality problem with refGuides: Intersection points were not working correctly in 3ds Max 2022.
* Fixed configuration option to change refGuide object to standard splines.

### Enhancements

* Tested compatibility with 3ds Max 2023

## Version 2.9.4.1

### Fixes

* The angle measure tool was not displaying the angle correctly
* The area measure tool was not displaying the value and was throwing an error

### Enhancements

* reDimension tool has now an option to keep object proportions.
* Photographic composition guides updated to include golden ratio proportions.

## Version 2.9.4.0

### Enhancements

* New UI icons: Due to a data loss, the icons had to be redone. The new aesthetic is more consistent and blends well with native icons.
* Camera manager
  * Added control for f-number, shutter, and ISO
  * Replaced image aspect presets to aspect ratio «X:Y» format.
  * Added buttons to get the resolution/ratio from an image and the current viewport background.
* mtlReplacer received several improvements:
  * Simplified UI: to assign a replacement, select a material (or a range) in the list and double click to open the Material explorer.
  * Multi-materials are listed by default. Added support to list & replace sub-materials (one level deep, no nested materials, for now, a multi-level solution is on plans).
  * Added a "Use" column to the list that shows if the material is used in the scene or as sub-material.
* Incremental Isolation:
  * Added an indication of the current level (i.e: level 7)
  * Decreasing the level selected all visible objects. This was corrected to maintain the current selection. Known Issue: working in sub-object and changing the level will return to object mode.
  * Newly created objects in a level were not correctly added to the stack.
  * Hiding an object when at a level will not keep the visibility state going one level up/down. This was changed so the object will remain hidden.

### New

* Included extras*:
  * Texture maps filename search and replace
  * viewport composition guides

* Extras are tools that either do not fit well in another group of tools or are provided for free on our website and it is included in the package for convenience.

### Fixes

* layTools: Fixed undo actions
* mapTools: Optimized slow UI, fixed broken functionality
* Some general maintenance and optimizations.

## Version 2.9.3.1

### Fixes

* Divider tool: segments display didn't follow the mouse cursor in orthographic views
* Rotation tools
  * Crash when using 2.5D snap mode.
  * Ortho views were not restored after using the tool

## Version 2.9.3.0

### Enhancements

* Entirely rewritten Array tools
Besides setting up a framework that allows to expand the tools feature sets, these are the changes for now:
  * 2D Array: If you press SHIFT when executing the tool, the object will be cloned to the grid cells instead. Also a new Macro was added to use this mode: 2D Array - grid cells.
  * Pattern Array:
    * Simplified the UI, just one button to add/update the row-column rule.
    * Major enhancement and performance improvement in some cases.
* Paneling tool: Replaced the tool completely; the results will be the same, but is easier to use and follows the same mechanics that the 2D Array tool. For how-to-use, refer to the user guide.
* Replaced the "Welcome" dialog with some more useful information for new users.
* Some general optimizations all over the place, some tools should work faster in some cases.

### New

* Stamp tool (Experimental): Use an object to Interactively stamp its shape or cut holes in a mesh.

### Fixes

* Fixed a problem with eyedropper tool that caused the display of an error dialog after one use.
* The Drop Objects tool did not work as expected when the target object's pivot was displaced.
* Distribute tools that were broken.

## Version 2.9.2.0

* Reverted changes in Move and Align tool: Instead of picking an align origin point and reposition it until the tool is ended, now you can pick a origin-destination point pair each time.
* Fixed some issues with Camera manager not updating correctly.
* Material replacer: Now, after Applying changes, the list of materials is refreshed.
* Added a settings option to disable updates check.
* Incremental isolation now should include new objects created in the current isolation level.

## Version 2.9.1.2

### Fixes

* Distance measurements in orthogonal viewport were misplaced.
* Bounding box snap was still on after using Offset and reDimension tools.

## Version 2.9.1.1

### New

* Pivot to snap point: Quickly move an object's pivot to a snapping point.

### Enhancements

* Divide distance tool: viewport text that displays the number of segments and length was moved to follow the mouse position instead of being near start point
* Explode and Merge: Now pressing **CTRL** when executing the tool will skip the "keep original object" prompt.

### Fixes

* refGuides: Fixed broken "standard splines creation mode". NOTICE: It is reported that refGuides tools can conflict with the plugin "VG Snaps" and cause a total crash of 3ds Max, if you're having this issue, please let us know.

### Issues

* Tooltips: 3ds Max uses the MacroScripts tooltips to list them in customization and the new hotkey editor. This makes difficult to find the right tool. As a workaround the prefix "Dstlbx -" was added to the tooltips.

## Version 2.9.1.0

### New

* **Drop objects:** Drop objects on below surfaces. Press SHIFT when activating the tool to align the objects to the surface form.
* **Arrange objects (start-end objects):** Distribute objects (equally spaced) on a linear direction.  Direction and length of the distribution determined by the position of two objects: 1. Select the START OBJECT -- 2. Select the END OBJECT -- 3. Select the objects to distribute between them. * Press the TOOL BUTTON+SHIFT to conform and align the objects to the underlying surfaces.
* **Arrange objects (real-time):** Distribute objects (equally spaced) on a linear direction. Tracks the objects new position's in Real Time. Warning! slow.  When tracking positions: *Press SHIFT to conform to the underlying surfaces* Press CONTROL to orient to the underlying surfaces
* **Arrange objects (interactive):** Distribute objects (equally spaced) on a linear direction. Tracks the objects new position's with marks in the viewport.  When tracking positions: *Press SHIFT to conform to the underlying surfaces* Press CONTROL to orient to the underlying surfaces

>Check the user guide for detailed instruction of how this tools work

### Enhancements

* Renamed "Move around" tool to "Polar array" to better reflect its intent.
* Updated some icons to better match the overall look.
* Combined tools launch floater dialogs:
  * Updated to include latest tools.
  * Treated now as a "legacy" feature. Is moved to "Extras" optional installation category. Considering not to update it anymore (user feedback welcome) since it was introduced in the firsts versions, then the current 3ds Max menu system was not implemented yet, and it makes this dialogs irrelevant now.
* Added support for 3ds Max 2022

### Fixes

* Eyedropper: Fixed UVWmapping mode, it was broken in 2.9.0.0.
* Just some internal changes.

## Version 2.9.0.0

### New

* Three points align: Relocate a node from three pairs of points, from an origin position to a target position.
* Material replacer: Automate the process of replacing materials. Intended to be used when importing scenes from other sources.

### Enhancements

* Camera manager:
  * Added per camera preview of resolution aspect ratio.
  * Added support for state sets
* Improved some UI inconsistencies
* Added some missing icons
* Improved menu organization
* Reorganization of the ribbon interface
* Internal changes:
  * Changed how the tool is initialized.

### Fixes

* Paneling tool:
  * Fixed a crash when using "custom object" mode.
  * Improved UI for ease of use
  * Added a live preview of the panel grid
* Move and align tool: Better alignment result in some situations.
* Licensing: changed the way of obtaining a machine ID, to address the lack of support for devices without an ethernet port.
* General fixes and optimizations.

## Version 2.8.2.1

### improvements

* Eyedropper:
  * Added: option to match G-buffer ID.
  * Updated: Changed how node properties are classified: Common properties (by node type), Visual Properties and Render properties are now independent.
* Pivot tools: Added a command to match the node pivot position to the current Working pivot.

### Fixes

* Align assets: Fixed problem causing the pivots to be misplaced or the transform matrix corrupted.
* Crash on start due to ribbon panel.
* Minor fixes and improvements.

## Version 2.8.2.0

### New

* Quick Merge(attach) and Explode(Detach) for editable poly / editable mesh elements.
* Quick manage polygon material IDs

### improvements

* Improved Incremental Isolation tool. Added a dialog to control isolation level (Up and Down). moved it to the main toolset and added it to the ribbon.
* Improved ribbon organization and vertical layout.
* Improved algorithm of reference scale tool.
* Quick pivot: Added command to match a node pivot to the current working pivot position.

### Fixes

* Fixed a problem with the Macros activation under 3ds Max 2017
* Fixed behavior of reference guide in orthogonal views.
* Fixed problem with  reference delete tool. It removed just one at a time.
* Several bug fixes and optimizations.
* Fixed and improved "Scale factor" setting for Measure tools:
  * Units where wrongly calculated
  * Implemented an independent factor for linear - square - cubic units.

    Changing any of these values from the default 1.0 will not scale the values in the current Display Unit Scale (i.e.: 1.0m to 0.1m).
    The values will be printed in a generic unit representing the measured value transformed by the scale factor.
    The mapping is done this way:  
    Display Unit * Factor -> Scaled value in generic units  
    I.E.:
    * MEASUREMENT: 1.0m
    * Linear Units Scale factor: 0.01 (for printing the value in centimeters)
    * PRINTED RESULT: 100.0 u
* Fixed error in guide objects that disabled the command panel UI parameters.
* Fixed error in "Asset align" tool. Node pivots where wrongly repositioned.

## Version 2.8.1.0

This is a maintenance release, centered in fixing some critical bugs.

### Addressed Issues

* First Run or Reinstall actions: Under certain conditions, multiple error messages where displayed when opening Max. This has been fixed, also, some functionality (UI Reset and cleanup after uninstall or reinstall) that was mostly broken should be working now.
* Multi-Language compatibility improvements: If you change 3ds Max language, the ribbon Tab will be lost, and probably some tools will stop working. At installation time, 3ds Max language settings has been changed to allow selecting more than one. (Note that the only available language for DesignToolBox remains to be English)
* UVW transform tool: using random transform option was broken.
* 3ds Max compatibility issues:
  * versions 2015-2016: Fixed a problem causing tools to be disabled, UI issues, startup errors.
  * version 2021: Removed the use of no longer present default icons in ribbon or macros.
* Update checker: Now you can opt to not include this, un-checking the component in the installer.

## Version 2.8.0.0

### New

* **Points:** New tool for placing reference points at temporary guides intersections.
* **Renderable dimensions:** This was a old users request. The tool isn't perfect, and creates standard line shapes and text, but it does his commit.

### General and existing tools improvements

* Reworked how spinners values behave at different Max units configuration. It should be more consistent. i.e. Some default values where intended to be centimeters, if you set max to work with meters. In case the units where configured to centimeters, the value of the spinners where in millimeters, resulting in too small defaults.
* UI related: Ribbon tab, simplified reiterative tools and moved settings toggles to panel breaks to leave more room.
* General stability and improvements in viewport drawing methods. Some actions should be more fluid.
* Reworked how settings works. This is mostly internal and performance related, but in previous versions, there was some problems with tools not reflecting the changes.

### Fixes

* Resolved some problems with activation.
* In Demo mode (unlicensed) "activate now" dialogs and "Not activated" alerts where too obtrusive, and some features where broken.
* Issues with several tools were identified and fixed.

---

## Version 2.7.3.2

* Fixed problem with paneling tools and simplified UI
* Simplified Ribbon panel
* Improved Pivot from 3 points
* Fixed Problem with activation dialog

## Version 2.7.3.1

### Fixes

* Fixed critical issue with reflect tool.
* Fixed issue with older (pre 2017) Max versions. 3ds Max 2015 should work, but it will remain marked as unsupported.

## Version 2.7.3.0

### Improvements

* Reworked Isolate layer tool: now is faster and supports nested layers correctly
* Chances in layer on/off tool: Now pressing SHIFT when selecting the tool, it will work in ON mode with frozen objects.
* Reworked spatial info tool to make it more useful.
* Paneling tools had some major rework to make it faster and more reliable.
* Fixed some critical bugs.
* Fixed behavior of UI dialogs and buttons in toolbars/menus. Now buttons on toolbars, menu and ribbon properly opens-close tools with UI dialogs.
* Improved viewport graphics performance.
* Overall optimizations.

## Version 2.7.2.0

### Improvements

* Mirror tool:
  * Fixed "clone" mode not acting if no mirror axis is changed.
  * Improved:
    * Now mirror planes, and flip axis can be multi-checked.
    * Canceling the last plane-gizmo rotation does not end the tool.
* ColorBar: Added option to adjust colors brightness, saturation and hue.

### New

* Wirecolor adjust: Adjust selection wire colors. brightness, saturation and hue.
* Extras (Tools under "DSTLBX tools" category):
  * Bitmap multi-loader: Create SME Texture Nodes from multiple images with one action. With option to override gamma of loaded images.
  * Map name from file: rename scene texture maps with their correspondent filename.
  * Select without material.

### Fixes

* Error that causes the activation dialog to reopen.
* Improved licensing messages
* Error causing to accept invalid licenses.
* Error causing a valid license to fail.
* Error with menu generator

## Version 2.7.1.2

This is a maintenance version with small fixes.

## Version 2.7.1.1

### Fixes

* Addressed some issues with the activation system.
* Broken refGuides track angle snap.
* Fixed High DPI Icons

### New

* **Reflect tool**: Viewport interactive mirror tool. let's you set a 3d gizmo for freely position mirror planes.
* Added a simple action to rename Bitmap Textures to the filename of the corresponding image.

### Extra tools list as of version 2.7.1

* **File name to Map**:      Change the names of Bitmap Textures to the name of the loaded files.
* **Remove material**:       Remove material from selection
* **ID from camera**:        Set objects ID for current camera view
* **Face Id**:               Select faces w/ same ID
* **Random ID Set**:         Set random IDs
* **Incremental Isolation**: re-Isolate current selection
* **Toggle Trackbar**:       Toggle Time slider and Trackbar
* **Random Select**:         Select random nodes
* **Align Assets**:          Put nodes in line
* **Camera manager**:        Manage Cameras and render batch views.
* **Replace with Xref**:     Replace selected node with Xref Record.

## Version 2.7.0.0

THIS VERSION HAS SOME MAJOR CHANGES AND IS RECOMMENDED FOR ALL USERS

### Changes

* Updated license engine.
* Updated installer to support multiple 3ds Max versions on a single run.
* Rearranged some menu items. Fixed a problem with menu registration.
* Replicator:
  * Added option to replace the current selection. With an active nodes selection, press CTRL when activating Replicator tool and pick a source node to replace selection with.
  * Fixed error when replicating groups.
* Eyedropper
  * Added option to work with current selection (bucket mode). With an active nodes selection, press CTRL when activating one of the tools.
* Pattern Array.
  * Improved algorithm speed.
  * Small UI redesign.
  * Fixed crash bug when adding patterns.
* MultiMap tool: Separated functionalities in individual dialogs to improve speed.
* Improved speed of pivot tool.
* Fixed Ribbon tab not showing in certain conditions in 3ds Max 2020.

### New Features

* Added "Check for updates" feature.
* Extra tool added: Incremental Isolation.

## Version 2.6.4.2

Minor patch that address some issues and small features

* Added missing refGuides units parameter: Intersection point extension.
* Added more color customization options to refGuides configuration.
* Fixed problem with Live Info and protractor tool.
* Changed default refGuides ribbon button behavior: now the default action is "continued mode"
* Fixed uninstall leftover files that causes a MacroScript error.

## Version 2.6.4

* Changed behavior of rotation tools in 2D orthographic views: Now when working in a 2D view, the rotation axis will be set perpendicular to the view and then, the view will temporary change to the rotation work plane.
* Fixed error with rotation tools in Demo version.
* Fixed some MacroScript errors.
* Fixed problem with replicator.

## Version 2.6.3

* Fixed Resource error for 3ds Max versions prior to 2017

## Version 2.6.2

* Fixed fatal plugin error in 3ds Max 2016

## Version 2.6.1

* Fixed Offset tool error
* Fixed error with Parametric Array preview

## Version 2.6.0

This version addresses some problems found in the previous release and add some new features:

### New features

#### Move and align (1D Align tool)

Align objects using two directions from a common base point.

1. Select a target node. Pick a reference point and a target point to displace the node to a new position. This is a free space operation.
2. Pick one point to set a reference direction, and a target point to match the original direction to it.
3. Use Right Click or ESCAPE to end the tool.

#### Random transformations tool

Tool packed with several options to randomize and clone nodes.

#### Extra tool: Camera/Render batch manager

Tool intended to speed up the use of the native batch render tool.
Some features: Set render size per camera, add active view to batch render with auto naming and output path, Add multiple cameras with one action.

### Tools improvements and fixes

* Removed some outdated tools.
* Replicator tool:
  * Fixed problem with grouped objects
  * Changed the "groups mode" option to two separate parameters (for grouped nodes only):
    * Use source node entire group. On/Off Setting.
    * Replace target node entire group. On/Off setting.
  * Fixed instancing mode (was broken), added a note explaining this mode only works for ungrouped nodes.
* Local rotation tool:
  * Fixed problem with merged objects
  * Fixed incorrect angle measurement issue
  * Added option to have an additional reference point to offset the rotation angle measurement
* Area and volume measure:
  * Added parameter for units multiply factor.
* UVW Map tools:
  * Improved fitting algorithm.
  * Added option to change axis alignment
* Fixed problem with menu registration
* Fixed MacroScripts errors with 3ds Max 2016
* Fixed installer issues with version 2016 compatibility.

## Version 2.5.5

This version addresses some problems found in the previous release:

* **Backburner crash when submitting job fix** (This fix required to remove spinners from the Ribbon).
* Replaced Ribbon Spinners with dedicated dialogs, Ribbon cosmetic changes.
* Hardware Lock retrieval error fix.
* Eyedropper issues with groups, added some options.
* refGuides InfoDisplay fix.
* Incompatibility of previous version of refGuides objects causing "paramblock2" crash in scenes with saved refGuides objects. Solution: merge all except refGuides objects in new scene.

## Version 2.5.4

* Added complete tool set menu
* Fixed (partially) problem with *paramblock2*
* Fixed issues with UVW map transform tool
* Fixed behavior of Replicator with groups
* Added option to Replicator to propagate or not to instances
* Added random transformation tool
* Added extras: Random selection
* Code cleanup
* Minor UI fixes and rollout layouts change

## Version 2.5.3

* Fixed MacroScript error on max 2016
* Fixed Ribbon error on max 2019

## Version 2.5.2

### Tools improvements and fixes

* Updated Pivot tool
* Fixed Ribbon problem in Max 2019
* Fixed Multimap for referenced nodes
* Partially added Ribbon support for vertical layout

## Version 2.5

### Tools improvements and fixes

* Transform tools: Improved polar and orthogonal tracking.
* refGuides
  * Polar placing: Now, when placing the polar reference plane, you can orient and rotate (yaw-pitch-roll) it.
  * Orthogonal mode: Pressing *CTRL* will lock z-axis.
  * Removed option to place protractor with guide line.
  * New objects: Now line, protractor and intersection points are configurable **custom objects**, you can now snap to vertex at a intersection point.
* General performance improvements and fixes
  * Fixed error that causes the first install dialog to reappear at each launch.
  * Fixed error with random UVW map transformations.
  * Improved Pattern array.
  * Improved distance measure history dialog.
* Fixed problems in demo version.
* UI enhancements
  * Better tooltips, complete description in ribbon tooltips.
  * Some other refinements.
* Net rendering (Backburner): Install the demo version in the render nodes to avoid warnings and potential render job fail.
* Moved refGuides MacroScripts to category "refGuides"
* Moved DesignToolbox MacroScripts to category "Designtoolbox"; Optional features remains on category ~~"HAG tools"~~ (Replaced by DSTLBX tools).
* 3ds Max 2019 compatibility. Fixed compatibility with versions prior to 2017.

### New features

* New layer tools:
  * Isolate layers: Isolate the layers of the current selected nodes, or pick a node in the viewport.
  * Hide/freeze/Box Mode layer picking a node in the viewport.
  * Added shortcuts to ribbon for some useful layer commands not present in 3ds max UI.

## Version 2.4

* 3ds Max 2018 full support.
* Implemented Demo version.
* Fixes:
  * Fixed measure tool report.
  * General optimizations and fixes.
  * Updated activation dialog.
* New tool: Measure distance history dialog.

## Version 2.3 (internal - unpublished)

### New features

* Offset tool: added support for editable poly sub-selection.

## Version 2.2

### New features

* Pattern Array maker
* Fast Interactive (from viewport) 2D Array. Like the divide distance and clone tool, but in 2D.

#### New extras

* Resizer Modifier

### Tools improvements and fixes

* Fixed error on replicator when picking groups as target.
* reworked move around tool:
  * Added option to use current coordinates as rotation center. If you don't pick a center node, it will work with current coordinates origin instead.
  * Now works wit groups.
* Local rotation:
  * **Now works with Editable Poly sub objects.**
  * Fixed to work with groups.
  * Visual enhancements.
  * Fixed tracking with angle snap (shift) mode.
* Offset tool:
  * Complete rework to make it more simple to use and have a more logic approach.
* Fixed undo problems.
* Fixed downscale problem in dimension tool. Added "measure report" to listener.
* Fixed issues with map tools.
* Fixed redimension tool problem with displaced pivots.
* Addressed some problems with replicator tool: inverted UI switches, fixed problem when working with groups.
* refGuides Info display optimization.

#### General improvements and fixes

* Minor UI enhancements to better match UI color profile and 2017 interface.
* Core performance and fixes.

## Version 2.1

### Tools improvements and fixes

#### Local reference rotation

* Added preview of rotation axis
* Now works properly when working in grid space mode.

#### reDimension tool

* Resolved incorrect resizing
* Now works properly when working in grid space mode.

#### Reference scale

* Rewritten functionality, now should work on more situations and produce more correct results.
  * The behavior has changed, it no longer tries to match the first reference direction with the second, now it will match the first reference line length with the second, keeping the first line direction and proportions.

#### Local isolate

* Now works with Edit poly / Edit mesh face selection.

#### Offset tool

* Fixed incorrect undo handling

#### Angle measure

* Fixed wrong angular measurements

#### Divide distance

* Fixed Orthogonal tracking when working with an active grid

#### Measure distance

* Improved orthogonal tracking.
* Fixed behavior working in grid space.

#### General improvements and fixes

* Addressed incompatibility with 3Ds Max versions previous to 2016 (starting from 2014)
* Changed viewport elements colors, added a dialog to change the colors, including some presets.
* improved some performance and some general fixes all over the place.

## Version 2.00

* New Tools
  * unFreeze by selection.
  * Continued measure distance.
  * Spatial and standard transformations live info.
  * Map tools.
* New Features
  * reDimension:
    * Added orthogonal tracking.
    * Fixed incorrect results in scaled objects.
  * reference Scale:
    * Added keep proportions option.
    * Added Xform modifier mode.
    * Added Orthogonal tracking.
    * Enhanced behavior on certain situations, less incorrect results.
  * Measure Tool: Now the tape will be drawn until the next measurement.
  * Area measure: Added orthogonal tracking.
  * Divide tool
    * Added keyboard input mode instead of mouse movement.
    * Added Orthogonal tracking.
  * Move Around: Added clone object option.
* General changes
  * General stability improvements and fixes.
  * Improved viewports performance of refGuides tools.
  * Fixed "Lock" tool
    * Lock Object Scale wasn't working properly.
    * Fixed behavior when some locks were already enabled.
  * Measure Tool: Now the tape will be drawn until the next measurement.
  * Divide tool: more responsive segments selection.
  * MultiMap : Previous extra tools (fit, center and reset UVW Gizmo...) are now a separate tool.
  * Improved "put assets in line" with a options dialog.
* UI Improvements
  * Tooltips completion, information and ease of use tweaks
  * Redesigned "move Around" UI to make it more usable and straightforward.
  * Updated tools dialogs

## Version 1.87

* Due to activation problems on systems with virtual hardware drivers, an option has been added for selecting the device to lock the activation to.
* Fixed "Unhide by Selection" tool. Behavior with hidden layers, and hidden objects on hidden layers was not the expected.
* Fixed error when installing refGuides for the first time or on a fresh 3ds Max installation.
* Some other minor bug fixes.
* Added new Extras: "Put Assets in line": Aligns selected objects in a row. Useful for when you need to populate objects on a scene, for easy find and pick them.

## Version 1.86

* Fixed an error when pressing ESCAPE using Replicator/Eyedropper tools.
* User request feature: Added Orthogonal mode to Measure distance tool:
  * Pressing SHIFT when tracking distance will restrict to XYZ axes, on current active grid coordinates.
  * Pressing CONTROL on Orthogonal mode will lock the tracking to the current axis.

## Version 1.85

* **New Tools:**
  * **New Tool**: 2-point planar rotation (in local coordinates): DesignToolBox - 2point local rotation
  * New convenient Tool : Unhide by selection.
  * New Tool category: **Eyedropper**. Includes:
    * **Replicator**: in-viewport (pick and point) object replacer and instancer.
    * Eyedropper: in-viewport (pick and point) mass copier (transformation, material, general properties, mapping, modifiers …)
* Tool speed improvements:
  * Measure Area should work more fast.
  * Rework done to Paneling tool. Fixed thickness parameter, better object mode.
  * Paneling Detailer: Now it can be launch as a separate tool. Objects selection fixed, and added more mirror options (by number list).
* UI changes:
  * More complete Tooltips in Toolbars, Added tooltips in Ribbon and tools w/UI.
  * Some rework in Ribbon layout.
  * Added intersection mode (all guides or current) toggle command.
  * Reworked broken refGuides floater UI, fixed bugs and cosmetic changes.
  * Added a floater UI for the ToolBox.
  * Added a floater UI for the rest of the tools.
  * Some other small cosmetic changes (Icons, Paneling tool, in-viewport information to improve reading).

## Version 1.80

* Corrected broken functions in refGuides (lock guides, Objects color...)
* Added some refguides configuration options (intersections behavior)
* Updated refguides ribbon UI
* Minor bug fixes, Some improvements in core tools.
* Added: Transform Lock shortcuts. New Tool: Move Around.
* Added Ribbon Reset after uninstall
* Corrected licensing problems with some systems.
* IMPORTANT NOTE: This update requires reactivation, it's necessary to generate a new activation code request.

## Version 1.7

* Rewritten Dimension tool. Now it should work in most situations.
* Fixed reference Isolation Tool.
* Fixed some activation problems
* Improvements in Scale tool
* Several bug fixes
* Some cosmetic changes and cleaning

## Version 1.6

* Fixed compatibility issue with 3ds max 2014
* Fixed major bugs on "Dimension" tool
* refGuides now creates it's own custom object instead of splines.
* refGuides objects has now an option in the Modify panel for display properties and enable or disable LiveInfo for each object.

## Version 1.5

* New Tool:
  * "Distance Scale": Select an Object, Pick a reference vector and scale in current max's units instead of a scale factor.
* New extra Utility:
  * "Color Clipboard": Dockable color palette.
* Paneling tool improvements:
* Add detail function:
  * Option to mirror Odd or Even copies.
  * Added option for re-center detail's pivot
* Fixed an error causing bad positioning of objects
* Multimap: Randomizers should work as expected now.
* General Bug fixes.
* Other minor improvements.
* Added "lite" version.
