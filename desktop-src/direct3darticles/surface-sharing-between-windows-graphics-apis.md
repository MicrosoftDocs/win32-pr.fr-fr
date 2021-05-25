---
title: Partage de surface entre les API graphiques Windows
description: Cette rubrique fournit une vue d’ensemble technique de l’interopérabilité à l’aide du partage de surface entre les API graphiques Windows, notamment Direct3D 11, Direct2D, DirectWrite, Direct3D 10 et Direct3D 9Ex.
ms.assetid: 65abf33e-3d15-42ff-99bd-674f24da773e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1032cb1cf9b16280088f00e79e7e59bb7f1510b1
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343614"
---
# <a name="surface-sharing-between-windows-graphics-apis"></a><span data-ttu-id="cc37b-103">Partage de surface entre les API graphiques Windows</span><span class="sxs-lookup"><span data-stu-id="cc37b-103">Surface sharing between Windows graphics APIs</span></span>

<span data-ttu-id="cc37b-104">Cette rubrique fournit une vue d’ensemble technique de l’interopérabilité à l’aide du partage de surface entre les API graphiques Windows, notamment Direct3D 11, Direct2D, DirectWrite, Direct3D 10 et Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="cc37b-104">This topic provides a technical overview of interoperability using surface sharing between Windows graphics APIs, including Direct3D 11, Direct2D, DirectWrite, Direct3D 10, and Direct3D 9Ex.</span></span> <span data-ttu-id="cc37b-105">Si vous avez déjà une connaissance de ces API, ce document peut vous aider à utiliser plusieurs API pour effectuer un rendu sur la même surface dans une application conçue pour les systèmes d’exploitation Windows 7 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cc37b-105">If you already have a working knowledge of these APIs, this paper can help you use multiple APIs to render to the same surface in an application designed for the Windows 7 or Windows Vista operating systems.</span></span> <span data-ttu-id="cc37b-106">Cette rubrique présente également les meilleures pratiques et les pointeurs vers des ressources supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="cc37b-106">This topic also provides best practice guidelines and pointers to additional resources.</span></span>

> [!Note]  
> <span data-ttu-id="cc37b-107">Pour l’interopérabilité de Direct2D et DirectWrite sur le runtime DirectX 11,1, vous pouvez utiliser des [appareils Direct2D et des contextes de périphérique](/windows/desktop/Direct2D/devices-and-device-contexts) pour effectuer un rendu direct sur les périphériques Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="cc37b-107">For Direct2D and DirectWrite interoperability on the DirectX 11.1 runtime, you can use [Direct2D devices and device contexts](/windows/desktop/Direct2D/devices-and-device-contexts) to render directly to Direct3D 11 devices.</span></span>

 

<span data-ttu-id="cc37b-108">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="cc37b-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="cc37b-109">Introduction</span><span class="sxs-lookup"><span data-stu-id="cc37b-109">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="cc37b-110">Vue d’ensemble de l’interopérabilité des API</span><span class="sxs-lookup"><span data-stu-id="cc37b-110">API Interoperability Overview</span></span>](#api-interoperability-overview)
-   [<span data-ttu-id="cc37b-111">Scénarios d’interopérabilité</span><span class="sxs-lookup"><span data-stu-id="cc37b-111">Interoperability Scenarios</span></span>](#interoperability-scenarios)
    -   [<span data-ttu-id="cc37b-112">Partage d’appareils Direct3D 10,1 avec Direct2D</span><span class="sxs-lookup"><span data-stu-id="cc37b-112">Direct3D 10.1 Device Sharing with Direct2D</span></span>](#direct3d-101-device-sharing-with-direct2d)
    -   [<span data-ttu-id="cc37b-113">DXGI 1,1 surfaces partagées synchronisées</span><span class="sxs-lookup"><span data-stu-id="cc37b-113">DXGI 1.1 Synchronized Shared Surfaces</span></span>](#dxgi-11-synchronized-shared-surfaces)
    -   [<span data-ttu-id="cc37b-114">Interopérabilité entre les API Direct3D 9Ex et DXGI</span><span class="sxs-lookup"><span data-stu-id="cc37b-114">Interoperability between Direct3D 9Ex and DXGI based APIs</span></span>](#interoperability-between-direct3d-9ex-and-dxgi-based-apis)
-   [<span data-ttu-id="cc37b-115">Conclusion</span><span class="sxs-lookup"><span data-stu-id="cc37b-115">Conclusion</span></span>](#conclusion)

## <a name="introduction"></a><span data-ttu-id="cc37b-116">Introduction</span><span class="sxs-lookup"><span data-stu-id="cc37b-116">Introduction</span></span>

<span data-ttu-id="cc37b-117">Dans ce document, l’interopérabilité des API Windows Graphics fait référence au partage de la même surface de rendu par différentes API.</span><span class="sxs-lookup"><span data-stu-id="cc37b-117">In this document, Windows graphics API interoperability refers to the sharing of the same rendering surface by different APIs.</span></span> <span data-ttu-id="cc37b-118">Ce type d’interopérabilité permet aux applications de créer des affichages attrayants en tirant parti de plusieurs API graphiques Windows et de faciliter la migration vers de nouvelles technologies en conservant la compatibilité avec les API existantes.</span><span class="sxs-lookup"><span data-stu-id="cc37b-118">This kind of interoperability enables applications to create compelling displays by leveraging multiple Windows graphics APIs, and to ease migration to new technologies by maintaining compatibility with existing APIs.</span></span>

<span data-ttu-id="cc37b-119">Dans Windows 7 (et Windows Vista SP2 avec Windows 7 Interop Pack, Vista 7IP), les API de rendu graphiques sont Direct3D 11, Direct2D, Direct3D 10,1, Direct3D 10,0, Direct3D 9Ex, Direct3D 9c et les API Direct3D antérieures, ainsi que GDI et GDI+.</span><span class="sxs-lookup"><span data-stu-id="cc37b-119">In Windows 7 (and Windows Vista SP2 with Windows 7 Interop Pack, Vista 7IP), the graphics rendering APIs are Direct3D 11, Direct2D, Direct3D 10.1, Direct3D 10.0, Direct3D 9Ex, Direct3D 9c and earlier Direct3D APIs, as well GDI and GDI+.</span></span> <span data-ttu-id="cc37b-120">WIC (Windows Imaging Component) et DirectWrite sont des technologies associées au traitement des images, et Direct2D effectue le rendu du texte.</span><span class="sxs-lookup"><span data-stu-id="cc37b-120">Windows Imaging Component (WIC) and DirectWrite are related technologies for image processing, and Direct2D performs text rendering.</span></span> <span data-ttu-id="cc37b-121">L’API d’accélération vidéo DirectX (DXVA), basée sur Direct3D 9c et Direct3D 9Ex, est utilisée pour le traitement vidéo.</span><span class="sxs-lookup"><span data-stu-id="cc37b-121">DirectX Video Acceleration API (DXVA), based on Direct3D 9c and Direct3D 9Ex, is used for video processing.</span></span>

<span data-ttu-id="cc37b-122">À mesure que les API graphiques Windows évoluent vers la base Direct3D, Microsoft investit plus d’efforts pour garantir l’interopérabilité entre les API.</span><span class="sxs-lookup"><span data-stu-id="cc37b-122">As Windows graphics APIs evolve towards being Direct3D-based, Microsoft is investing more effort in ensuring interoperability across APIs.</span></span> <span data-ttu-id="cc37b-123">Les API Direct3D récemment développées et les API de niveau supérieur basées sur les API Direct3D prennent également en charge les cas nécessaires pour assurer la compatibilité avec les anciennes API.</span><span class="sxs-lookup"><span data-stu-id="cc37b-123">Newly developed Direct3D APIs and higher level APIs based on Direct3D APIs also provide support where needed for bridging compatibility with older APIs.</span></span> <span data-ttu-id="cc37b-124">Pour illustrer cela, les applications Direct2D peuvent utiliser Direct3D 10,1 en partageant un appareil Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="cc37b-124">To illustrate, Direct2D applications can use Direct3D 10.1 by sharing a Direct3D 10.1 device.</span></span> <span data-ttu-id="cc37b-125">En outre, les API Direct3D 11, Direct2D et Direct3D 10,1 peuvent tous tirer parti de DirectX Graphics infrastructure (DXGI) 1,1, qui permet des surfaces partagées synchronisées qui prennent entièrement en charge l’interopérabilité entre ces API.</span><span class="sxs-lookup"><span data-stu-id="cc37b-125">Also, Direct3D 11, Direct2D, and Direct3D 10.1 APIs can all take advantage of DirectX Graphics Infrastructure (DXGI) 1.1, which enables synchronized shared surfaces that fully support interoperability among these APIs.</span></span> <span data-ttu-id="cc37b-126">Les API DXGI 1,1 interagissent avec GDI et avec GDI+ par Association, en obtenant le contexte de périphérique GDI à partir d’une surface DXGI 1,1.</span><span class="sxs-lookup"><span data-stu-id="cc37b-126">DXGI 1.1-based APIs interoperate with GDI, and with GDI+ by association, by obtaining the GDI device context from a DXGI 1.1 surface.</span></span> <span data-ttu-id="cc37b-127">Pour plus d’informations, consultez la documentation relative à l’interopérabilité DXGI et GDI disponible sur MSDN.</span><span class="sxs-lookup"><span data-stu-id="cc37b-127">For more information, see the DXGI and GDI interoperability documentation available on MSDN.</span></span>

<span data-ttu-id="cc37b-128">Le partage de surface non synchronisé est pris en charge par le runtime Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="cc37b-128">Unsynchronized surface sharing is supported by the Direct3D 9Ex runtime.</span></span> <span data-ttu-id="cc37b-129">Les applications vidéo DXVA peuvent utiliser l’application auxiliaire Direct3D 9Ex et DXGI Interoperability pour l’interopérabilité DXVA basée sur Direct3D 9Ex avec Direct3D 11 pour le nuanceur de calcul, ou peuvent interagir avec Direct2D pour les contrôles 2D ou le rendu de texte.</span><span class="sxs-lookup"><span data-stu-id="cc37b-129">DXVA-based video applications can use the Direct3D 9Ex and DXGI interoperability helper for Direct3D 9Ex-based DXVA interoperability with Direct3D 11 for compute shader, or can interoperate with Direct2D for 2D controls or text rendering.</span></span> <span data-ttu-id="cc37b-130">WIC et DirectWrite interagissent également avec GDI, Direct2D et par Association, d’autres API Direct3D.</span><span class="sxs-lookup"><span data-stu-id="cc37b-130">WIC and DirectWrite also interoperate with GDI, Direct2D, and by association, other Direct3D APIs.</span></span>

<span data-ttu-id="cc37b-131">Direct3D 10,0, Direct3D 9c et les runtimes Direct3D plus anciens ne prennent pas en charge les surfaces partagées.</span><span class="sxs-lookup"><span data-stu-id="cc37b-131">Direct3D 10.0, Direct3D 9c, and older Direct3D runtimes do not support shared surfaces.</span></span> <span data-ttu-id="cc37b-132">Les copies de mémoire système seront toujours utilisées pour l’interopérabilité avec les API GDI ou DXGI.</span><span class="sxs-lookup"><span data-stu-id="cc37b-132">System memory copies will continue to be used for interoperability with GDI or DXGI-based APIs.</span></span>

<span data-ttu-id="cc37b-133">Notez que les scénarios d’interopérabilité dans ce document font référence à plusieurs API graphiques qui sont rendues sur une surface de rendu partagée, plutôt que dans la même fenêtre d’application.</span><span class="sxs-lookup"><span data-stu-id="cc37b-133">Note that the interoperability scenarios within this document refer to multiple graphics APIs rendering to a shared rendering surface, rather than to the same application window.</span></span> <span data-ttu-id="cc37b-134">La synchronisation pour des API distinctes ciblant des surfaces différentes qui sont ensuite réparties dans la même fenêtre n’entre pas dans le cadre de ce document.</span><span class="sxs-lookup"><span data-stu-id="cc37b-134">Synchronization for separate APIs targeting different surfaces that are then composited onto the same window is outside the scope of this paper.</span></span>

## <a name="api-interoperability-overview"></a><span data-ttu-id="cc37b-135">Vue d’ensemble de l’interopérabilité des API</span><span class="sxs-lookup"><span data-stu-id="cc37b-135">API Interoperability Overview</span></span>

<span data-ttu-id="cc37b-136">L’interopérabilité du partage de surface des API graphiques Windows peut être décrite en termes de scénarios API-API et de fonctionnalités d’interopérabilité correspondantes.</span><span class="sxs-lookup"><span data-stu-id="cc37b-136">Surface sharing interoperability of Windows graphics APIs can be described in terms of API-to-API scenarios and the corresponding interoperability functionality.</span></span> <span data-ttu-id="cc37b-137">À compter de Windows 7 et de Windows Vista SP2 avec 7IP, les nouvelles API et les runtimes associés incluent Direct2D et les technologies associées : Direct3D 11 et DXGI 1,1.</span><span class="sxs-lookup"><span data-stu-id="cc37b-137">As of Windows 7 and beginning with Windows Vista SP2 with 7IP, new APIs and associated runtimes include Direct2D and related technologies: Direct3D 11 and DXGI 1.1.</span></span> <span data-ttu-id="cc37b-138">Les performances GDI ont également été améliorées dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cc37b-138">GDI performance was also improved in Windows 7.</span></span> <span data-ttu-id="cc37b-139">Direct3D 10,1 a été introduit dans Windows Vista SP1.</span><span class="sxs-lookup"><span data-stu-id="cc37b-139">Direct3D 10.1 was introduced in Windows Vista SP1.</span></span> <span data-ttu-id="cc37b-140">Le diagramme suivant illustre la prise en charge de l’interopérabilité entre les API.</span><span class="sxs-lookup"><span data-stu-id="cc37b-140">The following diagram shows the interoperability support between APIs.</span></span>

![diagramme de prise en charge de l’interopérabilité entre les API graphiques Windows](images/surface-sharing-interoperability.png)

<span data-ttu-id="cc37b-142">Dans ce diagramme, les flèches indiquent les scénarios d’interopérabilité dans lesquels la même surface peut être accessible par les API connectées.</span><span class="sxs-lookup"><span data-stu-id="cc37b-142">In this diagram, arrows show interoperability scenarios in which the same surface can be accessible by the connected APIs.</span></span> <span data-ttu-id="cc37b-143">Les flèches bleues indiquent les mécanismes d’interopérabilité introduits dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cc37b-143">Blue arrows indicate interoperability mechanisms introduced in Windows Vista.</span></span> <span data-ttu-id="cc37b-144">Les flèches vertes indiquent la prise en charge de l’interopérabilité pour les nouvelles API ou les améliorations qui aident les API plus anciennes à interagir avec les API plus récentes.</span><span class="sxs-lookup"><span data-stu-id="cc37b-144">Green arrows indicate interoperability support for new APIs or improvements that help older APIs to interoperate with newer APIs.</span></span> <span data-ttu-id="cc37b-145">Par exemple, les flèches vertes représentent le partage d’appareil, la prise en charge de la surface partagée, la prise en charge de la synchronisation Direct3D 9Ex/DXGI et l’obtention d’un contexte de périphérique GDI à partir d’une surface compatible.</span><span class="sxs-lookup"><span data-stu-id="cc37b-145">For example, green arrows represent device sharing, synchronized shared surface support, Direct3D 9Ex/DXGI synchronization helper, and obtaining a GDI device context from a compatible surface.</span></span>

## <a name="interoperability-scenarios"></a><span data-ttu-id="cc37b-146">Scénarios d’interopérabilité</span><span class="sxs-lookup"><span data-stu-id="cc37b-146">Interoperability Scenarios</span></span>

<span data-ttu-id="cc37b-147">À compter de Windows 7 et Windows Vista 7IP, les offres standard des API graphiques Windows prennent en charge plusieurs API de rendu sur la même surface DXGI 1,1.</span><span class="sxs-lookup"><span data-stu-id="cc37b-147">As of Windows 7 and Windows Vista 7IP, mainstream offerings from Windows graphics APIs support multiple APIs rendering to the same DXGI 1.1 surface.</span></span>

<span data-ttu-id="cc37b-148">**Direct3D 11, Direct3D 10,1, Direct2D : interopérabilité les unes avec les autres**</span><span class="sxs-lookup"><span data-stu-id="cc37b-148">**Direct3D 11, Direct3D 10.1, Direct2D — Interoperability with each other**</span></span>

<span data-ttu-id="cc37b-149">Les API Direct3D 11, Direct3D 10,1 et Direct2D (et les API associées telles que DirectWrite et WIC) peuvent interagir entre elles à l’aide des surfaces partagées de partage d’appareil ou de partage Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="cc37b-149">Direct3D 11, Direct3D 10.1 and Direct2D APIs (and its related APIs such as DirectWrite and WIC) can interoperate with each other using either Direct3D 10.1 device sharing or synchronized shared surfaces.</span></span>

### <a name="direct3d-101-device-sharing-with-direct2d"></a><span data-ttu-id="cc37b-150">Partage d’appareils Direct3D 10,1 avec Direct2D</span><span class="sxs-lookup"><span data-stu-id="cc37b-150">Direct3D 10.1 Device Sharing with Direct2D</span></span>

<span data-ttu-id="cc37b-151">Le partage d’appareils entre Direct2D et Direct3D 10,1 permet à une application d’utiliser les deux API pour effectuer un rendu fluide et efficace sur la même surface DXGI 1,1, à l’aide du même objet appareil Direct3D sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="cc37b-151">Device sharing between Direct2D and Direct3D 10.1 allows an application to use both APIs to seamlessly and efficiently render onto the same DXGI 1.1 surface, using the same underlying Direct3D device object.</span></span> <span data-ttu-id="cc37b-152">Direct2D offre la possibilité d’appeler des API Direct2D à l’aide d’un périphérique Direct3D 10,1 existant, en tirant parti du fait que Direct2D repose sur les runtimes Direct3D 10,1 et DXGI 1,1.</span><span class="sxs-lookup"><span data-stu-id="cc37b-152">Direct2D provides the ability to call Direct2D APIs using an existing Direct3D 10.1 device, leveraging the fact that Direct2D is built on top of Direct3D 10.1 and DXGI 1.1 runtimes.</span></span> <span data-ttu-id="cc37b-153">Les extraits de code suivants montrent comment Direct2D obtient la cible de rendu de l’appareil Direct3D 10,1 à partir d’une surface DXGI 1,1 associée à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cc37b-153">The following code snippets illustrate how Direct2D obtains the Direct3D 10.1 device render target from a DXGI 1.1 surface associated with the device.</span></span> <span data-ttu-id="cc37b-154">La cible de rendu de l’appareil Direct3D 10,1 peut exécuter des appels de dessin Direct2D entre les API BeginDraw et EndDraw.</span><span class="sxs-lookup"><span data-stu-id="cc37b-154">The Direct3D 10.1 device render target can execute Direct2D drawing calls between BeginDraw and EndDraw APIs.</span></span>


```C++
// Direct3D 10.1 Device and Swapchain creation
HRESULT hr = D3D10CreateDeviceandSwapChain1(
                pAdapter,
                DriverType,
                Software,
                D3D10_CREATE_DEVICE_BGRA_SUPPORT,
                featureLevel,
                D3D10_1_SDK_VERSION,
                pSwapChainDesc,
                &pSwapChain,
                &pDevice
                );

hr = pSwapChain->GetBuffer(
        0,
        __uuidof(IDXGISurface),
        (void **)&pDXGIBackBuffer
        ));

// Direct3D 10.1 API rendering calls
...

hr = D2D1CreateFactory(
        D2D1_FACTORY_TYPE_SINGLE_THREADED,
        &m_spD2DFactory
        ));

pD2DFactory->CreateDxgiSurfaceRenderTarget(
        pDXGIBackBuffer,
        &renderTargetProperties,
        &pD2DBackBufferRenderTarget
        ));
...

pD2DBackBufferRenderTarget->BeginDraw();
//Direct2D API rendering calls
...

pD2DBackBufferRenderTarget->EndDraw();

pSwapChain->Present(0, 0);
```



<span data-ttu-id="cc37b-155">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="cc37b-155">**Remarks**</span></span>

-   <span data-ttu-id="cc37b-156">L’appareil Direct3D 10,1 associé doit prendre en charge le format BGRA.</span><span class="sxs-lookup"><span data-stu-id="cc37b-156">The associated Direct3D 10.1 device must support BGRA format.</span></span> <span data-ttu-id="cc37b-157">Cet appareil a été créé en appelant D3D10CreateDevice1 avec le paramètre D3D10 \_ Create \_ Device \_ BGRA \_ support.</span><span class="sxs-lookup"><span data-stu-id="cc37b-157">That device was created by calling D3D10CreateDevice1 with parameter D3D10\_CREATE\_DEVICE\_BGRA\_SUPPORT.</span></span> <span data-ttu-id="cc37b-158">Le format BGRA est pris en charge à partir du niveau de fonctionnalité 9,1 de Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="cc37b-158">BGRA format is supported starting with Direct3D 10 feature level 9.1.</span></span>
-   <span data-ttu-id="cc37b-159">L’application ne doit pas créer plusieurs ID2D1RenderTargets qui s’associent au même appareil Direct3D 10.1.</span><span class="sxs-lookup"><span data-stu-id="cc37b-159">The application should not create multiple ID2D1RenderTargets associating to the same Direct3D10.1 device.</span></span>
-   <span data-ttu-id="cc37b-160">Pour des performances optimales, gardez à tout moment au moins une ressource, comme des textures ou des surfaces associées à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cc37b-160">For optimal performance, keep at least one resource around at all times, such as textures or surfaces associated with the device.</span></span>

<span data-ttu-id="cc37b-161">Le partage d’appareils est adapté à l’utilisation monothread et à thread unique d’un appareil de rendu partagé par les API de rendu Direct3D 10,1 et Direct2D.</span><span class="sxs-lookup"><span data-stu-id="cc37b-161">Device sharing is suitable for in-process, single-threaded usage of one rendering device shared by both Direct3D 10.1 and Direct2D rendering APIs.</span></span> <span data-ttu-id="cc37b-162">Les surfaces partagées synchronisées permettent l’utilisation multithread, in-process et out-of-process de plusieurs appareils de rendu utilisés par les API Direct3D 10,1, Direct2D et Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="cc37b-162">Synchronized shared surfaces enable multi-threaded, in-process and out-of-process usage of multiple rendering devices used by Direct3D 10.1, Direct2D and Direct3D 11 APIs.</span></span>

<span data-ttu-id="cc37b-163">Une autre méthode d’interopérabilité Direct3D 10,1 et Direct2D consiste à utiliser ID3D1RenderTarget :: CreateSharedBitmap, qui crée un objet ID2D1Bitmap à partir de IDXGISurface.</span><span class="sxs-lookup"><span data-stu-id="cc37b-163">Another method of Direct3D 10.1 and Direct2D interoperability is by using ID3D1RenderTarget::CreateSharedBitmap, which creates an ID2D1Bitmap object from IDXGISurface.</span></span> <span data-ttu-id="cc37b-164">Vous pouvez écrire une scène Direct3D 10.1 dans le bitmap et la restituer avec Direct2D.</span><span class="sxs-lookup"><span data-stu-id="cc37b-164">You can write a Direct3D10.1 scene to the bitmap and render it with Direct2D.</span></span> <span data-ttu-id="cc37b-165">Pour plus d’informations, consultez la [méthode ID2D1RenderTarget :: CreateSharedBitmap](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap).</span><span class="sxs-lookup"><span data-stu-id="cc37b-165">For more information, see [ID2D1RenderTarget::CreateSharedBitmap Method](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap).</span></span>

### <a name="direct2d-software-rasterization"></a><span data-ttu-id="cc37b-166">Pixellisation de logiciels Direct2D</span><span class="sxs-lookup"><span data-stu-id="cc37b-166">Direct2D Software Rasterization</span></span>

<span data-ttu-id="cc37b-167">Le partage d’appareils avec Direct3D 10,1 n’est pas pris en charge lors de l’utilisation du convertisseur de logiciel Direct2D, par exemple, en spécifiant l' \_ \_ utilisation de la cible de rendu d2d1 \_ \_ force \_ \_ le rendu logiciel dans l’utilisation de la cible de rendu d2d1 \_ lors de \_ \_ la création d’une cible de rendu Direct2D.</span><span class="sxs-lookup"><span data-stu-id="cc37b-167">Device sharing with Direct3D 10.1 is not supported when using the Direct2D software renderer, for example, by specifying D2D1\_RENDER\_TARGET\_USAGE\_FORCE\_SOFTWARE\_RENDERING in D2D1\_RENDER\_TARGET\_USAGE when creating a Direct2D render target.</span></span>

<span data-ttu-id="cc37b-168">Direct2D peut utiliser le rastériseur logiciel WARP10 pour partager des appareils avec Direct3D 10 ou Direct3D 11, mais les performances diminuent considérablement.</span><span class="sxs-lookup"><span data-stu-id="cc37b-168">Direct2D can use the WARP10 software rasterizer to share device with Direct3D 10 or Direct3D 11, but the performance declines significantly.</span></span>

### <a name="dxgi-11-synchronized-shared-surfaces"></a><span data-ttu-id="cc37b-169">DXGI 1,1 surfaces partagées synchronisées</span><span class="sxs-lookup"><span data-stu-id="cc37b-169">DXGI 1.1 Synchronized Shared Surfaces</span></span>

<span data-ttu-id="cc37b-170">Direct3D 11, Direct3D 10,1 et les API Direct2D utilisent tous DXGI 1,1, qui fournit les fonctionnalités permettant de synchroniser la lecture et l’écriture dans la même surface de mémoire vidéo (DXGISurface1) par deux ou plusieurs périphériques Direct3D.</span><span class="sxs-lookup"><span data-stu-id="cc37b-170">Direct3D 11, Direct3D 10.1 and Direct2D APIs all use DXGI 1.1, which provides the functionality to synchronize reading from and writing to the same video memory surface (DXGISurface1) by two or more Direct3D devices.</span></span> <span data-ttu-id="cc37b-171">Les appareils de rendu utilisant des surfaces partagées synchronisées peuvent être des appareils Direct3D 10,1 ou Direct3D 11, chacun s’exécutant dans le même processus ou des processus interactifs.</span><span class="sxs-lookup"><span data-stu-id="cc37b-171">The rendering devices using synchronized shared surfaces can be Direct3D 10.1 or Direct3D 11 devices, each running in the same process or cross-processes.</span></span>

<span data-ttu-id="cc37b-172">Les applications peuvent utiliser des surfaces partagées synchronisées pour interagir entre n’importe quel appareil DXGI 1,1, tel que Direct3D 11 et Direct3D 10,1, ou entre Direct3D 11 et Direct2D, en obtenant l’appareil Direct3D 10,1 à partir de l’objet cible de rendu Direct2D.</span><span class="sxs-lookup"><span data-stu-id="cc37b-172">Applications can use synchronized shared surfaces to interoperate between any DXGI 1.1-based devices, such as Direct3D 11 and Direct3D 10.1, or between Direct3D 11 and Direct2D, by obtaining the Direct3D 10.1 device from Direct2D render target object.</span></span>

<span data-ttu-id="cc37b-173">Dans les API Direct3D 10,1 et versions ultérieures, pour utiliser DXGI 1,1, assurez-vous que le périphérique Direct3D est créé à l’aide d’un objet d’adaptateur DXGI 1,1, qui est énuméré à partir de l’objet de fabrique DXGI 1,1.</span><span class="sxs-lookup"><span data-stu-id="cc37b-173">In Direct3D 10.1 and later APIs, to use DXGI 1.1, ensure that the Direct3D device is created using a DXGI 1.1 adapter object, which is enumerated from the DXGI 1.1 factory object.</span></span> <span data-ttu-id="cc37b-174">Appelez CreateDXGIFactory1 pour créer l’objet IDXGIFactory1, et EnumAdapters1 pour énumérer l’objet IDXGIAdapter1.</span><span class="sxs-lookup"><span data-stu-id="cc37b-174">Call CreateDXGIFactory1 to create the IDXGIFactory1 object, and EnumAdapters1 to enumerate the IDXGIAdapter1 object.</span></span> <span data-ttu-id="cc37b-175">L’objet IDXGIAdapter1 doit être passé dans le cadre de l’appel D3D10CreateDevice ou D3D10CreateDeviceAndSwapChain.</span><span class="sxs-lookup"><span data-stu-id="cc37b-175">The IDXGIAdapter1 object needs to be passed in as part of D3D10CreateDevice or D3D10CreateDeviceAndSwapChain call.</span></span> <span data-ttu-id="cc37b-176">Pour plus d’informations sur les API DXGI 1,1, consultez le [Guide de programmation pour dxgi](https://msdn.microsoft.com/library/ee418147(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="cc37b-176">For more information on DXGI 1.1 APIs, please refer to the [Programming Guide for DXGI](https://msdn.microsoft.com/library/ee418147(VS.85).aspx).</span></span>

### <a name="apis"></a><span data-ttu-id="cc37b-177">API</span><span class="sxs-lookup"><span data-stu-id="cc37b-177">APIs</span></span>

<span data-ttu-id="cc37b-178">**D3D10 \_ ressources \_ \_ partagées divers \_ KEYEDMUTEX**</span><span class="sxs-lookup"><span data-stu-id="cc37b-178">**D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX**</span></span>  
<span data-ttu-id="cc37b-179">Lors de la création de la ressource partagée synchronisée, définissez D3D10 \_ Resource \_ misc \_ Shared \_ KEYEDMUTEX dans l' \_ indicateur misc des ressources D3D10 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cc37b-179">When creating the synchronized shared resource, set D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX in D3D10\_RESOURCE\_MISC\_FLAG.</span></span>  


```C++
typedef enum D3D10_RESOURCE_MISC_FLAG {
    D3D10_RESOURCE_MISC_GENERATE_MIPS      = 0x1L,
    D3D10_RESOURCE_MISC_SHARED             = 0x2L,
    D3D10_RESOURCE_MISC_TEXTURECUBE        = 0x4L,
    D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX  = 0x10L,
    D3D10_RESOURCE_MISC_GDI_COMPATIBLE     = 0x20L,
}   D3D10_RESOURCE_MISC_FLAG;
```



<span data-ttu-id="cc37b-180">**D3D10 \_ ressources \_ \_ partagées divers \_ KEYEDMUTEX**</span><span class="sxs-lookup"><span data-stu-id="cc37b-180">**D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX**</span></span>  
<span data-ttu-id="cc37b-181">Permet à la ressource créée d’être synchronisée à l’aide des API IDXGIKeyedMutex :: AcquireSync et ReleaseSync.</span><span class="sxs-lookup"><span data-stu-id="cc37b-181">Enables the resource created to be synchronized using the IDXGIKeyedMutex::AcquireSync and ReleaseSync APIs.</span></span> <span data-ttu-id="cc37b-182">Les API de création de ressource Direct3D 10,1 suivantes qui prennent toutes \_ un \_ \_ paramètre d’indicateur de ressource D3D10 ont été étendues pour prendre en charge le nouvel indicateur.</span><span class="sxs-lookup"><span data-stu-id="cc37b-182">The following resource creation Direct3D 10.1 APIs that all take a D3D10\_RESOURCE\_MISC\_FLAG parameter have been extended to support the new flag.</span></span>  

-   <span data-ttu-id="cc37b-183">ID3D10Device1::CreateTexture1D</span><span class="sxs-lookup"><span data-stu-id="cc37b-183">ID3D10Device1::CreateTexture1D</span></span>
-   <span data-ttu-id="cc37b-184">ID3D10Device1::CreateTexture2D</span><span class="sxs-lookup"><span data-stu-id="cc37b-184">ID3D10Device1::CreateTexture2D</span></span>
-   <span data-ttu-id="cc37b-185">ID3D10Device1::CreateTexture3D</span><span class="sxs-lookup"><span data-stu-id="cc37b-185">ID3D10Device1::CreateTexture3D</span></span>
-   <span data-ttu-id="cc37b-186">ID3D10Device1 :: CreateBuffer</span><span class="sxs-lookup"><span data-stu-id="cc37b-186">ID3D10Device1::CreateBuffer</span></span>

  
<span data-ttu-id="cc37b-187">Si l’une des fonctions répertoriées est appelée avec l' \_ indicateur de KEYEDMUTEX partagé divers de la ressource D3D10, \_ \_ \_ l’interface retournée peut être interrogée pour une interface IDXGIKeyedMutex, qui implémente les API AcquireSync et ReleaseSync pour synchroniser l’accès à la surface.</span><span class="sxs-lookup"><span data-stu-id="cc37b-187">If any of the listed functions are called with the D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX flag set, the interface returned can be queried for an IDXGIKeyedMutex interface, which implements AcquireSync and ReleaseSync APIs to synchronize access to the surface.</span></span> <span data-ttu-id="cc37b-188">L’appareil qui crée la surface et tout autre appareil ouvrant l’aire (à l’aide de OpenSharedResource) est requis pour appeler IDXGIKeyedMutex :: AcquireSync avant toute commande de rendu sur la surface, et IDXGIKeyedMutex :: ReleaseSync une fois le rendu terminé.</span><span class="sxs-lookup"><span data-stu-id="cc37b-188">The device creating the surface and any other device opening the surface (using OpenSharedResource) is required to call IDXGIKeyedMutex::AcquireSync before any rendering commands to the surface, and IDXGIKeyedMutex::ReleaseSync when it is done rendering.</span></span>  
<span data-ttu-id="cc37b-189">Les appareils WARP et REF ne prennent pas en charge les ressources partagées.</span><span class="sxs-lookup"><span data-stu-id="cc37b-189">WARP and REF devices do not support shared resources.</span></span> <span data-ttu-id="cc37b-190">Si vous tentez de créer une ressource avec cet indicateur sur un appareil WARP ou REF, la méthode Create renverra un \_ code d’erreur E OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="cc37b-190">Attempting to create a resource with this flag on either a WARP or REF device will cause the create method to return an E\_OUTOFMEMORY error code.</span></span>  
<span data-ttu-id="cc37b-191">**INTERFACE IDXGIKEYEDMUTEX**</span><span class="sxs-lookup"><span data-stu-id="cc37b-191">**IDXGIKEYEDMUTEX INTERFACE**</span></span>  
<span data-ttu-id="cc37b-192">Une nouvelle interface dans DXGI 1,1, IDXGIKeyedMutex, représente un mutex à clé qui permet un accès exclusif à une ressource partagée qui est utilisée par plusieurs appareils.</span><span class="sxs-lookup"><span data-stu-id="cc37b-192">A new interface in DXGI 1.1, IDXGIKeyedMutex, represents a keyed mutex, which allows exclusive access to a shared resource that is used by multiple devices.</span></span> <span data-ttu-id="cc37b-193">Pour obtenir une documentation de référence sur cette interface et ses deux méthodes, AcquireSync et ReleaseSync, consultez [IDXGIKeyedMutex](https://msdn.microsoft.com/library/ee421920(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="cc37b-193">For reference documentation about this interface and its two methods, AcquireSync and ReleaseSync, see [IDXGIKeyedMutex](https://msdn.microsoft.com/library/ee421920(VS.85).aspx).</span></span>  
</dl>

### <a name="sample-synchronized-surface-sharing-between-two-direct3d-101-devices"></a><span data-ttu-id="cc37b-194">Exemple : partage de surface synchronisé entre deux appareils Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="cc37b-194">Sample: Synchronized Surface Sharing Between two Direct3D 10.1 Devices</span></span>

<span data-ttu-id="cc37b-195">L’exemple ci-dessous illustre le partage d’une surface entre deux périphériques Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="cc37b-195">The example below illustrates sharing a surface between two Direct3D 10.1 devices.</span></span> <span data-ttu-id="cc37b-196">La surface partagée synchronisée est créée par un appareil Direct3D 10.1.</span><span class="sxs-lookup"><span data-stu-id="cc37b-196">The synchronized shared surface is created by a Direct3D10.1 device.</span></span>


```C++
// Create Sync Shared Surface using Direct3D10.1 Device 1.
D3D10_TEXTURE2D_DESC desc;
ZeroMemory( &desc, sizeof(desc) );
desc.Width = width;
desc.Height = height;
desc.MipLevels = 1;
desc.ArraySize = 1;
// must match swapchain format in order to CopySubresourceRegion.
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DEFAULT;
// creates 2D texture as a Synchronized Shared Surface.
desc.MiscFlags = D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX;
desc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;
ID3D10Texture2D* g_pShared = NULL;
g_pd3dDevice1->CreateTexture2D( &desc, NULL, &g_pShared );

// QI IDXGIResource interface to synchronized shared surface.
IDXGIResource* pDXGIResource = NULL;
g_pShared->QueryInterface(__uuidof(IDXGIResource), (LPVOID*) &pDXGIResource);

// obtain handle to IDXGIResource object.
pDXGIResource->GetSharedHandle(&g_hsharedHandle);
pDXGIResource->Release();
if ( !g_hsharedHandle )
    return E_FAIL;

// QI IDXGIKeyedMutex interface of synchronized shared surface's resource handle.
hr = g_pShared->QueryInterface( __uuidof(IDXGIKeyedMutex),
    (LPVOID*)&g_pDXGIKeyedMutex_dev1 );
If ( FAILED( hr ) || ( g_pDXGIKeyedMutex_dev1 == NULL ) )
    return E_FAIL;
```



<span data-ttu-id="cc37b-197">Le même appareil Direct3D 10.1 peut obtenir la surface partagée synchronisée pour le rendu en appelant AcquireSync, puis libérer la surface pour le rendu de l’autre appareil en appelant ReleaseSync.</span><span class="sxs-lookup"><span data-stu-id="cc37b-197">The same Direct3D10.1 device can obtain the synchronized shared surface for rendering by calling AcquireSync, then releasing the surface for the other device's rendering by calling ReleaseSync.</span></span> <span data-ttu-id="cc37b-198">Lorsqu’il ne partage pas la surface partagée synchronisée avec un autre périphérique Direct3D, le créateur peut obtenir et libérer la surface partagée synchronisée (pour démarrer et terminer le rendu) en acquérant et en libérant à l’aide de la même valeur de clé.</span><span class="sxs-lookup"><span data-stu-id="cc37b-198">When not sharing the synchronized shared surface with any other Direct3D device, the creator can obtain and release the synchronized shared surface (to start and end rendering) by acquiring and release using the same key value.</span></span>


```C++
// Obtain handle to Sync Shared Surface created by Direct3D10.1 Device 1.
hr = g_pd3dDevice2->OpenSharedResource( g_hsharedHandle,__uuidof(ID3D10Texture2D),
                                        (LPVOID*) &g_pdev2Shared);
if (FAILED (hr))
    return hr;
hr = g_pdev2Shared->QueryInterface( __uuidof(IDXGIKeyedMutex),
                                    (LPVOID*) &g_pDXGIKeyedMutex_dev2);
if( FAILED( hr ) || ( g_pDXGIKeyedMutex_dev2 == NULL ) )
    return E_FAIL;

// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 2.
UINT acqKey = 1;
UINT relKey = 0;
DWORD timeOut = 5;
DWORD result = g_pDXGIKeyedMutex_dev2->AcquireSync(acqKey, timeOut);
if ( result == WAIT_OBJECT_0 )
    // Rendering calls using Device 2.
else
    // Handle unable to acquire shared surface error.
result = g_pDXGIKeyedMutex_dev2->ReleaseSync(relKey));
if (result == WAIT_OBJECT_0)
    return S_OK;
```



<span data-ttu-id="cc37b-199">Le deuxième appareil Direct3D 10.1 peut obtenir la surface partagée synchronisée pour le rendu en appelant AcquireSync, puis libérer la surface pour le rendu du premier appareil en appelant ReleaseSync.</span><span class="sxs-lookup"><span data-stu-id="cc37b-199">The second Direct3D10.1 device can obtain the synchronized shared surface for rendering by calling AcquireSync, then releasing the surface for the first device's rendering by calling ReleaseSync.</span></span> <span data-ttu-id="cc37b-200">Notez que l’appareil 2 est en mesure d’acquérir la surface partagée synchronisée à l’aide de la même valeur de clé que celle spécifiée dans l’appel ReleaseSync par l’appareil 1.</span><span class="sxs-lookup"><span data-stu-id="cc37b-200">Note that device 2 is able to acquire the synchronized shared surface using the same key value as the one specified in the ReleaseSync call by device 1.</span></span>


```C++
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 1.
UINT acqKey = 0;
UINT relKey = 1;
DWORD timeOut = 5;
DWORD result = g_pDXGIKeyedMutex_dev1->AcquireSync(acqKey, timeOut);
if (result == WAIT_OBJECT_0)
    // Rendering calls using Device 1.
else
    // Handle unable to acquire shared surface error.
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(relKey));
if ( result == WAIT_OBJECT_0 )
    return S_OK;
```



<span data-ttu-id="cc37b-201">Les appareils supplémentaires qui partagent la même surface peuvent avoir l’acquisition et la libération de la surface à l’aide de clés supplémentaires, comme indiqué dans les appels suivants.</span><span class="sxs-lookup"><span data-stu-id="cc37b-201">Additional devices sharing the same surface can take turns acquiring and releasing the surface by using additional keys, as shown in the following calls.</span></span>


```C++
// Within Device 1's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 1
result = g_pDXGIKeyedMutex_dev1->AcquireSync(0, timeOut);
// Rendering calls using Device 1
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(1);
...
////////////////////////////////////////////////////////////////////////////
// Within Device 2's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 2
result = g_pDXGIKeyedMutex_dev2->AcquireSync(1, timeOut);
// Rendering calls using Device 2
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(2);

////////////////////////////////////////////////////////////////////////////
// Within Device 3's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 3
result = g_pDXGIKeyedMutex_dev1->AcquireSync(2, timeOut);
// Rendering calls using Device 3
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(0);
...
```



<span data-ttu-id="cc37b-202">Notez qu’une application réelle peut toujours être rendue sur une surface intermédiaire qui est ensuite copiée dans la surface partagée pour empêcher tout appareil en attente sur un autre appareil partageant l’aire.</span><span class="sxs-lookup"><span data-stu-id="cc37b-202">Note that a real-world application might always render to an intermediate surface that is then copied into the shared surface to prevent any one device waiting on another device that shares the surface.</span></span>

### <a name="using-synchronized-shared-surfaces-with-direct2d-and-direct3d-11"></a><span data-ttu-id="cc37b-203">Utilisation de surfaces partagées synchronisées avec Direct2D et Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="cc37b-203">Using Synchronized Shared Surfaces with Direct2D and Direct3D 11</span></span>

<span data-ttu-id="cc37b-204">De même, pour le partage entre les API Direct3D 11 et Direct3D 10,1, une surface partagée synchronisée peut être créée à partir d’un périphérique d’API et partagée avec les autres périphériques d’API, in ou out of process.</span><span class="sxs-lookup"><span data-stu-id="cc37b-204">Similarly, for sharing between Direct3D 11 and Direct3D 10.1 APIs, a synchronized shared surface can be created from either API device and shared with the other API device(s), in or out of process.</span></span>

<span data-ttu-id="cc37b-205">Les applications qui utilisent Direct2D peuvent partager un appareil Direct3D 10,1 et utiliser une surface partagée synchronisée pour interagir avec Direct3D 11 ou d’autres périphériques Direct3D 10,1, qu’ils appartiennent au même processus ou à des processus différents.</span><span class="sxs-lookup"><span data-stu-id="cc37b-205">Applications that use Direct2D can share a Direct3D 10.1 device and use a synchronized shared surface to interoperate with Direct3D 11 or other Direct3D 10.1 devices, whether they belong to the same process or different processes.</span></span> <span data-ttu-id="cc37b-206">Toutefois, pour les applications à un seul thread, le partage d’appareils est la méthode d’interopérabilité la plus performante et la plus efficace entre Direct2D et Direct3D 10 ou Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="cc37b-206">However, for single-process, single-thread applications, device sharing is the most high-performance and efficient method of interoperability between Direct2D and either Direct3D 10 or Direct3D 11.</span></span>

### <a name="software-rasterizer"></a><span data-ttu-id="cc37b-207">Rastériseur logiciel</span><span class="sxs-lookup"><span data-stu-id="cc37b-207">Software Rasterizer</span></span>

<span data-ttu-id="cc37b-208">Les surfaces partagées synchronisées ne sont pas prises en charge lorsque les applications utilisent les rastériseurs de logiciel Direct3D ou Direct2D, y compris le rastériseur de référence et la déformation, au lieu d’utiliser l’accélération matérielle graphique.</span><span class="sxs-lookup"><span data-stu-id="cc37b-208">Synchronized shared surfaces are not supported when applications use the Direct3D or Direct2D software rasterizers, including the reference rasterizer and WARP, instead of using graphics hardware acceleration.</span></span>

### <a name="interoperability-between-direct3d-9ex-and-dxgi-based-apis"></a><span data-ttu-id="cc37b-209">Interopérabilité entre les API Direct3D 9Ex et DXGI</span><span class="sxs-lookup"><span data-stu-id="cc37b-209">Interoperability between Direct3D 9Ex and DXGI based APIs</span></span>

<span data-ttu-id="cc37b-210">Les API Direct3D 9Ex comprenaient la notion de partage de surface pour permettre à d’autres API de lire à partir de la surface partagée.</span><span class="sxs-lookup"><span data-stu-id="cc37b-210">Direct3D 9Ex APIs included the notion of surface sharing to allow other APIs to read from the shared surface.</span></span> <span data-ttu-id="cc37b-211">Pour partager la lecture et l’écriture dans une surface partagée Direct3D 9Ex, vous devez ajouter une synchronisation manuelle à l’application elle-même.</span><span class="sxs-lookup"><span data-stu-id="cc37b-211">In order to share reading and writing to a Direct3D 9Ex shared surface, you must add manual synchronization to the application itself.</span></span>

### <a name="direct3d-9ex-shared-surfaces-plus-manual-synchronization-helper"></a><span data-ttu-id="cc37b-212">Applications partagées Direct3D 9Ex et application auxiliaire de synchronisation manuelle</span><span class="sxs-lookup"><span data-stu-id="cc37b-212">Direct3D 9Ex Shared Surfaces Plus Manual Synchronization Helper</span></span>

<span data-ttu-id="cc37b-213">La tâche la plus fondamentale dans Direct3D 9Ex et Direct3D 10 ou 11 Interoperability consiste à passer une seule surface du premier appareil (appareil A) au deuxième (appareil B) de telle sorte que lorsque l’appareil B acquiert un handle sur la surface, le rendu de l’appareil A est garanti comme étant terminé.</span><span class="sxs-lookup"><span data-stu-id="cc37b-213">The most fundamental task in Direct3D 9Ex and Direct3D 10 or 11 interoperability is passing a single surface from the first device (device A) to the second (device B) such that when device B acquires a handle on the surface, device A's rendering is guaranteed to have completed.</span></span> <span data-ttu-id="cc37b-214">Par conséquent, l’appareil B peut utiliser cette surface sans crainte.</span><span class="sxs-lookup"><span data-stu-id="cc37b-214">Therefore, device B can use this surface without worry.</span></span> <span data-ttu-id="cc37b-215">Cela est très similaire au problème classique des consommateurs de producteurs et cette discussion modélise le problème de cette façon.</span><span class="sxs-lookup"><span data-stu-id="cc37b-215">This is very similar to the classic producer-consumer problem and this discussion models the problem that way.</span></span> <span data-ttu-id="cc37b-216">Le premier appareil qui utilise la surface, puis l’abandon est le producteur (appareil A), et l’appareil qui est initialement en attente est le consommateur (appareil B).</span><span class="sxs-lookup"><span data-stu-id="cc37b-216">The first device that uses the surface and then relinquishes it is the producer (Device A), and the device that is initially waiting is the consumer (Device B).</span></span> <span data-ttu-id="cc37b-217">Toutes les applications réelles sont plus sophistiquées que cela, et enchaînent plusieurs blocs de construction producteur-consommateur pour créer les fonctionnalités souhaitées.</span><span class="sxs-lookup"><span data-stu-id="cc37b-217">Any real-world application is more sophisticated than this, and will chain together multiple producer-consumer building blocks to create the desired functionality.</span></span>

<span data-ttu-id="cc37b-218">Les blocs de construction producteur-consommateur sont implémentés dans l’application auxiliaire à l’aide d’une file d’attente de surfaces.</span><span class="sxs-lookup"><span data-stu-id="cc37b-218">The producer-consumer building blocks are implemented in the helper by using a queue of surfaces.</span></span> <span data-ttu-id="cc37b-219">Les surfaces sont mises en file d’attente par le producteur et déplacées en file d’attente par le consommateur.</span><span class="sxs-lookup"><span data-stu-id="cc37b-219">Surfaces are enqueued by the producer and dequeued by the consumer.</span></span> <span data-ttu-id="cc37b-220">Le programme d’assistance introduit trois interfaces COM : ISurfaceQueue, ISurfaceProducer et ISurfaceConsumer.</span><span class="sxs-lookup"><span data-stu-id="cc37b-220">The helper introduces three COM interfaces: ISurfaceQueue, ISurfaceProducer, and ISurfaceConsumer.</span></span>

### <a name="high-level-overview-of-helper"></a><span data-ttu-id="cc37b-221">High-Level vue d’ensemble de l’application auxiliaire</span><span class="sxs-lookup"><span data-stu-id="cc37b-221">High-Level Overview of Helper</span></span>

<span data-ttu-id="cc37b-222">L’objet ISurfaceQueue est le bloc de construction pour l’utilisation des surfaces partagées.</span><span class="sxs-lookup"><span data-stu-id="cc37b-222">The ISurfaceQueue object is the building block for using the shared surfaces.</span></span> <span data-ttu-id="cc37b-223">Il est créé avec un appareil Direct3D initialisé et une description pour créer un nombre fixe de surfaces partagées.</span><span class="sxs-lookup"><span data-stu-id="cc37b-223">It is created with an initialized Direct3D device and a description to create a fixed number of shared surfaces.</span></span> <span data-ttu-id="cc37b-224">L’objet de file d’attente gère la création de ressources et l’ouverture de code.</span><span class="sxs-lookup"><span data-stu-id="cc37b-224">The queue object manages creation of resources and opening of code.</span></span> <span data-ttu-id="cc37b-225">Le nombre et le type de surfaces sont fixes ; une fois les surfaces créées, l’application ne peut pas les ajouter ou les supprimer.</span><span class="sxs-lookup"><span data-stu-id="cc37b-225">The number and type of surfaces are fixed; once the surfaces are created, the application cannot add or remove them.</span></span>

<span data-ttu-id="cc37b-226">Chaque instance de l’objet ISurfaceQueue fournit une sorte de rue unidirectionnelle qui peut être utilisée pour envoyer des surfaces de l’appareil producteur à l’appareil consommateur.</span><span class="sxs-lookup"><span data-stu-id="cc37b-226">Each instance of the ISurfaceQueue object provides a sort of one-way street that can be used to send surfaces from the producing device to the consuming device.</span></span> <span data-ttu-id="cc37b-227">Plusieurs rues à sens unique peuvent être utilisées pour activer des scénarios de partage de surface entre des appareils d’applications spécifiques.</span><span class="sxs-lookup"><span data-stu-id="cc37b-227">Multiple such one-way streets can be used to enable surface sharing scenarios between devices of specific applications.</span></span>

<span data-ttu-id="cc37b-228">**Création/durée de vie des objets**</span><span class="sxs-lookup"><span data-stu-id="cc37b-228">**Creation/Object Lifetime**</span></span>  
<span data-ttu-id="cc37b-229">Il existe deux façons de créer l’objet de file d’attente : via CreateSurfaceQueue ou via la méthode Clone de ISurfaceQueue.</span><span class="sxs-lookup"><span data-stu-id="cc37b-229">There are two ways to create the queue object: through CreateSurfaceQueue, or through the Clone method of ISurfaceQueue.</span></span> <span data-ttu-id="cc37b-230">Étant donné que les interfaces sont des objets COM, la gestion de la durée de vie COM standard s’applique.</span><span class="sxs-lookup"><span data-stu-id="cc37b-230">Because the interfaces are COM objects, standard COM lifetime management applies.</span></span>  
<span data-ttu-id="cc37b-231">**Modèle producteur/consommateur**</span><span class="sxs-lookup"><span data-stu-id="cc37b-231">**Producer/Consumer Model**</span></span>  
<span data-ttu-id="cc37b-232">Emqueue () : le producteur appelle cette fonction pour indiquer qu’elle est effectuée avec la surface, qui peut désormais devenir disponible pour un autre appareil.</span><span class="sxs-lookup"><span data-stu-id="cc37b-232">Enqueue (): The producer calls this function to indicate it is done with the surface, which can now become available to another device.</span></span> <span data-ttu-id="cc37b-233">Lors du retour de cette fonction, l’appareil producteur ne dispose plus de droits sur la surface et il n’est pas possible de continuer à l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="cc37b-233">Upon returning from this function, the producer device no longer has rights to the surface and it is unsafe to continue using it.</span></span>  
<span data-ttu-id="cc37b-234">Dequeue () : l’appareil consommateur appelle cette fonction pour obtenir une surface partagée.</span><span class="sxs-lookup"><span data-stu-id="cc37b-234">Dequeue (): The consuming device calls this function to get a shared surface.</span></span> <span data-ttu-id="cc37b-235">L’API garantit que toutes les surfaces déplacées en file d’attente sont prêtes à être utilisées.</span><span class="sxs-lookup"><span data-stu-id="cc37b-235">The API guarantees that any dequeued surfaces are ready to be used.</span></span>  
<span data-ttu-id="cc37b-236">**Métadonnées**</span><span class="sxs-lookup"><span data-stu-id="cc37b-236">**Metadata**</span></span>  
<span data-ttu-id="cc37b-237">L’API prend en charge l’Association de métadonnées aux surfaces partagées.</span><span class="sxs-lookup"><span data-stu-id="cc37b-237">The API supports associating metadata with the shared surfaces.</span></span>  
<span data-ttu-id="cc37b-238">Enqueue () a la possibilité de spécifier des métadonnées supplémentaires qui seront transmises à l’appareil consommateur.</span><span class="sxs-lookup"><span data-stu-id="cc37b-238">Enqueue() has the option of specifying additional metadata that will be passed to the consuming device.</span></span> <span data-ttu-id="cc37b-239">Les métadonnées doivent être inférieures à un maximum connu au moment de la création.</span><span class="sxs-lookup"><span data-stu-id="cc37b-239">The metadata must be less than a maximum known at creation time.</span></span>  
<span data-ttu-id="cc37b-240">Dequeue () peut éventuellement passer une mémoire tampon et un pointeur vers la taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="cc37b-240">Dequeue() can optionally pass a buffer and a pointer to the size of the buffer.</span></span> <span data-ttu-id="cc37b-241">La file d’attente remplit la mémoire tampon avec les métadonnées de l’appel de mise en file d’attente correspondant.</span><span class="sxs-lookup"><span data-stu-id="cc37b-241">The queue fills in the buffer with the metadata from the corresponding Enqueue call.</span></span>  
<span data-ttu-id="cc37b-242">**clonage**</span><span class="sxs-lookup"><span data-stu-id="cc37b-242">**Cloning**</span></span>  
<span data-ttu-id="cc37b-243">Chaque objet ISurfaceQueue résout une synchronisation unidirectionnelle.</span><span class="sxs-lookup"><span data-stu-id="cc37b-243">Each ISurfaceQueue object solves a one-way synchronization.</span></span> <span data-ttu-id="cc37b-244">Nous partons du principe que la grande majorité des applications utilisant cette API utilisera un système fermé.</span><span class="sxs-lookup"><span data-stu-id="cc37b-244">We assume that the vast majority of applications using this API will use a closed system.</span></span> <span data-ttu-id="cc37b-245">Le système le plus simple et fermé avec deux appareils qui envoient des surfaces en arrière-plan requiert deux files d’attente.</span><span class="sxs-lookup"><span data-stu-id="cc37b-245">The simplest closed system with two devices sending surfaces back and forth requires two queues.</span></span> <span data-ttu-id="cc37b-246">L’objet ISurfaceQueue possède une méthode Clone () pour permettre la création de plusieurs files d’attente qui font toutes partie du même pipeline plus grand.</span><span class="sxs-lookup"><span data-stu-id="cc37b-246">The ISurfaceQueue object has a Clone() method to make it possible to create multiple queues that are all part of the same larger pipeline.</span></span>  
<span data-ttu-id="cc37b-247">Clone crée un nouvel objet ISurfaceQueue à partir d’un objet existant et partage toutes les ressources ouvertes entre eux.</span><span class="sxs-lookup"><span data-stu-id="cc37b-247">Clone creates a new ISurfaceQueue object from an existing one, and shares all the opened resources between them.</span></span> <span data-ttu-id="cc37b-248">L’objet obtenu a exactement les mêmes surfaces que la file d’attente source.</span><span class="sxs-lookup"><span data-stu-id="cc37b-248">The resulting object has exactly the same surfaces as the source queue.</span></span> <span data-ttu-id="cc37b-249">Les files d’attente clonées peuvent avoir des tailles de métadonnées différentes les unes des autres.</span><span class="sxs-lookup"><span data-stu-id="cc37b-249">Cloned queues can have different metadata sizes from each other.</span></span>  
<span data-ttu-id="cc37b-250">**Surfaces**</span><span class="sxs-lookup"><span data-stu-id="cc37b-250">**Surfaces**</span></span>  
<span data-ttu-id="cc37b-251">Le ISurfaceQueue est responsable de la création et de la gestion de ses surfaces.</span><span class="sxs-lookup"><span data-stu-id="cc37b-251">The ISurfaceQueue takes responsibility for creating and managing its surfaces.</span></span> <span data-ttu-id="cc37b-252">La mise en file d’attente des surfaces arbitraires n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cc37b-252">It is not valid to enqueue arbitrary surfaces.</span></span> <span data-ttu-id="cc37b-253">En outre, une surface ne doit avoir qu’un seul « propriétaire » actif.</span><span class="sxs-lookup"><span data-stu-id="cc37b-253">Furthermore, a surface should only have one active "owner."</span></span> <span data-ttu-id="cc37b-254">Elle doit se trouver dans une file d’attente spécifique ou être utilisée par un appareil spécifique.</span><span class="sxs-lookup"><span data-stu-id="cc37b-254">It should either be on a specific queue or being used by a specific device.</span></span> <span data-ttu-id="cc37b-255">Il n’est pas possible de le faire sur plusieurs files d’attente ou pour que les appareils continuent à utiliser l’aire après qu’elle a été mise en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="cc37b-255">It is not valid to have it on multiple queues or for devices to continue using the surface after it is enqueued.</span></span>  
</dl>

### <a name="api-details"></a><span data-ttu-id="cc37b-256">Détails de l’API</span><span class="sxs-lookup"><span data-stu-id="cc37b-256">API Details</span></span>

### <a name="isurfacequeue"></a><span data-ttu-id="cc37b-257">IsurfaceQueue</span><span class="sxs-lookup"><span data-stu-id="cc37b-257">IsurfaceQueue</span></span>

<span data-ttu-id="cc37b-258">La file d’attente est chargée de créer et de gérer les ressources partagées.</span><span class="sxs-lookup"><span data-stu-id="cc37b-258">The queue is responsible for creating and maintaining the shared resources.</span></span> <span data-ttu-id="cc37b-259">Il fournit également les fonctionnalités permettant de chaîner plusieurs files d’attente à l’aide du clone.</span><span class="sxs-lookup"><span data-stu-id="cc37b-259">It also provides the functionality to chain multiple queues using Clone.</span></span> <span data-ttu-id="cc37b-260">La file d’attente a des méthodes qui ouvrent l’appareil de production et un appareil consommateur.</span><span class="sxs-lookup"><span data-stu-id="cc37b-260">The queue has methods that open the producing device and a consuming device.</span></span> <span data-ttu-id="cc37b-261">Un seul d’entre eux peut être ouvert à tout moment.</span><span class="sxs-lookup"><span data-stu-id="cc37b-261">Only one of each can be opened at any time.</span></span>

<span data-ttu-id="cc37b-262">La file d’attente expose les API suivantes :</span><span class="sxs-lookup"><span data-stu-id="cc37b-262">The queue exposes the following APIs:</span></span>



| <span data-ttu-id="cc37b-263">API</span><span class="sxs-lookup"><span data-stu-id="cc37b-263">API</span></span>                            | <span data-ttu-id="cc37b-264">Description</span><span class="sxs-lookup"><span data-stu-id="cc37b-264">Description</span></span>                                                                                 |
|-----------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cc37b-265">CreateSurfaceQueue</span><span class="sxs-lookup"><span data-stu-id="cc37b-265">CreateSurfaceQueue</span></span>          | <span data-ttu-id="cc37b-266">Crée un objet ISurfaceQueue (la file d’attente « racine »).</span><span class="sxs-lookup"><span data-stu-id="cc37b-266">Creates an ISurfaceQueue object (the "root" queue).</span></span>                              |
| <span data-ttu-id="cc37b-267">ISurfaceQueue::OpenConsumer</span><span class="sxs-lookup"><span data-stu-id="cc37b-267">ISurfaceQueue::OpenConsumer</span></span> | <span data-ttu-id="cc37b-268">Retourne une interface pour l’appareil consommateur à défiler.</span><span class="sxs-lookup"><span data-stu-id="cc37b-268">Returns an interface for the consuming device to dequeue.</span></span>                        |
| <span data-ttu-id="cc37b-269">ISurfaceQueue::OpenProducer</span><span class="sxs-lookup"><span data-stu-id="cc37b-269">ISurfaceQueue::OpenProducer</span></span> | <span data-ttu-id="cc37b-270">Retourne une interface pour l’appareil producteur à enqueuer.</span><span class="sxs-lookup"><span data-stu-id="cc37b-270">Returns an interface for the producing device to enqueue.</span></span>                        |
| <span data-ttu-id="cc37b-271">ISurfaceQueue :: Clone</span><span class="sxs-lookup"><span data-stu-id="cc37b-271">ISurfaceQueue::Clone</span></span>        | <span data-ttu-id="cc37b-272">Crée un objet ISurfaceQueue qui partage des surfaces avec l’objet de file d’attente racine.</span><span class="sxs-lookup"><span data-stu-id="cc37b-272">Creates an ISurfaceQueue object that shares surfaces with the root queue object.</span></span> |



 

<span data-ttu-id="cc37b-273">**CreateSurfaceQueue**</span><span class="sxs-lookup"><span data-stu-id="cc37b-273">**CreateSurfaceQueue**</span></span>  


```C++
typedef struct SURFACE_QUEUE_DESC {
  UINT            Width;
  UINT            Height;
  DXGI_FORMAT     Format;
  UINT            NumSurfaces;
  UINT            MetaDataSize;
  DWORD           Flags;
} SURFACE_QUEUE_DESC;
```



<span data-ttu-id="cc37b-274">**Members** (Membres)</span><span class="sxs-lookup"><span data-stu-id="cc37b-274">**Members**</span></span>  

<span data-ttu-id="cc37b-275">**Largeur**, **hauteur**  des dimensions des surfaces partagées.</span><span class="sxs-lookup"><span data-stu-id="cc37b-275">**Width**, **Height**  The dimensions of the shared surfaces.</span></span> <span data-ttu-id="cc37b-276">Toutes les surfaces partagées doivent avoir les mêmes dimensions.</span><span class="sxs-lookup"><span data-stu-id="cc37b-276">All shared surfaces must have the same dimensions.</span></span>  
<span data-ttu-id="cc37b-277">**Format** Format des surfaces partagées.</span><span class="sxs-lookup"><span data-stu-id="cc37b-277">**Format** The format of the shared surfaces.</span></span> <span data-ttu-id="cc37b-278">Toutes les surfaces partagées doivent avoir le même format.</span><span class="sxs-lookup"><span data-stu-id="cc37b-278">All shared surfaces must have the same format.</span></span> <span data-ttu-id="cc37b-279">Les formats valides dépendent des appareils qui seront utilisés, car différentes paires d’appareils peuvent partager différents types de format.</span><span class="sxs-lookup"><span data-stu-id="cc37b-279">The valid formats depend on the devices that will be used, because different pairs of devices can share different format types.</span></span>  
<span data-ttu-id="cc37b-280">**NumSurfaces**  Nombre de surfaces qui font partie de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="cc37b-280">**NumSurfaces**  The number of surfaces that are part of the queue.</span></span> <span data-ttu-id="cc37b-281">Il s’agit d’un nombre fixe.</span><span class="sxs-lookup"><span data-stu-id="cc37b-281">This is a fixed number.</span></span>  
 <span data-ttu-id="cc37b-282">**MetaDataSize**  Taille maximale de la mémoire tampon des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="cc37b-282">**MetaDataSize**  The maximum size of the metadata buffer.</span></span>  
<span data-ttu-id="cc37b-283">**Indicateurs**  Indicateurs permettant de contrôler le comportement de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="cc37b-283">**Flags**  Flags to control the behavior of the queue.</span></span> <span data-ttu-id="cc37b-284">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="cc37b-284">See Remarks.</span></span>  



```C++
HRESULT CreateSurfaceQueue(
  [in]   SURFACE_QUEUE_DESC *pDesc,
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



<span data-ttu-id="cc37b-285">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="cc37b-285">**Parameters**</span></span>

 <span data-ttu-id="cc37b-286">*pDesc* \[ dans \]  la description de la file d’attente de surface partagée à créer.</span><span class="sxs-lookup"><span data-stu-id="cc37b-286">*pDesc* \[in\]  The description of the shared surface queue to be created.</span></span>  

 <span data-ttu-id="cc37b-287">*pDevice* \[ dans \]  l’appareil qui doit être utilisé pour créer les surfaces partagées.</span><span class="sxs-lookup"><span data-stu-id="cc37b-287">*pDevice* \[in\]  The device that should be used to create the shared surfaces.</span></span> <span data-ttu-id="cc37b-288">Il s’agit d’un paramètre explicite en raison d’une fonctionnalité de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cc37b-288">This is an explicit parameter because of a feature in Windows Vista.</span></span> <span data-ttu-id="cc37b-289">Pour les surfaces partagées entre Direct3D 9 et Direct3D 10, les surfaces doivent être créées avec Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="cc37b-289">For surfaces shared between Direct3D 9 and Direct3D 10, the surfaces must be created with Direct3D 9.</span></span>  

 <span data-ttu-id="cc37b-290">*ppQueue* \[ out au \]  retour, contient un pointeur vers l’objet ISurfaceQueue.</span><span class="sxs-lookup"><span data-stu-id="cc37b-290">*ppQueue* \[out\]  On return, contains a pointer to the ISurfaceQueue object.</span></span>  


<span data-ttu-id="cc37b-291">**Valeurs renvoyées**</span><span class="sxs-lookup"><span data-stu-id="cc37b-291">**Return Values**</span></span>

<span data-ttu-id="cc37b-292">Si *pDevice* n’est pas en capacité de partager des ressources, cette fonction retourne l’appel de dxgi \_ Error \_ non valide \_ .</span><span class="sxs-lookup"><span data-stu-id="cc37b-292">If *pDevice* is not capable of sharing resources, this function returns DXGI\_ERROR\_INVALID\_CALL.</span></span> <span data-ttu-id="cc37b-293">Cette fonction crée les ressources.</span><span class="sxs-lookup"><span data-stu-id="cc37b-293">This function creates the resources.</span></span> <span data-ttu-id="cc37b-294">En cas d’échec, elle retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="cc37b-294">If it fails, it returns an error.</span></span> <span data-ttu-id="cc37b-295">Si elle est réussie, elle retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cc37b-295">If it succeeds, it returns S\_OK.</span></span>

<span data-ttu-id="cc37b-296">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="cc37b-296">**Remarks**</span></span>

<span data-ttu-id="cc37b-297">La création de l’objet de file d’attente crée également toutes les surfaces.</span><span class="sxs-lookup"><span data-stu-id="cc37b-297">Creating the queue object also creates all of the surfaces.</span></span> <span data-ttu-id="cc37b-298">Toutes les surfaces sont supposées être des cibles de rendu 2D et seront créées avec les indicateurs de la cible de rendu de liaison D3D10 et de la \_ \_ ressource de \_ \_ \_ nuanceur de liaison D3D10 \_ définis (ou les indicateurs équivalents pour les différents runtimes).</span><span class="sxs-lookup"><span data-stu-id="cc37b-298">All surfaces are assumed to be 2D render targets and will be created with the D3D10\_BIND\_RENDER\_TARGET and D3D10\_BIND\_SHADER\_RESOURCE flags set (or the equivalent flags for the different runtimes).</span></span>

<span data-ttu-id="cc37b-299">Le développeur peut spécifier un indicateur qui indique si la file d’attente est accessible par plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="cc37b-299">The developer can specify a flag that indicates whether the queue will be accessed by multiple threads.</span></span> <span data-ttu-id="cc37b-300">Si aucun indicateur n’est défini (**Flags** = = 0), la file d’attente est utilisée par plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="cc37b-300">If no flags are set (**Flags** == 0), the queue will be used by multiple threads.</span></span> <span data-ttu-id="cc37b-301">Le développeur peut spécifier un accès à thread unique, ce qui désactive le code de synchronisation et améliore les performances dans ces cas.</span><span class="sxs-lookup"><span data-stu-id="cc37b-301">The developer can specify single threaded access, which turns off the synchronization code and provides a performance improvement for those cases.</span></span> <span data-ttu-id="cc37b-302">Chaque file d’attente clonée possède son propre indicateur. par conséquent, il est possible que des files d’attente différentes dans le système aient des contrôles de synchronisation différents.</span><span class="sxs-lookup"><span data-stu-id="cc37b-302">Each cloned queue has its own flag, so it is possible for different queues in the system to have different synchronization controls.</span></span>

 <span data-ttu-id="cc37b-303">**Ouvrir un producteur**</span><span class="sxs-lookup"><span data-stu-id="cc37b-303">**Open a Producer**</span></span>  


```C++
HRESULT OpenProducer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceProducer **ppProducer
);
```



<span data-ttu-id="cc37b-304">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="cc37b-304">**Parameters**</span></span>  

<span data-ttu-id="cc37b-305">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cc37b-305">*pDevice* \[in\]</span></span>  

<span data-ttu-id="cc37b-306">Appareil producteur qui met en file d’attente des surfaces sur la file d’attente de surface.</span><span class="sxs-lookup"><span data-stu-id="cc37b-306">The producer device that enqueues surfaces onto the surface queue.</span></span> 

<span data-ttu-id="cc37b-307">*ppProducer* \[ out \] retourne un objet à l’interface de producteur.</span><span class="sxs-lookup"><span data-stu-id="cc37b-307">*ppProducer* \[out\] Returns an object to the producer interface.</span></span>  


<span data-ttu-id="cc37b-308">**Valeurs renvoyées**</span><span class="sxs-lookup"><span data-stu-id="cc37b-308">**Return Values**</span></span>

<span data-ttu-id="cc37b-309">Si l’appareil n’est pas en capacité de partager des surfaces, retourne l’erreur DXGI de l' \_ \_ appel non valide \_ .</span><span class="sxs-lookup"><span data-stu-id="cc37b-309">If the device is not capable of sharing surfaces, returns DXGI\_ERROR\_INVALID\_CALL.</span></span>

<span data-ttu-id="cc37b-310">**Ouvrir un consommateur**</span><span class="sxs-lookup"><span data-stu-id="cc37b-310">**Open a Consumer**</span></span>  


```C++
HRESULT OpenConsumer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceConsumer **ppConsumer
);
```



<span data-ttu-id="cc37b-311">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="cc37b-311">**Parameters**</span></span>  
 <span data-ttu-id="cc37b-312">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cc37b-312">*pDevice* \[in\]</span></span>  
 <span data-ttu-id="cc37b-313">Appareil grand public qui défile les surfaces de la file d’attente de surface.</span><span class="sxs-lookup"><span data-stu-id="cc37b-313">The consumer device that dequeues surfaces from the surface queue.</span></span> 
 <span data-ttu-id="cc37b-314">*ppConsumer* \[ out \]  retourne un objet à l’interface du consommateur.</span><span class="sxs-lookup"><span data-stu-id="cc37b-314">*ppConsumer* \[out\]  Returns an object to the consumer interface.</span></span>  


<span data-ttu-id="cc37b-315">**Valeurs renvoyées**</span><span class="sxs-lookup"><span data-stu-id="cc37b-315">**Return Values**</span></span>

<span data-ttu-id="cc37b-316">Si l’appareil n’est pas en capacité de partager des surfaces, retourne l’erreur DXGI de l' \_ \_ appel non valide \_ .</span><span class="sxs-lookup"><span data-stu-id="cc37b-316">If the device is not capable of sharing surfaces, returns DXGI\_ERROR\_INVALID\_CALL.</span></span>

<span data-ttu-id="cc37b-317">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="cc37b-317">**Remarks**</span></span>

<span data-ttu-id="cc37b-318">Cette fonction ouvre toutes les surfaces de la file d’attente pour le périphérique d’entrée et les met en cache.</span><span class="sxs-lookup"><span data-stu-id="cc37b-318">This function opens all of the surfaces in the queue for the input device and caches them.</span></span> <span data-ttu-id="cc37b-319">Les appels suivants à Dequeue sont simplement placés dans le cache et n’ont pas besoin de rouvrir les surfaces à chaque fois.</span><span class="sxs-lookup"><span data-stu-id="cc37b-319">Subsequent calls to Dequeue will simply go to the cache and not have to reopen the surfaces each time.</span></span>



### <a name="cloning-an-idxgixsurfacequeue"></a><span data-ttu-id="cc37b-320">Clonage d’un IDXGIXSurfaceQueue</span><span class="sxs-lookup"><span data-stu-id="cc37b-320">Cloning an IDXGIXSurfaceQueue</span></span>




```C++
typedef struct SHARED_SURFACE_QUEUE_CLONE_DESC {
  UINT         MetaDataSize;
  DWORD        Flags;
} SHARED_SURFACE_QUEUE_CLONE_DESC;
```



<span data-ttu-id="cc37b-321">Les **membres** **MetaDataSize** et **Flags** ont le même comportement que pour CreateSurfaceQueue.</span><span class="sxs-lookup"><span data-stu-id="cc37b-321">**Members** **MetaDataSize** and **Flags** have the same behavior as they do for CreateSurfaceQueue.</span></span>  



```C++
HRESULT Clone(
  [in]   SHARED_SURFACE_QUEUE_CLONE_DESC *pDesc,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



<span data-ttu-id="cc37b-322">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="cc37b-322">**Parameters**</span></span>

<span data-ttu-id="cc37b-323">*pDesc* \[ dans \] un struct qui fournit une description de l’objet clone à créer.</span><span class="sxs-lookup"><span data-stu-id="cc37b-323">*pDesc* \[in\] A struct that provides a description of the Clone object to be created.</span></span> <span data-ttu-id="cc37b-324">Ce paramètre doit être initialisé.</span><span class="sxs-lookup"><span data-stu-id="cc37b-324">This parameter should be initialized.</span></span>  
<span data-ttu-id="cc37b-325">*ppQueue* \[ out \] retourne l’objet initialisé.</span><span class="sxs-lookup"><span data-stu-id="cc37b-325">*ppQueue* \[out\] Returns the initialized object.</span></span>  
</dl>

<span data-ttu-id="cc37b-326">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="cc37b-326">**Remarks**</span></span>

<span data-ttu-id="cc37b-327">Vous pouvez cloner à partir de n’importe quel objet de file d’attente existant, même s’il ne s’agit pas de la racine.</span><span class="sxs-lookup"><span data-stu-id="cc37b-327">You can clone from any existing queue object, even if it is not the root.</span></span>  
</dl>

### <a name="idxgixsurfaceconsumer"></a><span data-ttu-id="cc37b-328">IDXGIXSurfaceConsumer</span><span class="sxs-lookup"><span data-stu-id="cc37b-328">IDXGIXSurfaceConsumer</span></span>

<dl>


```C++
HRESULT Dequeue(
  [in]      REFIID    id,
  [out]     void      **ppSurface,
  [in,out]  void      *pBuffer,
  [in,out]  UINT      *pBufferSize,
  [in]      DWORD     dwTimeout
);
```



<span data-ttu-id="cc37b-329">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="cc37b-329">**Parameters**</span></span>  
<span data-ttu-id="cc37b-330">*ID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cc37b-330">*id* \[in\]</span></span>  
<span data-ttu-id="cc37b-331">REFIID d’une surface 2D de l’appareil consommateur.</span><span class="sxs-lookup"><span data-stu-id="cc37b-331">The REFIID of a 2D surface of the consuming device.</span></span>  

-   <span data-ttu-id="cc37b-332">Pour un IDirect3DDevice9, REFIID doit être \_ \_ uuidof (IDirect3DTexture9).</span><span class="sxs-lookup"><span data-stu-id="cc37b-332">For a IDirect3DDevice9, the REFIID should be \_\_uuidof(IDirect3DTexture9).</span></span>
-   <span data-ttu-id="cc37b-333">Pour un ID3D10Device, REFIID doit être \_ \_ uuidof (ID3D10Texture2D).</span><span class="sxs-lookup"><span data-stu-id="cc37b-333">For a ID3D10Device, the REFIID should be \_\_uuidof(ID3D10Texture2D).</span></span>
-   <span data-ttu-id="cc37b-334">Pour un ID3D11Device, REFIID doit être \_ \_ uuidof (ID3D11Texture2D).</span><span class="sxs-lookup"><span data-stu-id="cc37b-334">For a ID3D11Device, the REFIID should be \_\_uuidof(ID3D11Texture2D).</span></span>

<span data-ttu-id="cc37b-335">*ppSurface* \[ out \] retourne un pointeur vers l’aire.</span><span class="sxs-lookup"><span data-stu-id="cc37b-335">*ppSurface* \[out\] Returns a pointer to the surface.</span></span>  
<span data-ttu-id="cc37b-336">*pbuffer* \[ dans, sortie \] d’un paramètre facultatif et, si la **valeur** n’est pas null, en cas de retour, contient les métadonnées qui ont été passées sur l’appel de mise en file d’attente correspondant.</span><span class="sxs-lookup"><span data-stu-id="cc37b-336">*pBuffer* \[in, out\] An optional parameter and if not **NULL**, on return, contains the metadata that was passed in on the corresponding enqueue call.</span></span>  
<span data-ttu-id="cc37b-337">*pBufferSize* \[ dans, sortie \] de la taille de *pbuffer*, en octets.</span><span class="sxs-lookup"><span data-stu-id="cc37b-337">*pBufferSize* \[in, out\] The size of *pBuffer*, in bytes.</span></span> <span data-ttu-id="cc37b-338">Retourne le nombre d’octets retournés dans *pbuffer*.</span><span class="sxs-lookup"><span data-stu-id="cc37b-338">Returns the number of bytes returned in *pBuffer*.</span></span> <span data-ttu-id="cc37b-339">Si l’appel de mise en file d’attente n’a pas fourni de métadonnées, *pbuffer* a la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="cc37b-339">If the enqueue call did not provide metadata, *pBuffer* is set to 0.</span></span>  
<span data-ttu-id="cc37b-340">*dwTimeout* \[ dans \] spécifie une valeur de délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="cc37b-340">*dwTimeout* \[in\] Specifies a timeout value.</span></span> <span data-ttu-id="cc37b-341">Pour plus d’informations, consultez les notes.</span><span class="sxs-lookup"><span data-stu-id="cc37b-341">See the Remarks for more detail.</span></span>  
</dl>

<span data-ttu-id="cc37b-342">**Valeurs renvoyées**</span><span class="sxs-lookup"><span data-stu-id="cc37b-342">**Return Values**</span></span>

<span data-ttu-id="cc37b-343">Cette fonction peut retourner \_ un délai d’attente si une valeur de délai d’attente est spécifiée et que la fonction ne retourne pas avant la valeur du délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="cc37b-343">This function can return WAIT\_TIMEOUT if a timeout value is specified and the function does not return before the time out value.</span></span> <span data-ttu-id="cc37b-344">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="cc37b-344">See Remarks.</span></span> <span data-ttu-id="cc37b-345">Si aucune surface n’est disponible, la fonction retourne avec *ppSurface* défini sur **null**, *pBufferSize* défini sur 0 et la valeur de retour est 0x80070120 (Win32 \_ à \_ HRESULT ( \_ délai d’attente)).</span><span class="sxs-lookup"><span data-stu-id="cc37b-345">If no surfaces are available, the function returns with *ppSurface* set to **NULL**, *pBufferSize* set to 0 and the return value is 0x80070120 (WIN32\_TO\_HRESULT(WAIT\_TIMEOUT)).</span></span>  
</dl>

<span data-ttu-id="cc37b-346">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="cc37b-346">**Remarks**</span></span>

<span data-ttu-id="cc37b-347">Cette API peut se bloquer si la file d’attente est vide.</span><span class="sxs-lookup"><span data-stu-id="cc37b-347">This API can block if the queue is empty.</span></span> <span data-ttu-id="cc37b-348">Le paramètre *dwTimeout* fonctionne de la même façon que les API de synchronisation Windows, telles que WaitForSingleObject.</span><span class="sxs-lookup"><span data-stu-id="cc37b-348">The *dwTimeout* parameter works identically to the Windows synchronization APIs, such as WaitForSingleObject.</span></span> <span data-ttu-id="cc37b-349">Pour un comportement non bloquant, utilisez un délai d’expiration de 0.</span><span class="sxs-lookup"><span data-stu-id="cc37b-349">For non-blocking behavior, use a timeout of 0.</span></span>  
</dl>

### <a name="isurfaceproducer"></a><span data-ttu-id="cc37b-350">ISurfaceProducer</span><span class="sxs-lookup"><span data-stu-id="cc37b-350">ISurfaceProducer</span></span>

<span data-ttu-id="cc37b-351">Cette interface fournit deux méthodes qui permettent à l’application d’empiler des surfaces.</span><span class="sxs-lookup"><span data-stu-id="cc37b-351">This interface provides two methods that allow the app to enqueue surfaces.</span></span> <span data-ttu-id="cc37b-352">Une fois qu’une surface est mise en file d’attente, le pointeur de surface n’est plus valide et ne peut pas être utilisé en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="cc37b-352">After a surface is enqueued, the surface pointer is no longer valid and is not safe to use.</span></span> <span data-ttu-id="cc37b-353">La seule action que l’application doit effectuer avec le pointeur consiste à la libérer.</span><span class="sxs-lookup"><span data-stu-id="cc37b-353">The only action that the application should perform with the pointer is to release it.</span></span>



| <span data-ttu-id="cc37b-354">Méthode</span><span class="sxs-lookup"><span data-stu-id="cc37b-354">Method</span></span>                          | <span data-ttu-id="cc37b-355">Description</span><span class="sxs-lookup"><span data-stu-id="cc37b-355">Description</span></span>                                                                                                                                                      |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc37b-356">ISurfaceProducer :: emqueue</span><span class="sxs-lookup"><span data-stu-id="cc37b-356">ISurfaceProducer::Enqueue</span></span> | <span data-ttu-id="cc37b-357">Met en file d’attente une surface vers l’objet de file d’attente.</span><span class="sxs-lookup"><span data-stu-id="cc37b-357">Enqueues a surface to the queue object.</span></span> <span data-ttu-id="cc37b-358">Une fois cet appel terminé, le producteur est réalisé avec la surface et la surface est prête pour un autre appareil.</span><span class="sxs-lookup"><span data-stu-id="cc37b-358">After this call completes, the producer is done with the surface and the surface is ready for another device.</span></span> |
| <span data-ttu-id="cc37b-359">ISurfaceProducer :: Flush</span><span class="sxs-lookup"><span data-stu-id="cc37b-359">ISurfaceProducer::Flush</span></span>   | <span data-ttu-id="cc37b-360">Utilisé si les applications doivent avoir un comportement non bloquant.</span><span class="sxs-lookup"><span data-stu-id="cc37b-360">Used if the applications should have non-blocking behavior.</span></span> <span data-ttu-id="cc37b-361">Pour plus de détails, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="cc37b-361">See Remarks for details.</span></span>                                                                  |



 

<span data-ttu-id="cc37b-362">**Enqueue (empiler)**</span><span class="sxs-lookup"><span data-stu-id="cc37b-362">**Enqueue**</span></span>  


```C++
HRESULT Enqueue(
  [in]  IUnknown *pSurface,
  [in]  void *pBuffer,
  [in]  UINT BufferSize,
  [in]  DWORD Flags
);
```



<span data-ttu-id="cc37b-363">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="cc37b-363">**Parameters**</span></span>  
<span data-ttu-id="cc37b-364">*pSurface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cc37b-364">*pSurface* \[in\]</span></span>  
<span data-ttu-id="cc37b-365">Surface du périphérique de production qui doit être mise en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="cc37b-365">The surface of the producing device that needs to be enqueued.</span></span> <span data-ttu-id="cc37b-366">Cette surface doit être une surface déplacée de la file d’attente du même réseau de file d’attente.</span><span class="sxs-lookup"><span data-stu-id="cc37b-366">This surface must be a dequeued surface from the same queue network.</span></span> <span data-ttu-id="cc37b-367">*pbuffer* \[ dans \] un paramètre facultatif, qui est utilisé pour passer des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="cc37b-367">*pBuffer* \[in\] An optional parameter, which is used to pass in metadata.</span></span> <span data-ttu-id="cc37b-368">Il doit pointer vers les données qui seront transmises à l’appel de retrait de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="cc37b-368">It should point to the data that will be passed on to the dequeue call.</span></span>  
<span data-ttu-id="cc37b-369">*BufferSize* \[ dans \] la taille de *pbuffer*, en octets.</span><span class="sxs-lookup"><span data-stu-id="cc37b-369">*BufferSize* \[in\] The size of *pBuffer*, in bytes.</span></span>  
<span data-ttu-id="cc37b-370">*Indicateurs* \[ dans \] un paramètre facultatif qui contrôle le comportement de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="cc37b-370">*Flags* \[in\] An optional parameter that controls the behavior of this function.</span></span> <span data-ttu-id="cc37b-371">Le seul indicateur est l' \_ indicateur de file d’attente de surface n’est pas en attente \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cc37b-371">The only flag is SURFACE\_QUEUE\_FLAG\_ DO\_NOT\_WAIT.</span></span> <span data-ttu-id="cc37b-372">Consultez les notes relatives au vidage.</span><span class="sxs-lookup"><span data-stu-id="cc37b-372">See the Remarks for Flush.</span></span> <span data-ttu-id="cc37b-373">Si aucun indicateur n’est passé (*Flags* = = 0), le comportement de blocage par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="cc37b-373">If no flag is passed (*Flags* == 0), then the default blocking behavior is used.</span></span>  
</dl>

<span data-ttu-id="cc37b-374">**Valeurs renvoyées**</span><span class="sxs-lookup"><span data-stu-id="cc37b-374">**Return Values**</span></span>

<span data-ttu-id="cc37b-375">Cette fonction peut retourner \_ une erreur dxgi lors du \_ \_ \_ dessin quand un indicateur d’attente de la file d’attente de surface n' \_ \_ \_ \_ \_ est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="cc37b-375">This function can return DXGI\_ERROR\_WAS\_STILL\_DRAWING if a SURFACE\_QUEUE\_FLAG\_DO\_NOT\_WAIT flag is used.</span></span>  
</dl>

<span data-ttu-id="cc37b-376">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="cc37b-376">**Remarks**</span></span>

-   <span data-ttu-id="cc37b-377">Cette fonction place la surface sur la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="cc37b-377">This function puts the surface on the queue.</span></span> <span data-ttu-id="cc37b-378">Si l’application ne spécifie pas l' \_ indicateur de file d’attente \_ de surface \_ n' \_ \_ attend pas, cette fonction bloque et effectue une synchronisation GPU-CPU pour s’assurer que tout le rendu sur la surface en file d’attente est terminé.</span><span class="sxs-lookup"><span data-stu-id="cc37b-378">If the application does not specify SURFACE\_QUEUE\_FLAG\_DO\_NOT\_WAIT, this function is blocking and will do a GPU-CPU synchronization to assure that all the rendering on the enqueued surface is complete.</span></span> <span data-ttu-id="cc37b-379">Si cette fonction est réussie, une surface est disponible pour la défile d’attente.</span><span class="sxs-lookup"><span data-stu-id="cc37b-379">If this function succeeds, a surface will be available for dequeue.</span></span> <span data-ttu-id="cc37b-380">Si vous souhaitez un comportement non bloquant, utilisez l' \_ indicateur do not \_ Wait.</span><span class="sxs-lookup"><span data-stu-id="cc37b-380">If you want non-blocking behavior, use the DO\_NOT\_WAIT flag.</span></span> <span data-ttu-id="cc37b-381">Pour plus d’informations, consultez Flush ().</span><span class="sxs-lookup"><span data-stu-id="cc37b-381">See Flush() for details.</span></span>
-   <span data-ttu-id="cc37b-382">Conformément aux règles de décompte de références COM, la surface retournée par Dequeue est AddRef (), de sorte que l’application n’a pas besoin de le faire.</span><span class="sxs-lookup"><span data-stu-id="cc37b-382">As per the COM reference counting rules, the surface returned by Dequeue will be AddRef() so the application does not need to do this.</span></span> <span data-ttu-id="cc37b-383">Après l’appel de la mise en file d’attente, l’application doit libérer la surface, car elle ne l’utilise plus.</span><span class="sxs-lookup"><span data-stu-id="cc37b-383">After calling Enqueue, the application must Release the surface because they are no longer using it.</span></span>

<span data-ttu-id="cc37b-384">**Purge**</span><span class="sxs-lookup"><span data-stu-id="cc37b-384">**Flush**</span></span>  


```C++
HRESULT Flush(
  [in]  DWORD Flags,
  [out] UINT *nSurfaces
);
```



<span data-ttu-id="cc37b-385">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="cc37b-385">**Parameters**</span></span>  
<span data-ttu-id="cc37b-386">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="cc37b-386">*Flags* \[in\]</span></span>  
<span data-ttu-id="cc37b-387">Le seul indicateur est l' \_ indicateur de file d’attente de surface n’est pas en attente \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cc37b-387">The only flag is SURFACE\_QUEUE\_FLAG\_ DO\_NOT\_WAIT.</span></span> <span data-ttu-id="cc37b-388">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="cc37b-388">See Remarks.</span></span> <span data-ttu-id="cc37b-389">*nSurfaces* \[ out \] retourne le nombre de surfaces toujours en attente et non vidées.</span><span class="sxs-lookup"><span data-stu-id="cc37b-389">*nSurfaces* \[out\] Returns the number of surfaces that are still pending and not flushed.</span></span>  
</dl>

<span data-ttu-id="cc37b-390">**Valeurs renvoyées**</span><span class="sxs-lookup"><span data-stu-id="cc37b-390">**Return Values**</span></span>

<span data-ttu-id="cc37b-391">Cette fonction peut retourner une \_ erreur \_ dxgi \_ quand \_ l' \_ indicateur d’attente de la file d’attente de surface n' \_ \_ \_ \_ est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="cc37b-391">This function can return DXGI\_ERROR\_WAS\_STILL\_DRAWING if the SURFACE\_QUEUE\_FLAG\_DO\_NOT\_WAIT flag is used.</span></span> <span data-ttu-id="cc37b-392">Cette fonction retourne S \_ OK si des surfaces ont été vidées avec succès.</span><span class="sxs-lookup"><span data-stu-id="cc37b-392">This function returns S\_OK if any surfaces were successfully flushed.</span></span> <span data-ttu-id="cc37b-393">Cette fonction retourne l' \_ erreur dxgi en \_ \_ \_ dessinant uniquement si aucune surface n’a été vidée.</span><span class="sxs-lookup"><span data-stu-id="cc37b-393">This function returns DXGI\_ERROR\_WAS\_STILL\_DRAWING only if no surfaces were flushed.</span></span> <span data-ttu-id="cc37b-394">Ensemble, la valeur de retour et *nSurfaces* indiquent à l’application ce qui a été effectué et si un travail reste à faire.</span><span class="sxs-lookup"><span data-stu-id="cc37b-394">Together, the return value and *nSurfaces* indicate to the application what work has been done and if any work is left to do.</span></span>  
</dl>

<span data-ttu-id="cc37b-395">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="cc37b-395">**Remarks**</span></span>

<span data-ttu-id="cc37b-396">Le vidage est explicite uniquement si l’appel précédent à Enqueue a utilisé \_ l' \_ indicateur do not Wait ; sinon, il s’agit d’une absence d’opération.</span><span class="sxs-lookup"><span data-stu-id="cc37b-396">Flush is meaningful only if the previous call to enqueue used the DO\_NOT\_WAIT flag; otherwise, it will be a no-op.</span></span> <span data-ttu-id="cc37b-397">Si l’appel à Enqueue a utilisé l' \_ indicateur do not \_ Wait, la file d’attente est retournée immédiatement et la synchronisation GPU-CPU n’est pas garantie.</span><span class="sxs-lookup"><span data-stu-id="cc37b-397">If the call to enqueue used the DO\_NOT\_WAIT flag, enqueue returns immediately and the GPU-CPU synchronization is not guaranteed.</span></span> <span data-ttu-id="cc37b-398">La surface est toujours considérée comme étant mise en file d’attente, l’appareil producteur ne peut pas continuer à l’utiliser, mais elle n’est pas disponible pour la défile d’attente.</span><span class="sxs-lookup"><span data-stu-id="cc37b-398">The surface is still considered enqueued, the producing device cannot continue using it, but it is not available for dequeue.</span></span> <span data-ttu-id="cc37b-399">Pour essayer de valider la surface de la file d’attente, Flush doit être appelé.</span><span class="sxs-lookup"><span data-stu-id="cc37b-399">In order to try to commit the surface for dequeue, Flush must be called.</span></span> <span data-ttu-id="cc37b-400">Le vidage tente de valider toutes les surfaces actuellement mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="cc37b-400">Flush attempts to commit all of the surfaces that are currently enqueued.</span></span> <span data-ttu-id="cc37b-401">Si aucun indicateur n’est passé au vidage, il bloque et efface l’intégralité de la file d’attente, en prêtant toutes les surfaces qu’il contient pour la défile d’attente.</span><span class="sxs-lookup"><span data-stu-id="cc37b-401">If no flag is passed to Flush, it will block and clear out the entire queue, readying all surfaces in it for dequeue.</span></span> <span data-ttu-id="cc37b-402">Si l' \_ indicateur ne pas \_ attendre est utilisé, la file d’attente vérifie les surfaces pour voir si l’une d’elles est prête ; cette étape est non bloquante.</span><span class="sxs-lookup"><span data-stu-id="cc37b-402">If the DO\_NOT\_WAIT flag is used, the queue will check the surfaces to see if any of them are ready; this step is non-blocking.</span></span> <span data-ttu-id="cc37b-403">Les surfaces qui ont terminé la synchronisation GPU-UC sont prêtes pour l’appareil grand public.</span><span class="sxs-lookup"><span data-stu-id="cc37b-403">Surfaces that have finished the GPU-CPU sync will be ready for the consumer device.</span></span> <span data-ttu-id="cc37b-404">Les surfaces toujours en attente ne seront pas affectées.</span><span class="sxs-lookup"><span data-stu-id="cc37b-404">Surfaces that are still pending will be unaffected.</span></span> <span data-ttu-id="cc37b-405">La fonction retourne le nombre de surfaces qui doivent encore être vidées.</span><span class="sxs-lookup"><span data-stu-id="cc37b-405">The function returns the number of surfaces that still need to be flushed.</span></span>

> [!Note]  
> <span data-ttu-id="cc37b-406">Flush n’interrompt pas la sémantique de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="cc37b-406">Flush will not break the queue semantics.</span></span> <span data-ttu-id="cc37b-407">L’API garantit que les surfaces mises en file d’attente seront validées avant que les surfaces soient mises en file d’attente par la suite, quel que soit le moment où la synchronisation GPU-CPU se produit.</span><span class="sxs-lookup"><span data-stu-id="cc37b-407">The API guarantees that surfaces enqueued first will be committed before surfaces enqueued later, regardless of when the GPU-CPU sync happens.</span></span>

 

  
</dl>

### <a name="direct3d-9ex-and-dxgi-interop-helper-how-to-use"></a><span data-ttu-id="cc37b-408">Application auxiliaire Direct3D 9Ex et DXGI Interop : comment utiliser</span><span class="sxs-lookup"><span data-stu-id="cc37b-408">Direct3D 9Ex and DXGI Interop Helper: How To Use</span></span>

<span data-ttu-id="cc37b-409">Nous pensons que la plupart des cas d’utilisation impliquent deux appareils partageant un certain nombre de surfaces.</span><span class="sxs-lookup"><span data-stu-id="cc37b-409">We expect most of the usage cases to involve two devices sharing a number of surfaces.</span></span> <span data-ttu-id="cc37b-410">Étant donné qu’il s’agit également du scénario le plus simple, ce document explique en détail comment utiliser les API pour atteindre cet objectif, aborde une variation non bloquante et se termine par une brève section sur l’initialisation de trois appareils.</span><span class="sxs-lookup"><span data-stu-id="cc37b-410">Because this also happens to be the simplest scenario, this paper details how to use the APIs to achieve this goal, discusses a non-blocking variation, and ends with a brief section about initializing for three devices.</span></span>

### <a name="two-devices"></a><span data-ttu-id="cc37b-411">Deux appareils</span><span class="sxs-lookup"><span data-stu-id="cc37b-411">Two Devices</span></span>

<span data-ttu-id="cc37b-412">L’exemple d’application qui utilise cette application d’assistance peut utiliser Direct3D 9Ex et Direct3D 11 ensemble.</span><span class="sxs-lookup"><span data-stu-id="cc37b-412">The example application that uses this helper can use Direct3D 9Ex and Direct3D 11 together.</span></span> <span data-ttu-id="cc37b-413">L’application peut traiter le contenu avec les deux appareils et présenter le contenu à l’aide de Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="cc37b-413">The application can process content with both devices, and present content using Direct3D 9.</span></span> <span data-ttu-id="cc37b-414">Le traitement peut signifier le rendu du contenu, le décodage de la vidéo, l’exécution des nuanceurs de calcul, etc.</span><span class="sxs-lookup"><span data-stu-id="cc37b-414">Processing could mean rendering content, decoding video, running compute shaders, and so on.</span></span> <span data-ttu-id="cc37b-415">Pour chaque trame, l’application traite tout d’abord avec Direct3D 11, puis traite avec Direct3D 9 et enfin présente avec Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="cc37b-415">For every frame, the application will first process with Direct3D 11, then process with Direct3D 9, and finally present with Direct3D 9.</span></span> <span data-ttu-id="cc37b-416">En outre, le traitement avec Direct3D 11 produira des métadonnées que le Direct3D 9 doit utiliser.</span><span class="sxs-lookup"><span data-stu-id="cc37b-416">Furthermore, the processing with Direct3D 11 will produce some metadata that the Direct3D 9 present will need to consume.</span></span> <span data-ttu-id="cc37b-417">Cette section traite de l’utilisation de l’application d’assistance en trois parties qui correspondent à cette séquence : initialisation, boucle principale et nettoyage.</span><span class="sxs-lookup"><span data-stu-id="cc37b-417">This section covers the helper usage in three parts that correspond to this sequence: Initialization, Main Loop, and Cleanup.</span></span>

<span data-ttu-id="cc37b-418">**Initialisation**</span><span class="sxs-lookup"><span data-stu-id="cc37b-418">**Initialization**</span></span>  
<span data-ttu-id="cc37b-419">L’initialisation implique les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="cc37b-419">Initialization involves the following steps:</span></span>  

1.  <span data-ttu-id="cc37b-420">Initialisez les deux appareils.</span><span class="sxs-lookup"><span data-stu-id="cc37b-420">Initialize both devices.</span></span>
2.  <span data-ttu-id="cc37b-421">Créez la file d’attente racine : m \_ 11to9Queue.</span><span class="sxs-lookup"><span data-stu-id="cc37b-421">Create the Root Queue: m\_11to9Queue.</span></span>
3.  <span data-ttu-id="cc37b-422">Cloner à partir de la file d’attente racine : m \_ 9to11Queue.</span><span class="sxs-lookup"><span data-stu-id="cc37b-422">Clone from the Root Queue: m\_9to11Queue.</span></span>
4.  <span data-ttu-id="cc37b-423">Appelez OpenProducer/OpenConsumer sur les deux files d’attente.</span><span class="sxs-lookup"><span data-stu-id="cc37b-423">Call OpenProducer/OpenConsumer on both queues.</span></span>

<span data-ttu-id="cc37b-424">Les noms de files d’attente utilisent les chiffres 9 et 11 pour indiquer l’API qui est le producteur et qui est le _producteur_*_de_* l’utilisateur : **m \_** à la *_file d’attente_* du _consommateur_.</span><span class="sxs-lookup"><span data-stu-id="cc37b-424">The queue names use the numbers 9 and 11 to indicate which API is the producer and which is the consumer: **m\_**_producer_*_to_*_consumer_*_Queue_*.</span></span> <span data-ttu-id="cc37b-425">En conséquence, m \_ 11to9Queue indique une file d’attente pour laquelle l’appareil Direct3D 11 produit des surfaces consommées par l’appareil Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="cc37b-425">Accordingly, m\_11to9Queue indicates a queue for which the Direct3D 11 device produces surfaces that the Direct3D 9 device consumes.</span></span> <span data-ttu-id="cc37b-426">De même, m \_ 9to11Queue indique une file d’attente pour laquelle Direct3D 9 produit des surfaces consommées par Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="cc37b-426">Similarly, m\_9to11Queue indicates a queue for which Direct3D 9 produces surfaces that Direct3D 11 consumes.</span></span>  
<span data-ttu-id="cc37b-427">La file d’attente racine est initialement remplie et toutes les files d’attente clonées sont initialement vides.</span><span class="sxs-lookup"><span data-stu-id="cc37b-427">The Root queue is initially full and all cloned queues are initially empty.</span></span> <span data-ttu-id="cc37b-428">Cela ne doit pas être un problème pour l’application, à l’exception du premier cycle des enfilements et des retraits de file d’attente et de la disponibilité des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="cc37b-428">This should not be a problem for the application except for the first cycle of the Enqueues and Dequeues and the availability of metadata.</span></span> <span data-ttu-id="cc37b-429">Si une file d’attente demande des métadonnées mais qu’aucune n’a été définie (soit parce qu’aucune n’a été initialement, soit la file d’attente n’a rien défini), Dequeue constate qu’aucune métadonnée n’a été reçue.</span><span class="sxs-lookup"><span data-stu-id="cc37b-429">If a dequeue asks for metadata but none was set (either because nothing is there initially or the enqueue did not set anything), dequeue sees that no metadata was received.</span></span>  

1.  <span data-ttu-id="cc37b-430">**Initialisez les deux appareils.**</span><span class="sxs-lookup"><span data-stu-id="cc37b-430">**Initialize Both Devices.**</span></span>  
    ```C++
    m_pD3D9Device = InitializeD3D9ExDevice();
    m_pD3D11Device = InitializeD3D11Device();
    ```

    

2.  <span data-ttu-id="cc37b-431">**Créez la file d’attente racine.**</span><span class="sxs-lookup"><span data-stu-id="cc37b-431">**Create the Root Queue.**</span></span>  
    <span data-ttu-id="cc37b-432">Cette étape crée également les surfaces.</span><span class="sxs-lookup"><span data-stu-id="cc37b-432">This step also creates the surfaces.</span></span> <span data-ttu-id="cc37b-433">Les restrictions de taille et de format sont identiques à la création d’une ressource partagée.</span><span class="sxs-lookup"><span data-stu-id="cc37b-433">Size and format restrictions are identical to creating any shared resource.</span></span> <span data-ttu-id="cc37b-434">La taille de la mémoire tampon des métadonnées est fixée au moment de la création, et dans ce cas, nous allons simplement passer un UINT.</span><span class="sxs-lookup"><span data-stu-id="cc37b-434">The size of the metadata buffer is fixed at create time, and in this case, we'll just be passing a UINT.</span></span>  
    <span data-ttu-id="cc37b-435">La file d’attente doit être créée avec un nombre fixe de surfaces.</span><span class="sxs-lookup"><span data-stu-id="cc37b-435">The queue must be created with a fixed number of surfaces.</span></span> <span data-ttu-id="cc37b-436">Les performances varient en fonction du scénario.</span><span class="sxs-lookup"><span data-stu-id="cc37b-436">Performance will vary depending on the scenario.</span></span> <span data-ttu-id="cc37b-437">Le fait de disposer de plusieurs surfaces augmente le risque que les appareils soient occupés.</span><span class="sxs-lookup"><span data-stu-id="cc37b-437">Having multiple surfaces increases the chances that devices are busy.</span></span> <span data-ttu-id="cc37b-438">Par exemple, s’il n’y a qu’une seule surface, il n’y aura aucune parallélisation entre les deux appareils.</span><span class="sxs-lookup"><span data-stu-id="cc37b-438">For example, if there is only one surface, then there will be no parallelization between the two devices.</span></span> <span data-ttu-id="cc37b-439">D’un autre côté, l’augmentation du nombre de surfaces augmente l’encombrement mémoire, ce qui peut dégrader les performances.</span><span class="sxs-lookup"><span data-stu-id="cc37b-439">On the other hand, increasing the number of surfaces increases the memory footprint, which can degrade performance.</span></span> <span data-ttu-id="cc37b-440">Cet exemple utilise deux surfaces.</span><span class="sxs-lookup"><span data-stu-id="cc37b-440">This example uses two surfaces.</span></span>  
    ```C++
    SURFACE_QUEUE_DESC Desc;
    Desc.Width        = 640;
    Desc.Height       = 480;
    Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
    Desc.NumSurfaces  = 2;
    Desc.MetaDataSize = sizeof(UINT);
    Desc.Flags        = 0;

    CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
    ```

    

3.  <span data-ttu-id="cc37b-441">**Clonez la file d’attente racine.**</span><span class="sxs-lookup"><span data-stu-id="cc37b-441">**Clone the Root Queue.**</span></span>  
    <span data-ttu-id="cc37b-442">Chaque file d’attente clonée doit utiliser les mêmes surfaces, mais elle peut avoir des tailles de mémoire tampon de métadonnées différentes et des indicateurs différents.</span><span class="sxs-lookup"><span data-stu-id="cc37b-442">Each cloned queue must use the same surfaces but can have different metadata buffer sizes and different flags.</span></span> <span data-ttu-id="cc37b-443">Dans ce cas, il n’y a pas de métadonnées de Direct3D 9 vers Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="cc37b-443">In this case, there is no metadata from Direct3D 9 to Direct3D 11.</span></span>  
    ```C++
    SURFACE_QUEUE_CLONE_DESC Desc;
    Desc.MetaDataSize = 0;
    Desc.Flags        = 0;

    m_11to9Queue->Clone(&Desc, &m_9to11Queue);
    ```

    

4.  <span data-ttu-id="cc37b-444">**Ouvrez les appareils producteur et grand public.**</span><span class="sxs-lookup"><span data-stu-id="cc37b-444">**Open the Producer and Consumer Devices.**</span></span>  
    <span data-ttu-id="cc37b-445">L’application doit effectuer cette étape avant d’appeler Enqueue et Dequeue.</span><span class="sxs-lookup"><span data-stu-id="cc37b-445">The application must perform this step before calling Enqueue and Dequeue.</span></span> <span data-ttu-id="cc37b-446">L’ouverture d’un producteur et d’un consommateur retourne des interfaces qui contiennent les API d’empilement/retrait de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="cc37b-446">Opening a producer and consumer returns interfaces which contain the enqueue/dequeue APIs.</span></span>  
    ```C++
    // Open for m_p9to11Queue.
    m_p9to11Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
    m_p9to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

    // Open for m_p11to9Queue.
    m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
    m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
    ```

    

<span data-ttu-id="cc37b-447">**Boucle principale**</span><span class="sxs-lookup"><span data-stu-id="cc37b-447">**Main Loop**</span></span>  
<span data-ttu-id="cc37b-448">L’utilisation de la file d’attente est modélisée après le problème de producteur/consommateur classique.</span><span class="sxs-lookup"><span data-stu-id="cc37b-448">The usage of the queue is modeled after the classical producer/consumer problem.</span></span> <span data-ttu-id="cc37b-449">Pensez à cela d’un point de vue de chaque appareil.</span><span class="sxs-lookup"><span data-stu-id="cc37b-449">Think of this from a per-device perspective.</span></span> <span data-ttu-id="cc37b-450">Chaque appareil doit effectuer les étapes suivantes : Dequeue pour obtenir une surface de sa file d’attente de consommation, traiter sur l’aire, puis mettre en file d’attente dans sa file d’attente de production.</span><span class="sxs-lookup"><span data-stu-id="cc37b-450">Each device must perform these steps: dequeue to get a surface from its consuming queue, process on the surface, and then enqueue onto its producing queue.</span></span> <span data-ttu-id="cc37b-451">Pour l’appareil Direct3D 11, l’utilisation de Direct3D 9 est presque identique.</span><span class="sxs-lookup"><span data-stu-id="cc37b-451">For the Direct3D 11 device, the Direct3D 9 usage is almost identical.</span></span>  


```C++
// Direct3D 9 Device.
IDirect3DTexture9* pTexture9 = NULL;
REFIID             surfaceID9 = _uuidof(IDirect3DTexture9);
UINT               metaData;
UINT               metaDataSize;
while (!done)
{
    // Dequeue surface.
    m_pD3D9Consumer->Dequeue(surfaceID9, (void**)&pSurface9,
                             &metaData, &metaDataSize, INFINITE);

    // Process the surface.
    ProcessD3D9(pSurface9);

    // Present the surface using the meta data.
    PresentD3D9(pSurface9, metaData, metaDataSize);

    // Enqueue surface.
    m_pD3D9Producer->Enqueue(pSurface9, NULL, 0, 0);
}
```



<span data-ttu-id="cc37b-452">**Nettoyage en trop**</span><span class="sxs-lookup"><span data-stu-id="cc37b-452">**Cleaning Up**</span></span>  
<span data-ttu-id="cc37b-453">Cette étape est très simple.</span><span class="sxs-lookup"><span data-stu-id="cc37b-453">This step is very straightforward.</span></span> <span data-ttu-id="cc37b-454">En plus des étapes normales de nettoyage des API Direct3D, l’application doit libérer les interfaces COM de retour.</span><span class="sxs-lookup"><span data-stu-id="cc37b-454">In addition to the normal steps for cleaning up Direct3D APIs, the application must release the return COM interfaces.</span></span>  


```C++
m_pD3D9Producer->Release();
m_pD3D9Consumer->Release();
m_pD3D11Producer->Release();
m_pD3D11Consumer->Release();
m_p9to11Queue->Release();
m_p11to9Queue->Release();
```



</dl>

### <a name="non-blocking-use"></a><span data-ttu-id="cc37b-455">Utilisation non bloquante</span><span class="sxs-lookup"><span data-stu-id="cc37b-455">Non-Blocking Use</span></span>

<span data-ttu-id="cc37b-456">L’exemple précédent est logique pour un cas d’utilisation multithread dans lequel chaque appareil a son propre thread.</span><span class="sxs-lookup"><span data-stu-id="cc37b-456">The previous example makes sense for a multithreaded usage case in which each device has its own thread.</span></span> <span data-ttu-id="cc37b-457">L’exemple utilise les versions bloquantes des API : infini pour timeout et aucun indicateur pour Enqueue.</span><span class="sxs-lookup"><span data-stu-id="cc37b-457">The example uses the blocking versions of the APIs: INFINITE for timeout, and no flag to enqueue.</span></span> <span data-ttu-id="cc37b-458">Si vous souhaitez utiliser le programme d’assistance de façon non bloquante, vous ne devez apporter que quelques modifications.</span><span class="sxs-lookup"><span data-stu-id="cc37b-458">If you want to use the helper in a non-blocking way, you need to make only a few changes.</span></span> <span data-ttu-id="cc37b-459">Cette section montre une utilisation non bloquante avec les deux appareils sur un thread.</span><span class="sxs-lookup"><span data-stu-id="cc37b-459">This section shows non-blocking use with both devices on one thread.</span></span>

<span data-ttu-id="cc37b-460">**Initialisation**</span><span class="sxs-lookup"><span data-stu-id="cc37b-460">**Initialization**</span></span>  
<span data-ttu-id="cc37b-461">L’initialisation est identique à l’exception des indicateurs.</span><span class="sxs-lookup"><span data-stu-id="cc37b-461">Initialization is identical except for the flags.</span></span> <span data-ttu-id="cc37b-462">Étant donné que l’application est monothread, utilisez cet indicateur pour la création.</span><span class="sxs-lookup"><span data-stu-id="cc37b-462">Because the application is single-threaded, use that flag for creation.</span></span> <span data-ttu-id="cc37b-463">Cela désactive une partie du code de synchronisation, ce qui peut potentiellement améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="cc37b-463">This turns off some of the synchronization code, which potentially improves performance.</span></span>  


```C++
SURFACE_QUEUE_DESC Desc;
Desc.Width        = 640;
Desc.Height       = 480;
Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
Desc.NumSurfaces  = 2;
Desc.MetaDataSize = sizeof(UINT);
Desc.Flags        = SURFACE_QUEUE_FLAG_SINGLE_THREADED;

CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
```




```C++
SURFACE_QUEUE_CLONE_DESC Desc;
Desc.MetaDataSize = 0;
Desc.Flags        = SURFACE_QUEUE_FLAG_SINGLE_THREADED;

m_11to9Queue->Clone(&Desc, &m_9to11Queue);
```



<span data-ttu-id="cc37b-464">L’ouverture des appareils producteur et grand public est identique à celle de l’exemple de blocage.</span><span class="sxs-lookup"><span data-stu-id="cc37b-464">Opening the producer and consumer devices are the same as in the blocking example.</span></span>  
<span data-ttu-id="cc37b-465">**Utilisation de la file d’attente**</span><span class="sxs-lookup"><span data-stu-id="cc37b-465">**Using the Queue**</span></span>  
<span data-ttu-id="cc37b-466">Il existe de nombreuses façons d’utiliser la file d’attente de façon non bloquante, avec différentes caractéristiques de performances.</span><span class="sxs-lookup"><span data-stu-id="cc37b-466">There are many ways of using the queue in a non-blocking fashion with various performance characteristics.</span></span> <span data-ttu-id="cc37b-467">L’exemple suivant est simple, mais a des performances médiocres en raison d’une rotation et d’une interrogation excessives.</span><span class="sxs-lookup"><span data-stu-id="cc37b-467">The following example is simple but has poor performance due to excessive spinning and polling.</span></span> <span data-ttu-id="cc37b-468">Malgré ces problèmes, l’exemple montre comment utiliser l’application auxiliaire.</span><span class="sxs-lookup"><span data-stu-id="cc37b-468">Despite these problems, the example shows how to use the helper.</span></span> <span data-ttu-id="cc37b-469">L’approche consiste à se positionner en permanence dans une boucle et à supprimer la file d’attente, le processus, l’empilement et le vidage.</span><span class="sxs-lookup"><span data-stu-id="cc37b-469">The approach is to constantly sit in a loop and dequeue, process, enqueue, and flush.</span></span> <span data-ttu-id="cc37b-470">Si l’une des étapes échoue parce que la ressource n’est pas disponible, l’application essaie simplement de relancer la boucle suivante.</span><span class="sxs-lookup"><span data-stu-id="cc37b-470">If any of the steps fail because the resource is not available, the application simply tries again the next loop.</span></span>  


```C++
// Direct3D 11 Device.
ID3D11Texture2D* pSurface11 = NULL;
REFIID           surfaceID11 = __uuidof(ID3D11Texture2D);
UINT             metaData;
while (!done)
{
    //
    // D3D11 Portion.
    //

    // Dequeue surface.
    hr = m_pD3D11Consumer->Dequeue(surfaceID11,
                                   (void**)&pSurface11,
                                   NULL, 0, 0);
    // Only continue if we got a surface.
    if (SUCCEEDED(hr))
    {
        // Process the surface and return some meta data.
        ProcessD3D11(pSurface11, &metaData);

        // Enqueue surface.
        m_pD3D11Producer->Enqueue(pSurface11, &metaData,
                                  sizeof(UINT),
                                  SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
    }
    // Flush the queue to check if any surfaces completed.
    m_pD3D11Producer->Flush(NULL,SURFACE_QUEUE_FLAG_DO_NOT_WAIT);

    //
    // Do the same with the Direct3D 9 Device.
    //

    // Dequeue surface.
    hr = m_pD3D9Consumer->Dequeue(surfaceID9,
                                  (void**)&pSurface9,
                                  &metaData,
                                  &metaDataSize, 0);
    // Only continue if we got a surface.
    if (SUCCEEDED(hr)))
    {
        // Process the surface.
        ProcessD3D9(pSurface9);

        // Present the surface using the meta data.
        PresentD3D9(pSurface9, metaData, metaDataSize);

        // Enqueue surface.
        m_pD3D9Producer->Enqueue(pSurface9, NULL, 0,
                                 SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
    }
    // Flush the queue to check if any surfaces completed.
    m_pD3D9Producer->Flush(NULL,SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
}
```



<span data-ttu-id="cc37b-471">Une solution plus complexe pourrait vérifier la valeur de retour de Enqueue et de Flush pour déterminer si le vidage est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="cc37b-471">A more complex solution could check the return value from enqueue and from flush to determine if flushing is necessary.</span></span>  
</dl>

### <a name="three-devices"></a><span data-ttu-id="cc37b-472">Trois appareils</span><span class="sxs-lookup"><span data-stu-id="cc37b-472">Three Devices</span></span>

<span data-ttu-id="cc37b-473">L’extension des exemples précédents pour couvrir plusieurs appareils est simple.</span><span class="sxs-lookup"><span data-stu-id="cc37b-473">Extending the previous examples to cover multiple devices is straightforward.</span></span> <span data-ttu-id="cc37b-474">Le code suivant effectue l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="cc37b-474">The following code performs the initialization.</span></span> <span data-ttu-id="cc37b-475">Une fois que les objets producteur/consommateur ont été créés, le code permettant de les utiliser est le même.</span><span class="sxs-lookup"><span data-stu-id="cc37b-475">After the Producer/Consumer objects have been created, the code to use them is the same.</span></span> <span data-ttu-id="cc37b-476">Cet exemple a trois appareils et donc trois files d’attente.</span><span class="sxs-lookup"><span data-stu-id="cc37b-476">This example has three devices and therefore three queues.</span></span> <span data-ttu-id="cc37b-477">Les surfaces circulent de Direct3D 9 vers Direct3D 10 vers Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="cc37b-477">Surfaces flow from Direct3D 9 to Direct3D 10 to Direct3D 11.</span></span>


```C++
SURFACE_QUEUE_DESC Desc;
Desc.Width        = 640;
Desc.Height       = 480;
Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
Desc.NumSurfaces  = 2;
Desc.MetaDataSize = sizeof(UINT);
Desc.Flags        = 0;

SURFACE_QUEUE_CLONE_DESC Desc;
Desc.MetaDataSize = 0;
Desc.Flags        = 0;

CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
m_11to9Queue->Clone(&Desc, &m_9to10Queue);
m_11to9Queue->Clone(&Desc, &m_10to11Queue);
```



<span data-ttu-id="cc37b-478">Comme mentionné précédemment, le clonage fonctionne de la même façon, quelle que soit la file d’attente clonée.</span><span class="sxs-lookup"><span data-stu-id="cc37b-478">As mentioned earlier, cloning works the same way, no matter which queue is cloned.</span></span> <span data-ttu-id="cc37b-479">Par exemple, le deuxième appel de clonage aurait pu être en dehors de l' \_ objet m 9to10Queue.</span><span class="sxs-lookup"><span data-stu-id="cc37b-479">For example, the second Clone call could have been off of the m\_9to10Queue object.</span></span>


```C++
// Open for m_p9to10Queue.
m_p9to10Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
m_p9to10Queue->OpenConsumer(m_pD3D10Device, &m_pD3D10Consumer);

// Open for m_p10to11Queue.
m_p10to11Queue->OpenProducer(m_pD3D10Device, &m_pD3D10Producer);
m_p10to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

// Open for m_p11to9Queue.
m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
```



## <a name="conclusion"></a><span data-ttu-id="cc37b-480">Conclusion</span><span class="sxs-lookup"><span data-stu-id="cc37b-480">Conclusion</span></span>

<span data-ttu-id="cc37b-481">Vous pouvez créer des solutions qui utilisent l’interopérabilité pour utiliser la puissance de plusieurs API DirectX.</span><span class="sxs-lookup"><span data-stu-id="cc37b-481">You can create solutions that use interoperability to employ the power of multiple DirectX APIs.</span></span> <span data-ttu-id="cc37b-482">L’interopérabilité de l’API Windows Graphics offre désormais un Common surface Management Runtime DXGI 1,1.</span><span class="sxs-lookup"><span data-stu-id="cc37b-482">Windows graphics API interoperability now offers a common surface management runtime DXGI 1.1.</span></span> <span data-ttu-id="cc37b-483">Ce Runtime active la prise en charge de partage de surface synchronisé dans les API récemment développées, telles que Direct3D 11, Direct3D 10,1 et Direct2D.</span><span class="sxs-lookup"><span data-stu-id="cc37b-483">This runtime enables synchronized surface sharing support within newly developed APIs, such as Direct3D 11, Direct3D 10.1 and Direct2D.</span></span> <span data-ttu-id="cc37b-484">Les améliorations de l’interopérabilité entre les nouvelles API et les API existantes contribuent à la migration des applications et à la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="cc37b-484">Interoperability improvements between new APIs and existing APIs aid application migration and backward compatibility.</span></span> <span data-ttu-id="cc37b-485">Les API de consommateur Direct3D 9Ex et DXGI 1,1 peuvent interagir, comme le montre le mécanisme de synchronisation fourni via l’exemple de code d’assistance sur MSDN Code Gallery.</span><span class="sxs-lookup"><span data-stu-id="cc37b-485">Direct3D 9Ex and DXGI 1.1 consumer APIs can interoperate, as shown with the synchronization mechanism provided through sample helper code on MSDN Code Gallery.</span></span>

 

 