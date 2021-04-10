---
title: Prise en charge de DRM dans DirectShow
description: Prise en charge de DRM dans DirectShow
ms.assetid: f464d4a4-3478-489a-b9ce-8ab1acabc3c8
keywords:
- Windows Media Format SDK, prise en charge de DRM dans DirectShow
- Windows Media Format SDK, DirectShow
- Kit de développement logiciel (SDK) Windows Media format, gestion des droits numériques (DRM)
- ASF (Advanced Systems Format), prise en charge de DRM dans DirectShow
- ASF (format de systèmes avancés), prise en charge de DRM dans DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- ASF (Advanced Systems Format), gestion des droits numériques (DRM)
- ASF (format de systèmes avancés), gestion des droits numériques (DRM)
- DirectShow, prise en charge de DRM
- gestion des droits numériques (DRM), DirectShow
- DRM (gestion des droits numériques), DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85a211a3d3b438bac246c0bd90759f648818ac2e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103940671"
---
# <a name="drm-support-in-directshow"></a><span data-ttu-id="ac79b-115">Prise en charge de DRM dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="ac79b-115">DRM Support in DirectShow</span></span>

<span data-ttu-id="ac79b-116">La lecture et l’écriture de fichiers protégés par DRM dans DirectShow s’effectuent de la même façon que lorsque vous utilisez directement le kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ac79b-116">Reading and writing DRM-protected files in DirectShow is done in basically the same way as when you use the Windows Media Format SDK directly.</span></span> <span data-ttu-id="ac79b-117">Pour commencer, vous avez besoin de la bibliothèque statique wmstubdrm, qui est obtenue séparément de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ac79b-117">To begin with, you need the wmstubdrm static library, which is obtained separately from Microsoft.</span></span> <span data-ttu-id="ac79b-118">En outre, vous devez implémenter l’interface **IKeyProvider** pour permettre à votre application d’accéder aux objets d’exécution du kit de développement logiciel (SDK) du format Windows Media lorsque la gestion DRM est activée.</span><span class="sxs-lookup"><span data-stu-id="ac79b-118">In addition, you must implement the **IKeyProvider** interface to enable your application to access the Windows Media Format SDK run-time objects when DRM is enabled.</span></span>

<span data-ttu-id="ac79b-119">Lors de l’application de la protection DRM version 1, utilisez l’interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) , qui est obtenue comme décrit dans [lecture de fichiers ASF dans DirectShow](reading-asf-files-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="ac79b-119">When applying DRM version 1 protection, use the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface, which is obtained as described in [Reading ASF Files in DirectShow](reading-asf-files-in-directshow.md).</span></span> <span data-ttu-id="ac79b-120">Lors de l’application de la protection DRM version 7, obtenez l’interface [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) en appelant **QueryService** sur le filtre du [writer WM ASF](wm-asf-writer-filter.md) , comme indiqué dans l’extrait de code, plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="ac79b-120">When applying DRM version 7 protection, obtain the [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) interface by calling **QueryService** on the [WM ASF Writer](wm-asf-writer-filter.md) filter, as shown in the code snippet later in this topic.</span></span>

<span data-ttu-id="ac79b-121">Toutes les autres configurations spécifiques à DRM sont exactement les mêmes que celles décrites dans activation de la [prise en charge de DRM](enabling-drm-support.md).</span><span class="sxs-lookup"><span data-stu-id="ac79b-121">All other DRM-specific configuration is exactly the same as described in [Enabling DRM Support](enabling-drm-support.md).</span></span> <span data-ttu-id="ac79b-122">Utilisez **QueryService** pour obtenir l’interface [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) à partir du filtre de [lecteur ASF WM](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="ac79b-122">Use **QueryService** to obtain the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface from the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>

<span data-ttu-id="ac79b-123">DirectX 9,0 contient un exemple, PlayWndASF, une application de lecteur DirectShow compatible DRM qui illustre l’acquisition de licence DRM version 1 et version 7.</span><span class="sxs-lookup"><span data-stu-id="ac79b-123">DirectX 9.0 contains a sample, PlayWndASF, a DRM-enabled DirectShow player application that demonstrates DRM version 1 and version 7 license acquisition.</span></span> <span data-ttu-id="ac79b-124">Cet exemple comprend également une implémentation de la classe **CKeyProvider** , qui prend en charge l’interface **IKeyProvider** .</span><span class="sxs-lookup"><span data-stu-id="ac79b-124">This sample also includes an implementation of the **CKeyProvider** class, which supports the **IKeyProvider** interface.</span></span>

 

 




