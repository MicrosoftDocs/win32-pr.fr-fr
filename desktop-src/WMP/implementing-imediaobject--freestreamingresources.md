---
title: Implémentation de IMediaObject FreeStreamingResources
description: Implémentation de IMediaObject FreeStreamingResources
ms.assetid: 970dd10b-a7a0-4ba0-97e3-725d5c914500
keywords:
- Plug-ins du lecteur Windows Media, exemples de ressources de streaming d’écho
- plug-ins, exemples de ressources de streaming
- plug-ins de traitement de signal numérique, exemples de ressources de streaming d’écho
- Plug-ins DSP, exemples de ressources de streaming
- Echo DSP, exemple de plug-in, ressources de streaming
- Echo DSP, exemple de plug-in, libérer de la mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a31a293cfc68caf43496d031426de2441c9c1d05
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839686"
---
# <a name="implementing-imediaobjectfreestreamingresources"></a><span data-ttu-id="d9c10-109">Implémentation de IMediaObject :: FreeStreamingResources</span><span class="sxs-lookup"><span data-stu-id="d9c10-109">Implementing IMediaObject::FreeStreamingResources</span></span>

<span data-ttu-id="d9c10-110">Il est important que votre code libère toute mémoire allouée avant la destruction de l’objet de plug-in.</span><span class="sxs-lookup"><span data-stu-id="d9c10-110">It is important that your code releases any allocated memory before the plug-in object is destroyed.</span></span> <span data-ttu-id="d9c10-111">Le lecteur Windows Media appelle **FreeStreamingResources** pour vous permettre de le faire.</span><span class="sxs-lookup"><span data-stu-id="d9c10-111">Windows Media Player calls **FreeStreamingResources** to allow you to do this.</span></span> <span data-ttu-id="d9c10-112">Pour des raisons de sécurité, l’exemple créé par l’Assistant de plug-in comprend un appel à **FreeStreamingResources** dans la méthode **FinalRelease** pour garantir que la mémoire est libérée.</span><span class="sxs-lookup"><span data-stu-id="d9c10-112">For safety, the sample created by the plug-in wizard includes a call to **FreeStreamingResources** in the **FinalRelease** method to ensure that the memory is freed.</span></span> <span data-ttu-id="d9c10-113">Vous devez ajouter le code suivant à **FreeStreamingResources** pour l’exemple ECHO :</span><span class="sxs-lookup"><span data-stu-id="d9c10-113">You must add the following code to **FreeStreamingResources** for the Echo sample:</span></span>


```
// Test whether a buffer exists.
if (m_pbDelayBuffer)
{
    delete m_pbDelayBuffer;
    m_pbDelayBuffer = NULL;
    m_pbDelayPointer = NULL;
    m_cbDelayBuffer = 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="d9c10-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d9c10-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9c10-115">**Utilisation des ressources de streaming**</span><span class="sxs-lookup"><span data-stu-id="d9c10-115">**Working with Streaming Resources**</span></span>](working-with-streaming-resources.md)
</dt> </dl>

 

 




