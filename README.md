# Aturtur's Cinema 4D Scripts
![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_Scripts.png "AR_Scripts")

My collection of Maxon Cinema 4D scripts. Made by [@aturtur](https://twitter.com/aturtur). Almost all scripts are commented to make learning Python scripting for Cinema 4D easier, faster and nicer. You can find more of Cinema 4D related stuff on my [blog](https://aturtur.com/) like: Generators, Effectors, Xpresso rigs etc. I share here scripts that I have wrote mainly for **myself**. Some scripts are for really specific tasks, some might be a bit old and obsolete and some are quite weird and experimental. Nonetheless, all scripts are done for learning purposes and having fun (and to help day to day work).

## Change Log
_No any changes so far..._

## How to use
In this section I go through how you install AR_Scripts to your Cinema 4D. These scripts are written for Maxon Cinema 4D R21.207 using Python version 2.7.14. Scripts are tested using Microsoft Windows. All of the script might not work with Mac.

Use at your own risk!

### Installation
Scripts should be installed to the folder where scripts have priviledges to write files, since some takes advantages for that.
Download this [repo](https://github.com/aturtur/cinema4d-scripts/archive/master.zip) and put AR_Scripts folder to following path:

#### Windows
`C:\Users\<USER>\AppData\Roaming\MAXON\Maxon Cinema 4D RXX\library\scripts`

#### OSX
`/Applications/MAXON/CINEMA 4D RXX/library/scripts`

Other way to find folder for installing scripts is to opening C4D and opening preferences (Ctrl+E / Cmd+E) and pressing 'Open Preferences Folder...' -button and navigating to library > scripts.

### Using scripts
When you have installed AR_Scripts you have to reboot Cinema 4D if it is already running. On start up Cinema 4D will scan scripts and you can find those under Extensions -> User Scripts -> AR_Scripts (R21). Script can also be found in commander (Shift+C).

You run the script simply by clicking it. Some scripts have multiple functions and you can use those with key modifiers (Alt / Ctrl / Shift) and different combinations.

## Script descriptions

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_AxisToCenter.png "AR_AxisToCenter") AR_AxisToCenter.py
Puts axis to center of the selected object(s) (works only with editable objects). If non-editable object is selected, tries to move the object to center of the children (does not support render instances).

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_BakeCameras.png "AR_BakeCameras") AR_BakeCameras.py
Bakes selected cameras to world space. It might feel that when running the script Cinema 4D freezes, but the script is just calculating. Give it some time. Preview range determines the baking range.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_BakeObjectPLA.png "AR_BakeObjectPLA") AR_BakeObjectPLA.py
Bakes selected object(s) to point level animation (PLA) in world space. Preview range determines the baking range.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_BakeObjectPSR.png "AR_BakeObjectPSR") AR_BakeObjectPSR.py
*Default:* Bakes selected object(s) to PSR animation in world space.
*Shift:* Bakes selected object(s) to PSR animation in local space.
Preview range determines the baking range.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_BooleMuch.png "AR_BooleMuch") AR_BooleMuch.py
Boole multiple objects with a single click. Creates intances of one 'booler' with PSR-constraint.
**Default:** First selected object is booler.
**Ctrl:** Last selected object is booler.
**Shift:** Creates a huge booler cube.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_BooleSplit.png "AR_BooleSplit") AR_BooleSplit.py
Creates a boole setup from two selected objects that creates a piece effect.
**Shift:** Uses instances.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_ConsolidateMaterialTags.png "AR_ConsolidateMaterialTags") AR_ConsolidateMaterialTags.py
Consolidates different polygon selections together that uses same materials. Messes up with material projection. Uses object selection.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_CopyTags.png "AR_CopyTags") AR_CopyTags.py
Copy selected tag(s) to selected object(s).

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_CopyToChild.png "AR_CopyToChild") AR_CopyToChild.py
**Default:** Creates a copy from the first selected object to the child of the rest of the selected objects.
**Shift:** Creates a copy from the last selected object to the child of the rest of the selected objects.
**Ctrl:** Creates an instance from the first selected object to the child of the rest of the selected objects.
**Ctrl+Shift:** Creates an instance from the last selected object to the child of the rest of the selected objects.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_CreateControlNulls.png "AR_CreateControlNulls") AR_CreateControlNulls.py
Create control null objects from selected point(s). Control nulls have frozen PSR by default.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_CreateFolderNull.png "AR_CreateFolderNull") AR_CreateFolderNull.py
Creates a folder null for easier organizing. I use this when I'm not using my Separator Null. Requires C4D R21. If there are selection, selected objects will be grouped under to the folder null.
**Shift:** Assign folder null's layer to selected objects. Doesn't overwrite existing layers.
**Ctrl:** Assign folder null's layer to selected objects. Overwrites old layer.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_CreateGuide.py.png "AR_CreateGuide.py") AR_CreateGuide.py.py
Creates a guide object from two selected objects or two selected points.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_CreateOwnMaterials.png "AR_CreateOwnMaterials") AR_CreateOwnMaterials.py
Creates (clones) own materials for selected object(s) from existing materials.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_CreateSpline.png "AR_CreateSpline") AR_CreateSpline.py
Creates a spline(s) multiple different ways. Sometimes also with dynamics!
#### No any object selection
**Default:** Creates a simple two point spline on Z-axis.
**Shift:** Creates a simple two point spline on Y-axis.
**Ctrl:** Creates a simple two point spline on X-axis.
#### One or multiple spline object(s) selected**
**Default:** Creates a dynamic spline from a static spline with controllers on both ends (user input for subdivision).
**Shift:** Creates a dynamic spline from a static spline with controllers for every spline point (user input for subdivision).
#### Multiple objects selected
**Default:** Creates a one static spline from selected objects' positions.
**Shift:** Creates multiple static splines betweeen selected objects.
**Ctrl:** Creates a one dynamic spline from selected objects (user input for subdivision). 
**Ctrl+Shift:** Creates multiple dynamic splines from selected objects (user input for subdivision).

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_CreateStickyNulls.png "AR_CreateStickyNulls") AR_CreateStickyNulls.py
Creates null object(s) with constraint tag (clamp) from selected point(s) or creates null objects with constraint tag (PSR) from selected object(s).

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_CreateVertexMap.png "AR_CreateVertexMap") AR_CreateVertexMap.py
**Default:** Creates a vertex map tag for selected object(s)
**Shift:** Creates a vertex map tag with linear field object.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_DistributeKeys.png "AR_DistributeKeys.py") AR_DistributeKeys.py
**Default:** Distributes selected keyframes evenly.
**Shift:** Give step (in frames) to distribute (user input).

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_DoomThisTagType.png "AR_DoomThisTagType") AR_DoomThisTagType.py
Removes selected tag type from selected objects. If there is no object selection, selected tag type will be doomed in whole project.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_EaseCopy.png "AR_EaseCopy") AR_EaseCopy.py
**Default:** Copies easing of selected keyframes in Timeline editor.
**Shift:** Copies easing of selected keyframes in F-Curve editor.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_EasePaste.png "AR_EasePaste") AR_EasePaste.py
**Default:** Pastes copied easing to selected keyframes in Timeline editor.
**Shift:** Pastes copied easing to selected keyframes in F-Curve editor.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_ExportOBJs.png "AR_ExportOBJs") AR_ExportOBJs.py
Exports top level objects individually to OBJ file. Does not export animation.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_ExportSplineSeq.png "AR_ExportSplineSeq") AR_ExportSplineSeq.py
Exports selected spline objects to Adobe Illustrator file sequence. Preview range will determine which frames will be exported. Don't use very complex shapes.
Check my After Effects script to import file sequence to Masks or Shape Objects.
**Shift:** Export objects to separated folders.
_Note: Do not use any special charactes in your objects names, do not even use a dot (.)._

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_ImportImageFolder.png "AR_ImportImageFolder") AR_ImportImageFolder.py
**Default:** Import image folder to materials.
**Shift:** Generates image planes.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_ImportOBJFolder.png "AR_ImportOBJFolder") AR_ImportOBJFolder.py
Imports OBJ-files from selected folder to the active document.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_MergeSelectionTags.png "AR_MergeSelectionTags") AR_MergeSelectionTags
Merges selection tags from selected objects. You can also select only tags that you want to merge together. Tags have to be same type.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_MoGraphSelectionTags.png "AR_MoGraphSelectionTags") AR_MoGraphSelectionTags
Creates MoGraph Selection Tag for every single clone.
_Note: If you have nested MoGraph generator, disable parent generator(s) before running this script._

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_MoGraphSelectionTagsFromSelectedClones.png "AR_MoGraphSelectionTagsFromSelectedClones") AR_MoGraphSelectionTagsFromSelectedClones.py
Creates MoGraph Selection Tag for every single clone that are selected.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_MoGraphSelectionTagsRange.png "AR_MoGraphSelectionTagsRange") AR_MoGraphSelectionTagsRange.py
**Default:** Create MoGraph Selection Tags from given range (user input).
**Shift:** Create one MoGraph Selection Tag from given range (user input).

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_NodesAlignHorizontally.png "AR_NodesAlignHorizontally") AR_NodesAlignHorizontally.py
Aligns selected graph nodes horizontally. Works in Xpresso graph and in Redshift material graph.
Xpresso tag or Redshift material has to be selected before running the script.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_NodesAlignVertically.png "AR_NodesAlignVertically") AR_NodesAlignVertically.py
Aligns selected graph nodes vertically. Works in Xpresso graph and in Redshift material graph.
Xpresso tag or Redshift material has to be selected before running the script.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_NodesConnect.png "AR_NodesConnect") AR_NodesConnect.py
**Default:** Connect nodes, if possible. Priorities empty ports. Works with multiple node selections. The node that are located the most left is the node that is outputting connections.
**Shift:** User input - which port is outputting to which port.
**Ctrl:** Same as the default function, but start at the last port.
Works in Xpresso graph and in Redshift material graph. Xpresso tag or Redshift material has to be selected before running the script.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_NodesDisconnect.png "AR_NodesDisconnect") AR_NodesDisconnect.py
Disconnect all connection(s) of selected node or connection(s) between selected nodes. Works in Xpresso graph and in Redshift material graph. Xpresso tag or Redshift material has to be selected before running the script.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_NodesDistributeHorizontally.png "AR_NodesDistributeHorizontally") AR_NodesDistributeHorizontally.py
Distributes selected nodes horizontally. Works in Xpresso graph and in Redshift material graph. Xpresso tag or Redshift material has to be selected before running the script.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_NodesDistributeVertically.png "AR_NodesDistributeVertically") AR_NodesDistributeVertically.py
Distributes selected nodes vertically. Works in Xpresso graph and in Redshift material graph. Xpresso tag or Redshift material has to be selected before running the script.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_NodesLineUpHorizontally.png "AR_NodesLineUpHorizontally") AR_NodesLineUpHorizontally.py
**Default:** Lines up selected graph nodes horizontally.
**Shift:** Lines up selected graph nodes horizontally by given amount (user input).
Works in Xpresso graph and in Redshift material graph. Xpresso tag or Redshift material has to be selected before running the script.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_NodesLineUpVertically.png "AR_NodesLineUpVertically") AR_NodesLineUpVertically.py
**Default:** Lines up selected graph nodes vertically.
**Shift:** Lines up selected graph nodes vertically by given amount (user input).
Works in Xpresso graph and in Redshift material graph. Xpresso tag or Redshift material has to be selected before running the script.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_NodesRSQuickMatte.png "AR_NodesRSQuickMatte") AR_NodesRSQuickMatte.py
Adds quickly Redshift matte AOV to selected material(s) and object(s) and material tag(s). Requires Redshift. Make sure that you have already set Redshift as your render engine for the document.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_NodesTextureControllers.png "AR_NodesTextureControllers") AR_NodesTextureControllers.py
Creates shared scale, offset and rotate control nodes for selected Redshift texture and triplanar node(s). Requires Redshift. Redshift material has to be selected before running the script.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_ObjectToSpline.png "AR_ObjectToSpline") AR_ObjectToSpline.py
Converts selected object(s) to splines.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_OpenProjectFolder.png "AR_OpenProjectFolder") AR_OpenProjectFolder.py
Opens the folder in explorer where the project is saved.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_OpenRenderFolder.png "AR_OpenRenderFolder") AR_OpenRenderFolder.py
Opens the folder in explorer where the project is rendered. Supports some tokens, but not all. Supported tokes: $prj, $res, $camera, $take, $fps. Supports folder variables: './../'.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_PixeurToMaterials.png "AR_PixeurToMaterials") AR_PixeurToMaterials.py
Create materials from Pixeur color palette file.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_PrintType.png "AR_PrintType") AR_PrintType.py
Prints selected object(s) type (ID). Utility script for helping for scripting.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_RandomColors.png "AR_RandomColors") AR_RandomColors.py
**Default:** Sets random display color to selected object(s).
**Shift:** Sets random grey value to selected object(s).
**Alt:** Resets display colors to selected object(s).

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_RandomizeOrder.png "AR_RandomizeOrder") AR_RandomizeOrder.py
**Default:** Randomize order of selected objects in Object Manager.
**Shift:** Sort selected objects in alphabetical order (A-Z).
**Ctrl:** Sort selected objects in reversed alphabetical order (Z-A).
Objects have to be in same level in the hierarchy.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_ReferenceViewport.png "AR_ReferenceViewport") AR_ReferenceViewport.py
**Default:** Creates a reference view port for helping to animate stuff.
**Shift:** Create reference background.
**Ctrl:** Delete reference setups.
_Note 1: You have to enable 'Full Animation Redraw' in Preferences/View._
_Note 2: If you cant see the reference plane, try to change 'View Clipping' settings in 'Project Settings'._

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_RemoveEmptySelectionTags.png "AR_RemoveEmptySelectionTags") AR_RemoveEmptySelectionTags.py
Removes empty selection tags from selected object(s) or if no selection all possible ones in the whole project.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_RemoveMissingTextureTags.png "AR_RemoveMissingTextureTags") AR_RemoveMissingTextureTags.py
**Default:** Removes texture tags that does not have assigned material.
**Shift:** Remove texture tags with missing selection tags.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_RemoveTags.png "AR_RemoveTags") AR_RemoveTags.py
Removes all tags. If object(s) selected removes tags only from selected object(s).

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_RemoveTextureTags.png "AR_RemoveTextureTags") AR_RemoveTextureTags.py
If there is no selected objects, script will remove every texture tags in the whole project. If there is selected object(s), script will remove texture tags from selected object(s).

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_ReplaceObjects.png "AR_ReplaceObjects") AR_ReplaceObjects.py
Replace objects with instance/copies of first/last selected object.
**Default:** Replace objects with instances of the first selected object.
**Shift:** Replace objects with instances of the last selected object.
**Ctrl:** Replace objects with copies of the first selected object.
**Ctrl+Shift:** Replace objects with copies of the last selected object.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_ResizeCanvas.png "AR_ResizeCanvas") AR_ResizeCanvas.py
Resizes canvas without changing the perspective. Changes active render settings resolution and selected/active camera's sensor size (film gate) and possibly also film offsets. 
_Note: If you don't have custom camera active or selected, script will modify default viewport camera's settings. You can reset default viewport camera with "View -> Frame Default"._

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_SelectActiveCamera.png "AR_SelectActiveCamera") AR_SelectActiveCamera.py
Selects the active camera in the object manager.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_SelectByVisibility.png "AR_SelectByVisibility") AR_SelectByVisibility.py
**Default:** Select objects that are visible in editor.
**Shift:** Select objects that are visible in render.
**Alt:** Select objects that are invisible in editor.
**Alt+Shift:** Select objects that are invisible in render.
**Ctrl:** Deselect objects that are visible in editor.
**Alt+Ctrl:** Deselect objects that are invisible in editor.
**Ctrl+Shift:** Deselect objects that are visible in render.
**Alt+Strl+Shift:** Deselect objects that are invisible in render.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_SelectChildren.png "AR_SelectChildren") AR_SelectChildren.py
**Default:** Select children of selected object(s).
**Shift:** Keeps also original selection selected.
**Ctrl:** Select children from given level _(+Shift: Keep old selection)._
**Alt:** Select siblings from given level _(+Shift: Keep old selection)._

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_SelectCousins.png "AR_SelectCousins") AR_SelectCousins.py
**Default:** Selects the object's Cousins.
**Ctrl:** Deselect original selection.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_SelectDeepest.png "AR_SelectDeepest") AR_SelectDeepest.py
**Default:** Select children of selected object(s) that are the most deep in hierarchy.
**Shift:** Keep the original selection.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_SelectDown.png "AR_SelectDown") AR_SelectDown.py
**Default:** Selects the first child object(s).
**Shift:** Keeps the old selection.
**Ctrl:** Safe mode (keeps the last selected if next not found).

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_SelectEffectors.png "AR_SelectEffectors") AR_SelectEffectors.py
Selects MoGraph Effector(s) that use(s) selected Field. Selects MoGraph Effector(s) that are used in selected Generator. Does not support subfields or tags.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_SelectEveryNth.png "AR_SelectEveryNth") AR_SelectEveryNth.py
**Default:** Selects every odd object in the object manager.
**Shift:** Select every even object in the object manager.
**Ctrl:** Select every nth object in the object manager (user input).
**Alt:** Select reversed nth object in the object manager (user input).
Supports object selections.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_SelectGenerators.png "AR_SelectGenerators") AR_SelectGenerators.py
Selects MoGraph generator(s) that use(s) selected effector. Prints info also to console.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_SelectNext.png "AR_SelectNext") AR_SelectNext.py
**Default:** Selects the next object(s).
**Shift:** Keeps the old selection.
**Ctrl:** Safe mode (keeps the last selected if next not found).

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_SelectObject.png "AR_SelectObject") AR_SelectObject.py
**Default:** Select tag(s) object(s).
**Shift:** Keeps the old selection.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_SelectPrev.png "AR_SelectPrev") AR_SelectPrev.py
**Default:** Selects the previous object(s).
**Ctrl:** Deselect original selection.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_SelectRoots.png "AR_SelectRoots") AR_SelectRoots.py
**Default:** Selects the root object(s).
**Shift:** Keeps the old selection.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_SelectSameColor.png "AR_SelectSameColor") AR_SelectSameColor.py
Selects object(s) with the same diplay color that the active object has.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_SelectSiblings.png "AR_SelectSiblings") AR_SelectSiblings.py
**Default:** Selects the object's siblings.
**Shift:** Keeps the old selection.
**Ctrl:** Safe mode (keeps the last selected if next not found).

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_SelectSourceObject.png "AR_SelectSourceObject") AR_SelectSourceObject.py
**Default:** Selects the source object. Supports Instance, Connect, MoInstance, MoSpline, Cloner and Matrix objects.
**Shift:** Keeps also original selection.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_SelectTags.png "AR_SelectTags") AR_SelectTags.py
**Default:** Select object(s) tag(s).
**Shift:** Keeps the old selection.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_SelectUp.png "AR_SelectUp") AR_SelectUp.py
**Default:** Selects the parent object(s).
**Shift:** Keeps the old selection.
**Ctrl:** Safe mode (keeps the last selected if next not found).

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_SequenceTracks.png "AR_SequenceTracks") AR_SequenceTracks.py
**Default:** Sequences selected animation tracks.
**Shift:** Set custom gap (frames) (values can be negative and positive).
**Ctrl:** Sequences selected animation tracks in ascending order.
**CtrlShift:** Ascending order + set custom gap.
_Note: Select whole tracks, not just keyframes!_

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_SetMoGraphWeightMap.png "AR_SetMoGraphWeightMap") AR_SetMoGraphWeightMap.py
Sets current MoGraph weights to new MoGraph weight map tag.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_ShiftSelectedTag.png "AR_ShiftSelectedTag") AR_ShiftSelectedTag.py
**Default:** Shifts selected tag(s) one step to the right.
**Shift:** Shifts selected tag(s) one step to the left.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_SplitByPolySelection.png "AR_SplitByPolySelection") AR_SplitByPolySelection.py
Splits object to individual objects by polygon selection tags.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_SwapObjects.png "AR_SwapObjects") AR_SwapObjects.py
**Default:** Swaps selected objects between each other.
**Shift:** Swaps also objects place in the hierarchy.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_TargetSniper_beta.png "AR_TargetSniper_beta") AR_TargetSniper_beta.py
Shoots ray from the selected camera(s) and cretes focus null to closest hitting point. Not recommended with heavy projects.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_ToggleEnable.png "AR_ToggleEnable") AR_ToggleEnable.py
Meant to be a replacement for the default 'Q' (Toggle Parent Generator) command.
**Default:** Enables or disables every possible selected generator.
**Shift:** Toggle next parent generator that is in the specific generator list.
**Ctrl:** Toggle root generator that is in the specific generator list.
**Alt:** Toggle generator family that are in the specific generator list.
_To make the script work like it is meant to be assing Q, Shift+Q, Ctrl+Q and Alt+Q shorcuts to the script in 'Customize Commands...' editor!_

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_ToggleGrid.png "AR_ToggleGrid") AR_ToggleGrid.py
Toggle grid visibility in viewport.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_ToggleTintedBorder.png "AR_ToggleTintedBorder") AR_ToggleTintedBorder.py
**Default:** Toggle opacity of tinted border in viewport.
**Shift:** Set the custom opacity value.
**Ctrl:** Toggle tinted border, but leave guide lines.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_VertexMapInvert.png "AR_VertexMapInvert") AR_VertexMapInvert.py
Inverts selected Vertex Map tag's data.

### ![alt text](https://raw.github.com/aturtur4d-scripts/img/AR_ViewportGradients.png "AR_ViewportGradients") AR_ViewportGradients.py
**Default:** Cycles through different background gradients for viewport. 
**Shift:** Default gradient (R21).
**Ctrl:** Dark gradient theme.
**Alt:** Cycles through user gradients.
**Alt+Ctrl:** Set gradient by name (user input).
**Alt+Ctrl+Shift:** Open txt-file for saving user gradients. Use hex color codes (#0000, #FFFFFF).
Basic gradients: Houdini, Maya, Dark, Old Cinema 4D, New Cinema 4D.
_Note: Change is permanent._

## Support me
If you find these scripts useful, consider to supporting me. It helps me to do more of these scripts and keeps my blog running. Make a tiny donation: [Tip jar](https://paypal.me/aturtur)

If you have any script ideas, you can DM me at [Twitter](https://twitter.com/aturtur).