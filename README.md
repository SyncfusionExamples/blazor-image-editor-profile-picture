# Blazor Image Editor Profile Picture Sample

## Overview

This sample demonstrates how to build a profile-picture editing experience using the Syncfusion [Blazor Image Editor](https://www.syncfusion.com/blazor-components/blazor-image-editor). Users can load an image, adjust its orientation, select the required region, and crop the image to generate a profile-picture-style result.

The sample focuses on common avatar-editing operations by using the Image Editor APIs exposed by the component. Both Blazor Server and Blazor WebAssembly sample projects are included in the repository to demonstrate the same functionality across hosting models.

## Key Features

- Uses the Syncfusion Blazor Image Editor component inside an `SfDialog` to provide a dedicated profile-picture editing experience.
- Provides a custom profile avatar preview using an HTML `canvas` element and image container.
- Integrates JavaScript interop through `IJSRuntime` and a custom `canvasInterop` helper for image loading, canvas rendering, file selection, and profile-image updates.
- Opens the image editor dialog when users click the custom edit icon displayed on the profile avatar.
- Loads the current profile image into the Image Editor by using the `Created` event and the `OpenAsync()` method.
- Automatically creates a circular profile-picture selection using the `FileOpened` event and `SelectAsync("circle")`.
- Supports image upload through a hidden file input element triggered from the custom **Open** dialog button.
- Supports loading user-selected images through the `[JSInvokable] FileSelected()` callback method.
- Allows users to rotate images using the **Rotate** button and the `RotateAsync(90)` method.
- Allows users to reset all edits using the **Reset** button and the `ResetAsync()` method.
- Reapplies the circular crop selection automatically after image reset.
- Supports circular profile-picture generation using the `CropAsync()` method.
- Applies the cropped image to the profile avatar preview through JavaScript interop when users click the **Apply** button.
- Uses dialog lifecycle events (`Opened` and `Closed`) to control Image Editor initialization and component rendering.
- Implements conditional rendering of the Image Editor to optimize component creation only when the dialog is opened.
- Uses a custom toolbar configuration by supplying an empty `List<ImageEditorToolbarItemModel>` collection.
- Includes custom styling for avatar presentation, edit action overlay, circular canvas rendering, responsive dialog buttons, and theme-specific visual adjustments.

## Prerequisites

- [Visual Studio 2022](https://visualstudio.microsoft.com/vs/) or [Visual Studio Code](https://code.visualstudio.com/)
- [.NET SDK](https://dotnet.microsoft.com/en-us/download/dotnet) compatible with the project's target framework

## How to Run the Project

**Visual Studio 2022**

1. Clone the repository.
2. Open the appropriate solution file.
3. Restore NuGet packages.
4. If multiple projects are available, select the required startup project:
   - `Image-Editor_Server`
   - `Image-Editor_Wasm`
5. Build the project.
6. Run the application using `Ctrl+F5`.

**Visual Studio Code**

1. Clone the repository.
2. Open the repository folder in Visual Studio Code.
3. Navigate to the required project directory.

```bash
cd Image-Editor_Server
dotnet restore
dotnet run
```

or

```bash
cd Image-Editor_Wasm
dotnet restore
dotnet run
```

4. Open the local URL displayed in the terminal after the application starts.

## Project Structure

`Image-Editor_Server/Pages/Index.razor` - Main sample page that hosts the profile-picture editor, Syncfusion `SfImageEditor`, `SfDialog`, image editing logic, JavaScript interop integration, custom avatar UI, event handling, and styling.

## Support and Feedback

- For general product questions, visit the [Syncfusion Community Forum](https://www.syncfusion.com/forums) or [Syncfusion Support](https://www.syncfusion.com/support).
- To report an issue specific to this sample, open a GitHub issue in this repository.
- Documentation: https://blazor.syncfusion.com/documentation/image-editor/getting-started

## License

This is a Syncfusion sample project provided to demonstrate product usage. Review the [Syncfusion license terms](https://www.syncfusion.com/sales/pricing?category=ui-components) before using Syncfusion components in your own applications.