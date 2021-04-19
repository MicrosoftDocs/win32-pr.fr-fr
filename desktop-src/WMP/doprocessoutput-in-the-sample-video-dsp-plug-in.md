---
title: DoProcessOutput dans l’exemple de plug-in DSP de vidéo
description: DoProcessOutput dans l’exemple de plug-in DSP de vidéo
ms.assetid: 67536e35-a049-49c8-bd89-fad1fab37e6c
keywords:
- Plug-ins du lecteur Windows Media, DSP vidéo
- plug-ins, DSP vidéo
- plug-ins de traitement de signal numérique, DoProcessOutput
- Plug-ins DSP, DoProcessOutput
- plug-ins vidéo DSP, DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff3bc844890930209a1c6007213d3c466f0cd15b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106541582"
---
# <a name="doprocessoutput-in-the-sample-video-dsp-plug-in"></a><span data-ttu-id="aa53a-108">DoProcessOutput dans l’exemple de plug-in DSP de vidéo</span><span class="sxs-lookup"><span data-stu-id="aa53a-108">DoProcessOutput in the Sample Video DSP Plug-in</span></span>

<span data-ttu-id="aa53a-109">Étant donné qu’un plug-in de DSP vidéo prend généralement en charge plusieurs formats vidéo, il est commode de séparer le code d’implémentation de traitement dans une fonction distincte pour chaque format.</span><span class="sxs-lookup"><span data-stu-id="aa53a-109">Because a video DSP plug-in typically supports several video formats, it is convenient to separate the processing implementation code into a separate function for each format.</span></span> <span data-ttu-id="aa53a-110">Cela signifie que l’implémentation de **DoProcessOutput** pour les plug-ins de vidéo DSP est relativement simple.</span><span class="sxs-lookup"><span data-stu-id="aa53a-110">This means that the implementation of **DoProcessOutput** for video DSP plug-ins is relatively simple.</span></span>

<span data-ttu-id="aa53a-111">L’implémentation dans l’exemple de plug-in teste d’abord si l’utilisateur a activé le plug-in.</span><span class="sxs-lookup"><span data-stu-id="aa53a-111">The implementation in the sample plug-in first tests whether the user has enabled the plug-in.</span></span> <span data-ttu-id="aa53a-112">Si le plug-in est désactivé, le code copie les données fournies dans la mémoire tampon d’entrée dans la mémoire tampon de sortie sans le modifier, comme le montre le code suivant :</span><span class="sxs-lookup"><span data-stu-id="aa53a-112">If the plug-in is disabled, the code copies the data provided in the input buffer to the output buffer without changing it, as the following code demonstrates:</span></span>


```C++
// Test whether the plug-in has been disabled by the user.
if (!m_bEnabled)
{
    // Just copy the data without changing it. You should
    // also do any necessary format conversion here.
    memcpy(pbOutputData, pbInputData, m_dwBufferSize);
    *cbBytesProcessed = m_dwBufferSize;

    return S_OK;
}

```



<span data-ttu-id="aa53a-113">Si le plug-in est activé, le code effectue simplement une série de vérifications sur le membre de sous- **type** de type de média d’entrée pour déterminer le format vidéo actuel.</span><span class="sxs-lookup"><span data-stu-id="aa53a-113">If the plug-in is enabled, the code simply performs a series of checks on the input media type **subtype** member to determine the current video format.</span></span> <span data-ttu-id="aa53a-114">Lorsqu’une correspondance est trouvée, le code appelle la fonction de traitement appropriée.</span><span class="sxs-lookup"><span data-stu-id="aa53a-114">When a match is found, the code calls the appropriate processing function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa53a-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aa53a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa53a-116">**Implémentation d’un plug-in de DSP vidéo**</span><span class="sxs-lookup"><span data-stu-id="aa53a-116">**Implementing a Video DSP Plug-in**</span></span>](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 




