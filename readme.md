# VRC AV3 Creator Tooling/Workflows

A mix of tooling, references, and other useful bits for Avatars 3.0 Creation.



# Tools

## VRC-Related

- [SDK3-Avatars](https://vrchat.com/download/sdk3-avatars) - Core SDK
- [VRChat Creator Companion (VCC)](https://vcc.docs.vrchat.com/) - This will become very useful soon, hopefully

## Unity

### Core

Tools that are universally useful when creating avatars.

- [Avatars 3.0 Emulator](https://github.com/lyuma/Av3Emulator) (Lyuma) - Test av3 systems in-editor. Can test local-remote sync, toggles, gesture layer, etc.
- [Pumkin's Avatar Tools](https://github.com/rurre/PumkinsAvatarTools) - Copy components hierarchically between scene prefabs, reset avatar pose, etc.
- [Avatar Evaluator (VRAM Estimator)](https://github.com/Thryrallo/VRCAvatarTools/) (Thryrallo) - Estimate avatar VRAM usage. Essential for optimization.
- [Hierarchy2](https://assetstore.unity.com/packages/tools/utilities/hierarchy-2-166483) (truongnguyentungduy) - Annotate and organize Unity hierarchy, showing scripts. Free alternative to other hierarchy tooling.
- [Avatars 3.0 Manager](https://github.com/VRLabs/Avatars-3.0-Manager) (VRLabs) - Flexibly merge animator controllers. Useful for building systems modularly and installing prefabs.
- [Copy Bounding Box](https://jessycat92.gumroad.com/l/RQDoUj) (Jessica92) - Transfer or generate bounding box from one Skinned Mesh Renderer to all children of a specified prefab. Prevents premature renderer culling.

### Unity-related

- [AssetBundleStat](https://vsk.lox9973.com/abstat/) (lox9973) - View actual compressed size makeup of `.vrca` files. Useful for optimizing download size.

### Niche

Tools that are very useful in the area of their specific functionality.

- [AnimatorExtensions](https://github.com/lukis101/VRCUnityStuffs) (DJLukis.LT) - Fix some rough edges in Animator editing. Requires [Harmony](https://github.com/pardeike/Harmony/releases).
- [VRWorld Toolkit](https://github.com/oneVR/VRWorldToolkit) (OneVR) - Use to set up post-processing. Ignore most other functions.
- [Lightbox Viewer](https://github.com/hai-vr/lightbox-viewer) (Hai) - Material lookdev assistant, double check shading setups.
- [ComboGestureExpressions](https://github.com/hai-vr/combo-gesture-expressions-av3) (Hai) - Handle complex hand gestures. Doing it by hand isn't worth it.
- [VRCFury](https://gitlab.com/VRCFury/VRCFury) (Senky Dragon) - Tool with eclectic functionality. Useful Write Defaults ON -> OFF converter included.
- [VRCAutoUpload](https://gitlab.com/VRCFury/VRCAutoUpload) (Senky Dragon) - Skip upload confirmation screen. Useful for fast iteration.
- [SmartTexture](https://github.com/s-ilent/SmartTexture) (Silent) - ScriptedImporter to create packed textures. Doesn't create extra assets.
- [Texture2dArray Import Pipeline](https://github.com/pschraut/UnityTexture2DArrayImportPipeline) (pschraut) - ScriptedImporter to create a tex2darray from a set of textures. Doesn't create extra assets.

## Blender

- [Blender to Unity FBX Exporter](https://github.com/EdyJ/blender-to-unity-fbx-exporter) (EdyJ) - export FBX with correct settings, removes unnecessary armature rotations and ensures uniform 1.0 scaling.
- [Apply Modifier With Shape Keys](https://github.com/przemir/ApplyModifierForObjectWithShapeKeys) (przemir) - Apply modifiers to meshes with shape keys. Slow but effective.
- [Bone Manager](https://fin.gumroad.com/l/STdb) (fin) - Name and manage bone layers without Blender's ancient, unintuitive system.
- LoopTools - Included with blender. Trivializes loop cleanup (spacing, circularizing, smoothing).

# Workflow Notes

## Unity

- Prefix filenames with asset type. `m_` for materials, `t_` for textures, `fbx_` for models, `a_` for animations, `ac_` for animator controllers, etc. This sorts them automatically. 
- Enter Play Mode Settings (Edit -> Project Settings -> Editor): Experimental option to disable reloading scene/domain on play mode. Speeds up playmode immensely. May cause issues.
- Slider at the bottom right of the project window controls thumbnail/item size - fully left makes it a detail list
