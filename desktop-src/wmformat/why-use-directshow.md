---
title: Pourquoi utiliser DirectShow ?
description: Pourquoi utiliser DirectShow ?
ms.assetid: 0ab33526-73d0-425e-a03f-29c74555f578
keywords:
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, matériel
- Kit de développement logiciel (SDK) Windows Media format, Windows Driver Model (WDM)
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- ASF (Advanced Systems Format), matériel
- ASF (format des systèmes avancés), matériel
- ASF (Advanced Systems Format), Windows Driver Model (WDM)
- ASF (format des systèmes avancés), Windows Driver Model (WDM)
- DirectShow, à propos de
- DirectShow, matériel
- DirectShow, Windows Driver Model (WDM)
- Windows Driver Model (WDM)
- WDM (Windows Driver Model)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f90fa1de01a7b136b938f9b09cc7fb2b3c229fad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673114"
---
# <a name="why-use-directshow"></a><span data-ttu-id="7984c-117">Pourquoi utiliser DirectShow ?</span><span class="sxs-lookup"><span data-stu-id="7984c-117">Why Use DirectShow?</span></span>

<span data-ttu-id="7984c-118">Il existe deux raisons principales pour lesquelles une application peut utiliser DirectShow plutôt que le kit de développement logiciel (SDK) de format Windows Media directement : pour la commodité de l’architecture de diffusion en continu DirectShow et pour l’accès au matériel.</span><span class="sxs-lookup"><span data-stu-id="7984c-118">There are two main reasons why an application might use DirectShow rather than the Windows Media Format SDK directly: for the convenience of the DirectShow streaming architecture, and for access to hardware.</span></span>

## <a name="convenience"></a><span data-ttu-id="7984c-119">Aspect pratique</span><span class="sxs-lookup"><span data-stu-id="7984c-119">Convenience</span></span>

<span data-ttu-id="7984c-120">Avec l’architecture de diffusion en continu DirectShow, il n’y a que quelques appels de méthode pour lire Windows Media Audio ou Windows Media Video fichiers.</span><span class="sxs-lookup"><span data-stu-id="7984c-120">With DirectShow streaming architecture, it takes only a few method calls to play Windows Media Audio or Windows Media Video files.</span></span> <span data-ttu-id="7984c-121">La création de fichiers est également simplifiée.</span><span class="sxs-lookup"><span data-stu-id="7984c-121">Creating files is also simplified.</span></span> <span data-ttu-id="7984c-122">Vous spécifiez simplement un profil à l’aide de l’interface **IConfigAsfWriter** sur le filtre, et DirectShow charge automatiquement les composants requis pour le rendu ou l’écriture des flux, et fournit les mécanismes de transfert et de synchronisation du flux de données multimédias.</span><span class="sxs-lookup"><span data-stu-id="7984c-122">You simply specify a profile using the **IConfigAsfWriter** interface on the filter, and DirectShow automatically loads the required components for rendering or writing the streams, and provides the mechanisms for transferring and synchronizing the flow of media data.</span></span> <span data-ttu-id="7984c-123">DirectShow est particulièrement utile lors de la conversion de contenu à partir de formats variés au format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="7984c-123">DirectShow is especially useful when converting content from varied formats into Windows Media Format.</span></span> <span data-ttu-id="7984c-124">Vous pouvez créer des graphiques de filtre DirectShow qui décodent un large éventail de types de fichiers et de compression, puis qui alimentent les flux décodés dans le filtre de l' [enregistreur ASF WM](wm-asf-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="7984c-124">You can create DirectShow filter graphs that decode a wide variety of file and compression types, and then feed the decoded streams into the [WM ASF Writer](wm-asf-writer-filter.md) filter.</span></span> <span data-ttu-id="7984c-125">Par comparaison, l’exemple UncompAVItoWMV dans ce kit de développement logiciel (SDK) fonctionne uniquement avec les fichiers AVI non compressés.</span><span class="sxs-lookup"><span data-stu-id="7984c-125">By comparison, the UncompAVItoWMV sample in this SDK works only with uncompressed AVI files.</span></span> <span data-ttu-id="7984c-126">Les flux de texte et les flux de données arbitraires peuvent également être créés et/ou rendus par le biais de DirectShow, mais cela peut nécessiter la création de filtres DirectShow personnalisés pour le traitement de ces flux.</span><span class="sxs-lookup"><span data-stu-id="7984c-126">Text streams and arbitrary data streams can also be created and/or rendered through DirectShow, but this might require you to create custom DirectShow filters for processing those streams.</span></span>

## <a name="access-to-hardware"></a><span data-ttu-id="7984c-127">Accès au matériel</span><span class="sxs-lookup"><span data-stu-id="7984c-127">Access to Hardware</span></span>

<span data-ttu-id="7984c-128">DirectShow est le seul moyen pour le code d’application d’accéder à des périphériques matériels basés sur des Windows Driver Model (WDM), tels que les caméras DV 1394, les tuners TV et les webcams USB.</span><span class="sxs-lookup"><span data-stu-id="7984c-128">DirectShow is the only way for application code to access Windows Driver Model (WDM)–based hardware devices such as 1394 DV cameras, TV tuners, and USB webcams.</span></span> <span data-ttu-id="7984c-129">Si votre application doit capturer les données directement à partir d’un périphérique matériel WDM et les transcoder au format Windows Media, et que le kit de développement logiciel (SDK) de l’encodeur Windows Media ne répond pas à vos besoins, DirectShow est la seule alternative.</span><span class="sxs-lookup"><span data-stu-id="7984c-129">If your application must capture data directly from a WDM-based hardware device and transcode it to Windows Media Format, and the Windows Media Encoder SDK does not suit your needs, then DirectShow is the only alternative.</span></span> <span data-ttu-id="7984c-130">DirectShow peut également être utilisé pour accéder à des appareils hérités basés sur la vidéo pour Windows.</span><span class="sxs-lookup"><span data-stu-id="7984c-130">DirectShow can also be used to access legacy devices based on Video for Windows.</span></span>

 

 




