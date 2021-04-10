---
title: Entrée et sortie de données
description: Entrée et sortie de données
ms.assetid: a03b5327-65df-4cb9-a639-1e943ac28bfc
keywords:
- Plug-ins du lecteur Windows Media, entrée et sortie de données
- plug-ins, entrée et sortie de données
- plug-ins de traitement de signal numérique, entrée et sortie de données
- Plug-ins DSP, entrée et sortie de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39f66946dc796337d1f1e638cfe3828b3cbfbb6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100721"
---
# <a name="data-input-and-output"></a><span data-ttu-id="289c9-107">Entrée et sortie de données</span><span class="sxs-lookup"><span data-stu-id="289c9-107">Data Input and Output</span></span>

<span data-ttu-id="289c9-108">Le lecteur Windows Media fournit des données audio ou vidéo aux plug-ins DSP par le biais d’une mémoire tampon d’entrée allouée par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="289c9-108">Windows Media Player provides audio or video data to DSP plug-ins through an input buffer allocated by Windows Media Player.</span></span> <span data-ttu-id="289c9-109">Les plug-ins DSP renvoient des données traitées au lecteur Windows Media par le biais d’une mémoire tampon de sortie qui est également allouée par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="289c9-109">DSP plug-ins return processed data to Windows Media Player through an output buffer that is also allocated by Windows Media Player.</span></span> <span data-ttu-id="289c9-110">Le lecteur Windows Media gère le processus de passage de données entre lui-même et le plug-in DSP en appelant des méthodes implémentées par le plug-in.</span><span class="sxs-lookup"><span data-stu-id="289c9-110">Windows Media Player manages the process of passing data between itself and the DSP plug-in by calling methods implemented by the plug-in.</span></span> <span data-ttu-id="289c9-111">Pour un plug-in agissant comme un objet de média DirectX (DMO), le processus fonctionne comme suit :</span><span class="sxs-lookup"><span data-stu-id="289c9-111">For a plug-in acting as a DirectX Media Object (DMO), the process works as follows:</span></span>

1.  <span data-ttu-id="289c9-112">Le lecteur Windows Media appelle **IMediaObject ::P rocessinput**, en passant un pointeur vers un objet **IMediaBuffer** vers le plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="289c9-112">Windows Media Player calls **IMediaObject::ProcessInput**, passing a pointer to an **IMediaBuffer** object to the DSP plug-in.</span></span>
2.  <span data-ttu-id="289c9-113">Le plug-in DSP conserve un décompte de références sur l’objet de mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="289c9-113">The DSP plug-in keeps a reference count on the input buffer object.</span></span> <span data-ttu-id="289c9-114">Le plug-in DSP retourne une valeur **HRESULT** de réussite ou d’échec appropriée.</span><span class="sxs-lookup"><span data-stu-id="289c9-114">The DSP plug-in returns an appropriate success or failure **HRESULT**.</span></span>
3.  <span data-ttu-id="289c9-115">Le lecteur Windows Media appelle **IMediaObject ::P rocessoutput**, en passant un pointeur vers un tableau de structures de **\_ \_ \_ tampons de données de sortie DMO** (qui contiennent des mémoires tampons de sortie) vers le plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="289c9-115">Windows Media Player calls **IMediaObject::ProcessOutput**, passing a pointer to an array of **DMO\_OUTPUT\_DATA\_BUFFER** structures (which contain output buffers) to the DSP plug-in.</span></span>
4.  <span data-ttu-id="289c9-116">Le plug-in DSP traite les données dans la mémoire tampon d’entrée, puis copie les données dans la mémoire tampon de sortie appropriée.</span><span class="sxs-lookup"><span data-stu-id="289c9-116">The DSP plug-in processes the data in the input buffer and then copies the data to the appropriate output buffer.</span></span> <span data-ttu-id="289c9-117">Le plug-in DSP libère le décompte de références sur l’objet de mémoire tampon d’entrée lorsque toutes les données de la mémoire tampon ont été traitées.</span><span class="sxs-lookup"><span data-stu-id="289c9-117">The DSP plug-in releases the reference count on the input buffer object when all the data in the buffer has been processed.</span></span> <span data-ttu-id="289c9-118">Le plug-in DSP retourne alors un **HRESULT** de réussite ou d’échec approprié.</span><span class="sxs-lookup"><span data-stu-id="289c9-118">The DSP plug-in then returns an appropriate success or failure **HRESULT**.</span></span>
5.  <span data-ttu-id="289c9-119">Le lecteur Windows Media affiche le contenu dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="289c9-119">Windows Media Player renders the content in the output buffer.</span></span>

<span data-ttu-id="289c9-120">Pour un plug-in agissant en tant que Media Foundation Transform (MFT), le processus fonctionne comme suit :</span><span class="sxs-lookup"><span data-stu-id="289c9-120">For a plug-in acting as a Media Foundation Transform (MFT), the process works as follows:</span></span>

-   <span data-ttu-id="289c9-121">Le lecteur Windows Media appelle **IMFTransform ::P rocessinput**, en passant un pointeur vers un objet d’interface **IMFSample** vers le plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="289c9-121">Windows Media Player calls **IMFTransform::ProcessInput**, passing a pointer to an **IMFSample** interface object to the DSP plug-in.</span></span>
    1.  <span data-ttu-id="289c9-122">Le plug-in DSP conserve un décompte de références sur l’interface **IMFSample** .</span><span class="sxs-lookup"><span data-stu-id="289c9-122">The DSP plug-in keeps a reference count on the **IMFSample** interface.</span></span> <span data-ttu-id="289c9-123">Le plug-in DSP retourne une valeur **HRESULT** de réussite ou d’échec appropriée.</span><span class="sxs-lookup"><span data-stu-id="289c9-123">The DSP plug-in returns an appropriate success or failure **HRESULT**.</span></span>
    2.  <span data-ttu-id="289c9-124">Le lecteur Windows Media appelle **IMFTransform ::P rocessoutput**, en passant un pointeur vers un tableau de structures de **\_ \_ \_ mémoire tampon de données de sortie MFT** (qui contiennent des mémoires tampons de sortie) vers le plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="289c9-124">Windows Media Player calls **IMFTransform::ProcessOutput**, passing a pointer to an array of **MFT\_OUTPUT\_DATA\_BUFFER** structures (which contain output buffers) to the DSP plug-in.</span></span>
    3.  <span data-ttu-id="289c9-125">Le plug-in DSP traite les données dans la mémoire tampon d’entrée, puis copie les données dans la mémoire tampon de sortie appropriée.</span><span class="sxs-lookup"><span data-stu-id="289c9-125">The DSP plug-in processes the data in the input buffer and then copies the data to the appropriate output buffer.</span></span> <span data-ttu-id="289c9-126">Le plug-in DSP libère le décompte de références sur l’objet de mémoire tampon d’entrée lorsque toutes les données de la mémoire tampon ont été traitées.</span><span class="sxs-lookup"><span data-stu-id="289c9-126">The DSP plug-in releases the reference count on the input buffer object when all the data in the buffer has been processed.</span></span> <span data-ttu-id="289c9-127">Le plug-in DSP retourne alors un **HRESULT** de réussite ou d’échec approprié.</span><span class="sxs-lookup"><span data-stu-id="289c9-127">The DSP plug-in then returns an appropriate success or failure **HRESULT**.</span></span>
    4.  <span data-ttu-id="289c9-128">Le lecteur Windows Media affiche le contenu dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="289c9-128">Windows Media Player renders the content in the output buffer.</span></span>

<span data-ttu-id="289c9-129">Ce processus se répète continuellement lorsque le plug-in est activé et que le lecteur Windows Media a le contenu à afficher.</span><span class="sxs-lookup"><span data-stu-id="289c9-129">This process repeats continuously while the plug-in is enabled and Windows Media Player has content to render.</span></span>

> [!Note]  
> <span data-ttu-id="289c9-130">N’écrivez pas de code qui écrit des données dans la mémoire tampon d’entrée ou qui lit des données à partir de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="289c9-130">Do not write code that writes data to the input buffer or reads data from the output buffer.</span></span> <span data-ttu-id="289c9-131">L’accès incorrect aux tampons de données peut générer des résultats inattendus.</span><span class="sxs-lookup"><span data-stu-id="289c9-131">Incorrectly accessing data buffers may yield unexpected results.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="289c9-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="289c9-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="289c9-133">**Vue d’ensemble des développeurs de plug-ins DSP**</span><span class="sxs-lookup"><span data-stu-id="289c9-133">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




