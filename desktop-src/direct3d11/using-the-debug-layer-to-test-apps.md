---
title: Utilisation de la couche de débogage pour déboguer des applications
description: Ici, nous parlerons de la façon d’activer la couche de débogage et certains des problèmes que vous pouvez empêcher à l’aide de la couche de débogage.
ms.assetid: 3C2B0A12-FB57-4400-BE39-05ED23F552C7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa3f4748da6893470e3bb6631c4228ec1ae3d48
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671650"
---
# <a name="using-the-debug-layer-to-debug-apps"></a><span data-ttu-id="528ea-103">Utilisation de la couche de débogage pour déboguer des applications</span><span class="sxs-lookup"><span data-stu-id="528ea-103">Using the debug layer to debug apps</span></span>

<span data-ttu-id="528ea-104">Nous vous recommandons d’utiliser la [couche de débogage](overviews-direct3d-11-devices-layers.md) pour déboguer vos applications et vous assurer qu’il ne s’agit pas d’erreurs et d’avertissements.</span><span class="sxs-lookup"><span data-stu-id="528ea-104">We recommend that you use the [debug layer](overviews-direct3d-11-devices-layers.md) to debug your apps to ensure that they are clean of errors and warnings.</span></span> <span data-ttu-id="528ea-105">La couche de débogage vous aide à écrire du code Direct3D.</span><span class="sxs-lookup"><span data-stu-id="528ea-105">The debug layer helps you write Direct3D code.</span></span> <span data-ttu-id="528ea-106">En outre, votre productivité peut augmenter lorsque vous utilisez la couche de débogage, car vous pouvez voir immédiatement les causes d’erreurs de rendu obscures ou même d’écrans noirs à leur source.</span><span class="sxs-lookup"><span data-stu-id="528ea-106">In addition, your productivity can increase when you use the debug layer because you can immediately see the causes of obscure rendering errors or even black screens at their source.</span></span> <span data-ttu-id="528ea-107">La couche de débogage fournit des avertissements pour de nombreux problèmes.</span><span class="sxs-lookup"><span data-stu-id="528ea-107">The debug layer provides warnings for many issues.</span></span> <span data-ttu-id="528ea-108">Par exemple, la couche de débogage fournit des avertissements pour les problèmes suivants :</span><span class="sxs-lookup"><span data-stu-id="528ea-108">For example, the debug layer provides warnings for these issues:</span></span>

-   <span data-ttu-id="528ea-109">Vous avez oublié de définir une texture, mais de la lire dans votre nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="528ea-109">Forgot to set a texture but read from it in your pixel shader</span></span>
-   <span data-ttu-id="528ea-110">Profondeur de sortie, mais aucune limite d’État du gabarit de profondeur</span><span class="sxs-lookup"><span data-stu-id="528ea-110">Output depth but have no depth-stencil state bound</span></span>
-   <span data-ttu-id="528ea-111">Échec de la création de la texture avec INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="528ea-111">Texture creation failed with INVALIDARG</span></span>

<span data-ttu-id="528ea-112">Ici, nous parlerons de la façon d’activer la [couche de débogage](overviews-direct3d-11-devices-layers.md) et certains des problèmes que vous pouvez empêcher à l’aide de la couche de débogage.</span><span class="sxs-lookup"><span data-stu-id="528ea-112">Here we talk about how to enable the [debug layer](overviews-direct3d-11-devices-layers.md) and some of the issues that you can prevent by using the debug layer.</span></span>

-   [<span data-ttu-id="528ea-113">Activation de la couche de débogage</span><span class="sxs-lookup"><span data-stu-id="528ea-113">Enabling the debug layer</span></span>](#enabling-the-debug-layer)
-   [<span data-ttu-id="528ea-114">Prévention des erreurs dans votre application avec la couche de débogage</span><span class="sxs-lookup"><span data-stu-id="528ea-114">Preventing errors in your app with the debug layer</span></span>](#preventing-errors-in-your-app-with-the-debug-layer)
    -   [<span data-ttu-id="528ea-115">Ne pas passer de pointeurs NULL au mappage</span><span class="sxs-lookup"><span data-stu-id="528ea-115">Don't pass NULL pointers to Map</span></span>](#dont-pass-null-pointers-to-map)
    -   [<span data-ttu-id="528ea-116">Limiter la zone source dans les ressources source et de destination</span><span class="sxs-lookup"><span data-stu-id="528ea-116">Confine source box within source and destination resources</span></span>](#confine-source-box-within-source-and-destination-resources)
    -   [<span data-ttu-id="528ea-117">Ne supprimez pas DiscardResource ou DiscardView</span><span class="sxs-lookup"><span data-stu-id="528ea-117">Don't drop DiscardResource or DiscardView</span></span>](#dont-drop-discardresource-or-discardview)
-   [<span data-ttu-id="528ea-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="528ea-118">Related topics</span></span>](#related-topics)

## <a name="enabling-the-debug-layer"></a><span data-ttu-id="528ea-119">Activation de la couche de débogage</span><span class="sxs-lookup"><span data-stu-id="528ea-119">Enabling the debug layer</span></span>

<span data-ttu-id="528ea-120">Pour activer la [couche de débogage](overviews-direct3d-11-devices-layers.md), spécifiez l’indicateur de [**\_ \_ \_ débogage d3d11 créer un appareil**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) dans le paramètre *Flags* lorsque vous appelez la fonction [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) pour créer le périphérique de rendu.</span><span class="sxs-lookup"><span data-stu-id="528ea-120">To enable the [debug layer](overviews-direct3d-11-devices-layers.md), specify the [**D3D11\_CREATE\_DEVICE\_DEBUG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) flag in the *Flags* parameter when you call the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function to create the rendering device.</span></span> <span data-ttu-id="528ea-121">Cet exemple de code montre comment activer la couche de débogage lorsque votre projet Microsoft Visual Studio se trouve dans une version Debug :</span><span class="sxs-lookup"><span data-stu-id="528ea-121">This example code shows how to enable the debug layer when your Microsoft Visual Studio project is in a debug build:</span></span>


```C++
        UINT creationFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
#if defined(_DEBUG)
        // If the project is in a debug build, enable the debug layer.
        creationFlags |= D3D11_CREATE_DEVICE_DEBUG;
#endif
        // Define the ordering of feature levels that Direct3D attempts to create.
        D3D_FEATURE_LEVEL featureLevels[] =
        {
            D3D_FEATURE_LEVEL_11_1,
            D3D_FEATURE_LEVEL_11_0,
            D3D_FEATURE_LEVEL_10_1,
            D3D_FEATURE_LEVEL_10_0,
            D3D_FEATURE_LEVEL_9_3,
            D3D_FEATURE_LEVEL_9_1
        };

        ComPtr<ID3D11Device> d3dDevice;
        ComPtr<ID3D11DeviceContext> d3dDeviceContext;
        DX::ThrowIfFailed(
            D3D11CreateDevice(
                nullptr,                    // specify nullptr to use the default adapter
                D3D_DRIVER_TYPE_HARDWARE,
                nullptr,                    // specify nullptr because D3D_DRIVER_TYPE_HARDWARE 
                                            // indicates that this function uses hardware
                creationFlags,              // optionally set debug and Direct2D compatibility flags
                featureLevels,
                ARRAYSIZE(featureLevels),
                D3D11_SDK_VERSION,          // always set this to D3D11_SDK_VERSION
                &d3dDevice,
                nullptr,
                &d3dDeviceContext
                )
            );
```



## <a name="preventing-errors-in-your-app-with-the-debug-layer"></a><span data-ttu-id="528ea-122">Prévention des erreurs dans votre application avec la couche de débogage</span><span class="sxs-lookup"><span data-stu-id="528ea-122">Preventing errors in your app with the debug layer</span></span>

<span data-ttu-id="528ea-123">Si vous abusez de l’API Direct3D 11 ou si vous transmettez des paramètres incorrects, la sortie de débogage de la [couche de débogage](overviews-direct3d-11-devices-layers.md) signale une erreur ou un avertissement.</span><span class="sxs-lookup"><span data-stu-id="528ea-123">If you misuse the Direct3D 11 API or pass bad parameters, the debug output of the [debug layer](overviews-direct3d-11-devices-layers.md) reports an error or a warning.</span></span> <span data-ttu-id="528ea-124">Vous pouvez ensuite corriger votre erreur.</span><span class="sxs-lookup"><span data-stu-id="528ea-124">You can then correct your mistake.</span></span> <span data-ttu-id="528ea-125">Ensuite, nous examinons certains problèmes de codage qui peuvent provoquer un comportement indéfini ou même le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="528ea-125">Next, we look at some coding issues that can cause undefined behavior or even the operating system to crash.</span></span> <span data-ttu-id="528ea-126">Vous pouvez intercepter et éviter ces problèmes à l’aide de la couche de débogage.</span><span class="sxs-lookup"><span data-stu-id="528ea-126">You can catch and prevent these issues by using the debug layer.</span></span>

### <a name="dont-pass-null-pointers-to-map"></a><span data-ttu-id="528ea-127">Ne pas passer de pointeurs NULL au mappage</span><span class="sxs-lookup"><span data-stu-id="528ea-127">Don't pass NULL pointers to Map</span></span>

<span data-ttu-id="528ea-128">Si vous transmettez la **valeur null** au paramètre *PreSource* ou *pMappedResource* de la méthode [**ID3D11DeviceContext :: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) , le comportement de **Map** n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="528ea-128">If you pass **NULL** to the *pResource* or *pMappedResource* parameter of the [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) method, the behavior of **Map** is undefined.</span></span> <span data-ttu-id="528ea-129">Si vous avez créé un appareil qui prend uniquement en charge la [couche principale](overviews-direct3d-11-devices-layers.md), les paramètres non valides à **mapper** peuvent bloquer le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="528ea-129">If you created a device that just supports the [core layer](overviews-direct3d-11-devices-layers.md), invalid parameters to **Map** can crash the operating system.</span></span> <span data-ttu-id="528ea-130">Si vous avez créé un appareil qui prend en charge la [couche de débogage](overviews-direct3d-11-devices-layers.md), la sortie de débogage signale une erreur sur cet appel de **mappage** non valide.</span><span class="sxs-lookup"><span data-stu-id="528ea-130">If you created a device that supports the [debug layer](overviews-direct3d-11-devices-layers.md), the debug output reports an error on this invalid **Map** call.</span></span>

### <a name="confine-source-box-within-source-and-destination-resources"></a><span data-ttu-id="528ea-131">Limiter la zone source dans les ressources source et de destination</span><span class="sxs-lookup"><span data-stu-id="528ea-131">Confine source box within source and destination resources</span></span>

<span data-ttu-id="528ea-132">Dans un appel à la méthode [**ID3D11DeviceContext :: CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) , la zone source doit se trouver dans la ressource source.</span><span class="sxs-lookup"><span data-stu-id="528ea-132">In a call to the [**ID3D11DeviceContext::CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) method, the source box must be within the source resource.</span></span> <span data-ttu-id="528ea-133">Les décalages de destination, (x, y et z) permettent de compenser la zone source lors de l’écriture dans la ressource de destination, mais les dimensions de la zone source et des décalages doivent être comprises dans la taille de la ressource.</span><span class="sxs-lookup"><span data-stu-id="528ea-133">The destination offsets, (x, y, and z) allow the source box to be offset when writing into the destination resource, but the dimensions of the source box and the offsets must be within the size of the resource.</span></span> <span data-ttu-id="528ea-134">Si vous essayez de copier en dehors de la ressource de destination ou si vous spécifiez une zone source supérieure à la ressource source, le comportement de **CopySubresourceRegion** n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="528ea-134">If you try to copy outside the destination resource or specify a source box that is larger than the source resource, the behavior of **CopySubresourceRegion** is undefined.</span></span> <span data-ttu-id="528ea-135">Si vous avez créé un appareil qui prend en charge la [couche de débogage](overviews-direct3d-11-devices-layers.md), la sortie de débogage signale une erreur sur cet appel **CopySubresourceRegion** non valide.</span><span class="sxs-lookup"><span data-stu-id="528ea-135">If you created a device that supports the [debug layer](overviews-direct3d-11-devices-layers.md), the debug output reports an error on this invalid **CopySubresourceRegion** call.</span></span> <span data-ttu-id="528ea-136">Des paramètres non valides pour **CopySubresourceRegion** provoquent un comportement indéfini et peuvent entraîner un rendu incorrect, un découpage, aucune copie ou même la suppression du périphérique de rendu.</span><span class="sxs-lookup"><span data-stu-id="528ea-136">Invalid parameters to **CopySubresourceRegion** cause undefined behavior and might result in incorrect rendering, clipping, no copy, or even the removal of the rendering device.</span></span>

### <a name="dont-drop-discardresource-or-discardview"></a><span data-ttu-id="528ea-137">Ne supprimez pas DiscardResource ou DiscardView</span><span class="sxs-lookup"><span data-stu-id="528ea-137">Don't drop DiscardResource or DiscardView</span></span>

<span data-ttu-id="528ea-138">Le runtime supprime un appel à [**ID3D11DeviceContext1 ::D iscardresource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) ou [**ID3D11DeviceContext1 ::D iscardview**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) , sauf si vous créez correctement la ressource.</span><span class="sxs-lookup"><span data-stu-id="528ea-138">The runtime drops a call to [**ID3D11DeviceContext1::DiscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) or [**ID3D11DeviceContext1::DiscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) unless you correctly create the resource.</span></span>

<span data-ttu-id="528ea-139">La ressource que vous transmettez à [**ID3D11DeviceContext1 ::D iscardresource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) doit avoir été créée à l’aide de la [**\_ \_ valeur par défaut**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) de l’utilisation de d3d11 ou de l' [**\_ utilisation \_ dynamique de d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), sinon le runtime supprime l’appel à **DiscardResource**.</span><span class="sxs-lookup"><span data-stu-id="528ea-139">The resource that you pass to [**ID3D11DeviceContext1::DiscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) must have been created by using [**D3D11\_USAGE\_DEFAULT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) or [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), otherwise the runtime drops the call to **DiscardResource**.</span></span>

<span data-ttu-id="528ea-140">La ressource sous-jacente de la vue que vous transmettez à [**ID3D11DeviceContext1 ::D iscardview**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) doit avoir été créée à l’aide de la [**\_ \_ valeur par défaut**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) de l’utilisation de d3d11 ou de l' [**\_ utilisation \_ dynamique de d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), sinon le runtime supprime l’appel à **DiscardView**.</span><span class="sxs-lookup"><span data-stu-id="528ea-140">The resource that underlies the view that you pass to [**ID3D11DeviceContext1::DiscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) must have been created using [**D3D11\_USAGE\_DEFAULT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) or [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), otherwise the runtime drops the call to **DiscardView**.</span></span>

<span data-ttu-id="528ea-141">Si vous avez créé un appareil qui prend en charge la [couche de débogage](overviews-direct3d-11-devices-layers.md), la sortie de débogage signale une erreur concernant l’appel supprimé.</span><span class="sxs-lookup"><span data-stu-id="528ea-141">If you created a device that supports the [debug layer](overviews-direct3d-11-devices-layers.md), the debug output reports an error regarding the dropped call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="528ea-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="528ea-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="528ea-143">Couches logicielles</span><span class="sxs-lookup"><span data-stu-id="528ea-143">Software Layers</span></span>](overviews-direct3d-11-devices-layers.md)
</dt> </dl>

 

 




