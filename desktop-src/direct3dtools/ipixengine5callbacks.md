---
description: Rappels utilisés pour afficher les textures.
MS-HAID: vspixengine.IPixEngine5Callbacks
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IPixEngine5Callbacks
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F87F00ED-C816-49A3-926B-28E3C8330EA2
api_name:
- IPixEngine5Callbacks
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 80f00a0d7e2e3478114d94480e01e31add63ef90
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109315"
---
# <a name="span-idvspixengineipixengine5callbacksspanipixengine5callbacks-interface"></a><span data-ttu-id="3f62e-103"><span id="vspixengine.ipixengine5callbacks"></span>Interface IPixEngine5Callbacks</span><span class="sxs-lookup"><span data-stu-id="3f62e-103"><span id="vspixengine.ipixengine5callbacks"></span>IPixEngine5Callbacks interface</span></span>

<span data-ttu-id="3f62e-104">Rappels utilisés pour afficher les textures.</span><span class="sxs-lookup"><span data-stu-id="3f62e-104">Callbacks used for viewing textures.</span></span>

## <a name="members"></a><span data-ttu-id="3f62e-105">Membres</span><span class="sxs-lookup"><span data-stu-id="3f62e-105">Members</span></span>

<span data-ttu-id="3f62e-106">L’interface **IPixEngine5Callbacks** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3f62e-106">The **IPixEngine5Callbacks** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3f62e-107">**IPixEngine5Callbacks** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3f62e-107">**IPixEngine5Callbacks** also has these types of members:</span></span>

-   [<span data-ttu-id="3f62e-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3f62e-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="3f62e-109"><span id="methods"></span>Méthodes</span><span class="sxs-lookup"><span data-stu-id="3f62e-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="3f62e-110">L’interface **IPixEngine5Callbacks** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="3f62e-110">The **IPixEngine5Callbacks** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="3f62e-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="3f62e-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="3f62e-112">Description</span><span class="sxs-lookup"><span data-stu-id="3f62e-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="3f62e-113"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-freetexturecomplete"><strong>FreeTextureComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="3f62e-113"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-freetexturecomplete"><strong>FreeTextureComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="3f62e-114">Fonction de rappel utilisée pour notifier l’hôte lorsqu’une texture a été libérée.</span><span class="sxs-lookup"><span data-stu-id="3f62e-114">A callback function used to notify the host when a texture has been freed.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="3f62e-115"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadhistogramcomplete-pixenginehistogram-ptr"><strong>LoadHistogramComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="3f62e-115"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadhistogramcomplete-pixenginehistogram-ptr"><strong>LoadHistogramComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="3f62e-116">Fonction de rappel utilisée pour notifier l’hôte lorsqu’une charge d’histogramme est terminée.</span><span class="sxs-lookup"><span data-stu-id="3f62e-116">A callback function used to notify the host when a histogram load has been completed.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="3f62e-117"><a href="/previous-versions/windows/desktop/legacy/mt432759(v=vs.85)"><strong>LoadTextureFromFileComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="3f62e-117"><a href="/previous-versions/windows/desktop/legacy/mt432759(v=vs.85)"><strong>LoadTextureFromFileComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="3f62e-118">Fonction de rappel utilisée pour notifier l’hôte quand une charge de texture est terminée.</span><span class="sxs-lookup"><span data-stu-id="3f62e-118">A callback function used to notify the host when a texture load has been completed.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="3f62e-119"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadtextureslicecomplete-pixenginetextureslicedescriptor-pixenginehistogram-ptr"><strong>LoadTextureSliceComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="3f62e-119"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadtextureslicecomplete-pixenginetextureslicedescriptor-pixenginehistogram-ptr"><strong>LoadTextureSliceComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="3f62e-120">Fonction de rappel utilisée pour notifier l’hôte lorsqu’un chargement de la tranche de texture est terminé.</span><span class="sxs-lookup"><span data-stu-id="3f62e-120">A callback function used to notify the host when a texture slice load has been completed.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="3f62e-121"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-readtexelvaluecomplete-uint-bstr-arr-double-arr"><strong>ReadTexelValueComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="3f62e-121"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-readtexelvaluecomplete-uint-bstr-arr-double-arr"><strong>ReadTexelValueComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="3f62e-122">Fonction de rappel utilisée pour notifier l’hôte lorsqu’une valeur Texel lue est terminée.</span><span class="sxs-lookup"><span data-stu-id="3f62e-122">A callback function used to notify the host when a texel value read has been completed.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="3f62e-123"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-rendertexturecomplete"><strong>RenderTextureComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="3f62e-123"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-rendertexturecomplete"><strong>RenderTextureComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="3f62e-124">Fonction de rappel utilisée pour notifier l’hôte lorsqu’un rendu de texture est terminé.</span><span class="sxs-lookup"><span data-stu-id="3f62e-124">A callback function used to notify the host when a texture render has been completed.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="3f62e-125"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-savetexturecomplete"><strong>SaveTextureComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="3f62e-125"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-savetexturecomplete"><strong>SaveTextureComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="3f62e-126">Fonction de rappel utilisée pour notifier l’hôte lorsque l’enregistrement d’une texture est terminé.</span><span class="sxs-lookup"><span data-stu-id="3f62e-126">A callback function used to notify the host when saving a texture has been completed.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="3f62e-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f62e-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="3f62e-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="3f62e-128">Header</span></span></p></td><td><span data-ttu-id="3f62e-129">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="3f62e-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
