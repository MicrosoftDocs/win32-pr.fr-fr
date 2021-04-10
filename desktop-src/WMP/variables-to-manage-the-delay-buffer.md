---
title: Variables pour gérer la mémoire tampon de délai
description: Variables pour gérer la mémoire tampon de délai
ms.assetid: 2c5963a1-04e2-4421-8f56-14c1e059de4e
keywords:
- Plug-ins du lecteur Windows Media, exemples de ressources de streaming d’écho
- plug-ins, exemples de ressources de streaming
- plug-ins de traitement de signal numérique, exemples de ressources de streaming d’écho
- Plug-ins DSP, exemples de ressources de streaming
- Echo DSP, exemple de plug-in, ressources de streaming
- Echo DSP, exemple de plug-in, tampon de délai
- mémoire tampon de délai
- mémoires tampons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d7f9657d16d0805ff2fc85d2238635fbfa6e5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196940"
---
# <a name="variables-to-manage-the-delay-buffer"></a><span data-ttu-id="d6c2e-111">Variables pour gérer la mémoire tampon de délai</span><span class="sxs-lookup"><span data-stu-id="d6c2e-111">Variables to Manage the Delay Buffer</span></span>

<span data-ttu-id="d6c2e-112">Vous devez ajouter les déclarations pour les variables membres dont vous avez besoin pour gérer la mémoire tampon de délai.</span><span class="sxs-lookup"><span data-stu-id="d6c2e-112">You must add the declarations for the member variables you need to manage the delay buffer.</span></span> <span data-ttu-id="d6c2e-113">Ajoutez les déclarations suivantes à ECHO. h dans la section « private » :</span><span class="sxs-lookup"><span data-stu-id="d6c2e-113">Add the following declarations to Echo.h in the "private" section:</span></span>


```C++
DWORD  m_cbDelayBuffer;   // Count of bytes in delay buffer size.
BYTE*  m_pbDelayPointer;  // Movable pointer to delay buffer.
BYTE*  m_pbDelayBuffer;   // Pointer to the head of the delay buffer.

```



<span data-ttu-id="d6c2e-114">Ajoutez le code suivant au constructeur CEcho pour initialiser les variables de mémoire tampon de délai :</span><span class="sxs-lookup"><span data-stu-id="d6c2e-114">Add the following code to the CEcho constructor to initialize the delay buffer variables:</span></span>


```C++
m_pbDelayBuffer = NULL;
m_pbDelayPointer = NULL;
m_cbDelayBuffer = 0;

```



## <a name="related-topics"></a><span data-ttu-id="d6c2e-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d6c2e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6c2e-116">**Utilisation des ressources de streaming**</span><span class="sxs-lookup"><span data-stu-id="d6c2e-116">**Working with Streaming Resources**</span></span>](working-with-streaming-resources.md)
</dt> </dl>

 

 




