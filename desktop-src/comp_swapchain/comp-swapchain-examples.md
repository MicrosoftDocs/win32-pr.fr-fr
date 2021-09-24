---
title: Exemples de code de composition utilise permutation
description: Collection d’exemples de code montrant différents scénarios de utilise permutation de composition.
ms.topic: article
ms.date: 09/10/2021
ms.openlocfilehash: d538be46c6d41ed884ae9d4a735962317087e9c6
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128523828"
---
# <a name="composition-swapchain-code-examples"></a>Exemples de code de composition utilise permutation

> [!NOTE]
> **Certaines informations portent sur la préversion du produit, qui est susceptible d’être en grande partie modifié avant sa commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.**

Ces exemples de code utilisent les [bibliothèques d’implémentation Windows (Wil)](https://github.com/Microsoft/wil). Un moyen pratique d’installer Wil consiste à accéder à Visual Studio, puis à cliquer sur **projet** \> **gérer les packages NuGet...** \> **Parcourir**, taper ou coller **Microsoft. Windows. ImplementationLibrary** dans la zone de recherche, sélectionner l’élément dans les résultats de la recherche, puis cliquer sur **installer** pour installer le package pour ce projet.

## <a name="example-1mdashcreating-a-presentation-manager-on-systems-that-support-the-composition-swapchain-api"></a>Exemple 1 &mdash; création d’un gestionnaire de présentation sur des systèmes qui prennent en charge l’API utilise permutation de composition

Comme nous l’avons vu, l’API utilise permutation de la composition requiert que les pilotes pris en charge fonctionnent. L’exemple suivant montre comment votre application peut créer un gestionnaire de présentation si le système prend en charge l’API. Cela est illustré comme une `TryCreate` fonction de style qui retourne le gestionnaire de présentation uniquement si l’API est prise en charge. Cette fonction montre également comment créer correctement un appareil Direct3D pour sauvegarder un gestionnaire de présentation.

### <a name="c-example"></a>Exemple C++

```cpp
bool TryCreatePresentationManager(
    _In_ bool requestDirectPresentation,
    _Out_ ID3D11Device** ppD3DDevice,
    _Outptr_opt_result_maybenull_ IPresentationManager **ppPresentationManager)
{
    // Null the presentation manager and Direct3D device initially
    *ppD3DDevice = nullptr;
    *ppPresentationManager = nullptr;

    // Direct3D device creation flags. The composition swapchain API requires that applications disable internal
    // driver threading optimizations, as these optimizations are incompatible with the
    // composition swapchain API. If this flag is not present, then the API will fail the call to create the
    // presentation factory.
    UINT deviceCreationFlags =
        D3D11_CREATE_DEVICE_BGRA_SUPPORT |
        D3D11_CREATE_DEVICE_SINGLETHREADED |
        D3D11_CREATE_DEVICE_PREVENT_INTERNAL_THREADING_OPTIMIZATIONS;

    // Create the Direct3D device.
    com_ptr_failfast<ID3D11DeviceContext> d3dDeviceContext;
    FAIL_FAST_IF_FAILED(D3D11CreateDevice(
        nullptr,                   // No adapter
        D3D_DRIVER_TYPE_HARDWARE,  // Hardware device
        nullptr,                   // No module
        deviceCreationFlags,       // Device creation flags
        nullptr, 0,                // Highest available feature level
        D3D11_SDK_VERSION,         // API version
        ppD3DDevice,               // Resulting interface pointer
        nullptr,                   // Actual feature level
        &d3dDeviceContext));       // Device context

    // Call the composition swapchain API export to create the presentation factory.
    com_ptr_failfast<IPresentationFactory> presentationFactory;
    FAIL_FAST_IF_FAILED(CreatePresentationFactory(
        (*ppD3DDevice),
        IID_PPV_ARGS(&presentationFactory)));

    // Determine whether the system is capable of supporting the composition swapchain API based
    // on the capability that's reported by the presentation factory. If your application
    // wants direct presentation (that is, presentation without the need for DWM to
    // compose, using MPO or iflip), then we query for direct presentation support.
    bool isSupportedOnSystem;
    if (requestDirectPresentation)
    {
        isSupportedOnSystem = presentationFactory->IsPresentationSupportedWithIndependentFlip();
    }
    else
    {
        isSupportedOnSystem = presentationFactory->IsPresentationSupported();
    }

    // Create the presentation manager if it is supported on the current system.
    if (isSupportedOnSystem)
    {
        FAIL_FAST_IF_FAILED(presentationFactory->CreatePresentationManager(ppPresentationManager));
    }

    return isSupportedOnSystem;
}
```

## <a name="example-2mdashcreating-a-presentation-manager-and-presentation-surface"></a>Exemple 2 &mdash; création d’un gestionnaire de présentation et d’une surface de présentation

L’exemple suivant montre comment votre application crée un gestionnaire de présentation et une surface de présentation pour effectuer une liaison à un visuel dans une arborescence d’éléments visuels. Les exemples suivants montrent comment lier la surface de présentation dans les arborescences d’éléments visuels [**DirectComposition**](/windows/win32/directcomp/directcomposition-portal) et [**Windows. UI. composition**](/uwp/api/windows.ui.composition) .

### <a name="c-example-dcompositiongettargetstatistics"></a>Exemple C++ (DCompositionGetTargetStatistics)

```cpp
bool MakePresentationManagerAndPresentationSurface(
    _Out_ ID3D11Device** ppD3dDevice,
    _Out_ IPresentationManager** ppPresentationManager,
    _Out_ IPresentationSurface** ppPresentationSurface,
    _Out_ unique_handle& compositionSurfaceHandle)
{
    // Null the output pointers initially.
    *ppD3dDevice = nullptr;
    *ppPresentationManager = nullptr;
    *ppPresentationSurface = nullptr;
    compositionSurfaceHandle.reset();

    com_ptr_failfast<IPresentationManager> presentationManager;
    com_ptr_failfast<IPresentationSurface> presentationSurface;
    com_ptr_failfast<ID3D11Device> d3d11Device;

    // Call the function we defined previously to create a Direct3D device and presentation manager, if
    // the system supports it.
    if (TryCreatePresentationManager(
        true, // Request presentation with independent flip.
        &d3d11Device,
        &presentationManager) == false)
    {
        // Return 'false' out of the call if the composition swapchain API is unsupported. Assume the caller
        // will handle this somehow, such as by falling back to DXGI.
        return false;
    }

    // Use DirectComposition to create a composition surface handle.
    FAIL_FAST_IF_FAILED(DCompositionCreateSurfaceHandle(
        COMPOSITIONOBJECT_ALL_ACCESS,
        nullptr,
        compositionSurfaceHandle.addressof()));

    // Create presentation surface bound to the composition surface handle.
    FAIL_FAST_IF_FAILED(presentationManager->CreatePresentationSurface(
        compositionSurfaceHandle.get(),
        presentationSurface.addressof()));

    // Return the Direct3D device, presentation manager, and presentation surface to the caller for future
    // use.
    *ppD3dDevice = d3d11Device.detach();
    *ppPresentationManager = presentationManager.detach();
    *ppPresentationSurface = presentationSurface.detach();

    // Return 'true' out of the call if the composition swapchain API is supported and we were able to
    // create a presentation manager.
    return true;
}
```

## <a name="example-3mdashbinding-a-presentation-surface-to-a-windowsuicomposition-surface-brush"></a>Exemple 3 &mdash; liaison d’une surface de présentation à un pinceau de surface Windows. UI. composition

L’exemple suivant illustre la manière dont votre application lie un handle de surface de composition lié à une surface de présentation, tel qu’il a été créé dans l’exemple ci-dessus, à un pinceau surface [**Windows. UI. composition**](/uwp/api/windows.ui.composition) (*WinComp*), qui peut ensuite être lié à un visuel Sprite dans l’arborescence d’éléments visuels de votre application.

### <a name="c-example"></a>Exemple C++

```cpp
void BindPresentationSurfaceHandleToWinCompTree(
    _In_ ICompositor * pCompositor,
    _In_ ISpriteVisual * pVisualToBindTo, // The sprite visual we want to bind to.
    _In_ unique_handle& compositionSurfaceHandle)
{
    // QI an interop compositor from the passed compositor.
    com_ptr_failfast<ICompositorInterop> compositorInterop;
    FAIL_FAST_IF_FAILED(pCompositor->QueryInterface(IID_PPV_ARGS(&compositorInterop)));

    // Create a composition surface for the presentation surface's composition surface handle.
    com_ptr_failfast<ICompositionSurface> compositionSurface;
    FAIL_FAST_IF_FAILED(compositorInterop->CreateCompositionSurfaceForHandle(
        compositionSurfaceHandle.get(),
        &compositionSurface));

    // Create a composition surface brush, and bind the surface to it.
    com_ptr_failfast<ICompositionSurfaceBrush> surfaceBrush;
    FAIL_FAST_IF_FAILED(pCompositor->CreateSurfaceBrush(&surfaceBrush));
    FAIL_FAST_IF_FAILED(surfaceBrush->put_Surface(compositionSurface.get()));

    // Bind the brush to the visual.
    auto brush = surfaceBrush.query<ICompositionBrush>();
    FAIL_FAST_IF_FAILED(pVisualToBindTo->put_Brush(brush.get()));
}
```

## <a name="example-4mdashbinding-a-presentation-surface-to-a-directcomposition-visual"></a>Exemple 4 &mdash; liaison d’une surface de présentation à un visuel DirectComposition

L’exemple suivant illustre la manière dont votre application lie une surface de présentation à un visuel DirectComposition (*DComp*) dans une arborescence d’éléments visuels.

### <a name="c-example"></a>Exemple C++

```cpp
void BindPresentationSurfaceHandleToDCompTree(
    _In_ IDCompositionDevice* pDCompDevice,
    _In_ IDCompositionVisual* pVisualToBindTo,
    _In_ unique_handle& compositionSurfaceHandle) // The composition surface handle that was
                                                  // passed to CreatePresentationSurface.
{
    // Create a DComp surface to wrap the presentation surface.
    com_ptr_failfast<IUnknown> dcompSurface;
    FAIL_FAST_IF_FAILED(pDCompDevice->CreateSurfaceFromHandle(
        compositionSurfaceHandle.get(),
        &dcompSurface));

    // Bind the presentation surface to the visual.
    FAIL_FAST_IF_FAILED(pVisualToBindTo->SetContent(dcompSurface.get()));
}
```

## <a name="example-5mdashsetting-alpha-mode-and-color-space-on-a-presentation-surface"></a>Exemple 5 &mdash; définition du mode Alpha et de l’espace colorimétrique sur une surface de présentation

L’exemple suivant montre comment votre application définit le mode Alpha et l’espace colorimétrique sur une surface de présentation. Le mode Alpha décrit si, et comment, le canal alpha de la texture doit être interprété. L’espace colorimétrique décrit l’espace colorimétrique auquel les pixels de la texture font référence.

Toutes les mises à jour de propriété comme celles-ci prennent effet dans le cadre de la prochaine présentation de l’application, et prennent effet atomiquement avec les mises à jour de mémoire tampon qui font partie de ce présent. Un présent peut également, si votre application souhaite, ne pas mettre à jour les mémoires tampons, et à la place, comporter uniquement des mises à jour de propriété. Toutes les surfaces de présentation dont les mémoires tampons ne sont pas mises à jour sur un présent donné restent liées à la mémoire tampon à laquelle elles étaient liées avant cette présente.

### <a name="c-example"></a>Exemple C++

```cpp
void SetAlphaModeAndColorSpace(
    _In_ IPresentationSurface* pPresentationSurface)
{
    // Set alpha mode.
    FAIL_FAST_IF_FAILED(pPresentationSurface->SetAlphaMode(DXGI_ALPHA_MODE_IGNORE));

    // Set color space to full RGB.
    FAIL_FAST_IF_FAILED(pPresentationSurface->SetColorSpace(DXGI_COLOR_SPACE_RGB_FULL_G22_NONE_P709));
}
```

## <a name="example-6mdashsetting-letterboxing-margins-on-a-presentation-surface"></a>Exemple 6 &mdash; définition de marges cadre sur une surface de présentation

L’exemple suivant illustre la manière dont votre application spécifie les marges de cadre sur une surface de présentation. Cadre est utilisé pour remplir une zone spécifiée en dehors du contenu de la surface, afin de tenir compte des proportions différentes entre le contenu et le périphérique d’affichage sur lequel il est affiché. C’est le cas, par exemple, des *barres* noires qui sont souvent visibles au-dessus et au-dessous du contenu lorsque vous regardez sur un PC un film formaté pour les théâtres panoramiques. L’API utilise permutation de composition vous permet de spécifier les marges dans lesquelles le cadre doit être rendu dans de tels cas.

Actuellement, les zones cadre sont toujours remplies avec le noir opaque.

En tant que contenu de l’arborescence d’éléments visuels, la surface de présentation existe dans l’espace de coordonnées de son visuel hôte. Avec cadre présent, l’origine de l’espace de coordonnées du visuel correspond à l’angle supérieur gauche du cadre. Autrement dit, la mémoire tampon elle-même existe dans l’espace de coordonnées du visuel. Les limites sont calculées en fonction de la taille de la mémoire tampon plus la taille du cadre.

L’exemple suivant montre où se trouvent les tampons et les cadre dans l’espace de coordonnées visuelles et comment les limites sont calculées.

![Marges cadre](images/letterboxing-margins.png)

Enfin, si la transformation appliquée à une surface de présentation est accompagnée d’un décalage, la zone non couverte par le tampon ou le cadre est considérée comme étant en dehors des limites du contenu, et est traitée comme transparente de la &mdash; même façon que tout autre contenu de l’arborescence d’éléments visuels est traité en dehors des limites du contenu.

### <a name="letterboxing-and-transform-interaction"></a>Cadre et transformation interaction

Pour fournir des tailles de marge cadre cohérentes, quelle que soit l’échelle que votre application applique à une mémoire tampon afin de remplir une partie du contenu, DWM tente d’afficher les marges à une taille cohérente, quelle que soit l’échelle, mais prend en compte le résultat de la transformation appliquée à la surface de présentation.

En d’autres termes, les marges cadre sont techniquement appliquées avant l’application de la transformation de la surface de présentation, mais compensent toute échelle susceptible de faire partie de cette transformation. Autrement dit, la transformation de l’aire de présentation est décomposée en deux composants &mdash; , la partie de la transformation qui met à l’échelle et le reste de la transformation.

![Cadre et transformer interaction 1](images/letterboxing-and-transform-interaction-1.png)

Par exemple, avec les marges 100 PX cadre et aucune transformation appliquée à la surface de présentation, la mémoire tampon résultante est rendue sans mise à l’échelle, et les marges de cadre sont 100 PX larges.

![Cadre et transformer interaction 2](images/letterboxing-and-transform-interaction-2.png)

Un autre exemple, avec les marges 100 PX cadre, et une transformation d’échelle 2x appliquée sur la surface de présentation, la mémoire tampon résultante est rendue avec une échelle de 2 x et les marges cadre affichées à l’écran sont toujours 100 PX dans toutes les tailles.

![Cadre et transformer interaction 3](images/letterboxing-and-transform-interaction-3.png)

Autre exemple, avec une transformation de rotation de 45 degrés, les marges de cadre qui en résultent s’affichent 100 PX, et les marges cadre pivotent avec la mémoire tampon.

![Cadre et transformer interaction 4](images/letterboxing-and-transform-interaction-4.png)

Autre exemple, avec une transformation Scale 2x et rotation 45 degré, l’image est pivotée et mise à l’échelle, et les marges cadre sont également 100 px en largeur et pivotées avec la mémoire tampon.

![Cadre et transformer interaction 5](images/letterboxing-and-transform-interaction-5.png)

Si une transformation d’échelle ne peut pas être extraite sans ambiguïté de la transformation que votre application applique à la surface de présentation, par exemple si l’échelle X ou Y obtenue est 0, les marges cadre sont rendues avec l’intégralité de la transformation appliquée, et nous n’allons pas tenter de compenser l’échelle.

![Cadre et transformer interaction 6](images/letterboxing-and-transform-interaction-6.png)

### <a name="c-example"></a>Exemple C++

```cpp
 void SetContentLayoutAndFill(
    _In_ IPresentationSurface* pPresentationSurface)
{
    // Set layout properties. Each layout property is described below.

    // The source RECT describes the area from the bound buffer that will be sampled from. The
    // RECT is in source texture coordinates. Below we indicate that we'll sample from a
    // 100x100 area on the source texture.
    RECT sourceRect;
    sourceRect.left = 0;
    sourceRect.top = 0;
    sourceRect.right = 100;
    sourceRect.bottom = 100;
    FAIL_FAST_IF_FAILED(pPresentationSurface->SetSourceRect(&sourceRect));

    // The presentation transform defines how the source rect will be transformed when
    // rendering the buffer. In this case, we indicate we want to scale it 2x in both
    // width and height, and we also want to offset it 50 pixels to the right.
    PresentationTransform transform = { 0 };
    transform.M11 = 2.0f; // X scale 2x
    transform.M22 = 2.0f; // Y scale 2x
    transform.M31 = 50.0f; // X offset 50px
    FAIL_FAST_IF_FAILED(pPresentationSurface->SetTransform(&transform));

    // The letterboxing parameters describe how to letterbox the content. Letterboxing
    // is commonly used to fill area not covered by video/surface content when scaling to
    // an aspect ration that doesn't match the aspect ratio of the surface itself. For
    // example, when viewing content formatted for the theater on a 1080p home screen, one
    // can typically see black "bars" on the top and bottom of the video, covering the space
    // on screen that wasn't covered by the video due to the differing aspect ratios of the
    // content and the display device. The composition swapchain API allows the user to specify
    // letterboxing margins, which describe the number of pixels to surround the surface
    // content with on screen. In this case, surround the top and bottom of our content with
    // 100 pixel tall letterboxing.
    FAIL_FAST_IF_FAILED(pPresentationSurface->SetLetterboxingMargins(
        0.0f,
        100.0f,
        0.0f,
        100.0f));
}
```

## <a name="example-7mdashsetting-content-restrictions-on-a-presentation-surface"></a>Exemple 7 &mdash; définition de restrictions de contenu sur une surface de présentation

L’exemple suivant illustre la manière dont votre application empêche d’autres applications de lire le contenu de la surface de présentation (à partir de technologies telles que PrintScreen, DDA, API de capture et d’autres) à des fins de contenu protégé. Il montre également comment limiter l’affichage d’une surface de présentation à une seule sortie DXGI.

Si le contenu readback est désactivé, lorsque votre application tente de lire en retour, l’image capturée contient un noir opaque à la place de la surface de présentation. Si une surface de présentation est affichée-limitée à un [**IDXGIOutput**](/windows/win32/api/dxgi/nn-dxgi-idxgioutput), elle apparaîtra en noir opaque sur toutes les autres sorties.

### <a name="c-example"></a>Exemple C++

```cpp
void SetContentRestrictions(
    _In_ IPresentationSurface* pPresentationSurface,
    _In_ IDXGIOutput* pOutputToRestrictTo)
{
    // Disable readback of the surface via printscreen, bitblt, etc.
    FAIL_FAST_IF_FAILED(pPresentationSurface->SetDisableReadback(true));

    // Restrict display of surface to only the passed output.
    FAIL_FAST_IF_FAILED(pPresentationSurface->RestrictToOutput(pOutputToRestrictTo));
}
```

## <a name="example-8mdashadding-presentation-buffers-to-a-presentation-manager"></a>Exemple 8 &mdash; Ajout de mémoires tampons de présentation à un gestionnaire de présentation

L’exemple suivant montre comment votre application allouerait un ensemble de textures Direct3D et les ajoutera au gestionnaire de présentation pour l’utiliser comme mémoires tampons de présentation, qui peuvent être présentées aux surfaces de présentation.

Comme nous l’avons vu précédemment, il n’existe aucune restriction concernant le nombre de gestionnaires de présentation avec lesquels une texture peut être inscrite. Toutefois, dans la plupart des cas d’usage habituels, une texture est inscrite uniquement dans un gestionnaire de présentation unique.

Notez également que dans la mesure où l’API accepte les descripteurs de mémoire tampon partagés en tant que devise lors de l’enregistrement de textures comme mémoires tampons de présentation dans le gestionnaire de présentation, et puisque DXGI peut créer plusieurs mémoires tampons partagées pour un même texture2D, il est techniquement possible pour votre application de créer plusieurs descripteurs de tampon partagés pour une seule texture et de les  Cela a pour effet d’ajouter plusieurs fois la même mémoire tampon. Cela n’est pas recommandé, car les mécanismes de synchronisation fournis par le gestionnaire de présentation seront rompus, car deux mémoires tampons de présentation suivies de façon unique correspondent à la même texture. Étant donné qu’il s’agit d’une API avancée, et qu’il est en fait très difficile pour la détection de ce cas de figure, l’API ne tente pas de valider ce scénario.

### <a name="c-example"></a>Exemple C++

```cpp
void AddBuffersToPresentationManager(
    _In_ ID3D11Device* pD3D11Device, // The backing Direct3D device
    _In_ IPresentationManager* pPresentationManager, // Previously-made presentation manager
    _In_ UINT bufferWidth, // The width of the buffers to add
    _In_ UINT bufferHeight, // The height of the buffers to add
    _In_ UINT numberOfBuffersToAdd, // The number of buffers to add to the presentation manager
    _Out_ vector<com_ptr_failfast<ID3D11Texture2D>>& textures, // Array of textures returned
    _Out_ vector<com_ptr_failfast<IPresentationBuffer>>& presentationBuffers) // Array of presentation buffers returned
{
    // Clear the returned vectors initially.
    textures.clear();
    presentationBuffers.clear();

    // Add the desired buffers to the presentation manager.
    for (UINT i = 0; i < numberOfBuffersToAdd; i++)
    {
        com_ptr_failfast<ID3D11Texture2D> texture;
        com_ptr_failfast<IPresentationBuffer> presentationBuffer;

        // Call our helper to make a new buffer of the desired type.
        AddNewPresentationBuffer(
            pD3D11Device,
            pPresentationManager,
            bufferWidth,
            bufferHeight,
            &texture,
            &presentationBuffer);

        // Track our buffers in our own set of vectors.
        textures.push_back(texture);
        presentationBuffers.push_back(presentationBuffer);
    }
}

void AddNewPresentationBuffer(
    _In_ ID3D11Device* pD3D11Device,
    _In_ IPresentationManager* pPresentationManager,
    _In_ UINT bufferWidth,
    _In_ UINT bufferHeight,
    _Out_ ID3D11Texture2D** ppTexture2D,
    _Out_ IPresentationBuffer** ppPresentationBuffer)
{
    com_ptr_failfast<ID3D11Texture2D> texture2D;
    unique_handle sharedResourceHandle;

    // Create a shared Direct3D texture and handle with the passed attributes.
    MakeD3D11Texture(
        pD3D11Device,
        bufferWidth,
        bufferHeight,
        &texture2D,
        out_param(sharedResourceHandle));

    // Add the texture2D to the presentation manager, and get back a presentation buffer.
    com_ptr_failfast<IPresentationBuffer> presentationBuffer;
    FAIL_FAST_IF_FAILED(pPresentationManager->AddBufferFromSharedHandle(
        sharedResourceHandle.get(),
        &presentationBuffer));

    // Return back the texture and buffer presentation buffer.
    *ppTexture2D = texture2D.detach();
    *ppPresentationBuffer = presentationBuffer.detach();
}

void MakeD3D11Texture(
    _In_ ID3D11Device* pD3D11Device,
    _In_ UINT textureWidth,
    _In_ UINT textureHeight,
    _Out_ ID3D11Texture2D** ppTexture2D,
    _Out_ HANDLE* sharedResourceHandle)
{
    D3D11_TEXTURE2D_DESC textureDesc = {};

    // Width and height can be anything within max texture size of the adapter backing the Direct3D
    // device.
    textureDesc.Width = textureWidth;
    textureDesc.Height = textureHeight;

    // MipLevels and ArraySize must be 1.
    textureDesc.MipLevels = 1;
    textureDesc.ArraySize = 1;

    // Format can be one of the following:
    //   DXGI_FORMAT_B8G8R8A8_UNORM
    //   DXGI_FORMAT_R8G8B8A8_UNORM
    //   DXGI_FORMAT_R16G16B16A16_FLOAT
    //   DXGI_FORMAT_R10G10B10A2_UNORM
    //   DXGI_FORMAT_NV12
    //   DXGI_FORMAT_YUY2
    //   DXGI_FORMAT_420_OPAQUE
    // For this 
    textureDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;

    // SampleDesc count and quality must be 1 and 0 respectively.
    textureDesc.SampleDesc.Count = 1;
    textureDesc.SampleDesc.Quality = 0;

    // Usage must be D3D11_USAGE_DEFAULT.
    textureDesc.Usage = D3D11_USAGE_DEFAULT;

    // BindFlags must include D3D11_BIND_SHADER_RESOURCE for RGB textures, and D3D11_BIND_DECODER
    // for YUV textures. For RGB textures, it is likely your application will want to specify
    // D3D11_BIND_RENDER_TARGET in order to render to it.
    textureDesc.BindFlags =
        D3D11_BIND_SHADER_RESOURCE |
        D3D11_BIND_RENDER_TARGET;

    // MiscFlags should include D3D11_RESOURCE_MISC_SHARED and D3D11_RESOURCE_MISC_SHARED_NTHANDLE,
    // and might also include D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE if your application wishes to
    // qualify for MPO and iflip. If D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE is not provided, then the
    // content will not qualify for MPO or iflip, but can still be composed by DWM
    textureDesc.MiscFlags =
        D3D11_RESOURCE_MISC_SHARED |
        D3D11_RESOURCE_MISC_SHARED_NTHANDLE |
        D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE;

    // CPUAccessFlags must be 0.
    textureDesc.CPUAccessFlags = 0;

    // Use Direct3D to create a texture 2D matching the desired attributes.
    com_ptr_failfast<ID3D11Texture2D> texture2D;
    FAIL_FAST_IF_FAILED(pD3D11Device->CreateTexture2D(&textureDesc, nullptr, &texture2D));

    // Create a shared handle for the texture2D.
    unique_handle sharedBufferHandle;
    auto dxgiResource = texture2D.query<IDXGIResource1>();
    FAIL_FAST_IF_FAILED(dxgiResource->CreateSharedHandle(
        nullptr,
        GENERIC_ALL,
        nullptr,
        &sharedBufferHandle));

    // Return the handle to the caller.
    *ppTexture2D = texture2D.detach();
    *sharedResourceHandle = sharedBufferHandle.release();
}
```

## <a name="example-9mdashremoving-presentation-buffers-from-a-presentation-manager-and-object-lifetime"></a>Exemple 9 &mdash; Suppression de mémoires tampons de présentation d’un gestionnaire de présentation et durée de vie des objets

La suppression d’une mémoire tampon de présentation du gestionnaire de présentation est aussi simple que la libération de l’objet IPresentationBuffer à 0 refcount. Toutefois, dans ce cas, cela ne signifie pas nécessairement que la mémoire tampon de présentation peut être libérée. Il peut arriver qu’une mémoire tampon soit encore en cours d’utilisation, par exemple si la mémoire tampon de présentation est visible à l’écran, ou si elle contient des cadeaux en suspens qui la référencent.

En bref, le gestionnaire de présentation effectue le suivi de la façon dont chaque mémoire tampon est utilisée directement par votre application, et indirectement. Il effectue le suivi des mémoires tampons affichées, des éléments de mémoire tampon en suspens et de référence, et il effectue le suivi interne de tout cet État pour s’assurer qu’une mémoire tampon n’est pas réellement libérée/désinscrite tant qu’elle n’est pas réellement utilisée.

Une bonne façon de réfléchir à la durée de vie de la mémoire tampon est que si votre application libère un IPresentationBuffer, elle indique à l’API qu’elle n’utilisera plus ce tampon dans les appels ultérieurs. L’API utilise permutation de composition effectue le suivi de ce, ainsi que toute autre façon dont la mémoire tampon est utilisée, et elle libère entièrement la mémoire tampon uniquement lorsqu’elle est entièrement sécurisée.

En bref &mdash; , votre application doit libérer un [**IPresentationBuffer**](/windows/win32/api/presentation/nn-presentation-ipresentationbuffer) une fois qu’elle est terminée, et savoir que l’API utilise permutation de composition va libérer entièrement la mémoire tampon lorsque toutes les autres utilisations sont également effectuées.

Voici une illustration des concepts ci-dessus.

![Suppression de mémoires tampons de présentation](images/removing-presentation-buffers.png)

Dans cet exemple, nous avons un gestionnaire de présentation avec deux mémoires tampons de présentation. La mémoire tampon 1 a trois références qui la gardent actives.

* Votre application contient un **IPresentationBuffer** qui la référence.
* Interne à l’API, elle est stockée en tant que mémoire tampon de la limite actuelle de la surface de présentation, car il s’agissait de la dernière mémoire tampon liée à votre application, qu’elle a ensuite présentée.
* Il y a également un présent en suspens dans la file d’attente actuelle qui a tendance à afficher la mémoire tampon 1 sur la surface de présentation.

La mémoire tampon 1 contient en outre une référence sur l’allocation de texture Direct3D correspondante. Votre application a également un [**ID3D11Texture2D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) qui référence cette allocation.

La mémoire tampon 2 n’a plus de références en suspens du côté de l’application, ni l’allocation de texture qu’elle référence, mais la mémoire tampon 2 est maintenue active, car il s’agit de ce qui est actuellement affiché par la surface de présentation à l’écran. Lorsque le présent 1 est traité, et que la mémoire tampon 1 s’affiche à l’écran à la place, la mémoire tampon 2 n’aura plus de références et sera libérée, à son tour, pour libérer sa référence sur son allocation Direct3D texture2D.

### <a name="c-example"></a>Exemple C++

```cpp
void ReleasePresentationManagerBuffersExample(
    _In_ ID3D11Device* pD3D11Device,
    _In_ IPresentationManager* pPresentationManager)
{
    com_ptr_failfast<ID3D11Texture2D> texture2D;
    com_ptr_failfast<IPresentationBuffer> newBuffer;

    // Create a new texture/presentation buffer.
    AddNewPresentationBuffer(
        pD3D11Device,
        pPresentationManager,
        200, // Buffer width
        200, // Buffer height
        &texture2D,
        &newBuffer);

    // Release the IPresentationBuffer. This indicates that we have no more intention to use it
    // from the application side. However, if we have any presents outstanding that reference
    // the buffer, it will be kept alive internally and released when all outstanding presents
    // have been retired.
    newBuffer.reset();

    // When the presentation buffer is truly released internally, it will in turn release its
    // reference on the texture2D which it corresponds to. Your application must also release
    // its own references to the texture2D for it to be released.
    texture2D.reset();
}
```

## <a name="example-10mdashresizing-buffers-in-a-presentation-manager"></a>Exemple 10 &mdash; des tampons de redimensionnement dans un gestionnaire de présentation

L’exemple suivant illustre la manière dont votre application effectue un *redimensionnement* des mémoires tampons de présentation. Par exemple, si un service de vidéo en streaming diffuse en continu, mais décide de basculer les formats vers 1080p en raison de la disponibilité d’une bande passante réseau élevée, il est préférable de réallouer ses mémoires tampons de 480p à 1080 pour pouvoir commencer à présenter un contenu de 1080p.

Dans DXGI, il s’agit d’une opération de *redimensionnement* . DXGI réalloue toutes les mémoires tampons de manière atomique, ce qui est coûteux et peut produire un problème à l’écran. L’exemple ci-dessous décrit comment effectuer un redimensionnement atomique en utilisant avec DXGI dans l’API utilise permutation de composition. Un exemple plus tard montre comment effectuer un redimensionnement en *quinconce* , en écartant la réallocation entre plusieurs cadeaux, ce qui améliore les performances par rapport à un redimensionnement utilise permutation atomique.

### <a name="c-example"></a>Exemple C++

```cpp
void ResizePresentationManagerBuffersExample(
    _In_ ID3D11Device* pD3D11Device,
    _In_ IPresentationManager* pPresentationManager) // Previously-made presentation manager.
{
    // Vectors representing the IPresentationBuffer and ID3D11Texture2D collections.
    vector<com_ptr_failfast<ID3D11Texture2D>> textures;
    vector<com_ptr_failfast<IPresentationBuffer>> presentationBuffers;

    // Add 6 50x50 buffers to the presentation manager. See previous example for definition of
    // this function.
    AddBuffersToPresentationManager(
        pD3D11Device,
        pPresentationManager,
        50, // Buffer width
        50, // Buffer height
        6, // Number of buffers
        textures,
        presentationBuffers);

    // Release all the buffers we just added. The presentation buffers internally will be released
    // when any other references are also removed (outstanding presents, display references, etc.).
    textures.clear();
    presentationBuffers.clear();

    // Add 6 new 100x100 buffers to the presentation manager to replace the
    // old ones we just removed.
    AddBuffersToPresentationManager(
        pD3D11Device,
        pPresentationManager,
        100, // Buffer width
        100, // Buffer height
        6, // Number of buffers
        textures,
        presentationBuffers);
}
```

## <a name="example-11mdashsynchronizing-presentation-using-buffer-available-events-and-handling-presentation-manager-lost-events"></a>Exemple 11 &mdash; Présentation de la synchronisation à l’aide d’événements disponibles dans la mémoire tampon et gestion des événements perdus du gestionnaire de présentation

Si votre application doit émettre un présent qui implique une mémoire tampon de présentation qui a été utilisée dans une version antérieure, vous devez vous assurer que le précédent présent est terminé pour le rendu et la présentation de la mémoire tampon de présentation. L’API utilise permutation de composition fournit deux mécanismes différents pour faciliter cette synchronisation. Le plus simple est l' *événement available* d’une mémoire tampon de présentation, qui est un objet d’événement NT qui est signalé lorsqu’une mémoire tampon est disponible (autrement dit, tous les cadeaux précédents sont entrés dans le cadre d’un *retrait ou d'* une mise *hors* service) et non signalés dans le cas contraire. Cet exemple montre comment utiliser les événements disponibles dans la mémoire tampon pour sélectionner les mémoires tampon disponibles à présenter. Il montre également comment écouter les erreurs de *perte d’appareil* qui sont morally équivalentes à la perte d’appareil dxgi et nécessiter une recréation du gestionnaire de présentation.

### <a name="presentation-manager-lost-errors"></a>Erreurs perdues du gestionnaire de présentation

Un gestionnaire de présentation peut être perdu s’il rencontre une erreur en interne qu’il ne peut pas récupérer à partir de. Votre application doit détruire un gestionnaire de présentation perdu et en créer une autre pour l’utiliser à la place. Lorsqu’un gestionnaire de présentation est perdu, il cesse d’accepter d’autres présentations. Toute tentative d’appel de **présent** sur un gestionnaire de présentation perdu renverra **PRESENTATION_ERROR_LOST**. Toutes les autres méthodes, toutefois, fonctionneront normalement. Cela permet de s’assurer que votre application a uniquement besoin de vérifier les **PRESENTATION_ERROR_LOST** lors des appels présents et qu’elle n’a pas besoin d’anticiper/gérer les erreurs perdues à chaque appel d’API. Si votre application souhaite vérifier ou recevoir des erreurs perdues en dehors d’un appel présent, elle peut utiliser l’événement perdu retourné par [**IPresentationManager :: GetLostEvent**](/windows/win32/api/presentation/nf-presentation-ipresentationmanager-getlostevent).

### <a name="present-queue-and-timing"></a>Mise en file d’attente et synchronisation actuelles

Les cadeaux émis par le gestionnaire de présentation peuvent spécifier une heure spécifique à cibler. Cette heure cible est l’heure idéale à laquelle le système tentera d’afficher le présent. Étant donné que les écrans sont mis à jour à une cadence finie, il est peu probable qu’ils s’affichent précisément à l’heure spécifiée, mais ils s’affichent aussi près que possible de l’heure.

Cette heure cible est une heure relative au système, ou l’heure à laquelle le système s’est exécuté depuis qu’il est sous tension, en unités de centaines de nanosecondes. Un moyen simple de calculer l’heure actuelle consiste à interroger la valeur [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC) actuelle, à la diviser par la fréquence QPC du système et à la multiplier par 10 millions. Les limites d’arrondi et de précision ne sont pas utilisées pour calculer l’heure actuelle dans les unités applicables. Le système peut également recevoir l’heure actuelle en appelant [**MfGetSystemTime**](/windows/win32/api/mfidl/nf-mfidl-mfgetsystemtime)ou [**QueryInterruptTimePrecise**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise).

Une fois que l’heure actuelle est connue, votre application émet généralement des dépassements à la croissance de l’heure actuelle.

Quelle que soit l’heure cible, les cadeaux sont toujours traités dans l’ordre de la file d’attente. Même si un actuel cible une heure antérieure à la version précédente, il ne sera pas traité tant que le présent précédent n’aura pas été traité. Cela signifie essentiellement que tous les présents qui ne ciblent pas un délai plus tard que celui qui était nécessaire pour remplaceraient ce qui est déjà présent. Cela signifie également que si votre application veut émettre un présent le plus *tôt possible*, il peut simplement ne pas définir une heure cible (auquel cas l’heure cible doit rester l’heure de la dernière présence) ou définir une heure cible égale à 0. Les deux ont le même effet. Si votre application ne souhaite pas attendre la fin des versions précédentes pour qu’un nouveau présent soit présent, il doit annuler les cadeaux précédents. Un exemple ultérieur décrit comment procéder.

![Mise en file d’attente et synchronisation actuelles](images/present-queue-and-timing.png)

**T = 3S**: présent 1, 2, 3 Ready et 3, en tant que dernier présent, gagne en sortie. **T =** 4 : présent 4, 5, 6 Ready et 6, en tant que dernier présent, gagne en sortie.

Le diagramme ci-dessus illustre un exemple de cadeaux en suspens dans la file d’attente actuelle. La présente 1 cible une heure de 3S. Par conséquent, aucun produit n’aura lieu jusqu’à 3S. Toutefois, le présent 2 cible réellement une cible antérieure, 2S et présent 3 3S. Ainsi, à l’heure 3S, les 1, 2 et 3 se terminent, et le présent 3 est le présent pour réellement prendre effet. À la suite de cela, le prochain présent, 4, sera satisfait à 4, mais sera immédiatement remplacé par le présent 5, qui cible 0 et le présent 6, qui n’a aucune heure cible définie. 5 et 6 effectifs prennent effet le plus *tôt possible*.

### <a name="c-example"></a>Exemple C++

```cpp
bool SimpleEventSynchronizationExample(
    _In_ ID3D11Device* pD3D11Device,
    _In_ IPresentationManager* pPresentationManager,
    _In_ IPresentationSurface* pPresentationSurface,
    _In_ vector<com_ptr_failfast<ID3D11Texture2D>>& textures,
    _In_ vector<com_ptr_failfast<IPresentationBuffer>>& presentationBuffers)
{
    // Track a time we'll be presenting to below. Default to the current time, then increment by
    // 1/10th of a second every present.
    SystemInterruptTime presentTime;
    QueryInterruptTimePrecise(&presentTime.value);

    // Build an array of events that we can wait on to perform various actions in our work loop.
    vector<unique_event> waitEvents;

    // The lost event will be the first event in our list. This is an event that signifies that
    // something went wrong in the system (due to extreme conditions such as memory pressure, or
    // driver issues) that indicate that the presentation manager has been lost, and should no
    // longer be used, and instead should be recreated.
    unique_event lostEvent;
    pPresentationManager->GetLostEvent(&lostEvent);
    waitEvents.emplace_back(std::move(lostEvent));

    // Add each buffer's available event to the list of events we will be waiting on.
    for (UINT bufferIndex = 0; bufferIndex < presentationBuffers.size(); bufferIndex++)
    {
        unique_event availableEvent;
        presentationBuffers[bufferIndex]->GetAvailableEvent(&availableEvent);
        waitEvents.emplace_back(std::move(availableEvent));
    }

    // Iterate for 120 presents.
    constexpr UINT numberOfPresents = 120;
    for (UINT onPresent = 0; onPresent < numberOfPresents; onPresent++)
    {
        // Advance our present time 1/10th of a second in the future. Note the API accepts
        // time in 100ns units, or 1/1e7 of a second, meaning that 1 million units correspond to
        // 1/10th of a second.
        presentTime.value += 1'000'000;

        // Wait for the lost event or an available buffer. Since WaitForMultipleObjects prioritizes
        // lower-indexed events, it is recommended to put any higher importance events (like the
        // lost event) first, and then follow up with buffer available events.
        DWORD waitResult = WaitForMultipleObjects(
            static_cast<UINT>(waitEvents.size()),
            reinterpret_cast<HANDLE*>(waitEvents.data()),
            FALSE,
            INFINITE);

        // Failfast if the wait hit an error.
        FAIL_FAST_IF((waitResult - WAIT_OBJECT_0) >= waitEvents.size());

        // Our lost event was the first event in the array. If this is signaled, the caller
        // should recreate the presentation manager. This is very similar to how Direct3D devices
        // can be lost. Assume our caller knows to handle this return value appropriately.
        if (waitResult == WAIT_OBJECT_0)
        {
            return false;
        }

        // Otherwise, compute the buffer corresponding to the available event that was signaled.
        UINT bufferIndex = waitResult - (WAIT_OBJECT_0 + 1);

        // Draw red to that buffer
        DrawColorToSurface(
            pD3D11Device,
            textures[bufferIndex],
            1.0f, // red
            0.0f, // green
            0.0f); // blue

        // Bind the presentation buffer to the presentation surface. Changes in this binding will take
        // effect on the next present, and the binding persists across presents. That is, any number
        // of subsequent presents will imply this binding until it is changed. It is completely fine
        // to only update buffers for a subset of the presentation surfaces owned by a presentation
        // manager on a given present - the implication is that it simply didn't update.
        //
        // Similarly, note that if your application were to call SetBuffer on the same presentation
        // surface multiple times without calling present, this is fine. The policy is last writer
        // wins.
        //
        // Your application may present without first binding a presentation surface to a buffer.
        // The result will be that presentation surface will simply have no content on screen,
        // similar to how DComp and WinComp surfaces appear in a tree before they are rendered to.
        // In that case system content will show through where the buffer would have been.
        //
        // Your application may also set a 'null' buffer binding after previously having bound a
        // buffer and present - the end result is the same as if your application had presented
        // without ever having set the content.
        pPresentationSurface->SetBuffer(presentationBuffers[bufferIndex].get());

        // Present at the targeted time. Note that a present can target only a single time. If an
        // application wants to updates two buffers at two different times, then it must present
        // two times.
        //
        // Presents are always processed in queue order. A present will not take effect before any
        // previous present in the queue, even if it targets an earlier time. In such a case, when
        // the previous present is processed, the next present will also be processed immediately,
        // and override that previous present.
        //
        // For this reason, if your application wishes to present "now" or "early as possible", then
        // it can simply present, without setting a target time. The implied target time will be 0,
        // and the new present will override the previous present.
        //
        // If your application wants to present truly "now", and not wait for previous presents in the
        // queue to be processed, then it will need to cancel previous presents. A future example
        // demonstrates how to do this.
        //
        // Your application will receive PRESENTATION_ERROR_LOST if it attempts to Present a lost
        // presentation manager. This is the only call that will return such an error. A lost
        // presentation manager functions normally in every other case, so applications need only
        // to handle this error at the time they call Present.
        pPresentationManager->SetTargetTime(presentTime);
        HRESULT hrPresent = pPresentationManager->Present();
        if (hrPresent == PRESENTATION_ERROR_LOST)
        {
            // Our presentation manager has been lost. Return 'false' to the caller to indicate that
            // the presentation manager should be recreated.
            return false;
        }
        else
        {
            FAIL_FAST_IF_FAILED(hrPresent);
        }
    }

    return true;
}

void DrawColorToSurface(
    _In_ ID3D11Device* pD3D11Device,
    _In_ const com_ptr_failfast<ID3D11Texture2D>& texture2D,
    _In_ float redValue,
    _In_ float greenValue,
    _In_ float blueValue)
{
    com_ptr_failfast<ID3D11DeviceContext> D3DDeviceContext;
    com_ptr_failfast<ID3D11RenderTargetView> renderTargetView;

    // Get the immediate context from the D3D11 device.
    pD3D11Device->GetImmediateContext(&D3DDeviceContext);

    // Create a render target view of the passed texture.
    auto resource = texture2D.query<ID3D11Resource>();
    FAIL_FAST_IF_FAILED(pD3D11Device->CreateRenderTargetView(
        resource.get(),
        nullptr,
        renderTargetView.addressof()));

    // Clear the texture with the specified color.
    float clearColor[4] = { redValue, greenValue, blueValue, 1.0f }; // red, green, blue, alpha
    D3DDeviceContext->ClearRenderTargetView(renderTargetView.get(), clearColor);
}
```

## <a name="example-12mdashadvanced-synchronizationmdashthrottling-workflow-to-the-size-of-the-outstanding-present-queue-using-present-synchronization-fences-and-handling-presentation-manager-lost-events"></a>Exemple 12 &mdash; &mdash; flux de travail de limitation de synchronisation avancée vers la taille de la file d’attente présente en cours à l’aide des limites de synchronisation actuelles et gestion des événements perdus du gestionnaire de présentation

L’exemple suivant montre comment votre application peut soumettre un grand nombre de cadeaux à l’avenir, puis mettre en veille jusqu’à ce que le nombre de cadeaux restant en suspens passe à une quantité spécifique. les infrastructures telles que Windows Media Foundation limiter de cette façon pour réduire le nombre de réveils du processeur qui se produisent, tout en veillant à ce que la file d’attente actuelle ne soit pas épuisée (ce qui empêche la lecture douce et provoque un problème). Cela a pour effet de réduire l’utilisation de l’alimentation du processeur pendant le flux de travail de la présentation. Votre application met en file d’attente le nombre maximal de cadeaux (en fonction du nombre de tampons de présentation alloués), puis veille jusqu’à ce que la file d’attente actuelle soit épuisée pour remplir la file d’attente.

### <a name="c-example"></a>Exemple C++

```cpp
bool FenceSynchronizationExample(
    _In_ ID3D11Device* pD3D11Device,
    _In_ IPresentationManager* pPresentationManager,
    _In_ IPresentationSurface* pPresentationSurface,
    _In_ vector<com_ptr_failfast<ID3D11Texture2D>>& textures,
    _In_ vector<com_ptr_failfast<IPresentationBuffer>>& presentationBuffers)
{
    // Track a time we'll be presenting to below. Default to the current time, then increment by
    // 1/10th of a second every present.
    SystemInterruptTime presentTime;
    QueryInterruptTimePrecise(&presentTime.value);

    // Get present retiring fence.
    com_ptr_failfast<ID3D11Fence> presentRetiringFence;
    FAIL_FAST_IF_FAILED(pPresentationManager->GetPresentRetiringFence(
        IID_PPV_ARGS(&presentRetiringFence)));

    // Get the lost event to query before presentation.
    unique_event lostEvent;
    pPresentationManager->GetLostEvent(&lostEvent);

    // Create an event to synchronize to our queue depth with. We'll use Direct3D to signal this event
    // when our synchronization fence indicates reaching a specific present.
    unique_event presentQueueSyncEvent;
    presentQueueSyncEvent.create(EventOptions::ManualReset);

    // Cycle the present queue 10 times.
    constexpr UINT numberOfPresentRefillCycles = 10;
    for (UINT onRefillCycle = 0; onRefillCycle < numberOfPresentRefillCycles; onRefillCycle++)
    {
        // Fill up presents for all presentation buffers. We compare the presentation manager's
        // next present ID to the present confirmed fence's value to figure out how
        // far ahead we are. We stop when we've issued presents for all buffers.
        while ((pPresentationManager->GetNextPresentId() -
                presentRetiringFence->GetCompletedValue()) < presentationBuffers.size())
        {
            // Present buffers in cyclical pattern. We can figure out the current buffer to
            // present by taking the modulo of the next present ID by the number of buffers. Note that the
            // first present of a presentation manager always has a present ID of 1 and increments by 1 on
            // each subsequent present. A present ID of 0 is conceptually meant to indicate that "no
            // presents have taken place yet".
            UINT bufferIndex = static_cast<UINT>(
                pPresentationManager->GetNextPresentId() % presentationBuffers.size());

            // Assert that the passed buffer is tracked as available for presentation. Because we throttle
            // based on the total number of buffers, this should always be true.
            NT_ASSERT(presentationBuffers[bufferIndex]->IsAvailable());

            // Advance our present time 1/10th of a second in the future.
            presentTime.value += 1'000'000;

            // Draw red to the texture.
            DrawColorToSurface(
                pD3D11Device,
                textures[bufferIndex],
                1.0f, // red
                0.0f, // green
                0.0f); // blue

            // Bind the presentation buffer to the presentation surface.
            pPresentationSurface->SetBuffer(presentationBuffers[bufferIndex].get());

            // Present at the targeted time.
            pPresentationManager->SetTargetTime(presentTime);
            HRESULT hrPresent = pPresentationManager->Present();
            if (hrPresent == PRESENTATION_ERROR_LOST)
            {
                // Our presentation manager has been lost. Return 'false' to the caller to indicate that
                // the presentation manager should be recreated.
                return false;
            }
            else
            {
                FAIL_FAST_IF_FAILED(hrPresent);
            }
        };

        // Now that the buffer is full, go to sleep until the present queue has been drained to
        // the desired queue depth. To figure out the appropriate present to wake on, we subtract
        // the desired wake queue depth from the presentation manager's last present ID. We
        // use Direct3D's SetEventOnCompletion to signal our wait event when that particular present
        // is retiring, and then wait on that event. Note that the semantic of SetEventOnCompletion
        // is such that even if we happen to call it after the fence has already reached the
        // requested value, the event will be set immediately.
        constexpr UINT wakeOnQueueDepth = 2;
        presentQueueSyncEvent.ResetEvent();
        FAIL_FAST_IF_FAILED(presentRetiringFence->SetEventOnCompletion(
            pPresentationManager->GetNextPresentId() - 1 - wakeOnQueueDepth,
            presentQueueSyncEvent.get()));

        HANDLE waitHandles[] = { lostEvent.get(), presentQueueSyncEvent.get() };
        DWORD waitResult = WaitForMultipleObjects(
            ARRAYSIZE(waitHandles),
            waitHandles,
            FALSE,
            INFINITE);

        // Failfast if we hit an error during our wait.
        FAIL_FAST_IF((waitResult - WAIT_OBJECT_0) >= ARRAYSIZE(waitHandles));

        if (waitResult == WAIT_OBJECT_0)
        {
            // The lost event was signaled - return 'false' to the caller to indicate that
            // the presentation manager was lost.
            return false;
        }

        // Iterate into another refill cycle.
    }

    return true;
}
```

## <a name="example-13mdashvsync-interrupts-and-hardware-flip-queue-support"></a>Exemple 13 &mdash; Vsync interruptions et prise en charge de la file d’attente

Une nouvelle forme de gestion de la file d’attente avec basculement de *matériel* a été introduite avec cette API, ce qui permet de gérer le matériel GPU entièrement indépendamment de l’UC. Le principal avantage de cela est l’efficacité énergétique. Lorsque l’UC n’a pas besoin d’être impliquée dans le processus de présentation, moins d’énergie est dessinée.

Le descripteur de GPU présente un inconvénient : l’état du processeur ne peut plus refléter immédiatement le moment où les cadeaux sont affichés. les concepts de l’API utilise permutation de la composition, tels que les événements de mémoire tampon disponibles, les limites de synchronisation et les statistiques de présentation, ne sont pas mis à jour immédiatement. Au lieu de cela, le GPU actualise uniquement régulièrement l’état de l’UC en ce qui concerne les éléments qui s’affichent. Cela signifie que les commentaires aux applications concernant l’état présent sont fournis avec une latence.

Votre application se soucie généralement de l’affichage d’un certain nombre de cadeaux, mais cela n’a pas d’importance pour d’autres. Par exemple, si votre application émet 10, elle peut décider qu’elle veut savoir quand le 8ème est affiché, afin de pouvoir commencer à reremplir la file d’attente de la présente. Dans ce cas, le seul qui est présent veut vraiment que les commentaires de soient le huitième. Il n’est pas prévu de faire quoi que ce soit lorsque 1-7 ou 9 sont affichés.

Indique si l’état de la mise à jour du processeur varie selon que le matériel GPU est configuré pour générer une interruption VSync quand ce composant est affiché. Cette interruption VSync réactive le processeur si ce n’est pas déjà fait, et l’UC exécute alors un code spécial au niveau du noyau pour se mettre à jour sur les cadeaux qui se sont produits sur le GPU depuis la dernière vérification, à son tour, en mettant à jour les mécanismes de commentaires tels que les événements disponibles dans la mémoire tampon, la clôture de mise hors service actuelle et les statistiques.

Pour permettre à votre application d’indiquer explicitement les présentations qui doivent émettre une interruption VSync, le gestionnaire de présentation expose une méthode [**IPresentationManager :: ForceVSyncInterrupt**](/windows/win32/api/presentation/nf-presentation-ipresentationmanager-forcevsyncinterrupt) , qui spécifie si les présentations suivantes doivent émettre une interruption Vsync. Ce paramètre s’applique à tous les cadeaux futurs jusqu’à ce qu’il soit modifié, comme [**IPresentationManager :: SetTargetTime**](/windows/win32/api/presentation/nf-presentation-ipresentationmanager-settargettime) et [**IPresentationManager :: SetPreferredPresentDuration**](/windows/win32/api/presentation/nf-presentation-ipresentationmanager-setpreferredpresentduration).

Si ce paramètre est activé sur un présent, le matériel avertit immédiatement l’UC quand ce présent est affiché, en utilisant davantage de puissance, tout en veillant à ce que le processeur soit immédiatement averti quand un présent est présent pour permettre aux applications de répondre le plus rapidement possible. Si ce paramètre est désactivé sur un présent existant, le système est autorisé à différer la mise à jour de l’UC lorsque le présent s’affiche pour économiser de l' &mdash; énergie, mais différer les commentaires.

En général, votre application ne force pas l’interruption VSync pour les cadeaux, à l’exception d’un présent qu’elle souhaite synchroniser avec. Dans l’exemple ci-dessus, dans la mesure où votre application souhaitait se réveiller lorsque le 8ème présentait l’affichage de la file d’attente actuelle, elle demanderait que la présente 8 signale une interruption VSync, mais présente 1-7 et la présente 9. 

Par défaut, si votre application ne configure pas ce paramètre, le gestionnaire de présentation signalera toujours l’interruption VSync lorsque chaque présent sera affiché. Les applications qui ne se soucient pas de l’utilisation de l’alimentation, ou qui ne sont pas conscientes de la prise en charge de la file d’attente de basculement, peuvent tout simplement ne pas appeler **ForceVSyncInterrupt**, et il est donc garanti qu’elles se synchronisent correctement. Les applications qui prennent en charge la prise en charge du basculement de la file d’attente matérielle peuvent explicitement contrôler ce paramètre pour améliorer l’efficacité énergétique.

Vous trouverez ci-dessous un diagramme décrivant le comportement de l’API par rapport aux paramètres d’interruption VSync.

![Interruptions VSync](images/vsync-interrupts.png)

### <a name="c-example"></a>Exemple C++

```cpp
bool ForceVSyncInterruptPresentsExample(
    _In_ ID3D11Device* pD3D11Device,
    _In_ IPresentationManager* pPresentationManager,
    _In_ IPresentationSurface* pPresentationSurface,
    _In_ vector<com_ptr_failfast<ID3D11Texture2D>>& textures,
    _In_ vector<com_ptr_failfast<IPresentationBuffer>>& presentationBuffers)
{
    // Track a time we'll be presenting to below. Default to the current time, then increment by
    // 1/10th of a second every present.
    SystemInterruptTime presentTime;
    QueryInterruptTimePrecise(&presentTime.value);

    // Get present retiring fence.
    com_ptr_failfast<ID3D11Fence> presentRetiringFence;
    FAIL_FAST_IF_FAILED(pPresentationManager->GetPresentRetiringFence(
        IID_PPV_ARGS(&presentRetiringFence)));

    // Get the lost event to query before presentation.
    unique_event lostEvent;
    pPresentationManager->GetLostEvent(&lostEvent);

    // Create an event to synchronize to our queue depth with. We will use Direct3D to signal this event
    // when our synchronization fence indicates reaching a specific present.
    unique_event presentQueueSyncEvent;
    presentQueueSyncEvent.create(EventOptions::ManualReset);

    // Issue 10 presents, and wake when the present queue is 2 entries deep (which happens when
    // present 7 is retiring).
    constexpr UINT wakeOnQueueDepth = 2;
    constexpr UINT numberOfPresents = 10;
    const UINT presentIdToWakeOn = numberOfPresents - 1 - wakeOnQueueDepth;
    while (pPresentationManager->GetNextPresentId() <= numberOfPresents)
    {
        UINT bufferIndex = static_cast<UINT>(
            pPresentationManager->GetNextPresentId() % presentationBuffers.size());

        // Advance our present time 1/10th of a second in the future.
        presentTime.value += 1'000'000;

        // Draw red to the texture.
        DrawColorToSurface(
            pD3D11Device,
            textures[bufferIndex],
            1.0f, // red
            0.0f, // green
            0.0f); // blue

        // Bind the presentation buffer to the presentation surface.
        pPresentationSurface->SetBuffer(presentationBuffers[bufferIndex].get());

        // Present at the targeted time.
        pPresentationManager->SetTargetTime(presentTime);

        // If this present is not going to retire the present that we want to wake on when it is shown, then
        // we don't need immediate updates to buffer available events, present retiring fence, or present
        // statistics. As such, we can mark it as not requiring a VSync interrupt, to allow for greater
        // power efficiency on machines with hardware flip queue support.
        bool forceVSyncInterrupt = (pPresentationManager->GetNextPresentId() == (presentIdToWakeOn + 1));
        pPresentationManager->ForceVSyncInterrupt(forceVSyncInterrupt);

        HRESULT hrPresent = pPresentationManager->Present();
        if (hrPresent == PRESENTATION_ERROR_LOST)
        {
            // Our presentation manager has been lost. Return 'false' to the caller to indicate that
            // the presentation manager should be recreated.
            return false;
        }
        else
        {
            FAIL_FAST_IF_FAILED(hrPresent);
        }
    }

    // Now that the buffer is full, go to sleep until presentIdToWakeOn has begun retiring. We
    // configured the subsequent present to force a VSync interrupt when it is shown, which will ensure
    // this wait is completed immediately.
    presentQueueSyncEvent.ResetEvent();
    FAIL_FAST_IF_FAILED(presentRetiringFence->SetEventOnCompletion(
        presentIdToWakeOn,
        presentQueueSyncEvent.get()));

    HANDLE waitHandles[] = { lostEvent.get(), presentQueueSyncEvent.get() };
    DWORD waitResult = WaitForMultipleObjects(
        ARRAYSIZE(waitHandles),
        waitHandles,
        FALSE,
        INFINITE);

    // Failfast if we hit an error during our wait.
    FAIL_FAST_IF((waitResult - WAIT_OBJECT_0) >= ARRAYSIZE(waitHandles));

    if (waitResult == WAIT_OBJECT_0)
    {
        // The lost event was signaled - return 'false' to the caller to indicate that
        // the presentation manager was lost.
        return false;
    }

    return true;
}
```

## <a name="example-14mdashcanceling-presents-scheduled-for-the-future"></a>Exemple 14 &mdash; annulation des cadeaux planifiés à l’avenir

Les applications multimédias qui s’affichent en haut de la file d’attente peuvent décider d’annuler les cadeaux qu’elles ont déjà émis. Cela peut se produire, par exemple, si votre application lit une vidéo, a émis un grand nombre de trames à l’avenir et l’utilisateur décide de suspendre la lecture vidéo. Dans ce cas, votre application souhaitera respecter le frame en cours et annuler les images futures qui n’ont pas encore été mises en file d’attente. Cela peut également se produire si une application multimédia décide de déplacer la lecture vers un autre point de la vidéo. Dans ce cas, votre application souhaite annuler tous les cadeaux qui n’ont pas encore été mis en file d’attente pour l’ancienne position dans la vidéo, et les remplacer par des cadeaux pour la nouvelle position. Dans ce cas, après avoir annulé les présentation précédentes, votre application peut émettre de nouveaux cadeaux à l’avenir correspondant au nouveau point de la vidéo.

### <a name="c-example"></a>Exemple C++

```cpp
void PresentCancelExample(
    _In_ IPresentationManager* pPresentationManager,
    _In_ UINT64 firstPresentIDToCancelFrom)

{
    // Assume we've issued a number of presents in the future. Something happened in the app, and
    // we want to cancel the issued presents that occur after a specified time or present ID. This
    // may happen, for example, when the user pauses playback from inside a media application. The
    // application will want to cancel all presents posted targeting beyond the pause time. The
    // cancel will apply to all previously posted presents whose present IDs are at least
    // 'firstPresentIDToCancelFrom'. Note that Present IDs are always unique, and never recycled,
    // so even if a present is canceled, no subsequent present will ever reuse its present ID.
    //
    // Also note that if some presents we attempt to cancel can't be canceled because they've
    // already started queueing, then no error will be returned, they simply won't be canceled as
    // requested. Cancelation takes a "best effort" approach.
    FAIL_FAST_IF_FAILED(pPresentationManager->CancelPresentsFrom(firstPresentIDToCancelFrom));

    // In the case where the media application scrubbed to a different position in the video, it may now
    // choose to issue new presents to replace the ones canceled. This is not illustrated here, but
    // previous examples that demonstrate presentation show how this may be achieved.
}
```

## <a name="example-15mdashstaggered-buffer-resize-operation-for-improved-performance"></a>Exemple 15 &mdash; opération de redimensionnement de tampon échelonné pour des performances améliorées

Cet exemple montre comment votre application peut échelonner les redimensionnements de tampons pour améliorer les performances par rapport à DXGI. Rappelez-vous notre précédent exemple de redimensionnement, dans lequel un client de service de diffusion de films souhaite changer la résolution de la lecture de 720p à 1080p. Dans DXGI, l’application effectue une opération de redimensionnement sur le utilise permutation DXGI, ce qui permet de supprimer de manière atomique toutes les mémoires tampons précédentes et de réallouer toutes les nouvelles mémoires tampons 1080p simultanément, puis de les ajouter au utilise permutation. Ce type de redimensionnement atomique des tampons est onéreux et peut prendre beaucoup de temps et provoquer des problèmes. La nouvelle API offre un contrôle plus fin sur les mémoires tampons de présentation individuelles. Par conséquent, les mémoires tampons peuvent être réallouées et remplacées un par un sur plusieurs cadeaux pour fractionner la charge de travail au fil du temps. Cela a moins d’impact sur un présent et est bien moins susceptible de provoquer des problèmes. Essentiellement, pour un gestionnaire de présentation avec n mémoires tampons de présentation, pour « n », votre application peut supprimer une ancienne mémoire tampon de présentation à l’ancienne taille, allouer une nouvelle mémoire tampon de présentation à la nouvelle taille et la présenter. Une fois que « n » s’affiche, toutes les mémoires tampons sont à la nouvelle taille.

### <a name="c-example"></a>Exemple C++

```cpp
bool StaggeredResizeExample(
    _In_ ID3D11Device* pD3D11Device,
    _In_ IPresentationManager* pPresentationManager,
    _In_ IPresentationSurface* pPresentationSurface,
    _In_ vector<com_ptr_failfast<ID3D11Texture2D>> textures,
    _In_ vector<com_ptr_failfast<IPresentationBuffer>> presentationBuffers)
{
    // Track a time we'll be presenting to below. Default to the current time, then increment by
    // 1/10th of a second every present.
    SystemInterruptTime presentTime;
    QueryInterruptTimePrecise(&presentTime.value);

    // Assume textures/presentationBuffers vector contains 10 100x100 buffers, and we want to resize
    // our swapchain to 200x200. Instead of reallocating 10 200x200 buffers all at once,
    // like DXGI does today, we can stagger the reallocation across multiple presents. For
    // each present, we can allocate one buffer at the new size, and replace one old buffer
    // at the old size with the new one at the new size. After 10 presents, we will have
    // reallocated all our buffers, and we will have done so in a manner that's much less
    // likely to produce delays or glitches.
    constexpr UINT numberOfBuffers = 10;
    for (UINT bufferIndex = 0; bufferIndex < numberOfBuffers; bufferIndex++)
    {
        // Advance our present time 1/10th of a second in the future.
        presentTime.value += 1'000'000;

        // Release the old texture/presentation buffer at the presented index.
        auto& replacedTexture = textures[bufferIndex];
        auto& replacedPresentationBuffer = presentationBuffers[bufferIndex];
        replacedTexture.reset();
        replacedPresentationBuffer.reset();

        // Create a new texture/presentation buffer in its place.
        AddNewPresentationBuffer(
            pD3D11Device,
            pPresentationManager,
            200, // Buffer width
            200, // Buffer height
            &replacedTexture,
            &replacedPresentationBuffer);

        // Draw red to the new texture.
        DrawColorToSurface(
            pD3D11Device,
            replacedTexture,
            1.0f, // red
            0.0f, // green
            0.0f); // blue

        // Bind the presentation buffer to the presentation surface.
        pPresentationSurface->SetBuffer(replacedPresentationBuffer.get());

        // Present at the targeted time.
        pPresentationManager->SetTargetTime(presentTime);
        HRESULT hrPresent = pPresentationManager->Present();
        if (hrPresent == PRESENTATION_ERROR_LOST)
        {
            // Our presentation manager has been lost. Return 'false' to the caller to indicate that
            // the presentation manager should be recreated.
            return false;
        }
        else
        {
            FAIL_FAST_IF_FAILED(hrPresent);
        }
    }

    return true;
}
```

## <a name="example-16mdashreading-and-processing-present-statistics"></a>Exemple 16 &mdash; lecture et traitement des statistiques actuelles

L’API signale des statistiques pour chaque présentation qui est soumise. À un niveau élevé, la présentation des statistiques est un mécanisme de commentaires qui décrit comment un présent particulier a été traité ou affiché par le système. Il existe différents types de statistiques que votre application peut inscrire pour recevoir, et l’infrastructure des statistiques de l’API elle-même doit être développée, de sorte que davantage de types de statistiques peuvent être ajoutés à l’avenir. Cette API décrit comment lire les statistiques et décrit les types de statistiques définis aujourd’hui, ainsi que les informations qu’elles communiquent à un niveau élevé.

### <a name="c-example"></a>Exemple C++

```cpp
// This is an identifier we'll assign to our presentation surface that will be used to reference that
// presentation surface in statistics. This is to avoid referring to a presentation surface by pointer
// in a statistics structure, which has unclear refcounting and lifetime semantics.
static constexpr UINT_PTR myPresentedContentTag = 12345;

bool StatisticsExample(
    _In_ ID3D11Device* pD3D11Device,
    _In_ IPresentationManager* pPresentationManager,
    _In_ IPresentationSurface* pPresentationSurface,
    _In_ vector<com_ptr_failfast<ID3D11Texture2D>>& textures,
    _In_ vector<com_ptr_failfast<IPresentationBuffer>>& presentationBuffers)
{
    // Track a time we'll be presenting to below. Default to the current time, then increment by
    // 1/10th of a second every present.
    SystemInterruptTime presentTime;
    QueryInterruptTimePrecise(&presentTime.value);

    // Register to receive 3 types of statistics.
    FAIL_FAST_IF_FAILED(pPresentationManager->EnablePresentStatisticsKind(
        PresentStatisticsKind_CompositionFrame,
        true));
    FAIL_FAST_IF_FAILED(pPresentationManager->EnablePresentStatisticsKind(
        PresentStatisticsKind_PresentStatus,
        true));
    FAIL_FAST_IF_FAILED(pPresentationManager->EnablePresentStatisticsKind(
        PresentStatisticsKind_IndependentFlipFrame,
        true));

    // Stats come back referencing specific presentation surfaces. We assign 'tags' to presentation
    // surfaces in the API that statistics will use to reference the presentation surface in a
    // statistic.
    pPresentationSurface->SetTag(myPresentedContentTag);

    // Build an array of events that we can wait on.
    vector<unique_event> waitEvents;

    // The lost event will be the first event in our list. This is an event that signifies that
    // something went wrong in the system (due to extreme conditions like memory pressure, or
    // driver issues) that indicate that the presentation manager has been lost, and should no
    // longer be used, and instead should be recreated.
    unique_event lostEvent;
    FAIL_FAST_IF_FAILED(pPresentationManager->GetLostEvent(&lostEvent));
    waitEvents.emplace_back(std::move(lostEvent));

    // The statistics event will be the second event in our list. This event will be signaled
    // by the presentation manager when there are statistics to read back.
    unique_event statisticsEvent;
    FAIL_FAST_IF_FAILED(pPresentationManager->GetPresentStatisticsAvailableEvent(&statisticsEvent));
    waitEvents.emplace_back(std::move(statisticsEvent));

    // Add each buffer's available event to the list of events we will be waiting on.
    for (UINT bufferIndex = 0; bufferIndex < presentationBuffers.size(); bufferIndex++)
    {
        unique_event availableEvent;
        presentationBuffers[bufferIndex]->GetAvailableEvent(&availableEvent);
        waitEvents.emplace_back(std::move(availableEvent));
    }

    // Iterate our workflow 120 times.
    constexpr UINT iterationCount = 120;
    for (UINT i = 0; i < iterationCount; i++)
    {
        // Wait for an event to be signaled.
        DWORD waitResult = WaitForMultipleObjects(
            static_cast<UINT>(waitEvents.size()),
            reinterpret_cast<HANDLE*>(waitEvents.data()),
            FALSE,
            INFINITE);

        // Failfast if the wait hit an error.
        FAIL_FAST_IF((waitResult - WAIT_OBJECT_0) >= waitEvents.size());

        // Our lost event was the first event in the array. If this is signaled, then the caller
        // should recreate the presentation manager. This is very similar to how Direct3D devices
        // can be lost. Assume our caller knows to handle this return value appropriately.
        if (waitResult == WAIT_OBJECT_0)
        {
            return false;
        }

        // The second event in the array is the statistics event. If this event is signaled,
        // read and process our statistics.
        if (waitResult == (WAIT_OBJECT_0 + 1))
        {
            StatisticsExample_ProcessStatistics(pPresentationManager);
        }
        // Otherwise, the event corresponds to a buffer available event that is signaled.
        // Compute the buffer for the available event that was signaled and present a
        // frame.
        else
        {
            DWORD bufferIndex = waitResult - (WAIT_OBJECT_0 + 2);

            // Draw red to the texture.
            DrawColorToSurface(
                pD3D11Device,
                textures[bufferIndex],
                1.0f, // red
                0.0f, // green
                0.0f); // blue

            // Bind the texture to the presentation surface.
            pPresentationSurface->SetBuffer(presentationBuffers[bufferIndex].get());

            // Advance our present time 1/10th of a second in the future.
            presentTime.value += 1'000'000;

            // Present at the targeted time.
            pPresentationManager->SetTargetTime(presentTime);
            HRESULT hrPresent = pPresentationManager->Present();
            if (hrPresent == PRESENTATION_ERROR_LOST)
            {
                // Our presentation manager has been lost. Return 'false' to the caller to indicate that
                // the presentation manager should be recreated.
                return false;
            }
            else
            {
                FAIL_FAST_IF_FAILED(hrPresent);
            }
        }
    }

    return true;
}

void StatisticsExample_ProcessStatistics(
    _In_ IPresentationManager* pPresentationManager)
{
    // Dequeue a single present statistics item. This will return the item
    // and pop it off the queue of statistics.
    com_ptr_failfast<IPresentStatistics> presentStatisticsItem;
    pPresentationManager->GetNextPresentStatistics(&presentStatisticsItem);

    // Read back the present ID this corresponds to.
    UINT64 presentId = presentStatisticsItem->GetPresentId();
    UNREFERENCED_PARAMETER(presentId);

    // Switch on the type of statistic this item corresponds to.
    switch (presentStatisticsItem->GetKind())
    {
        case PresentStatisticsKind_PresentStatus:
        {
            // Present status statistics describe whether a given present was queued for display,
            // skipped due to some future present being a better candidate to display on a given
            // frame, or canceled via the API.
            auto presentStatusStatistics = presentStatisticsItem.query<IPresentStatusStatistics>();

            // Read back the status
            PresentStatus status = presentStatusStatistics->GetPresentStatus();
            UNREFERENCED_PARAMETER(status);

            // Possible values for status:
            //   PresentStatus_Queued
            //   PresentStatus_Skipped
            //   PresentStatus_Canceled;

            // Depending on the status returned, your application can adjust their workflow
            // accordingly. For example, if your application sees that a large percentage of their
            // presents are skipped, it means they are presenting more frames than the system can
            // display. In such a case, your application might decided to lower the rate at which
            // you present frames.
        }
        break;

        case PresentStatisticsKind_CompositionFrame:
        {
            // Composition frame statistics describe how a given present was used in a DWM frame.
            // It includes information such as which monitors displayed the present, whether the
            // present was composed or directly scanned out via an MPO plane, and rendering
            // properties such as what transforms were applied to the rendering. Composition
            // frame statistics are not issued for iflip presents - only for presents issued by the
            // compositor. iflip presents have their own type of statistic (described next).
            auto compositionFrameStatistics =
                presentStatisticsItem.query<ICompositionFramePresentStatistics>();

            // Stats should come back for the present statistics item that we tagged earlier.
            NT_ASSERT(compositionFrameStatistics->GetContentTag() == myPresentedContentTag);

            // The composition frame ID indicates the DWM frame ID that the present was used
            // in.
            CompositionFrameId frameId = compositionFrameStatistics->GetCompositionFrameId();

            // Get the display instance array to indicate which displays showed the present. Each
            // instance of the presentation surface will have an entry in this array. For example,
            // if your application adds the same presentation surface to four different visuals in the
            // visual tree, then each instance in the tree will have an entry in the display instance
            // array. Similarly, if the presentation surface shows up on multiple monitors, then each
            // monitor instance will be accounted for in the display instance array that is
            // returned.
            //
            // Note that the pointer returned from GetDisplayInstanceArray is valid for the
            // lifetime of the ICompositionFramePresentStatistics. Your application must not attempt
            // to read this pointer after the ICompositionFramePresentStatistics has been released
            // to a refcount of 0.
            UINT displayInstanceArrayCount;
            const CompositionFrameDisplayInstance* pDisplayInstances;
            compositionFrameStatistics->GetDisplayInstanceArray(
                &displayInstanceArrayCount,
                &pDisplayInstances);

            for (UINT i = 0; i < displayInstanceArrayCount; i++)
            {
                const auto& displayInstance = pDisplayInstances[i];

                // The following are fields that are available in a display instance.

                // The LUID, VidPnSource, and unique ID of the output and its owning
                // adapter. The unique ID will be bumped when a LUID/VidPnSource is
                // recycled. Applications should use the unique ID to determine when
                // this happens so that they don't try and correlate stats from one
                // monitor with another.
                displayInstance.outputAdapterLUID;
                displayInstance.outputVidPnSourceId;
                displayInstance.outputUniqueId;

                // The instanceKind field indicates how the present was used. It
                // indicates that the present was composed (rendered to DWM's backbuffer),
                // scanned out (via MPO/DFlip) or composed to an intermediate buffer by DWM
                // for effects.
                displayInstance.instanceKind;

                // The finalTransform field indicates the transform at which the present was
                // shown in world space. It will include all ancestor visual transforms and
                // can be used to know how it was rendered in the global visual tree.
                displayInstance.finalTransform;

                // The requiredCrossAdapterCopy field indicates whether or not we needed to
                // copy your application's buffer to a different adapter in order to display
                // it. Applications should use this to determine whether or not they should
                // reallocate their buffers onto a different adapter for better performance.
                displayInstance.requiredCrossAdapterCopy;

                // The colorSpace field indicates the colorSpace of the output that the
                // present was rendered to.
                displayInstance.colorSpace;

                // For example, if your application sees that the finalTransform is scaling your
                // content by 2x, you might elect to pre-render that scale into your presentation
                // surface, and then add a 1/2 scale. At which point, the finalTransform should
                // be 1x, and some MPO hardware will be more likely to MPO a presentation surface
                // with a 1x scale applied, since some hardware has a maximum they are able to
                // scale in an MPO plane. Similarly, if your application's content is being scaled
                // down on screen, you may wish to simply render its content at a
                // smaller scale to conserve resources, and apply an enlargement transform.
            }

            // Additionally, we can use the CompositionFrameId reported by the statistic
            // to query timing-related information about that specific frame via the new
            // composition timing API, such as when that frame showed up on screen.
            // Note this is achieved using a separate API from the composition swapchain API, but
            // using the composition frame ID reported in the composition swapchain API to
            // properly specify which frame your application wants timing information from.
            COMPOSITION_FRAME_TARGET_STATS frameTargetStats;
            COMPOSITION_TARGET_STATS targetStats[4];
            frameTargetStats.targetCount = ARRAYSIZE(targetStats);
            frameTargetStats.targetStats = targetStats;

            // Specify the frameId that we got from stats in order to pass to the call
            // below and retrieve timing information about that frame.
            frameTargetStats.frameId = frameId;
            FAIL_FAST_IF_FAILED(DCompositionGetTargetStatistics(1, &frameTargetStats));

            // If the frameTargetStats comes back with a 0 frameId, it means the frame isn't
            // part of statistics. This might mean that it has expired out of
            // DCompositionGetTargetStatistics history, but that call keeps a history buffer
            // roughly equivalent to ~5 seconds worth of frame history, so if your application
            // is processing statistics from the presentation manager relatively regularly,
            // by all accounts it shouldn't worry about DCompositionGetTargetStatistics
            // history expiring. The more likely scenario when this occurs is that it's too
            // early, and that this frame isn't part of statistics YET. In that case, your application
            // should defer processing for this frame, and try again later. For the purposes
            // if sample brevity, we don't bother trying again here. A good method to use would
            // be to add this present info to a list of presents that we haven't gotten target
            // statistics for yet, and try again for all presents in that list any time we get
            // a new PresentStatisticsKind_CompositionFrame for a future frame.
            if (frameTargetStats.frameId == frameId)
            {
                // The targetCount will represent the count of outputs the given frame
                // applied to.
                frameTargetStats.targetCount;

                // The targetTime corresponds to the wall clock QPC time DWM was
                // targeting for the frame.
                frameTargetStats.targetTime;

                for (UINT i = 0; i < frameTargetStats.targetCount; i++)
                {
                    const auto& targetStat = frameTargetStats.targetStats[i];

                    // The present time corresponds to the targeted present time of the composition
                    // frame.
                    targetStat.presentTime;

                    // The target ID corresponds to the LUID/VidPnSourceId/Unique ID for the given
                    // target.
                    targetStat.targetId;

                    // The completedStats convey information about the time a compositor frame was
                    // completed, which marks the time any of its associated composition swapchain API
                    // presents entered the displayed state. In particular, your application might wish
                    // to use the 'time' to know if a present showed at a time it expected.
                    targetStat.completedStats.presentCount;
                    targetStat.completedStats.refreshCount;
                    targetStat.completedStats.time;

                    // There is various other timing statistics information conveyed by
                    // DCompositionGetTargetStatistics.
                }
            }
        }
        break;

        case PresentStatisticsKind_IndependentFlipFrame:
        {
            // Independent flip frame statistics describe a present that was shown via
            // independent flip.
            auto independentFlipFrameStatistics =
                presentStatisticsItem.query<IIndependentFlipFramePresentStatistics>();

            // Stats should come back for the present statistics item that we tagged earlier.
            NT_ASSERT(independentFlipFrameStatistics->GetContentTag() == myPresentedContentTag);

            // The driver-approved present duration describes the custom present duration that was
            // approved by the driver and applied during the present. This is how, for example, media
            // will know whether or not they got 24hz mode for their content if they requested it.
            independentFlipFrameStatistics->GetPresentDuration();

            // The displayed time is the time the present was confirmed to have been shown
            // on screen.
            independentFlipFrameStatistics->GetDisplayedTime();

            // The adapter LUID/VidpnSource ID describe the output on which the present took
            // place. Unlike the composition statistic above, we don't report a unique ID here
            // because a monitor recycle would kick the presentation out of iflip.
            independentFlipFrameStatistics->GetOutputAdapterLUID();
            independentFlipFrameStatistics->GetOutputVidPnSourceId();
        }
        break;
    }
}
```

## <a name="example-17mdashusing-an-abstraction-layer-to-present-using-either-the-new-composition-swapchain-api-or-dxgi-from-your-application"></a>Exemple 17 &mdash; utilisation d’une couche d’abstraction pour présenter à l’aide de la nouvelle API utilise permutation de composition ou dxgi à partir de votre application

Compte tenu des exigences système/pilotes supérieures de la nouvelle API utilise permutation de composition, votre application peut souhaiter utiliser DXGI dans les cas où la nouvelle API n’est pas prise en charge. Heureusement, il est assez facile d’introduire une couche d’abstraction qui utilise l’API disponible pour la présentation. L’exemple suivant montre comment y parvenir.

### <a name="c-example"></a>Exemple C++

```cpp
// A base class presentation provider. We'll provide implementations using both DXGI and the new
// composition swapchain API, which the example will use based on what's supported.
class PresentationProvider
{
public:
    virtual void GetBackBuffer(
        _Out_ ID3D11Texture2D** ppBackBuffer) = 0;

    virtual void Present(
        _In_ SystemInterruptTime presentationTime) = 0;

    virtual bool ReadStatistics(
        _Out_ UINT* pPresentCount,
        _Out_ UINT64* pSyncQPCTime) = 0;

    virtual ID3D11Device* GetD3D11DeviceNoRef()
    {
        return m_d3dDevice.get();
    }

protected:
    com_ptr_failfast<ID3D11Device> m_d3dDevice;
};

// An implementation of PresentationProvider using a DXGI swapchain to provide presentation
// functionality.
class DXGIProvider :
    public PresentationProvider
{
public:
    DXGIProvider(
        _In_ UINT width,
        _In_ UINT height,
        _In_ UINT bufferCount)
    {
        com_ptr_failfast<IDXGIAdapter> dxgiAdapter;
        com_ptr_failfast<IDXGIFactory7> dxgiFactory;
        com_ptr_failfast<IDXGISwapChain1> dxgiSwapchain;
        com_ptr_failfast<ID3D11DeviceContext> d3dDeviceContext;

        // Direct3D device creation flags.
        UINT deviceCreationFlags =
            D3D11_CREATE_DEVICE_BGRA_SUPPORT |
            D3D11_CREATE_DEVICE_SINGLETHREADED;

        // Create the Direct3D device.
        FAIL_FAST_IF_FAILED(D3D11CreateDevice(
            nullptr,                   // No adapter
            D3D_DRIVER_TYPE_HARDWARE,  // Hardware device
            nullptr,                   // No module
            deviceCreationFlags,       // Device creation flags
            nullptr, 0,                // Highest available feature level
            D3D11_SDK_VERSION,         // API version
            &m_d3dDevice,              // Resulting interface pointer
            nullptr,                   // Actual feature level
            &d3dDeviceContext));       // Device context

        // Make our way from the Direct3D device to the DXGI factory.
        auto dxgiDevice = m_d3dDevice.query<IDXGIDevice>();
        FAIL_FAST_IF_FAILED(dxgiDevice->GetParent(IID_PPV_ARGS(&dxgiAdapter)));
        FAIL_FAST_IF_FAILED(dxgiAdapter->GetParent(IID_PPV_ARGS(&dxgiFactory)));

        // Create a swapchain matching the desired parameters.
        DXGI_SWAP_CHAIN_DESC1 desc = {};
        desc.Width = width;
        desc.Height = height;
        desc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
        desc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        desc.SampleDesc.Count = 1;
        desc.SampleDesc.Quality = 0;
        desc.BufferCount = bufferCount;
        desc.Scaling = DXGI_SCALING_STRETCH;
        desc.SwapEffect = DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL;
        desc.AlphaMode = DXGI_ALPHA_MODE_PREMULTIPLIED;
        FAIL_FAST_IF_FAILED(dxgiFactory->CreateSwapChainForComposition(
            m_d3dDevice.get(),
            &desc,
            nullptr,
            &dxgiSwapchain));

        // Store the swapchain.
        dxgiSwapchain.query_to(&m_swapchain);
    }

    void GetBackBuffer(
        _Out_ ID3D11Texture2D** ppBackBuffer) override
    {
        // Get the backbuffer directly from the swapchain.
        FAIL_FAST_IF_FAILED(m_swapchain->GetBuffer(
            m_swapchain->GetCurrentBackBufferIndex(),
            IID_PPV_ARGS(ppBackBuffer)));
    }

    void Present(
        _In_ SystemInterruptTime presentationTime) override
    {
        // Convert the passed presentation time to a present interval. The implementation is
        // not provided here, as there's a great deal of complexity around computing this
        // most accurately, but it essentially boils down to taking the time from now and
        // figuring out the number of vblanks that corresponds to that time duration.
        UINT vblankIntervals = ComputePresentIntervalFromTime(presentationTime);

        // Issue a present to the swapchain. If we wanted to allow for a time to be specified,
        // code here could convert the time to a present duration, which could be passed here.
        FAIL_FAST_IF_FAILED(m_swapchain->Present(vblankIntervals, 0));
    }

    bool ReadStatistics(
        _Out_ UINT* pPresentCount,
        _Out_ UINT64* pSyncQPCTime) override
    {
        // Zero our output parameters initially.
        *pPresentCount = 0;
        *pSyncQPCTime = 0;

        // Grab frame statistics from the swapchain.
        DXGI_FRAME_STATISTICS frameStatistics;
        FAIL_FAST_IF_FAILED(m_swapchain->GetFrameStatistics(&frameStatistics));

        // If the statistics have changed since our last read, then return the new information
        // to the caller.
        bool hasNewStats = false;
        if (frameStatistics.PresentCount > m_lastPresentCount)
        {
            m_lastPresentCount = frameStatistics.PresentCount;
            hasNewStats = true;
            *pPresentCount = frameStatistics.PresentCount;
            *pSyncQPCTime = frameStatistics.SyncQPCTime.QuadPart;
        }

        return hasNewStats;
    }

private:
    com_ptr_failfast<IDXGISwapChain4> m_swapchain;
    UINT m_lastPresentCount = 0;
};

// An implementation of PresentationProvider using the composition swapchain API to provide
// presentation functionality.
class PresentationAPIProvider :
    public PresentationProvider
{
public:
    PresentationAPIProvider(
        _In_ UINT width,
        _In_ UINT height,
        _In_ UINT bufferCount)
    {
        // Create the presentation manager and presentation surface using the function defined in a
        // previous example.
        MakePresentationManagerAndPresentationSurface(
            &m_d3dDevice,
            &m_presentationManager,
            &m_presentationSurface,
            m_presentationSurfaceHandle);

        // Register for present statistics.
        FAIL_FAST_IF_FAILED(m_presentationManager->EnablePresentStatisticsKind(
            PresentStatisticsKind_CompositionFrame,
            true));

        // Get the statistics event from the presentation manager.
        FAIL_FAST_IF_FAILED(m_presentationManager->GetPresentStatisticsAvailableEvent(
            &m_statisticsAvailableEvent));

        // Create and register the specified number of presentation buffers.
        for (UINT i = 0; i < bufferCount; i++)
        {
            com_ptr_failfast<ID3D11Texture2D> texture;
            com_ptr_failfast<IPresentationBuffer> presentationBuffer;
            AddNewPresentationBuffer(
                m_d3dDevice.get(),
                m_presentationManager.get(),
                width,
                height,
                &texture,
                &presentationBuffer);

            // Add the new presentation buffer and texture to our array.
            m_textures.push_back(texture);
            m_presentationBuffers.push_back(presentationBuffer);

            // Store the available event for the presentation buffer.
            unique_event availableEvent;
            FAIL_FAST_IF_FAILED(presentationBuffer->GetAvailableEvent(&availableEvent));
            m_bufferAvailableEvents.emplace_back(std::move(availableEvent));
        }
    }

    void GetBackBuffer(
        _Out_ ID3D11Texture2D** ppBackBuffer) override
    {
        // Query an available backbuffer using our available events.
        DWORD waitIndex = WaitForMultipleObjects(
            static_cast<UINT>(m_bufferAvailableEvents.size()),
            reinterpret_cast<HANDLE*>(m_bufferAvailableEvents.data()),
            FALSE,
            INFINITE);
        UINT bufferIndex = waitIndex - WAIT_OBJECT_0;

        // Set the backbuffer to be the next presentation buffer.
        FAIL_FAST_IF_FAILED(m_presentationSurface->SetBuffer(m_presentationBuffers[bufferIndex].get()));

        // Return the backbuffer to the caller.
        m_textures[bufferIndex].query_to(ppBackBuffer);
    }

    void Present(
        _In_ SystemInterruptTime presentationTime) override
    {
        // Present at the targeted time.
        m_presentationManager->SetTargetTime(presentationTime);
        HRESULT hrPresent = m_presentationManager->Present();
        if (hrPresent == PRESENTATION_ERROR_LOST)
        {
            // Our presentation manager has been lost. See previous examples regarding how to handle this.
            return;
        }
        else
        {
            FAIL_FAST_IF_FAILED(hrPresent);
        }
    }

    bool ReadStatistics(
        _Out_ UINT* pPresentCount,
        _Out_ UINT64* pSyncQPCTime) override
    {
        // Zero our out parameters initially.
        *pPresentCount = 0;
        *pSyncQPCTime = 0;

        bool hasNewStats = false;

        // Peek at the statistics available event state to see if we've got new statistics.
        while (WaitForSingleObject(m_statisticsAvailableEvent.get(), 0) == WAIT_OBJECT_0)
        {
            // Pop a statistics item to process.
            com_ptr_failfast<IPresentStatistics> statisticsItem;
            FAIL_FAST_IF_FAILED(m_presentationManager->GetNextPresentStatistics(
                &statisticsItem));

            // If this is a composition frame stat, process it.
            if (statisticsItem->GetKind() == PresentStatisticsKind_CompositionFrame)
            {
                // We've got new stats to report.
                hasNewStats = true;

                // Convert to composition frame statistic item.
                auto frameStatisticsItem = statisticsItem.query<ICompositionFramePresentStatistics>();

                // Query DirectComposition's target statistics API to determine the completed time.
                COMPOSITION_FRAME_TARGET_STATS frameTargetStats;
                COMPOSITION_TARGET_STATS targetStats[4];
                frameTargetStats.targetCount = ARRAYSIZE(targetStats);
                frameTargetStats.targetStats = targetStats;
                // Specify the frameId we got from stats in order to pass to the call
                // below and retrieve timing information about that frame.
                frameTargetStats.frameId = frameStatisticsItem->GetCompositionFrameId();
                FAIL_FAST_IF_FAILED(DCompositionGetTargetStatistics(1, &frameTargetStats));

                // Return the statistics information for the first target.
                *pPresentCount = static_cast<UINT>(frameStatisticsItem->GetPresentId());
                *pSyncQPCTime = frameTargetStats.targetStats[0].completedStats.time;

                // Note that there's a much richer variety of statistics information in the new
                // API that can be used to infer much more than is possible with DXGI frame
                // statistics.
            }
        }

        return hasNewStats;
    }

    static bool IsSupportedOnSystem()
    {
        // Direct3D device creation flags. The composition swapchain API requires that applications disable internal
        // driver threading optimizations, as these optimizations break synchronization of the API.
        // If this flag isn't present, then the API will fail the call to create the presentation factory.
        UINT deviceCreationFlags =
            D3D11_CREATE_DEVICE_BGRA_SUPPORT |
            D3D11_CREATE_DEVICE_SINGLETHREADED |
            D3D11_CREATE_DEVICE_PREVENT_INTERNAL_THREADING_OPTIMIZATIONS;

        // Create the Direct3D device.
        com_ptr_failfast<ID3D11Device> d3dDevice;
        com_ptr_failfast<ID3D11DeviceContext> d3dDeviceContext;
        FAIL_FAST_IF_FAILED(D3D11CreateDevice(
            nullptr,                   // No adapter
            D3D_DRIVER_TYPE_HARDWARE,  // Hardware device
            nullptr,                   // No module
            deviceCreationFlags,       // Device creation flags
            nullptr, 0,                // Highest available feature level
            D3D11_SDK_VERSION,         // API version
            &d3dDevice,                // Resulting interface pointer
            nullptr,                   // Actual feature level
            &d3dDeviceContext));       // Device context

        // Call the composition swapchain API export to create the presentation factory.
        com_ptr_failfast<IPresentationFactory> presentationFactory;
        FAIL_FAST_IF_FAILED(CreatePresentationFactory(
            d3dDevice.get(),
            IID_PPV_ARGS(&presentationFactory)));

        // Now determine whether the system is capable of supporting the composition swapchain API based
        // on the capability that's reported by the presentation factory.
        return presentationFactory->IsPresentationSupported();
    }

private:
    com_ptr_failfast<IPresentationManager> m_presentationManager;
    com_ptr_failfast<IPresentationSurface> m_presentationSurface;
    vector<com_ptr_failfast<ID3D11Texture2D>> m_textures;
    vector<com_ptr_failfast<IPresentationBuffer>> m_presentationBuffers;
    vector<unique_event> m_bufferAvailableEvents;
    unique_handle m_presentationSurfaceHandle;
    unique_event m_statisticsAvailableEvent;
};

void DXGIOrPresentationAPIExample()
{
    // Get the current system time. We'll base our 'PresentAt' time on this result.
    SystemInterruptTime currentTime;
    QueryInterruptTimePrecise(&currentTime.value);

    // Track a time we'll be presenting at below. Default to the current time, then increment by
    // 1/10th of a second every present.
    auto presentTime = currentTime;

    // Allocate a presentation provider using the composition swapchain API if it is supported;
    // otherwise fall back to DXGI.
    unique_ptr<PresentationProvider> presentationProvider;
    if (PresentationAPIProvider::IsSupportedOnSystem())
    {
        presentationProvider = std::make_unique<PresentationAPIProvider>(
            500, // Buffer width
            500, // Buffer height
            6);  // Number of buffers
    }
    else
    {
        // System doesn't support the composition swapchain API. Fall back to DXGI.
        presentationProvider = std::make_unique<DXGIProvider>(
            500, // Buffer width
            500, // Buffer height
            6);  // Number of buffers
    }

    // Present 50 times.
    constexpr UINT numPresents = 50;
    for (UINT i = 0; i < 50; i++)
    {
        // Advance our present time 1/10th of a second in the future.
        presentTime.value += 1'000'000;

        // Call the presentation provider to get a backbuffer to render to.
        com_ptr_failfast<ID3D11Texture2D> backBuffer;
        presentationProvider->GetBackBuffer(&backBuffer);

        // Render to the backbuffer.
        DrawColorToSurface(
            presentationProvider->GetD3D11DeviceNoRef(),
            backBuffer,
            1.0f, // red
            0.0f, // green
            0.0f); // blue

        // Present the backbuffer.
        presentationProvider->Present(presentTime);

        // Process statistics.
        bool hasNewStats;
        UINT64 presentTime;
        UINT presentCount;
        hasNewStats = presentationProvider->ReadStatistics(
            &presentCount,
            &presentTime);
        if (hasNewStats)
        {
            // Process these statistics however your application wishes.
        }
    }
}
```

## <a name="related-topics"></a>Rubriques connexes

* [Utilise permutation de la composition](comp-swapchain-portal.md)
