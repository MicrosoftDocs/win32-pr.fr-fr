---
title: Implémentation d’un plug-in DSP audio
description: Implémentation d’un plug-in DSP audio
ms.assetid: 93ff0c45-f418-443d-8fba-c0a62f6e4e80
keywords:
- Plug-ins du lecteur Windows Media, DSP audio
- plug-ins, DSP audio
- plug-ins de traitement de signal numérique, implémentation du code
- Plug-ins DSP, implémentation du code
- plug-ins de traitement de signal numérique, modification de l’exemple de code
- Plug-ins DSP, modification de l’exemple de code
- plug-ins de traitement de signal numérique, implémentation audio
- Plug-ins DSP, implémentation audio
- plug-ins DSP audio, implémentation du code
- plug-ins DSP audio, modification de l’exemple de code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdde8e7f00fc9ea3ad9bb8b7adb2d0a8bfba6b32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029527"
---
# <a name="implementing-an-audio-dsp-plug-in"></a><span data-ttu-id="f1939-113">Implémentation d’un plug-in DSP audio</span><span class="sxs-lookup"><span data-stu-id="f1939-113">Implementing an Audio DSP Plug-in</span></span>

<span data-ttu-id="f1939-114">Pour créer un plug-in Windows Media Player DSP qui traite le son, vous devez modifier l’exemple de code dans la fonction nommée **DoProcessOutput**.</span><span class="sxs-lookup"><span data-stu-id="f1939-114">To create a Windows Media Player DSP plug-in that processes audio, you'll need to modify the sample code in the function named **DoProcessOutput**.</span></span> <span data-ttu-id="f1939-115">**DoProcessOutput** est appelée chaque fois que le lecteur Windows Media appelle **IMediaObject ::P rocessoutput**.</span><span class="sxs-lookup"><span data-stu-id="f1939-115">**DoProcessOutput** is called each time Windows Media Player successfully calls **IMediaObject::ProcessOutput**.</span></span> <span data-ttu-id="f1939-116">C’est la fonction qui effectue les tâches de traitement de signal numérique qui produisent le résultat audible que le plug-in DSP est destiné à produire.</span><span class="sxs-lookup"><span data-stu-id="f1939-116">It is the function that performs the digital signal processing tasks that produce the audible result that the DSP plug-in is intended to produce.</span></span>

<span data-ttu-id="f1939-117">Le traitement d’un flux audio est semblable à la gestion d’un événement chronométré.</span><span class="sxs-lookup"><span data-stu-id="f1939-117">Processing an audio stream is like handling a timed event.</span></span> <span data-ttu-id="f1939-118">**DoProcessOutput** sera appelé à plusieurs reprises et à des intervalles spécifiques.</span><span class="sxs-lookup"><span data-stu-id="f1939-118">**DoProcessOutput** will be called repeatedly and at specific intervals.</span></span> <span data-ttu-id="f1939-119">Chaque fois que votre code s’exécute, il doit traiter un nombre spécifique d’octets de données.</span><span class="sxs-lookup"><span data-stu-id="f1939-119">Each time your code executes, it will need to process a specific number of bytes of data.</span></span> <span data-ttu-id="f1939-120">**DoProcessOutput** contient les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="f1939-120">**DoProcessOutput** contains the following parameters:</span></span>



| <span data-ttu-id="f1939-121">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f1939-121">Parameter</span></span>          | <span data-ttu-id="f1939-122">Description</span><span class="sxs-lookup"><span data-stu-id="f1939-122">Description</span></span>                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1939-123">*pbOutputData*</span><span class="sxs-lookup"><span data-stu-id="f1939-123">*pbOutputData*</span></span>     | <span data-ttu-id="f1939-124">Il s’agit d’un pointeur d' **octet** vers la mémoire tampon dans laquelle votre implémentation de **DoProcessOutput** doit copier ses données traitées.</span><span class="sxs-lookup"><span data-stu-id="f1939-124">This is a **BYTE** pointer to the buffer where your implementation of **DoProcessOutput** must copy its processed data.</span></span> |
| <span data-ttu-id="f1939-125">*pbInputData*</span><span class="sxs-lookup"><span data-stu-id="f1939-125">*pbInputData*</span></span>      | <span data-ttu-id="f1939-126">Il s’agit d’un pointeur d' **octet** constant vers la mémoire tampon qui contient les données à traiter.</span><span class="sxs-lookup"><span data-stu-id="f1939-126">This is a constant **BYTE** pointer to the buffer that contains the data to be processed.</span></span>                               |
| <span data-ttu-id="f1939-127">*cbBytesToProcess*</span><span class="sxs-lookup"><span data-stu-id="f1939-127">*cbBytesToProcess*</span></span> | <span data-ttu-id="f1939-128">Il s’agit d’une valeur **DWORD** qui contient le nombre d’octets dans la mémoire tampon d’entrée à traiter.</span><span class="sxs-lookup"><span data-stu-id="f1939-128">This is a **DWORD** value that contains a count of the number of bytes in the input buffer to be processed.</span></span>             |



 

<span data-ttu-id="f1939-129">Les sections suivantes fournissent des détails sur la modification du code généré par l’Assistant de plug-in du lecteur Windows Media pour créer votre propre plug-in de DSP audio :</span><span class="sxs-lookup"><span data-stu-id="f1939-129">The following sections provide details about how to modify the code generated by the Windows Media Player Plug-in Wizard to create your own audio DSP plug-in:</span></span>

-   [<span data-ttu-id="f1939-130">Implémentation de DoProcessOutput</span><span class="sxs-lookup"><span data-stu-id="f1939-130">Implementing DoProcessOutput</span></span>](implementing-doprocessoutput.md)
-   [<span data-ttu-id="f1939-131">Ajout de propriétés à l’exemple de plug-in DSP audio</span><span class="sxs-lookup"><span data-stu-id="f1939-131">Adding Properties to the Sample Audio DSP Plug-in</span></span>](adding-properties-to-the-sample-audio-dsp-plug-in.md)
-   [<span data-ttu-id="f1939-132">Implémentation de la page de propriétés pour un plug-in DSP</span><span class="sxs-lookup"><span data-stu-id="f1939-132">Implementing the Property Page for a DSP Plug-in</span></span>](implementing-the-property-page-for-a-dsp-plug-in.md)
-   [<span data-ttu-id="f1939-133">Modification de la propriété exemple de plug-in DSP audio</span><span class="sxs-lookup"><span data-stu-id="f1939-133">Changing the Sample Audio DSP Plug-in Property</span></span>](changing-the-sample-audio-dsp-plug-in-property.md)
-   [<span data-ttu-id="f1939-134">À propos de la discontinuité</span><span class="sxs-lookup"><span data-stu-id="f1939-134">About Discontinuity</span></span>](about-discontinuity.md)
-   [<span data-ttu-id="f1939-135">À propos de l’allocation des ressources de streaming</span><span class="sxs-lookup"><span data-stu-id="f1939-135">About Allocating Streaming Resources</span></span>](about-allocating-streaming-resources.md)

## <a name="related-topics"></a><span data-ttu-id="f1939-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f1939-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1939-137">**À propos des plug-ins DSP**</span><span class="sxs-lookup"><span data-stu-id="f1939-137">**About DSP Plug-ins**</span></span>](about-dsp-plug-ins.md)
</dt> </dl>

 

 




