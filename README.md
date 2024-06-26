# VL.Mapper
## Projection mapping tool for [VVVV Gamma](https://visualprogramming.net/)
![Mapper UI](https://raw.githubusercontent.com/zekeadam/VL.Mapper/main/doc/img1.png)

### Features
- Linear and bezier grid warping
- Additive and subtractive masking
- Complex soft edge masks
- Multiple inputs and outputs
- Caching the mapping, after that the mapper can be disabled and a GPU shader runs the warping which uses close to zero resources
- Save and load mappings in UI
- Automatic backup every 5 minutes and keeping the last 100 saves in "documents\vvvv\mapper"
- Overlay images in the mapper UI for reference

![Soft edge masks](https://raw.githubusercontent.com/zekeadam/VL.Mapper/main/doc/img2.png)

### Sponsor
[Limelight Art](https://www.limelight.art)

### Demo video
https://youtu.be/nU4qOoorldA

### Installing
```
nuget install VL.Mapper
```
[Managing nugets](https://thegraybook.vvvv.org/reference/hde/managing-nugets.html)

### Changelog
- 0.2.1 - Minor bugfix
- 0.2.0 - Keep grid shape when changing subdivisions
- 0.1.2 - Fixed saving/loading not working on some systems
- 0.1.1 - Help patch
- 0.1.0 - Initial release 

### Notes
- Pretty thoroughly tested but mapper still could have bugs. If you disable the mapper node and only use the cache and player nodes it should be very stable.
- Tested with VVVV 5.2 but should work with 6.x too.

### ToDo
- Soft edge mask shader uses unnecessary amount of RAM
- Show grid on output
- Snapping
- More robust undo
- Insert grid lines
- Autosave only if changed
- Input image cropping
- Image mirroring
- Settings panel
- Tooltips

### Dependencies
- Uses modified versions of: [VL.EditingFramework](https://www.nuget.org/packages/VL.EditingFramework) and [VL.EditingFramework.Skia](https://www.nuget.org/packages/VL.EditingFramework.Skia)
- [VL.ImGui](https://www.nuget.org/packages/VL.ImGui)
- [VL.Stride](https://www.nuget.org/packages/VL.Stride)
- [VL.Skia](https://www.nuget.org/packages/VL.Skia)
