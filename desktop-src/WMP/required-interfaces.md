---
title: Interfaces requises (Windows Media Player SDK)
description: En savoir plus sur les interfaces requises que le lecteur Windows Media implémente dans DirectShow ou Media Foundation.
ms.assetid: 202d5769-edff-46df-bc05-bbb630a8f3f4
keywords:
- Plug-ins du lecteur Windows Media, interfaces
- plug-ins, interfaces
- plug-ins de traitement de signal numérique, interfaces
- Plug-ins DSP, interfaces
- interfaces, plug-ins DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d27a0c0ed56db5f35c8cde8203fcf99a81a9260
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406092"
---
# <a name="required-interfaces-windows-media-player-sdk"></a><span data-ttu-id="eaf6c-108">Interfaces requises (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="eaf6c-108">Required Interfaces (Windows Media Player SDK)</span></span>

<span data-ttu-id="eaf6c-109">Le lecteur Windows Media effectue le rendu des données audio et vidéo à l’aide de l’un des pipelines suivants.</span><span class="sxs-lookup"><span data-stu-id="eaf6c-109">Windows Media Player renders audio and video by using one of the following pipelines.</span></span>

-   <span data-ttu-id="eaf6c-110">DirectShow</span><span class="sxs-lookup"><span data-stu-id="eaf6c-110">DirectShow</span></span>
-   <span data-ttu-id="eaf6c-111">Media Foundation</span><span class="sxs-lookup"><span data-stu-id="eaf6c-111">Media Foundation</span></span>

<span data-ttu-id="eaf6c-112">Dans Microsoft Windows XP et les versions antérieures, le lecteur utilise DirectShow.</span><span class="sxs-lookup"><span data-stu-id="eaf6c-112">In Microsoft Windows XP and earlier, the Player uses DirectShow.</span></span> <span data-ttu-id="eaf6c-113">Dans Windows Vista, le lecteur utilise parfois DirectShow et utilise parfois Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="eaf6c-113">In Windows Vista, the Player sometimes uses DirectShow and sometimes uses Media Foundation.</span></span>

<span data-ttu-id="eaf6c-114">Un plug-in DSP implémente une partie ou l’ensemble des interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="eaf6c-114">A DSP plug-in implements some or all of the following interfaces:</span></span>

-   <span data-ttu-id="eaf6c-115">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="eaf6c-115">**IMediaObject**</span></span>
-   <span data-ttu-id="eaf6c-116">**IWMPPluginEnable**</span><span class="sxs-lookup"><span data-stu-id="eaf6c-116">**IWMPPluginEnable**</span></span>
-   <span data-ttu-id="eaf6c-117">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="eaf6c-117">**IMFTransform**</span></span>
-   <span data-ttu-id="eaf6c-118">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="eaf6c-118">**IMFGetService**</span></span>
-   <span data-ttu-id="eaf6c-119">**ISpecifyPropertyPages**</span><span class="sxs-lookup"><span data-stu-id="eaf6c-119">**ISpecifyPropertyPages**</span></span>

<span data-ttu-id="eaf6c-120">Un plug-in qui implémente **IMediaObject** et **IWMPPluginEnable** peut s’exécuter dans le pipeline DirectShow.</span><span class="sxs-lookup"><span data-stu-id="eaf6c-120">A plug-in that implements **IMediaObject** and **IWMPPluginEnable** can run in the DirectShow pipeline.</span></span> <span data-ttu-id="eaf6c-121">Il peut également s’exécuter dans le pipeline Media Foundation à l’intérieur d’un wrapper fourni par Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="eaf6c-121">It can also run in the Media Foundation Pipeline inside a wrapper provided by Media Foundation.</span></span> <span data-ttu-id="eaf6c-122">Un plug-in de ce type est appelé Microsoft DirectX Media Object (DMO).</span><span class="sxs-lookup"><span data-stu-id="eaf6c-122">A plug-in of this type is called a Microsoft DirectX Media Object (DMO).</span></span> <span data-ttu-id="eaf6c-123">Il est courant de considérer qu’un DMO est analogue à un objet filtre dans DirectShow.</span><span class="sxs-lookup"><span data-stu-id="eaf6c-123">It is common to think of a DMO as being analogous to a filter object in DirectShow.</span></span> <span data-ttu-id="eaf6c-124">La documentation DMO se trouve dans la section DirectShow du SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="eaf6c-124">The DMO documentation is in the DirectShow section of the Windows SDK.</span></span>

<span data-ttu-id="eaf6c-125">Un plug-in qui implémente **IMFTransform** et **IMFGetService** peut s’exécuter en mode natif (aucun Wrapper requis) dans le pipeline Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="eaf6c-125">A plug-in that implements **IMFTransform** and **IMFGetService** can run natively (no wrapper required) in the Media Foundation pipeline.</span></span> <span data-ttu-id="eaf6c-126">Un plug-in de ce type est appelé Media Foundation transformation (MFT).</span><span class="sxs-lookup"><span data-stu-id="eaf6c-126">A plug-in of this type is called a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="eaf6c-127">La documentation MFT se trouve dans la section Media Foundation de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="eaf6c-127">The MFT documentation is in the Media Foundation section of the Windows SDK.</span></span>

<span data-ttu-id="eaf6c-128">Un plug-in qui implémente **IMediaObject**, **IWMPPluginEnable**, **IMFTransform** et **IMFGetService** peut s’exécuter dans le pipeline DirectShow et peut également s’exécuter en mode natif dans le pipeline Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="eaf6c-128">A plug-in that implements **IMediaObject**, **IWMPPluginEnable**, **IMFTransform**, and **IMFGetService** can run in the DirectShow pipeline and can also run natively in the Media Foundation pipeline.</span></span> <span data-ttu-id="eaf6c-129">Ce type de plug-in, qui est appelé un *plug-in DSP à double mode*, peut jouer le rôle d’un module DMO ou d’une table MFT.</span><span class="sxs-lookup"><span data-stu-id="eaf6c-129">This type of plug-in, which is called a *dual-mode DSP plug-in*, can play the role of a DMO or an MFT.</span></span>

<span data-ttu-id="eaf6c-130">Lorsque le lecteur Windows Media utilise un plug-in DSP à double mode dans le pipeline Media Foundation, il commence par interroger l’interface **IMFTransform** .</span><span class="sxs-lookup"><span data-stu-id="eaf6c-130">When Windows Media Player uses a dual-mode DSP plug-in in the Media Foundation pipeline, it first queries for the **IMFTransform** interface.</span></span> <span data-ttu-id="eaf6c-131">Si cette requête échoue, le lecteur Windows Media recherche l’interface **IMediaObject** .</span><span class="sxs-lookup"><span data-stu-id="eaf6c-131">If that query fails, Windows Media Player queries for the **IMediaObject** interface.</span></span> <span data-ttu-id="eaf6c-132">Si la requête **IMediaObject** est réussie, le plug-in est encapsulé et ajouté au pipeline Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="eaf6c-132">If the **IMediaObject** query is successful, the plug-in is wrapped and added to the Media Foundation pipeline.</span></span>

<span data-ttu-id="eaf6c-133">Quel que soit le pipeline, tout plug-in DSP permettant à l’utilisateur de définir des propriétés doit implémenter **ISpecifyPropertyPages**.</span><span class="sxs-lookup"><span data-stu-id="eaf6c-133">Regardless of the pipeline, any DSP plug-in that allows the user to set properties must implement **ISpecifyPropertyPages**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eaf6c-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eaf6c-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eaf6c-135">**Vue d’ensemble des développeurs de plug-ins DSP**</span><span class="sxs-lookup"><span data-stu-id="eaf6c-135">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> <dt>

[<span data-ttu-id="eaf6c-136">**Interfaces du plug-in DSP**</span><span class="sxs-lookup"><span data-stu-id="eaf6c-136">**DSP Plug-in Interfaces**</span></span>](dsp-plug-in-interfaces.md)
</dt> <dt>

[<span data-ttu-id="eaf6c-137">**Empaquetage du plug-in DSP**</span><span class="sxs-lookup"><span data-stu-id="eaf6c-137">**DSP Plug-in Packaging**</span></span>](dsp-plug-in-packaging.md)
</dt> </dl>

 

 




