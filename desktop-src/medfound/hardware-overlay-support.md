---
description: Décrit comment utiliser les superpositions de matériel dans Direct3D 9.
ms.assetid: fa9d5bf5-4c0f-471a-b639-d329b0cd89a4
title: Prise en charge de la superposition matérielle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adcae33cdf55de59bdcd074829d52b4c1c43ea5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521440"
---
# <a name="hardware-overlay-support"></a><span data-ttu-id="5ebfa-103">Prise en charge de la superposition matérielle</span><span class="sxs-lookup"><span data-stu-id="5ebfa-103">Hardware Overlay Support</span></span>

<span data-ttu-id="5ebfa-104">Une superposition matérielle est une zone dédiée de la mémoire vidéo qui peut être superposée sur la surface principale.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-104">A hardware overlay is a dedicated area of video memory that can be overlayed on the primary surface.</span></span> <span data-ttu-id="5ebfa-105">Aucune copie n’est effectuée lorsque la superposition est affichée.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-105">No copy is performed when the overlay is displayed.</span></span> <span data-ttu-id="5ebfa-106">L’opération de superposition est effectuée dans le matériel, sans modification des données dans la surface principale.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-106">The overlay operation is performed in hardware, without modifying the data in the primary surface.</span></span>

<span data-ttu-id="5ebfa-107">L’utilisation de superpositions de matériel pour la lecture vidéo était courante dans les versions antérieures de Windows, car les superpositions sont efficaces pour le contenu vidéo avec une fréquence d’images élevée.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-107">The use of hardware overlays for video playback was common in earlier versions of Windows, because overlays are efficient for video content with a high frame rate.</span></span> <span data-ttu-id="5ebfa-108">À compter de Windows 7, Direct3D 9 prend en charge les superpositions matérielles.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-108">Starting in Windows 7, Direct3D 9 supports hardware overlays.</span></span> <span data-ttu-id="5ebfa-109">Cette prise en charge est principalement destinée à la lecture vidéo et diffère à certains égards des API DirectDraw précédentes :</span><span class="sxs-lookup"><span data-stu-id="5ebfa-109">This support is intended primarily for video playback, and differs in some respects from earlier DirectDraw APIs:</span></span>

-   <span data-ttu-id="5ebfa-110">La superposition ne peut pas être réduite, mise en miroir ou désentrelacée.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-110">The overlay cannot be shrunk, mirrored, or deinterlaced.</span></span>
-   <span data-ttu-id="5ebfa-111">Les clés de couleur source et la fusion alpha ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-111">Source color keys and alpha blending are not supported.</span></span>
-   <span data-ttu-id="5ebfa-112">Les superpositions peuvent être étirées si le matériel de superposition le prend en charge.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-112">Overlays can be stretched if the overlay hardware supports it.</span></span> <span data-ttu-id="5ebfa-113">Dans le cas contraire, l’étirement n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-113">Otherwise, stretching is not supported.</span></span> <span data-ttu-id="5ebfa-114">En pratique, tous les pilotes graphiques ne prennent pas en charge l’étirement.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-114">In practice, not all graphics drivers support stretching.</span></span>
-   <span data-ttu-id="5ebfa-115">Chaque périphérique prend en charge au plus une superposition.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-115">Each device supports at most one overlay.</span></span>
-   <span data-ttu-id="5ebfa-116">La superposition est effectuée à l’aide d’une clé de couleur de destination, mais le runtime Direct3D sélectionne automatiquement la couleur et dessine le rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-116">Overlay is performed using a destination color key, but the Direct3D runtime automatically selects the color and draws the destination rectangle.</span></span> <span data-ttu-id="5ebfa-117">Direct3D effectue automatiquement le suivi de la position de la fenêtre et met à jour la position de superposition chaque fois que le **PresentEx** est appelé.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-117">Direct3D automatically tracks the position of the window and updates the overlay position whenever the **PresentEx** is called.</span></span>

### <a name="creating-a-hardware-overlay-surface"></a><span data-ttu-id="5ebfa-118">Création d’une surface de superposition matérielle</span><span class="sxs-lookup"><span data-stu-id="5ebfa-118">Creating a Hardware Overlay Surface</span></span>

<span data-ttu-id="5ebfa-119">Pour interroger la prise en charge de la superposition, appelez **IDirect3D9 :: GetDeviceCaps**.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-119">To query for overlay support, call **IDirect3D9::GetDeviceCaps**.</span></span> <span data-ttu-id="5ebfa-120">Si le pilote prend en charge la superposition matérielle, l’indicateur de **\_ superposition D3DCAPS** est défini dans **D3DCAPS9. Membre Caps** .</span><span class="sxs-lookup"><span data-stu-id="5ebfa-120">If the driver supports hardware overlay, the **D3DCAPS\_OVERLAY** flag is set in the **D3DCAPS9.Caps** member.</span></span>

<span data-ttu-id="5ebfa-121">Pour déterminer si un format de superposition spécifique est pris en charge pour un mode d’affichage donné, appelez [**IDirect3D9ExOverlayExtension :: CheckDeviceOverlayType**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9exoverlayextension-checkdeviceoverlaytype).</span><span class="sxs-lookup"><span data-stu-id="5ebfa-121">To find out whether a specific overlay format is supported for a given display mode, call [**IDirect3D9ExOverlayExtension::CheckDeviceOverlayType**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9exoverlayextension-checkdeviceoverlaytype).</span></span>

<span data-ttu-id="5ebfa-122">Pour créer la superposition, appelez **IDirect3D9Ex :: CreateDeviceEx** et spécifiez l’effet d’échange de **\_ superposition D3DSWAPEFFECT** .</span><span class="sxs-lookup"><span data-stu-id="5ebfa-122">To create the overlay, call **IDirect3D9Ex::CreateDeviceEx** and specify the **D3DSWAPEFFECT\_OVERLAY** swap effect.</span></span> <span data-ttu-id="5ebfa-123">La mémoire tampon d’arrière-plan peut utiliser un format non RVB si le matériel le prend en charge.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-123">The back buffer can use a non-RGB format if the hardware supports it.</span></span>

<span data-ttu-id="5ebfa-124">Les surfaces de superposition présentent les limitations suivantes :</span><span class="sxs-lookup"><span data-stu-id="5ebfa-124">Overlay surfaces have the following limitations:</span></span>

-   <span data-ttu-id="5ebfa-125">L’application ne peut pas créer plus d’une chaîne de permutation de superposition.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-125">The application cannot create more than one overlay swap chain.</span></span>
-   <span data-ttu-id="5ebfa-126">La superposition doit être utilisée en mode fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-126">The overlay must be used in windowed mode.</span></span> <span data-ttu-id="5ebfa-127">Elle ne peut pas être utilisée en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-127">It cannot be used in fullscreen mode.</span></span>
-   <span data-ttu-id="5ebfa-128">L’effet d’échange de superposition doit être utilisé avec l’interface **IDirect3DDevice9Ex** .</span><span class="sxs-lookup"><span data-stu-id="5ebfa-128">The overlay swap effect must be used with the **IDirect3DDevice9Ex** interface.</span></span> <span data-ttu-id="5ebfa-129">Elle n’est pas prise en charge pour **IDirect3DDevice9**.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-129">It is not supported for **IDirect3DDevice9**.</span></span>
-   <span data-ttu-id="5ebfa-130">L’échantillonnage multiple ne peut pas être utilisé.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-130">Multisampling cannot be used.</span></span>
-   <span data-ttu-id="5ebfa-131">Les indicateurs **D3DPRESENT \_ DONOTFLIP** et **D3DPRESENT \_ FLIPRESTART** ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-131">The **D3DPRESENT\_DONOTFLIP** and **D3DPRESENT\_FLIPRESTART** flags are not supported.</span></span>
-   <span data-ttu-id="5ebfa-132">Les statistiques de présentation ne sont pas disponibles pour la surface de recouvrement.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-132">Presentation statistics are not available for the overlay surface.</span></span>

<span data-ttu-id="5ebfa-133">Si le matériel ne prend pas en charge l’étirement, il est recommandé de créer une chaîne de permutation aussi grande que le mode d’affichage, afin que la fenêtre puisse être redimensionnée sur n’importe quelle dimension.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-133">If the hardware does not support stretching, it is recommended to create a swap chain as large as the display mode, so that the window can be resized to any dimensions.</span></span> <span data-ttu-id="5ebfa-134">La recréation de la chaîne de permutation n’est pas une méthode optimale pour gérer le redimensionnement de la fenêtre, car cela peut provoquer de graves artefacts de rendu.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-134">Recreating the swap chain is not an optimal way to handle resizing the window, because it can cause severe rendering artifacts.</span></span> <span data-ttu-id="5ebfa-135">En outre, en raison de la façon dont le GPU gère la mémoire de superposition, la recréation de la chaîne de permutation peut entraîner une application à manquer de mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-135">Also, because of the way the GPU manages the overlay memory, recreating the swap chain can potentially cause an application to run out of video memory.</span></span>

### <a name="new-d3dpresent_parameters-flags"></a><span data-ttu-id="5ebfa-136">Nouveaux \_ indicateurs de paramètres D3DPRESENT</span><span class="sxs-lookup"><span data-stu-id="5ebfa-136">New D3DPRESENT\_PARAMETERS Flags</span></span>

<span data-ttu-id="5ebfa-137">Les indicateurs **de \_ paramètres D3DPRESENT** suivants sont définis pour créer des superpositions.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-137">The following **D3DPRESENT\_PARAMETERS** flags are defined for creating overlays.</span></span>



| <span data-ttu-id="5ebfa-138">Indicateur</span><span class="sxs-lookup"><span data-stu-id="5ebfa-138">Flag</span></span>                                      | <span data-ttu-id="5ebfa-139">Description</span><span class="sxs-lookup"><span data-stu-id="5ebfa-139">Description</span></span>                                                                                                                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ebfa-140">**D3DPRESENTFLAG \_ superposition \_ LIMITEDRGB**</span><span class="sxs-lookup"><span data-stu-id="5ebfa-140">**D3DPRESENTFLAG\_OVERLAY\_LIMITEDRGB**</span></span>   | <span data-ttu-id="5ebfa-141">La plage RVB est comprise entre 16 et 235.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-141">The RGB range is 16–235.</span></span> <span data-ttu-id="5ebfa-142">La valeur par défaut est comprise entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-142">The default is 0–255.</span></span> <br/> <span data-ttu-id="5ebfa-143">Nécessite la fonctionnalité **D3DOVERLAYCAPS \_ LIMITEDRANGERGB** .</span><span class="sxs-lookup"><span data-stu-id="5ebfa-143">Requires the **D3DOVERLAYCAPS\_LIMITEDRANGERGB** capability.</span></span><br/>                                                 |
| <span data-ttu-id="5ebfa-144">**\_Superposition \_ D3DPRESENTFLAG \_ BT709 YCbCr**</span><span class="sxs-lookup"><span data-stu-id="5ebfa-144">**D3DPRESENTFLAG\_OVERLAY\_YCbCr\_BT709**</span></span> | <span data-ttu-id="5ebfa-145">Les couleurs YUV utilisent la définition BT. 709.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-145">YUV colors use the BT.709 definition.</span></span> <span data-ttu-id="5ebfa-146">La valeur par défaut est BT. 601.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-146">The default is BT.601.</span></span> <br/> <span data-ttu-id="5ebfa-147">Nécessite la fonctionnalité **D3DOVERLAYCAPS \_ YCbCr \_ BT709** .</span><span class="sxs-lookup"><span data-stu-id="5ebfa-147">Requires the **D3DOVERLAYCAPS\_YCbCr\_BT709** capability.</span></span><br/>                                      |
| <span data-ttu-id="5ebfa-148">**\_Superposition \_ D3DPRESENTFLAG \_ xvYCC YCbCr**</span><span class="sxs-lookup"><span data-stu-id="5ebfa-148">**D3DPRESENTFLAG\_OVERLAY\_YCbCr\_xvYCC**</span></span> | <span data-ttu-id="5ebfa-149">Sortie des données à l’aide d’une extension YCbCr étendue (xvYCC).</span><span class="sxs-lookup"><span data-stu-id="5ebfa-149">Output the data by using extended YCbCr (xvYCC).</span></span><br/> <span data-ttu-id="5ebfa-150">Requiert la fonctionnalité **D3DOVERLAYCAPS \_ YCbCr \_ BT601 \_ xvYCC** ou **D3DOVERLAYCAPS \_ YCbCr \_ BT709 \_ xvYCC** .</span><span class="sxs-lookup"><span data-stu-id="5ebfa-150">Requires the **D3DOVERLAYCAPS\_YCbCr\_BT601\_xvYCC** or **D3DOVERLAYCAPS\_YCbCr\_BT709\_xvYCC** capability.</span></span><br/> |



 

### <a name="using-hardware-overlays"></a><span data-ttu-id="5ebfa-151">Utilisation des superpositions matérielles</span><span class="sxs-lookup"><span data-stu-id="5ebfa-151">Using Hardware Overlays</span></span>

<span data-ttu-id="5ebfa-152">Pour afficher la surface de recouvrement, l’application appelle **IDirect3DDevice9Ex ::P resentex**.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-152">To display the overlay surface, the application calls **IDirect3DDevice9Ex::PresentEx**.</span></span> <span data-ttu-id="5ebfa-153">Le runtime Direct3D dessine automatiquement la clé de couleur de destination.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-153">The Direct3D runtime automatically draws the destination color key.</span></span>

<span data-ttu-id="5ebfa-154">Les indicateurs **PresentEx** suivants sont définis pour les superpositions.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-154">The following **PresentEx** flags are defined for overlays.</span></span>



| <span data-ttu-id="5ebfa-155">Indicateur</span><span class="sxs-lookup"><span data-stu-id="5ebfa-155">Flag</span></span>                              | <span data-ttu-id="5ebfa-156">Description</span><span class="sxs-lookup"><span data-stu-id="5ebfa-156">Description</span></span>                                                                                                                                                                                                                                                                           |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ebfa-157">**D3DPRESENT \_ UPDATECOLORKEY**</span><span class="sxs-lookup"><span data-stu-id="5ebfa-157">**D3DPRESENT\_UPDATECOLORKEY**</span></span>    | <span data-ttu-id="5ebfa-158">Définir cet indicateur si la Gestionnaire de fenêtrage (DWM) est désactivée.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-158">Set this flag if Desktop Window Manager (DWM) composition is disabled.</span></span> <span data-ttu-id="5ebfa-159">Avec cet indicateur, Direct3D redessine la clé de couleur.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-159">This flag causes Direct3D to redraw the color key.</span></span><br/> <span data-ttu-id="5ebfa-160">Si DWM est activé, cet indicateur n’est pas requis, car Direct3D dessine la clé de couleur une seule fois sur la surface que DWM utilise pour la redirection.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-160">If DWM is enabled, this flag is not required, because Direct3D draws the color key once on the surface that DWM uses for redirection.</span></span><br/> |
| <span data-ttu-id="5ebfa-161">**D3DPRESENT \_ HIDEOVERLAY**</span><span class="sxs-lookup"><span data-stu-id="5ebfa-161">**D3DPRESENT\_HIDEOVERLAY**</span></span>       | <span data-ttu-id="5ebfa-162">Masque la superposition.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-162">Hides the overlay.</span></span>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="5ebfa-163">**D3DPRESENT \_ UPDATEOVERLAYONLY**</span><span class="sxs-lookup"><span data-stu-id="5ebfa-163">**D3DPRESENT\_UPDATEOVERLAYONLY**</span></span> | <span data-ttu-id="5ebfa-164">Met à jour la superposition sans modifier le contenu.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-164">Updates the overlay without changing the contents.</span></span><br/> <span data-ttu-id="5ebfa-165">Cet indicateur est utile si la fenêtre se déplace alors que la vidéo est en pause.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-165">This flag is useful if the window moves while the video is paused.</span></span><br/>                                                                                                                                           |



 

<span data-ttu-id="5ebfa-166">Une application doit être préparée à gérer les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="5ebfa-166">An application should be prepared to handle the following cases:</span></span>

-   <span data-ttu-id="5ebfa-167">Si une autre application utilise la superposition, **PresentEx** retourne **D3DERR \_ NOTAVAILABLE**.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-167">If another application is using the overlay, **PresentEx** returns **D3DERR\_NOTAVAILABLE**.</span></span>
-   <span data-ttu-id="5ebfa-168">Si la fenêtre est déplacée vers un autre moniteur, l’application doit recréer la chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-168">If the window is moved to another monitor, the application must recreate the swap chain.</span></span> <span data-ttu-id="5ebfa-169">Sinon, si l’application appelle **PresentEx** pour afficher la superposition sur une autre analyse, **PresentEx** retourne **D3DERR \_ INVALIDDEVICE**.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-169">Otherwise, if the application calls **PresentEx** to display the overlay on a different monitor, **PresentEx** returns **D3DERR\_INVALIDDEVICE**.</span></span>
-   <span data-ttu-id="5ebfa-170">Si le mode d’affichage change, Direct3D tente de restaurer la superposition.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-170">If the display mode changes, Direct3D attempts to restore the overlay.</span></span> <span data-ttu-id="5ebfa-171">Si le nouveau mode ne prend pas en charge la superposition, **PresentEx** retourne **D3DERR \_ UNSUPPORTEDOVERLAY**.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-171">If the new mode does not support the overlay, **PresentEx** returns **D3DERR\_UNSUPPORTEDOVERLAY**.</span></span>

### <a name="example-code"></a><span data-ttu-id="5ebfa-172">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="5ebfa-172">Example Code</span></span>

<span data-ttu-id="5ebfa-173">L’exemple suivant montre comment créer une surface de recouvrement.</span><span class="sxs-lookup"><span data-stu-id="5ebfa-173">The following example shows how to create an overlay surface.</span></span>


```C++
const UINT VIDEO_WIDTH = 256;
const UINT VIDEO_HEIGHT = 256;

HRESULT CreateHWOverlay(
    HWND hwnd, 
    IDirect3D9Ex *pD3D, 
    IDirect3DDevice9Ex **ppDevice
    )
{
    *ppDevice = NULL;

    D3DCAPS9                caps;
    ZeroMemory(&caps, sizeof(caps));

    HRESULT hr = pD3D->GetDeviceCaps(
        D3DADAPTER_DEFAULT,
        D3DDEVTYPE_HAL,
        &caps
        );

    if (FAILED(hr))
    {
        return hr;
    }

    // Check if overlay is supported.
    if (!(caps.Caps & D3DCAPS_OVERLAY))
    {
        return D3DERR_UNSUPPORTEDOVERLAY;
    }

    D3DOVERLAYCAPS          overlayCaps = { 0 };

    IDirect3DDevice9Ex           *pDevice = NULL;
    IDirect3D9ExOverlayExtension *pOverlay = NULL;

    // Check specific overlay capabilities.
    hr = pD3D->QueryInterface(IID_PPV_ARGS(&pOverlay));

    if (SUCCEEDED(hr))
    {
        hr = pOverlay->CheckDeviceOverlayType(
            D3DADAPTER_DEFAULT,
            D3DDEVTYPE_HAL,
            VIDEO_WIDTH,
            VIDEO_HEIGHT,
            D3DFMT_X8R8G8B8,
            NULL,
            D3DDISPLAYROTATION_IDENTITY,
            &overlayCaps
            );
    }

    // Create the overlay.
    if (SUCCEEDED(hr))
    {

        DWORD flags =   D3DCREATE_FPU_PRESERVE | 
                        D3DCREATE_MULTITHREADED | 
                        D3DCREATE_SOFTWARE_VERTEXPROCESSING;

        
        D3DPRESENT_PARAMETERS   pp = { 0 };

        pp.BackBufferWidth = overlayCaps.MaxOverlayDisplayWidth;
        pp.BackBufferHeight = overlayCaps.MaxOverlayDisplayHeight;
        pp.BackBufferFormat = D3DFMT_X8R8G8B8;
        pp.SwapEffect = D3DSWAPEFFECT_OVERLAY;
        pp.hDeviceWindow = hwnd;
        pp.Windowed = TRUE;
        pp.Flags = D3DPRESENTFLAG_VIDEO;
        pp.FullScreen_RefreshRateInHz = D3DPRESENT_RATE_DEFAULT;
        pp.PresentationInterval       = D3DPRESENT_INTERVAL_ONE;

        hr = pD3D->CreateDeviceEx(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL,
            NULL, flags, &pp, NULL, &pDevice);
    }

    if (SUCCEEDED(hr))
    {
        (*ppDevice) = pDevice;
        (*ppDevice)->AddRef();
    }

    SafeRelease(&pD3D);
    SafeRelease(&pDevice);
    SafeRelease(&pOverlay);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="5ebfa-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5ebfa-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ebfa-175">API vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="5ebfa-175">Direct3D Video APIs</span></span>](direct3d-video-apis.md)
</dt> </dl>

 

 




